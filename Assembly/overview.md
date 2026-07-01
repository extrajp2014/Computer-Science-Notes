1. **CPU Instruction Sets** (x86, ARM, MIPS, RISC-V)
2. **System Calls** (Linux, Windows)
3. **C Library Bindings** (callable from assembly)
4. **Assembler Directives** (NASM, GAS, MASM)
5. **Macro Libraries and Common Utilities**

---

---

## **1. x86/x86-64 Instruction Set**
*(Intel/AMD processors)*

---

### **Data Movement Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MOV` | reg, reg/mem/imm | Move data between registers, memory, and immediate values |
| `MOVZX` | reg, reg/mem | Move with zero-extend (8/16-bit to 32/64-bit) |
| `MOVSX` | reg, reg/mem | Move with sign-extend (8/16-bit to 32/64-bit) |
| `MOVSB` | | Move byte from DS:SI to ES:DI |
| `MOVSW` | | Move word from DS:SI to ES:DI |
| `MOVSD` | | Move doubleword from DS:SI to ES:DI |
| `MOVSQ` | | Move quadword from DS:SI to ES:DI (x86-64) |
| `PUSH` | reg/mem/imm | Push operand onto stack |
| `POP` | reg/mem | Pop value from stack into operand |
| `PUSHA` / `PUSHAD` | | Push all general-purpose registers (EAX, ECX, EDX, EBX, ESP, EBP, ESI, EDI) |
| `POPA` / `POPAD` | | Pop all general-purpose registers |
| `XCHG` | reg, reg/mem | Exchange operands |
| `LEA` | reg, mem | Load effective address into register |
| `LDS` | reg, mem | Load pointer from memory into DS:reg |
| `LES` | reg, mem | Load pointer from memory into ES:reg |
| `LFS` | reg, mem | Load pointer from memory into FS:reg |
| `LGS` | reg, mem | Load pointer from memory into GS:reg |
| `LSS` | reg, mem | Load pointer from memory into SS:reg |
| `CMOVcc` | reg, reg/mem | Conditional move (cc = condition code: E, NE, G, GE, L, LE, A, AE, B, BE, C, NC, O, NO, P, NP, S, NS) |
| `XCHG` | reg, reg | Exchange contents of two registers |
| `BSWAP` | reg | Byte swap (reverses byte order in 32/64-bit register) |
| `MOVBE` | reg, mem | Move with byte swap (little/big-endian conversion) |

---

### **Arithmetic Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD` | reg/mem, reg/imm | Addition |
| `ADC` | reg/mem, reg/imm | Addition with carry |
| `SUB` | reg/mem, reg/imm | Subtraction |
| `SBB` | reg/mem, reg/imm | Subtraction with borrow |
| `INC` | reg/mem | Increment |
| `DEC` | reg/mem | Decrement |
| `NEG` | reg/mem | Two's complement negation |
| `CMP` | reg/mem, reg/imm | Compare (sets flags, does not store result) |
| `IMUL` | reg/mem, reg/imm | Signed multiply |
| `MUL` | reg/mem | Unsigned multiply (result in EDX:EAX or RDX:RAX) |
| `IDIV` | reg/mem | Signed division (dividend in EDX:EAX or RDX:RAX) |
| `DIV` | reg/mem | Unsigned division |
| `DAA` | | Decimal adjust after addition |
| `DAS` | | Decimal adjust after subtraction |
| `AAA` | | ASCII adjust after addition |
| `AAS` | | ASCII adjust after subtraction |
| `AAM` | | ASCII adjust after multiplication |
| `AAD` | | ASCII adjust before division |

---

### **Logical Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `AND` | reg/mem, reg/imm | Bitwise AND |
| `OR` | reg/mem, reg/imm | Bitwise OR |
| `XOR` | reg/mem, reg/imm | Bitwise XOR |
| `NOT` | reg/mem | Bitwise NOT |
| `TEST` | reg/mem, reg/imm | Bitwise AND (sets flags, does not store result) |
| `SHL` / `SAL` | reg/mem, imm/CL | Shift left (arithmetic) |
| `SHR` | reg/mem, imm/CL | Shift right (logical) |
| `SAR` | reg/mem, imm/CL | Shift right (arithmetic) |
| `ROL` | reg/mem, imm/CL | Rotate left |
| `ROR` | reg/mem, imm/CL | Rotate right |
| `RCL` | reg/mem, imm/CL | Rotate left through carry |
| `RCR` | reg/mem, imm/CL | Rotate right through carry |

---
### **Control Flow Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `JMP` | label/reg/mem | Unconditional jump |
| `Jcc` | label | Conditional jump (cc = E, NE, G, GE, L, LE, A, AE, B, BE, C, NC, O, NO, P, NP, S, NS) |
| `CALL` | label/reg/mem | Call a procedure |
| `RET` | [imm] | Return from procedure (optionally pop `imm` bytes from stack) |
| `LOOP` | label | Loop with ECX/RCX counter (decrement and jump if not zero) |
| `LOOPE` / `LOOPZ` | label | Loop if equal/zero |
| `LOOPNE` / `LOOPNZ` | label | Loop if not equal/not zero |
| `JCXZ` | label | Jump if ECX/RCX is zero |
| `INT` | imm | Software interrupt |
| `INTO` | | Interrupt if overflow flag is set |
| `IRET` / `IRETD` | | Interrupt return |
| `SYSCALL` | | Fast system call (x86-64) |
| `SYSRET` | | Return from fast system call (x86-64) |
| `SYSENTER` | | Fast system call entry (x86-64) |
| `SYSEXIT` | | Fast system call exit (x86-64) |

---
### **String Instructions**
*(Operate on strings of bytes/words/dwords. Use SI/DI, CL, AL/AX/EAX/RAX. Require DF=0 for forward, DF=1 for backward. Use REP prefix for repetition.)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `REP` | | Repeat while ECX/RCX != 0 |
| `REPE` / `REPZ` | | Repeat while ECX/RCX != 0 and ZF=1 |
| `REPNE` / `REPNZ` | | Repeat while ECX/RCX != 0 and ZF=0 |
| `MOVSB` | | Move byte from DS:SI to ES:DI |
| `MOVSW` | | Move word from DS:SI to ES:DI |
| `MOVSD` | | Move doubleword from DS:SI to ES:DI |
| `MOVSQ` | | Move quadword from DS:SI to ES:DI (x86-64) |
| `LODSB` | | Load byte from DS:SI into AL |
| `LODSW` | | Load word from DS:SI into AX |
| `LODSD` | | Load doubleword from DS:SI into EAX |
| `LODSQ` | | Load quadword from DS:SI into RAX (x86-64) |
| `STOSB` | | Store AL into ES:DI |
| `STOSW` | | Store AX into ES:DI |
| `STOSD` | | Store EAX into ES:DI |
| `STOSQ` | | Store RAX into ES:DI (x86-64) |
| `CMPSB` | | Compare bytes at DS:SI and ES:DI |
| `CMPSW` | | Compare words at DS:SI and ES:DI |
| `CMPSD` | | Compare doublewords at DS:SI and ES:DI |
| `CMPSQ` | | Compare quadwords at DS:SI and ES:DI (x86-64) |
| `SCASB` | | Scan byte at ES:DI against AL |
| `SCASW` | | Scan word at ES:DI against AX |
| `SCASD` | | Scan doubleword at ES:DI against EAX |
| `SCASQ` | | Scan quadword at ES:DI against RAX (x86-64) |

---
### **Flag Manipulation Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `CLC` | | Clear carry flag (CF=0) |
| `STC` | | Set carry flag (CF=1) |
| `CMC` | | Complement carry flag (CF = NOT CF) |
| `CLD` | | Clear direction flag (DF=0, forward) |
| `STD` | | Set direction flag (DF=1, backward) |
| `CLI` | | Clear interrupt flag (IF=0) |
| `STI` | | Set interrupt flag (IF=1) |
| `LAHF` | | Load AH from flags (SF, ZF, AF, PF, CF) |
| `SAHF` | | Store AH into flags (SF, ZF, AF, PF, CF) |
| `PUSHF` / `PUSHFD` / `PUSHQ` | | Push EFLAGS/RFLAGS onto stack |
| `POPF` / `POPFD` / `POPQ` | | Pop EFLAGS/RFLAGS from stack |
| `PUSH` | reg/mem/imm | Push operand onto stack |
| `POP` | reg/mem | Pop value from stack into operand |

---
### **Stack Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `PUSH` | reg/mem/imm | Push operand onto stack |
| `POP` | reg/mem | Pop value from stack into operand |
| `PUSHA` / `PUSHAD` | | Push all general-purpose registers (AX, CX, DX, BX, SP, BP, SI, DI) |
| `POPA` / `POPAD` | | Pop all general-purpose registers |
| `PUSH` | seg | Push segment register onto stack |
| `POP` | seg | Pop segment register from stack |
| `ENTER` | imm, imm | Create a stack frame (push EBP, set EBP=ESP-imm1, subtract imm2 from ESP) |
| `LEAVE` | | High-level procedure exit (MOV ESP, EBP; POP EBP) |

---
### **I/O Instructions**
*(x86 only, not available in x86-64 user mode)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `IN` | AL/AX/EAX, imm/port | Input from I/O port |
| `IN` | AL/AX/EAX, DX | Input from I/O port in DX |
| `OUT` | imm/port, AL/AX/EAX | Output to I/O port |
| `OUT` | DX, AL/AX/EAX | Output to I/O port in DX |

---
### **Floating-Point Instructions (x87 FPU)**
*(Legacy floating-point unit, mostly superseded by SSE/AVX)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `FLD` | mem/reg | Load floating-point value onto FPU stack |
| `FST` | mem | Store floating-point value from FPU stack to memory |
| `FSTP` | mem | Store and pop floating-point value |
| `FILD` | mem | Load integer into FPU stack |
| `FIST` | mem | Store integer from FPU stack to memory |
| `FISTP` | mem | Store integer and pop from FPU stack |
| `FADD` | mem/reg | Floating-point addition |
| `FSUB` | mem/reg | Floating-point subtraction |
| `FADDP` | | Floating-point addition and pop |
| `FSUBP` | | Floating-point subtraction and pop |
| `FMUL` | mem/reg | Floating-point multiplication |
| `FDIV` | mem/reg | Floating-point division |
| `FMULP` | | Floating-point multiplication and pop |
| `FDIVP` | | Floating-point division and pop |
| `FCOM` | mem/reg | Compare floating-point values |
| `FCOMP` | mem/reg | Compare and pop |
| `FCOMPP` | | Compare and pop twice |
| `FTST` | | Test ST(0) against 0.0 |
| `FXAM` | | Examine ST(0) |
| `FCHS` | | Change sign of ST(0) |
| `FABS` | | Absolute value of ST(0) |
| `FSQRT` | | Square root of ST(0) |
| `FSCALE` | | Scale ST(0) by ST(1) |
| `FPREM` | | Partial remainder |
| `FRNDINT` | | Round ST(0) to integer |
| `F2XM1` | | Compute 2^x - 1 |
| `FYL2X` | | Compute y * log2(x) |
| `FYL2XP1` | | Compute y * log2(x + 1) |
| `FPTAN` | | Compute partial tangent |
| `FPATAN` | | Compute partial arctangent |
| `FSIN` | | Compute sine |
| `FCOS` | | Compute cosine |
| `FSINCOS` | | Compute sine and cosine |
| `FXTRACT` | | Extract exponent and significand |
| `FLD1` | | Load +1.0 onto FPU stack |
| `FLDL2T` | | Load log2(10) onto FPU stack |
| `FLDL2E` | | Load log2(e) onto FPU stack |
| `FLDPI` | | Load pi onto FPU stack |
| `FLDLG2` | | Load log10(2) onto FPU stack |
| `FLDLN2` | | Load ln(2) onto FPU stack |
| `FLDZ` | | Load +0.0 onto FPU stack |
| `FNINIT` | | Initialize FPU |
| `FNOP` | | No operation |
| `FCLEX` | | Clear FPU exceptions |
| `FSTENV` | mem | Store FPU environment |
| `FLDENV` | mem | Load FPU environment |
| `FSAVE` | mem | Store FPU state |
| `FRSTOR` | mem | Restore FPU state |
| `FNSTENV` | mem | Store FPU environment (no wait) |
| `FNLDENV` | mem | Load FPU environment (no wait) |
| `FNSTSW` | mem/AX | Store FPU status word |
| `FNSTCW` | mem | Store FPU control word |
| `FLDCW` | mem | Load FPU control word |

---
### **SSE (Streaming SIMD Extensions) Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MOVAPS` | xmm, xmm/mem | Move aligned packed single-precision floating-point |
| `MOVUPS` | xmm, xmm/mem | Move unaligned packed single-precision floating-point |
| `MOVAPD` | xmm, xmm/mem | Move aligned packed double-precision floating-point |
| `MOVUPD` | xmm, xmm/mem | Move unaligned packed double-precision floating-point |
| `MOVSS` | xmm, xmm/mem | Move scalar single-precision floating-point |
| `MOVSD` | xmm, xmm/mem | Move scalar double-precision floating-point |
| `ADDPS` | xmm, xmm/mem | Add packed single-precision floating-point |
| `ADDPD` | xmm, xmm/mem | Add packed double-precision floating-point |
| `SUBPS` | xmm, xmm/mem | Subtract packed single-precision floating-point |
| `SUBPD` | xmm, xmm/mem | Subtract packed double-precision floating-point |
| `MULPS` | xmm, xmm/mem | Multiply packed single-precision floating-point |
| `MULPD` | xmm, xmm/mem | Multiply packed double-precision floating-point |
| `DIVPS` | xmm, xmm/mem | Divide packed single-precision floating-point |
| `DIVPD` | xmm, xmm/mem | Divide packed double-precision floating-point |
| `RCPPS` | xmm, xmm/mem | Reciprocal of packed single-precision floating-point |
| `RCPPD` | xmm, xmm/mem | Reciprocal of packed double-precision floating-point |
| `SQRTPS` | xmm, xmm/mem | Square root of packed single-precision floating-point |
| `SQRTPD` | xmm, xmm/mem | Square root of packed double-precision floating-point |
| `RSQRTPS` | xmm, xmm/mem | Reciprocal square root of packed single-precision floating-point |
| `RSQRTSS` | xmm, xmm/mem | Reciprocal square root of scalar single-precision floating-point |
| `ANDPS` | xmm, xmm/mem | Bitwise AND of packed single-precision floating-point |
| `ANDPD` | xmm, xmm/mem | Bitwise AND of packed double-precision floating-point |
| `ORPS` | xmm, xmm/mem | Bitwise OR of packed single-precision floating-point |
| `ORPD` | xmm, xmm/mem | Bitwise OR of packed double-precision floating-point |
| `XORPS` | xmm, xmm/mem | Bitwise XOR of packed single-precision floating-point |
| `XORPD` | xmm, xmm/mem | Bitwise XOR of packed double-precision floating-point |
| `SHUFPS` | xmm, xmm/mem, imm8 | Shuffle packed single-precision floating-point |
| `SHUFPD` | xmm, xmm/mem, imm8 | Shuffle packed double-precision floating-point |
| `UNPCKHPS` | xmm, xmm/mem | Unpack high packed single-precision floating-point |
| `UNPCKLPS` | xmm, xmm/mem | Unpack low packed single-precision floating-point |
| `UNPCKHPD` | xmm, xmm/mem | Unpack high packed double-precision floating-point |
| `UNPCKLPD` | xmm, xmm/mem | Unpack low packed double-precision floating-point |
| `CMPPS` | xmm, xmm/mem, imm8 | Compare packed single-precision floating-point |
| `CMPPD` | xmm, xmm/mem, imm8 | Compare packed double-precision floating-point |
| `CMPSS` | xmm, xmm/mem, imm8 | Compare scalar single-precision floating-point |
| `CMPSD` | xmm, xmm/mem, imm8 | Compare scalar double-precision floating-point |
| `COMISS` | xmm, xmm/mem | Compare scalar single-precision floating-point and set EFLAGS |
| `COMISD` | xmm, xmm/mem | Compare scalar double-precision floating-point and set EFLAGS |
| `UCOMISS` | xmm, xmm/mem | Unordered compare scalar single-precision floating-point and set EFLAGS |
| `UCOMISD` | xmm, xmm/mem | Unordered compare scalar double-precision floating-point and set EFLAGS |
| `MAXPS` | xmm, xmm/mem | Maximum of packed single-precision floating-point |
| `MAXPD` | xmm, xmm/mem | Maximum of packed double-precision floating-point |
| `MINPS` | xmm, xmm/mem | Minimum of packed single-precision floating-point |
| `MINPD` | xmm, xmm/mem | Minimum of packed double-precision floating-point |
| `PMAXUB` | mm, mm/mem | Packed maximum of unsigned bytes |
| `PMAXSW` | mm, mm/mem | Packed maximum of signed words |
| `PMINUB` | mm, mm/mem | Packed minimum of unsigned bytes |
| `PMINSW` | mm, mm/mem | Packed minimum of signed words |
| `PMAXSB` | mm, mm/mem | Packed maximum of signed bytes |
| `PMINSB` | mm, mm/mem | Packed minimum of signed bytes |
| `PEXTRW` | reg, mm, imm8 | Extract word from MMX register |
| `PINSRW` | mm, reg/mem, imm8 | Insert word into MMX register |
| `PMOVMSKB` | reg, mm | Move byte mask to integer register |
| `PMULHUW` | mm, mm/mem | Packed multiply high unsigned words |
| `PMULHW` | mm, mm/mem | Packed multiply high signed words |
| `PMULLW` | mm, mm/mem | Packed multiply low signed words |
| `PSADBW` | mm, mm/mem | Packed sum of absolute differences |
| `PSLLW` | mm, mm/mem | Packed shift left logical words |
| `PSLLQ` | mm, mm/mem | Packed shift left logical quadwords |
| `PSRLW` | mm, mm/mem | Packed shift right logical words |
| `PSRLQ` | mm, mm/mem | Packed shift right logical quadwords |
| `PSRAW` | mm, mm/mem | Packed shift right arithmetic words |
| `PAVGB` | mm, mm/mem | Packed average of unsigned bytes |
| `PAVGW` | mm, mm/mem | Packed average of unsigned words |

---
### **SSE2 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MOVAPD` | xmm, xmm/mem | Move aligned packed double-precision floating-point |
| `MOVUPD` | xmm, xmm/mem | Move unaligned packed double-precision floating-point |
| `MOVSD` | xmm, xmm/mem | Move scalar double-precision floating-point |
| `MOVDQA` | xmm, mem | Move aligned double quadword |
| `MOVDQU` | xmm, mem | Move unaligned double quadword |
| `MOVDQ2Q` | mm, xmm | Move double quadword from XMM to MMX |
| `MOVQ2DQ` | xmm, mm | Move quadword from MMX to XMM |
| `PACKSSWB` | mm/xmm, mm/xmm/mem | Pack signed word integers into bytes |
| `PACKSSDW` | mm/xmm, mm/xmm/mem | Pack signed dword integers into words |
| `PACKUSWB` | mm/xmm, mm/xmm/mem | Pack unsigned word integers into bytes |
| `PUNPCKHBW` | mm/xmm, mm/xmm/mem | Unpack high bytes |
| `PUNPCKHWD` | mm/xmm, mm/xmm/mem | Unpack high words |
| `PUNPCKHDQ` | xmm, xmm/mem | Unpack high dwords |
| `PUNPCKHQDQ` | xmm, xmm/mem | Unpack high quadwords |
| `PUNPCKLBW` | mm/xmm, mm/xmm/mem | Unpack low bytes |
| `PUNPCKLWD` | mm/xmm, mm/xmm/mem | Unpack low words |
| `PUNPCKLDQ` | xmm, xmm/mem | Unpack low dwords |
| `PUNPCKLQDQ` | xmm, xmm/mem | Unpack low quadwords |
| `PSHUFD` | xmm, xmm/mem, imm8 | Shuffle packed doublewords |
| `PSHUFHW` | xmm, xmm/mem, imm8 | Shuffle packed high words |
| `PSHUFLW` | xmm, xmm/mem, imm8 | Shuffle packed low words |
| `PSRLDQ` | xmm, imm8 | Shift packed doublewords right logical |
| `PSLLDQ` | xmm, imm8 | Shift packed doublewords left logical |
| `PADDQ` | mm/xmm, mm/xmm/mem | Add packed quadword integers |
| `PSUBQ` | mm/xmm, mm/xmm/mem | Subtract packed quadword integers |
| `PMULUDQ` | xmm, xmm/mem | Multiply unsigned dword integers |
| `PADDQ` | xmm, xmm/mem | Add packed quadword integers |
| `PSUBQ` | xmm, xmm/mem | Subtract packed quadword integers |
| `PSHUFD` | xmm, xmm/mem, imm8 | Shuffle packed doublewords |
| `PSRLDQ` | xmm, imm8 | Shift packed doublewords right logical |
| `PSLLDQ` | xmm, imm8 | Shift packed doublewords left logical |
| `PUNPCKHQDQ` | xmm, xmm/mem | Unpack high quadwords |
| `PUNPCKLQDQ` | xmm, xmm/mem | Unpack low quadwords |
| `MOVMSKPD` | reg, xmm | Move mask of packed double-precision floating-point |
| `MOVMSKPS` | reg, xmm | Move mask of packed single-precision floating-point |
| `PMOVMSKB` | reg, mm/xmm | Move byte mask to integer register |
| `PMULUDQ` | xmm, xmm/mem | Multiply unsigned dword integers |
| `PADDQ` | xmm, xmm/mem | Add packed quadword integers |
| `PSUBQ` | xmm, xmm/mem | Subtract packed quadword integers |
| `PSHUFD` | xmm, xmm/mem, imm8 | Shuffle packed doublewords |
| `PSRLDQ` | xmm, imm8 | Shift packed doublewords right logical |
| `PSLLDQ` | xmm, imm8 | Shift packed doublewords left logical |

---
### **AVX Instructions (Advanced Vector Extensions)**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `VMOVAPS` | xmm/ymm, xmm/ymm/mem | Move aligned packed single-precision floating-point |
| `VMOVUPS` | xmm/ymm, xmm/ymm/mem | Move unaligned packed single-precision floating-point |
| `VMOVAPD` | xmm/ymm, xmm/ymm/mem | Move aligned packed double-precision floating-point |
| `VMOVUPD` | xmm/ymm, xmm/ymm/mem | Move unaligned packed double-precision floating-point |
| `VADDPS` | xmm/ymm, xmm/ymm/mem | Add packed single-precision floating-point |
| `VADDPD` | xmm/ymm, xmm/ymm/mem | Add packed double-precision floating-point |
| `VSUBPS` | xmm/ymm, xmm/ymm/mem | Subtract packed single-precision floating-point |
| `VSUBPD` | xmm/ymm, xmm/ymm/mem | Subtract packed double-precision floating-point |
| `VMULPS` | xmm/ymm, xmm/ymm/mem | Multiply packed single-precision floating-point |
| `VMULPD` | xmm/ymm, xmm/ymm/mem | Multiply packed double-precision floating-point |
| `VDIVPS` | xmm/ymm, xmm/ymm/mem | Divide packed single-precision floating-point |
| `VDIVPD` | xmm/ymm, xmm/ymm/mem | Divide packed double-precision floating-point |
| `VSQRTPS` | xmm/ymm, xmm/ymm/mem | Square root of packed single-precision floating-point |
| `VSQRTPD` | xmm/ymm, xmm/ymm/mem | Square root of packed double-precision floating-point |
| `VANDPS` | xmm/ymm, xmm/ymm/mem | Bitwise AND of packed single-precision floating-point |
| `VANDPD` | xmm/ymm, xmm/ymm/mem | Bitwise AND of packed double-precision floating-point |
| `VORPS` | xmm/ymm, xmm/ymm/mem | Bitwise OR of packed single-precision floating-point |
| `VORPD` | xmm/ymm, xmm/ymm/mem | Bitwise OR of packed double-precision floating-point |
| `VXORPS` | xmm/ymm, xmm/mem | Bitwise XOR of packed single-precision floating-point |
| `VXORPD` | xmm/ymm, xmm/mem | Bitwise XOR of packed double-precision floating-point |
| `VSHUFPS` | xmm/ymm, xmm/ymm/mem, imm8 | Shuffle packed single-precision floating-point |
| `VSHUFPD` | xmm/ymm, xmm/ymm/mem, imm8 | Shuffle packed double-precision floating-point |
| `VBLENDPS` | xmm/ymm, xmm/ymm/mem, imm8 | Blend packed single-precision floating-point |
| `VBLENDPD` | xmm/ymm, xmm/ymm/mem, imm8 | Blend packed double-precision floating-point |
| `VEXTRACTF128` | xmm, ymm, imm8 | Extract 128 bits from YMM register |
| `VINSERTF128` | ymm, ymm, xmm, imm8 | Insert 128 bits into YMM register |
| `VPERM2F128` | ymm, ymm, ymm/mem, imm8 | Permute 128-bit values |
| `VZEROALL` | | Zero all YMM registers |
| `VZEROUPPER` | | Zero upper 128 bits of all YMM registers |

---
### **Control Register Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MOV` | control, reg | Move to/from control register |
| `MOV` | debug, reg | Move to/from debug register |
| `LGDT` | mem | Load Global Descriptor Table |
| `SGDT` | mem | Store Global Descriptor Table |
| `LIDT` | mem | Load Interrupt Descriptor Table |
| `SIDT` | mem | Store Interrupt Descriptor Table |
| `LLDT` | reg/mem | Load Local Descriptor Table |
| `SLDT` | reg/mem | Store Local Descriptor Table |
| `LTR` | reg/mem | Load Task Register |
| `STR` | reg/mem | Store Task Register |
| `VERR` | reg/mem | Verify segment for reading |
| `VERW` | reg/mem | Verify segment for writing |
| `ARPL` | reg/mem, reg | Adjust requested privilege level |
| `LAR` | reg, reg/mem | Load access rights byte |
| `LSL` | reg, reg/mem | Load segment limit |
| `INVD` | | Invalidate cache |
| `WBINVD` | | Write-back and invalidate cache |
| `INVLPG` | mem | Invalidate TLB entry |
| `CLFLUSH` | mem | Flush cache line |
| `CLFLUSHOPT` | mem | Flush cache line (optimized) |
| `MFENCE` | | Memory fence |
| `SFENCE` | | Store fence |
| `LFENCE` | | Load fence |
| `PAUSE` | | Spin-wait hint |
| `RDTSC` | | Read time-stamp counter |
| `RDTSCP` | | Read time-stamp counter and processor ID |
| `RDMSR` | | Read model-specific register |
| `WRMSR` | | Write model-specific register |
| `CPUID` | | CPU identification |
| `RDPMC` | | Read performance-monitoring counters |
| `SYSENTER` | | Fast system call entry |
| `SYSEXIT` | | Fast system call exit |
| `GETSEC` | | Get security information |
| `VMREAD` | reg, mem | Read virtual-machine control field |
| `VMWRITE` | mem, reg | Write to virtual-machine control field |

---
### **Privileged Instructions**
*(Only available in kernel mode)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `HLT` | | Halt the processor |
| `INVD` | | Invalidate cache |
| `INVLPG` | mem | Invalidate TLB entry |
| `LGDT` | mem | Load Global Descriptor Table |
| `LIDT` | mem | Load Interrupt Descriptor Table |
| `LLDT` | reg/mem | Load Local Descriptor Table |
| `LTR` | reg/mem | Load Task Register |
| `MOV` | control, reg | Move to/from control register |
| `MOV` | debug, reg | Move to/from debug register |
| `MOV` | test, reg | Move to/from test register |
| `CLTS` | | Clear task-switched flag in CR0 |
| `INVLPG` | mem | Invalidate TLB entry |
| `WBINVD` | | Write-back and invalidate cache |
| `CLFLUSH` | mem | Flush cache line |
| `RDTSC` | | Read time-stamp counter |
| `RDTSCP` | | Read time-stamp counter and processor ID |
| `RDMSR` | | Read model-specific register |
| `WRMSR` | | Write model-specific register |
| `CPUID` | | CPU identification |
| `RDPMC` | | Read performance-monitoring counters |
| `SYSCALL` | | Fast system call |
| `SYSRET` | | Return from fast system call |
| `SYSENTER` | | Fast system call entry |
| `SYSEXIT` | | Fast system call exit |
| `GETSEC` | | Get security information |
| `VMREAD` | reg, mem | Read virtual-machine control field |
| `VMWRITE` | mem, reg | Write to virtual-machine control field |
| `VMCALL` | | Call to VM monitor |
| `VMLAUNCH` | | Launch a virtual machine |
| `VMRESUME` | | Resume a virtual machine |
| `VMXOFF` | | Exit VMX mode |
| `VMCLEAR` | mem | Clear virtual-machine control structure |
| `VMXON` | mem | Enable VMX mode |
| `INVEPT` | reg, mem | Invalidate EPT entries |
| `INVVPID` | reg, mem | Invalidate VPID entries |

---
---
---
## **2. ARM Instruction Set**
*(32-bit and 64-bit ARM processors)*

---

### **Data Processing Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD` | Rd, Rn, Operand2 | Add |
| `ADC` | Rd, Rn, Operand2 | Add with carry |
| `SUB` | Rd, Rn, Operand2 | Subtract |
| `SBC` | Rd, Rn, Operand2 | Subtract with carry |
| `RSB` | Rd, Rn, Operand2 | Reverse subtract |
| `RSC` | Rd, Rn, Operand2 | Reverse subtract with carry |
| `MUL` | Rd, Rn, Rm | Multiply |
| `MLA` | Rd, Rn, Rm, Ra | Multiply and accumulate |
| `UMULL` | RdLo, RdHi, Rn, Rm | Unsigned multiply long |
| `SMULL` | RdLo, RdHi, Rn, Rm | Signed multiply long |
| `UMLAL` | RdLo, RdHi, Rn, Rm | Unsigned multiply accumulate long |
| `SMLAL` | RdLo, RdHi, Rn, Rm | Signed multiply accumulate long |
| `DIV` | Rd, Rn, Rm | Signed divide |
| `UDIV` | Rd, Rn, Rm | Unsigned divide |
| `AND` | Rd, Rn, Operand2 | Bitwise AND |
| `ORR` | Rd, Rn, Operand2 | Bitwise OR |
| `EOR` | Rd, Rn, Operand2 | Bitwise XOR |
| `BIC` | Rd, Rn, Operand2 | Bitwise clear |
| `MVN` | Rd, Operand2 | Move NOT |
| `LSL` | Rd, Rn, Operand2 | Logical shift left |
| `LSR` | Rd, Rn, Operand2 | Logical shift right |
| `ASR` | Rd, Rn, Operand2 | Arithmetic shift right |
| `ROR` | Rd, Rn, Operand2 | Rotate right |
| `RRX` | Rd, Rn | Rotate right extended (with carry) |
| `CLZ` | Rd, Rn | Count leading zeros |
| `REV` | Rd, Rn | Reverse byte order in a word |
| `REV16` | Rd, Rn | Reverse byte order in each halfword |
| `REVSH` | Rd, Rn | Reverse byte order in a signed halfword |
| `RBIT` | Rd, Rn | Reverse bits |
| `SEL` | Rd, Rn, Rm | Select bytes |

---
### **Load/Store Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LDR` | Rd, [Rn, Rm] | Load word from memory |
| `LDRB` | Rd, [Rn, Rm] | Load byte from memory |
| `LDRH` | Rd, [Rn, Rm] | Load halfword from memory |
| `LDRSB` | Rd, [Rn, Rm] | Load signed byte from memory |
| `LDRSH` | Rd, [Rn, Rm] | Load signed halfword from memory |
| `STR` | Rd, [Rn, Rm] | Store word to memory |
| `STRB` | Rd, [Rn, Rm] | Store byte to memory |
| `STRH` | Rd, [Rn, Rm] | Store halfword to memory |
| `LDM` | Rn!, {Rd, ...} | Load multiple registers |
| `STM` | Rn!, {Rd, ...} | Store multiple registers |
| `PUSH` | {Rd, ...} | Push registers onto stack |
| `POP` | {Rd, ...} | Pop registers from stack |
| `LDR` | Rd, =value | Load immediate value (pseudo-instruction) |
| `ADR` | Rd, label | Load address (pseudo-instruction) |
| `ADRL` | Rd, label | Load long address (pseudo-instruction) |

---
### **Branch Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `B` | label | Branch |
| `BL` | label | Branch with link |
| `BLX` | Rm | Branch with link and exchange (to ARM/Thumb) |
| `BX` | Rm | Branch and exchange (to ARM/Thumb) |
| `BEQ` | label | Branch if equal (Z set) |
| `BNE` | label | Branch if not equal (Z clear) |
| `BCS` | label | Branch if carry set (C set) |
| `BCC` | label | Branch if carry clear (C clear) |
| `BMI` | label | Branch if minus (N set) |
| `BPL` | label | Branch if plus (N clear) |
| `BVS` | label | Branch if overflow (V set) |
| `BVC` | label | Branch if no overflow (V clear) |
| `BHI` | label | Branch if unsigned higher (C set and Z clear) |
| `BLS` | label | Branch if unsigned lower or same (C clear or Z set) |
| `BGE` | label | Branch if signed greater than or equal (N == V) |
| `BLT` | label | Branch if signed less than (N != V) |
| `BGT` | label | Branch if signed greater than (Z clear and N == V) |
| `BLE` | label | Branch if signed less than or equal (Z set or N != V) |
| `BAL` | label | Branch always (alias for B) |

---
### **Control Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `NOP` | | No operation |
| `SEV` | | Send event |
| `WFE` | | Wait for event |
| `WFI` | | Wait for interrupt |
| `YIELD` | | Yield (hint for thread switching) |
| `BKPT` | | Breakpoint |
| `SVC` | imm | Supervisor call (software interrupt) |
| `HVC` | imm | Hypervisor call |
| `SMC` | imm | Secure monitor call |
| `UDF` | | Undefined instruction |
| `CPSIE` | | Change processor state (enable interrupts) |
| `CPSID` | | Change processor state (disable interrupts) |
| `MRS` | Rd, spec_reg | Move to register from system register |
| `MSR` | spec_reg, Rn | Move to system register from register |
| `ISB` | | Instruction synchronization barrier |
| `DSB` | | Data synchronization barrier |
| `DMB` | | Data memory barrier |
| `WFI` | | Wait for interrupt |
| `WFE` | | Wait for event |

---
### **ARMv6/ARMv7 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MLA` | Rd, Rn, Rm, Ra | Multiply and accumulate |
| `MLS` | Rd, Rn, Rm, Ra | Multiply and subtract |
| `UMULL` | RdLo, RdHi, Rn, Rm | Unsigned multiply long |
| `SMULL` | RdLo, RdHi, Rn, Rm | Signed multiply long |
| `UMLAL` | RdLo, RdHi, Rn, Rm | Unsigned multiply accumulate long |
| `SMLAL` | RdLo, RdHi, Rn, Rm | Signed multiply accumulate long |
| `SMLABB` | Rd, Rn, Rm, Ra | Signed multiply accumulate (bottom x bottom) |
| `SMLATB` | Rd, Rn, Rm, Ra | Signed multiply accumulate (top x bottom) |
| `SMLABT` | Rd, Rn, Rm, Ra | Signed multiply accumulate (bottom x top) |
| `SMLATT` | Rd, Rn, Rm, Ra | Signed multiply accumulate (top x top) |
| `SMUAD` | Rd, Rn, Rm | Signed multiply add dual |
| `SMUSD` | Rd, Rn, Rm | Signed multiply subtract dual |
| `SMMUL` | Rd, Rn, Rm | Signed multiply multiply |
| `SMMULR` | Rd, Rn, Rm | Signed multiply multiply with rounding |
| `SMMLA` | Rd, Rn, Rm, Ra | Signed multiply multiply accumulate |
| `SMMLAR` | Rd, Rn, Rm, Ra | Signed multiply multiply accumulate with rounding |
| `SMMUL` | Rd, Rn, Rm | Signed multiply multiply |
| `USAD8` | Rd, Rn, Rm | Unsigned sum of absolute differences |
| `USADA8` | Rd, Rn, Rm, Ra | Unsigned sum of absolute differences accumulate |
| `SSAT` | Rd, #imm, Rn | Signed saturate |
| `SSAT16` | Rd, #imm, Rn | Signed saturate 16-bit |
| `USAT` | Rd, #imm, Rn | Unsigned saturate |
| `USAT16` | Rd, #imm, Rn | Unsigned saturate 16-bit |
| `REV` | Rd, Rn | Reverse byte order in a word |
| `REV16` | Rd, Rn | Reverse byte order in each halfword |
| `REVSH` | Rd, Rn | Reverse byte order in a signed halfword |
| `RBIT` | Rd, Rn | Reverse bits |
| `CLZ` | Rd, Rn | Count leading zeros |
| `LDREX` | Rd, [Rn] | Load exclusive |
| `STREX` | Rd, Rt, [Rn] | Store exclusive |
| `LDREXB` | Rd, [Rn] | Load exclusive byte |
| `STREXB` | Rd, Rt, [Rn] | Store exclusive byte |
| `LDREXH` | Rd, [Rn] | Load exclusive halfword |
| `STREXH` | Rd, Rt, [Rn] | Store exclusive halfword |
| `LDREXD` | Rd, [Rn] | Load exclusive doubleword |
| `STREXD` | Rd, Rt, [Rn] | Store exclusive doubleword |

---
### **ARMv8 (AArch64) Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD` | Xd, Xn, Operand2 | Add (64-bit) |
| `ADDS` | Xd, Xn, Operand2 | Add with set flags (64-bit) |
| `SUB` | Xd, Xn, Operand2 | Subtract (64-bit) |
| `SUBS` | Xd, Xn, Operand2 | Subtract with set flags (64-bit) |
| `MUL` | Xd, Xn, Xm | Multiply (64-bit) |
| `UMULH` | Xd, Xn, Xm | Unsigned multiply high (64-bit) |
| `SMULH` | Xd, Xn, Xm | Signed multiply high (64-bit) |
| `UDIV` | Xd, Xn, Xm | Unsigned divide (64-bit) |
| `SDIV` | Xd, Xn, Xm | Signed divide (64-bit) |
| `LSL` | Xd, Xn, Xm | Logical shift left (64-bit) |
| `LSR` | Xd, Xn, Xm | Logical shift right (64-bit) |
| `ASR` | Xd, Xn, Xm | Arithmetic shift right (64-bit) |
| `ROR` | Xd, Xn, Xm | Rotate right (64-bit) |
| `AND` | Xd, Xn, Operand2 | Bitwise AND (64-bit) |
| `ORR` | Xd, Xn, Operand2 | Bitwise OR (64-bit) |
| `EOR` | Xd, Xn, Operand2 | Bitwise XOR (64-bit) |
| `NOT` | Xd, Xn | Bitwise NOT (64-bit) |
| `BIC` | Xd, Xn, Operand2 | Bitwise clear (64-bit) |
| `MVN` | Xd, Operand2 | Move NOT (64-bit) |
| `MOV` | Xd, Operand2 | Move (64-bit) |
| `MOVK` | Xd, Operand2, LSL #imm | Move with keep (64-bit) |
| `MOVZ` | Xd, Operand2, LSL #imm | Move with zero (64-bit) |
| `LDR` | Xt, [Xn, Xm] | Load register (64-bit) |
| `STR` | Xt, [Xn, Xm] | Store register (64-bit) |
| `LDP` | Xt1, Xt2, [Xn, #imm] | Load pair of registers |
| `STP` | Xt1, Xt2, [Xn, #imm] | Store pair of registers |
| `LDUR` | Xt, [Xn, #imm] | Load register with unprivileged access |
| `STUR` | Xt, [Xn, #imm] | Store register with unprivileged access |
| `LDAR` | Xt, [Xn] | Load-acquire register |
| `STLR` | Xt, [Xn] | Store-release register |
| `LDXR` | Xt, [Xn] | Load exclusive register |
| `STXR` | Ws, Xt, [Xn] | Store exclusive register |
| `CAS` | Xs, Xt, [Xn] | Compare and swap |
| `CASA` | Xs, Xt, [Xn] | Compare and swap (acquire) |
| `CASL` | Xs, Xt, [Xn] | Compare and swap (release) |
| `CASAL` | Xs, Xt, [Xn] | Compare and swap (acquire-release) |
| `SWPA` | Xs, Xt, [Xn] | Swap (acquire) |
| `SWPAL` | Xs, Xt, [Xn] | Swap (acquire-release) |
| `SWPB` | Xs, Xt, [Xn] | Swap byte |
| `SWPAB` | Xs, Xt, [Xn] | Swap byte (acquire) |
| `SWPLB` | Xs, Xt, [Xn] | Swap byte (release) |
| `SWPALB` | Xs, Xt, [Xn] | Swap byte (acquire-release) |
| `B` | label | Branch |
| `BL` | label | Branch with link |
| `BR` | Xn | Branch to register |
| `BLR` | Xn | Branch with link to register |
| `RET` | [Xn] | Return from subroutine |
| `ERET` | | Exception return |
| `SVC` | imm | Supervisor call |
| `HVC` | imm | Hypervisor call |
| `SMC` | imm | Secure monitor call |
| `BRK` | imm | Breakpoint |
| `HLT` | imm | Halt |
| `DCPS1` | | Debug change processor state 1 |
| `DCPS2` | | Debug change processor state 2 |
| `DCPS3` | | Debug change processor state 3 |
| `NOP` | | No operation |
| `YIELD` | | Yield |
| `WFE` | | Wait for event |
| `WFI` | | Wait for interrupt |
| `SEV` | | Send event |
| `SEVL` | | Send event local |
| `ISB` | | Instruction synchronization barrier |
| `DSB` | | Data synchronization barrier |
| `DMB` | | Data memory barrier |
| `SB` | | Storage barrier |
| `CLREX` | | Clear exclusive monitor |
| `DSB` | | Data synchronization barrier |
| `DMB` | | Data memory barrier |

---
### **AArch64 SIMD/NEON Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD` | Vd.T, Vn.T, Vm.T | Add vectors |
| `FADD` | Vd.T, Vn.T, Vm.T | Floating-point add vectors |
| `SUB` | Vd.T, Vn.T, Vm.T | Subtract vectors |
| `FSUB` | Vd.T, Vn.T, Vm.T | Floating-point subtract vectors |
| `MUL` | Vd.T, Vn.T, Vm.T | Multiply vectors |
| `FMUL` | Vd.T, Vn.T, Vm.T | Floating-point multiply vectors |
| `MLA` | Vd.T, Vn.T, Vm.T | Multiply-accumulate vectors |
| `FMLA` | Vd.T, Vn.T, Vm.T | Floating-point multiply-accumulate vectors |
| `LD1` | Vt.T, [Xn] | Load single 1-element structure |
| `LD2` | Vt.T, [Xn] | Load single 2-element structure |
| `LD3` | Vt.T, [Xn] | Load single 3-element structure |
| `LD4` | Vt.T, [Xn] | Load single 4-element structure |
| `ST1` | Vt.T, [Xn] | Store single 1-element structure |
| `ST2` | Vt.T, [Xn] | Store single 2-element structure |
| `ST3` | Vt.T, [Xn] | Store single 3-element structure |
| `ST4` | Vt.T, [Xn] | Store single 4-element structure |
| `LD1R` | Vt.T, [Xn] | Load and replicate single 1-element structure |
| `LD2R` | Vt.T, [Xn] | Load and replicate single 2-element structure |
| `LD3R` | Vt.T, [Xn] | Load and replicate single 3-element structure |
| `LD4R` | Vt.T, [Xn] | Load and replicate single 4-element structure |
| `FMLA` | Vd.T, Vn.T, Vm.T | Floating-point fused multiply-add |
| `FMLS` | Vd.T, Vn.T, Vm.T | Floating-point fused multiply-subtract |
| `FDIV` | Vd.T, Vn.T, Vm.T | Floating-point divide |
| `FSQRT` | Vd.T, Vn.T | Floating-point square root |
| `FABS` | Vd.T, Vn.T | Floating-point absolute value |
| `FNEG` | Vd.T, Vn.T | Floating-point negate |
| `FCVT` | Vd.T, Vn.T | Floating-point convert |
| `REV64` | Vd.T, Vn.T | Reverse elements in vectors (64-bit) |
| `REV32` | Vd.T, Vn.T | Reverse elements in vectors (32-bit) |
| `REV16` | Vd.T, Vn.T | Reverse elements in vectors (16-bit) |
| `TRN1` | Vd.T, Vn.T, Vm.T | Transpose vectors (high half) |
| `TRN2` | Vd.T, Vn.T, Vm.T | Transpose vectors (low half) |
| `UZP1` | Vd.T, Vn.T, Vm.T | Unzip vectors (high half) |
| `UZP2` | Vd.T, Vn.T, Vm.T | Unzip vectors (low half) |
| `ZIP1` | Vd.T, Vn.T, Vm.T | Zip vectors (high half) |
| `ZIP2` | Vd.T, Vn.T, Vm.T | Zip vectors (low half) |

---
---
---
## **3. MIPS Instruction Set**

---

### **Arithmetic Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD` | Rd, Rs, Rt | Add (with overflow) |
| `ADDU` | Rd, Rs, Rt | Add unsigned (no overflow) |
| `SUB` | Rd, Rs, Rt | Subtract (with overflow) |
| `SUBU` | Rd, Rs, Rt | Subtract unsigned (no overflow) |
| `MULT` | Rs, Rt | Multiply (result in HI/LO) |
| `MULTU` | Rs, Rt | Multiply unsigned (result in HI/LO) |
| `DIV` | Rs, Rt | Divide (quotient in LO, remainder in HI) |
| `DIVU` | Rs, Rt | Divide unsigned |
| `MADD` | Rs, Rt | Multiply and add (result in HI/LO) |
| `MADDU` | Rs, Rt | Multiply unsigned and add |
| `MSUB` | Rs, Rt | Multiply and subtract |
| `MSUBU` | Rs, Rt | Multiply unsigned and subtract |
| `AND` | Rd, Rs, Rt | Bitwise AND |
| `OR` | Rd, Rs, Rt | Bitwise OR |
| `XOR` | Rd, Rs, Rt | Bitwise XOR |
| `NOR` | Rd, Rs, Rt | Bitwise NOT OR |
| `SLL` | Rd, Rt, Sa | Shift left logical |
| `SRL` | Rd, Rt, Sa | Shift right logical |
| `SRA` | Rd, Rt, Sa | Shift right arithmetic |
| `SLLV` | Rd, Rt, Rs | Shift left logical variable |
| `SRLV` | Rd, Rt, Rs | Shift right logical variable |
| `SRAV` | Rd, Rt, Rs | Shift right arithmetic variable |
| `CLZ` | Rd, Rs | Count leading zeros |
| `CLO` | Rd, Rs | Count leading ones |

---
### **Load/Store Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LB` | Rt, offset(Base) | Load byte |
| `LH` | Rt, offset(Base) | Load halfword |
| `LW` | Rt, offset(Base) | Load word |
| `LD` | Rt, offset(Base) | Load doubleword (64-bit) |
| `LBU` | Rt, offset(Base) | Load byte unsigned |
| `LHU` | Rt, offset(Base) | Load halfword unsigned |
| `LWU` | Rt, offset(Base) | Load word unsigned (MIPS64) |
| `SB` | Rt, offset(Base) | Store byte |
| `SH` | Rt, offset(Base) | Store halfword |
| `SW` | Rt, offset(Base) | Store word |
| `SD` | Rt, offset(Base) | Store doubleword (64-bit) |
| `LWL` | Rt, offset(Base) | Load word left |
| `LWR` | Rt, offset(Base) | Load word right |
| `SWL` | Rt, offset(Base) | Store word left |
| `SWR` | Rt, offset(Base) | Store word right |
| `ULH` | Rt, offset(Base) | Unaligned load halfword |
| `ULHU` | Rt, offset(Base) | Unaligned load halfword unsigned |
| `ULW` | Rt, offset(Base) | Unaligned load word |
| `USH` | Rt, offset(Base) | Unaligned store halfword |
| `USW` | Rt, offset(Base) | Unaligned store word |

---
### **Branch and Jump Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `J` | target | Jump |
| `JAL` | target | Jump and link |
| `JR` | Rs | Jump register |
| `JALR` | Rs | Jump and link register |
| `BEQ` | Rs, Rt, label | Branch if equal |
| `BNE` | Rs, Rt, label | Branch if not equal |
| `BLEZ` | Rs, label | Branch if <= zero |
| `BGTZ` | Rs, label | Branch if > zero |
| `BLTZ` | Rs, label | Branch if < zero |
| `BGEZ` | Rs, label | Branch if >= zero |
| `BLTZAL` | Rs, label | Branch if < zero and link |
| `BGEZAL` | Rs, label | Branch if >= zero and link |
| `BC1F` | label | Branch if FP condition false |
| `BC1T` | label | Branch if FP condition true |
| `BC1FL` | label | Branch if FP condition false and link |
| `BC1TL` | label | Branch if FP condition true and link |

---
### **Immediate Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADDI` | Rt, Rs, imm | Add immediate |
| `ADDIU` | Rt, Rs, imm | Add immediate unsigned |
| `SLTI` | Rt, Rs, imm | Set if less than immediate (signed) |
| `SLTIU` | Rt, Rs, imm | Set if less than immediate unsigned |
| `ANDI` | Rt, Rs, imm | Bitwise AND immediate |
| `ORI` | Rt, Rs, imm | Bitwise OR immediate |
| `XORI` | Rt, Rs, imm | Bitwise XOR immediate |
| `LUI` | Rt, imm | Load upper immediate |
| `BEQZ` | Rs, label | Branch if equal to zero (pseudo-instruction) |
| `BNEZ` | Rs, label | Branch if not equal to zero (pseudo-instruction) |
| `BGTZ` | Rs, label | Branch if greater than zero |
| `BLEZ` | Rs, label | Branch if less than or equal to zero |
| `BGEZ` | Rs, label | Branch if greater than or equal to zero |
| `BLTZ` | Rs, label | Branch if less than zero |

---
### **Floating-Point Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADD.S` | Fd, Fs, Ft | Add single-precision |
| `SUB.S` | Fd, Fs, Ft | Subtract single-precision |
| `MUL.S` | Fd, Fs, Ft | Multiply single-precision |
| `DIV.S` | Fd, Fs, Ft | Divide single-precision |
| `ABS.S` | Fd, Fs | Absolute value single-precision |
| `NEG.S` | Fd, Fs | Negate single-precision |
| `SQRT.S` | Fd, Fs | Square root single-precision |
| `CVT.W.S` | Fd, Fs | Convert word to single-precision |
| `CVT.S.W` | Fd, Fs | Convert single-precision to word |
| `ADD.D` | Fd, Fs, Ft | Add double-precision |
| `SUB.D` | Fd, Fs, Ft | Subtract double-precision |
| `MUL.D` | Fd, Fs, Ft | Multiply double-precision |
| `DIV.D` | Fd, Fs, Ft | Divide double-precision |
| `ABS.D` | Fd, Fs | Absolute value double-precision |
| `NEG.D` | Fd, Fs | Negate double-precision |
| `SQRT.D` | Fd, Fs | Square root double-precision |
| `CVT.W.D` | Fd, Fs | Convert word to double-precision |
| `CVT.D.W` | Fd, Fs | Convert double-precision to word |
| `BC1F` | label | Branch if FP condition false |
| `BC1T` | label | Branch if FP condition true |
| `CF.C` | Fs | Compare condition false |
| `CF.S` | Fs | Compare condition false (single) |
| `CF.D` | Fs | Compare condition false (double) |

---
### **CP0 (Coproc 0) Instructions**
*(System control coprocessor)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MFC0` | Rt, Rd, Sel | Move from CP0 register |
| `MTC0` | Rt, Rd, Sel | Move to CP0 register |
| `TLBR` | | Read TLB entry |
| `TLBWI` | | Write TLB entry |
| `TLBWR` | | Write random TLB entry |
| `TLBP` | | Probe TLB for matching entry |
| `RFE` | | Return from exception |
| `ERET` | | Exception return |
| `WAIT` | | Wait for interrupt |
| `TLBINV` | | Invalidate TLB |
| `TLBINVF` | | Invalidate TLB entry |

---
---
---
## **4. RISC-V Instruction Set**
*(Open-source instruction set architecture)*

---

### **RV32I Base Integer Instruction Set**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LUI` | Rd, imm | Load upper immediate |
| `AUIPC` | Rd, imm | Add upper immediate to PC |
| `JAL` | Rd, imm | Jump and link |
| `JALR` | Rd, Rs1, imm | Jump and link register |
| `BEQ` | Rs1, Rs2, imm | Branch if equal |
| `BNE` | Rs1, Rs2, imm | Branch if not equal |
| `BLT` | Rs1, Rs2, imm | Branch if less than |
| `BGE` | Rs1, Rs2, imm | Branch if greater than or equal |
| `BLTU` | Rs1, Rs2, imm | Branch if less than (unsigned) |
| `BGEU` | Rs1, Rs2, imm | Branch if greater than or equal (unsigned) |
| `LB` | Rd, imm(Rs1) | Load byte |
| `LH` | Rd, imm(Rs1) | Load halfword |
| `LW` | Rd, imm(Rs1) | Load word |
| `LBU` | Rd, imm(Rs1) | Load byte unsigned |
| `LHU` | Rd, imm(Rs1) | Load halfword unsigned |
| `SB` | Rs2, imm(Rs1) | Store byte |
| `SH` | Rs2, imm(Rs1) | Store halfword |
| `SW` | Rs2, imm(Rs1) | Store word |
| `ADDI` | Rd, Rs1, imm | Add immediate |
| `SLTI` | Rd, Rs1, imm | Set if less than immediate |
| `SLTIU` | Rd, Rs1, imm | Set if less than immediate (unsigned) |
| `XORI` | Rd, Rs1, imm | Bitwise XOR immediate |
| `ORI` | Rd, Rs1, imm | Bitwise OR immediate |
| `ANDI` | Rd, Rs1, imm | Bitwise AND immediate |
| `SLLI` | Rd, Rs1, shamt | Shift left logical immediate |
| `SRLI` | Rd, Rs1, shamt | Shift right logical immediate |
| `SRAI` | Rd, Rs1, shamt | Shift right arithmetic immediate |
| `ADD` | Rd, Rs1, Rs2 | Add |
| `SUB` | Rd, Rs1, Rs2 | Subtract |
| `SLL` | Rd, Rs1, Rs2 | Shift left logical |
| `SLT` | Rd, Rs1, Rs2 | Set if less than |
| `SLTU` | Rd, Rs1, Rs2 | Set if less than (unsigned) |
| `XOR` | Rd, Rs1, Rs2 | Bitwise XOR |
| `SRL` | Rd, Rs1, Rs2 | Shift right logical |
| `SRA` | Rd, Rs1, Rs2 | Shift right arithmetic |
| `OR` | Rd, Rs1, Rs2 | Bitwise OR |
| `AND` | Rd, Rs1, Rs2 | Bitwise AND |
| `FENCE` | pred, succ | Fence (memory ordering) |
| `ECALL` | | Environment call |
| `EBREAK` | | Environment break |

---
### **RV64I Base Integer Instruction Set (64-bit)**
*(Same as RV32I but with 64-bit registers and instructions)*

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LD` | Rd, imm(Rs1) | Load doubleword |
| `SD` | Rs2, imm(Rs1) | Store doubleword |
| `ADDIW` | Rd, Rs1, imm | Add immediate word |
| `SLLIW` | Rd, Rs1, shamt | Shift left logical immediate word |
| `SRLIW` | Rd, Rs1, shamt | Shift right logical immediate word |
| `SRAIW` | Rd, Rs1, shamt | Shift right arithmetic immediate word |
| `ADDW` | Rd, Rs1, Rs2 | Add word |
| `SUBW` | Rd, Rs1, Rs2 | Subtract word |
| `SLLW` | Rd, Rs1, Rs2 | Shift left logical word |
| `SRLW` | Rd, Rs1, Rs2 | Shift right logical word |
| `SRAW` | Rd, Rs1, Rs2 | Shift right arithmetic word |

---
### **RV32M Multiply/Divide Extension**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MUL` | Rd, Rs1, Rs2 | Multiply |
| `MULH` | Rd, Rs1, Rs2 | Multiply high (signed x signed) |
| `MULHU` | Rd, Rs1, Rs2 | Multiply high (unsigned x unsigned) |
| `MULHSU` | Rd, Rs1, Rs2 | Multiply high (signed x unsigned) |
| `DIV` | Rd, Rs1, Rs2 | Divide (signed) |
| `DIVU` | Rd, Rs1, Rs2 | Divide (unsigned) |
| `REM` | Rd, Rs1, Rs2 | Remainder (signed) |
| `REMU` | Rd, Rs1, Rs2 | Remainder (unsigned) |

---
### **RV64M Multiply/Divide Extension (64-bit)**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `MULW` | Rd, Rs1, Rs2 | Multiply word |
| `DIVW` | Rd, Rs1, Rs2 | Divide word (signed) |
| `DIVUW` | Rd, Rs1, Rs2 | Divide word (unsigned) |
| `REMW` | Rd, Rs1, Rs2 | Remainder word (signed) |
| `REMUW` | Rd, Rs1, Rs2 | Remainder word (unsigned) |

---
### **RV32A Atomic Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LR.W` | Rd, (Rs1) | Load-reserved word |
| `SC.W` | Rd, Rs2, (Rs1) | Store-conditional word |
| `AMOSWAP.W` | Rd, Rs2, (Rs1) | Atomic swap word |
| `AMOADD.W` | Rd, Rs2, (Rs1) | Atomic add word |
| `AMOXOR.W` | Rd, Rs2, (Rs1) | Atomic XOR word |
| `AMOAND.W` | Rd, Rs2, (Rs1) | Atomic AND word |
| `AMOOR.W` | Rd, Rs2, (Rs1) | Atomic OR word |
| `AMOMIN.W` | Rd, Rs2, (Rs1) | Atomic minimum word |
| `AMOMAX.W` | Rd, Rs2, (Rs1) | Atomic maximum word |
| `AMOMINU.W` | Rd, Rs2, (Rs1) | Atomic minimum word (unsigned) |
| `AMOMAXU.W` | Rd, Rs2, (Rs1) | Atomic maximum word (unsigned) |

---
### **RV64A Atomic Instructions (64-bit)**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `LR.D` | Rd, (Rs1) | Load-reserved doubleword |
| `SC.D` | Rd, Rs2, (Rs1) | Store-conditional doubleword |
| `AMOSWAP.D` | Rd, Rs2, (Rs1) | Atomic swap doubleword |
| `AMOADD.D` | Rd, Rs2, (Rs1) | Atomic add doubleword |
| `AMOXOR.D` | Rd, Rs2, (Rs1) | Atomic XOR doubleword |
| `AMOAND.D` | Rd, Rs2, (Rs1) | Atomic AND doubleword |
| `AMOOR.D` | Rd, Rs2, (Rs1) | Atomic OR doubleword |
| `AMOMIN.D` | Rd, Rs2, (Rs1) | Atomic minimum doubleword |
| `AMOMAX.D` | Rd, Rs2, (Rs1) | Atomic maximum doubleword |
| `AMOMINU.D` | Rd, Rs2, (Rs1) | Atomic minimum doubleword (unsigned) |
| `AMOMAXU.D` | Rd, Rs2, (Rs1) | Atomic maximum doubleword (unsigned) |

---
### **RV32F Single-Precision Floating-Point Extension**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `FLW` | Fd, imm(Rs1) | Load single-precision floating-point |
| `FSW` | Fs2, imm(Rs1) | Store single-precision floating-point |
| `FADD.S` | Fd, Fs1, Fs2 | Add single-precision |
| `FSUB.S` | Fd, Fs1, Fs2 | Subtract single-precision |
| `FMUL.S` | Fd, Fs1, Fs2 | Multiply single-precision |
| `FDIV.S` | Fd, Fs1, Fs2 | Divide single-precision |
| `FSQRT.S` | Fd, Fs1 | Square root single-precision |
| `FMADD.S` | Fd, Fs1, Fs2, Fs3 | Fused multiply-add single-precision |
| `FMSUB.S` | Fd, Fs1, Fs2, Fs3 | Fused multiply-subtract single-precision |
| `FNMSUB.S` | Fd, Fs1, Fs2, Fs3 | Fused negate-multiply-subtract single-precision |
| `FNMADD.S` | Fd, Fs1, Fs2, Fs3 | Fused negate-multiply-add single-precision |
| `FLE.S` | Rd, Fs1, Fs2 | Floating-point less than or equal |
| `FLT.S` | Rd, Fs1, Fs2 | Floating-point less than |
| `FEQ.S` | Rd, Fs1, Fs2 | Floating-point equal |
| `FCVT.W.S` | Rd, Fs1 | Convert single-precision to word |
| `FCVT.S.W` | Fd, Rs1 | Convert word to single-precision |
| `FCVT.WU.S` | Rd, Fs1 | Convert single-precision to unsigned word |
| `FCVT.S.WU` | Fd, Rs1 | Convert unsigned word to single-precision |

---
### **RV64F Single-Precision Floating-Point Extension (64-bit)**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `FLD` | Fd, imm(Rs1) | Load double-precision floating-point |
| `FSD` | Fs2, imm(Rs1) | Store double-precision floating-point |
| `FADD.D` | Fd, Fs1, Fs2 | Add double-precision |
| `FSUB.D` | Fd, Fs1, Fs2 | Subtract double-precision |
| `FMUL.D` | Fd, Fs1, Fs2 | Multiply double-precision |
| `FDIV.D` | Fd, Fs1, Fs2 | Divide double-precision |
| `FSQRT.D` | Fd, Fs1 | Square root double-precision |
| `FMADD.D` | Fd, Fs1, Fs2, Fs3 | Fused multiply-add double-precision |
| `FMSUB.D` | Fd, Fs1, Fs2, Fs3 | Fused multiply-subtract double-precision |
| `FNMSUB.D` | Fd, Fs1, Fs2, Fs3 | Fused negate-multiply-subtract double-precision |
| `FNMADD.D` | Fd, Fs1, Fs2, Fs3 | Fused negate-multiply-add double-precision |
| `FLE.D` | Rd, Fs1, Fs2 | Floating-point less than or equal (double) |
| `FLT.D` | Rd, Fs1, Fs2 | Floating-point less than (double) |
| `FEQ.D` | Rd, Fs1, Fs2 | Floating-point equal (double) |
| `FCVT.L.S` | Rd, Fs1 | Convert single-precision to long |
| `FCVT.LU.S` | Rd, Fs1 | Convert single-precision to unsigned long |
| `FCVT.S.L` | Fd, Rs1 | Convert long to single-precision |
| `FCVT.S.LU` | Fd, Rs1 | Convert unsigned long to single-precision |
| `FCVT.L.D` | Rd, Fs1 | Convert double-precision to long |
| `FCVT.LU.D` | Rd, Fs1 | Convert double-precision to unsigned long |
| `FCVT.D.L` | Fd, Rs1 | Convert long to double-precision |
| `FCVT.D.LU` | Fd, Rs1 | Convert unsigned long to double-precision |

---
---
---
## **5. System Calls**
*(Operating system interface for user-space programs)*

---

### **Linux System Calls (x86-64)**
*(64-bit Linux uses `syscall` instruction with RAX = syscall number, RDI, RSI, RDX, R10, R8, R9 = arguments)*

| Syscall Number | Name | Description |
|----------------|------|-------------|
| 0 | `sys_read` | Read from a file descriptor |
| 1 | `sys_write` | Write to a file descriptor |
| 2 | `sys_open` | Open or create a file |
| 3 | `sys_close` | Close a file descriptor |
| 4 | `sys_stat` | Get file status |
| 5 | `sys_fstat` | Get file status (by file descriptor) |
| 6 | `sys_lstat` | Get file status (no symlink follow) |
| 7 | `sys_poll` | Poll for I/O events |
| 8 | `sys_lseek` | Seek on a file descriptor |
| 9 | `sys_mmap` | Map memory |
| 10 | `sys_mprotect` | Set memory protection |
| 11 | `sys_munmap` | Unmap memory |
| 12 | `sys_brk` | Change data segment size |
| 13 | `sys_rt_sigaction` | Set signal handler |
| 14 | `sys_rt_sigprocmask` | Set signal mask |
| 15 | `sys_rt_sigreturn` | Return from signal handler |
| 16 | `sys_ioctl` | I/O control |
| 17 | `sys_pread64` | Preaded file |
| 18 | `sys_pwrite64` | Pwrite to file |
| 19 | `sys_readv` | Read from multiple buffers |
| 20 | `sys_writev` | Write to multiple buffers |
| 21 | `sys_access` | Check file accessibility |
| 22 | `sys_pipe` | Create a pipe |
| 23 | `sys_select` | Synchronous I/O multiplexing |
| 24 | `sys_sched_yield` | Yield the processor |
| 25 | `sys_mremap` | Remap memory |
| 26 | `sys_msync` | Synchronize memory |
| 27 | `sys_mincore` | Get memory residency |
| 28 | `sys_madvise` | Give advice about memory usage |
| 29 | `sys_shmget` | Get shared memory segment |
| 30 | `sys_shmat` | Attach shared memory segment |
| 31 | `sys_shmctl` | Control shared memory |
| 32 | `sys_dup` | Duplicate file descriptor |
| 33 | `sys_dup2` | Duplicate file descriptor to a specific number |
| 34 | `sys_pause` | Pause process |
| 35 | `sys_nanosleep` | High-resolution sleep |
| 36 | `sys_getitimer` | Get interval timer |
| 37 | `sys_alarm` | Set alarm clock |
| 38 | `sys_setitimer` | Set interval timer |
| 39 | `sys_getpid` | Get process ID |
| 40 | `sys_sendfile` | Transfer data between file descriptors |
| 41 | `sys_socket` | Create a socket |
| 42 | `sys_connect` | Connect a socket |
| 43 | `sys_accept` | Accept a connection on a socket |
| 44 | `sys_sendto` | Send a message on a socket |
| 45 | `sys_recvfrom` | Receive a message from a socket |
| 46 | `sys_sendmsg` | Send a message on a socket |
| 47 | `sys_recvmsg` | Receive a message from a socket |
| 48 | `sys_shutdown` | Shut down a socket |
| 49 | `sys_bind` | Bind a socket to an address |
| 50 | `sys_listen` | Listen for connections on a socket |
| 51 | `sys_getsockname` | Get socket name |
| 52 | `sys_getpeername` | Get peer name |
| 53 | `sys_socketpair` | Create a pair of connected sockets |
| 54 | `sys_setsockopt` | Set socket options |
| 55 | `sys_getsockopt` | Get socket options |
| 56 | `sys_clone` | Create a child process |
| 57 | `sys_fork` | Create a child process |
| 58 | `sys_vfork` | Create a child process and block parent |
| 59 | `sys_execve` | Execute a program |
| 60 | `sys_exit` | Terminate the process |
| 61 | `sys_wait4` | Wait for a child process to exit |
| 62 | `sys_kill` | Send a signal to a process |
| 63 | `sys_uname` | Get system name |
| 64 | `sys_semget` | Get semaphore set |
| 65 | `sys_semop` | Semaphore operations |
| 66 | `sys_semctl` | Semaphore control |
| 67 | `sys_shmdt` | Detach shared memory segment |
| 68 | `sys_msgget` | Get message queue |
| 69 | `sys_msgsnd` | Send message |
| 70 | `sys_msgrcv` | Receive message |
| 71 | `sys_msgctl` | Message queue control |
| 72 | `sys_fcntl` | File control |
| 73 | `sys_flock` | Apply or remove an advisory lock |
| 74 | `sys_fsync` | Synchronize a file |
| 75 | `sys_fdatasync` | Synchronize file data |
| 76 | `sys_truncate` | Truncate a file |
| 77 | `sys_ftruncate` | Truncate a file (by file descriptor) |
| 78 | `sys_getdents` | Get directory entries |
| 79 | `sys_getcwd` | Get current working directory |
| 80 | `sys_chdir` | Change directory |
| 81 | `sys_fchdir` | Change directory (by file descriptor) |
| 82 | `sys_rename` | Rename a file |
| 83 | `sys_mkdir` | Create a directory |
| 84 | `sys_rmdir` | Remove a directory |
| 85 | `sys_creat` | Create or truncate a file |
| 86 | `sys_link` | Create a hard link |
| 87 | `sys_unlink` | Remove a hard link |
| 88 | `sys_symlink` | Create a symbolic link |
| 89 | `sys_readlink` | Read symbolic link |
| 90 | `sys_chmod` | Change file permissions |
| 91 | `sys_fchmod` | Change file permissions (by file descriptor) |
| 92 | `sys_chown` | Change file ownership |
| 93 | `sys_fchown` | Change file ownership (by file descriptor) |
| 94 | `sys_lchown` | Change file ownership (no symlink follow) |
| 95 | `sys_umask` | Set file mode creation mask |
| 96 | `sys_gettimeofday` | Get time of day |
| 97 | `sys_getrlimit` | Get resource limits |
| 98 | `sys_setrlimit` | Set resource limits |
| 99 | `sys_getrusage` | Get resource usage |
| 100 | `sys_sysinfo` | Get system information |
| 101 | `sys_times` | Get process times |
| 102 | `sys_ptrace` | Process trace |
| 103 | `sys_getuid` | Get user ID |
| 104 | `sys_syslog` | Read/write system log |
| 105 | `sys_getgid` | Get group ID |
| 106 | `sys_setuid` | Set user ID |
| 107 | `sys_setgid` | Set group ID |
| 108 | `sys_geteuid` | Get effective user ID |
| 109 | `sys_getegid` | Get effective group ID |
| 110 | `sys_setpgid` | Set process group ID |
| 111 | `sys_getppid` | Get parent process ID |
| 112 | `sys_getpgrp` | Get process group ID |
| 113 | `sys_setsid` | Set session ID |
| 114 | `sys_setreuid` | Set real and/or effective user ID |
| 115 | `sys_setregid` | Set real and/or effective group ID |
| 116 | `sys_getgroups` | Get group list |
| 117 | `sys_setgroups` | Set group list |
| 118 | `sys_setresuid` | Set real, effective, and saved user ID |
| 119 | `sys_getresuid` | Get real, effective, and saved user ID |
| 120 | `sys_setresgid` | Set real, effective, and saved group ID |
| 121 | `sys_getresgid` | Get real, effective, and saved group ID |
| 122 | `sys_getpgid` | Get process group ID |
| 123 | `sys_setfsuid` | Set filesystem user ID |
| 124 | `sys_setfsgid` | Set filesystem group ID |
| 125 | `sys_getsid` | Get session ID |
| 126 | `sys_capget` | Get capabilities |
| 127 | `sys_capset` | Set capabilities |
| 128 | `sys_rt_sigsuspend` | Suspend process until signal |
| 129 | `sys_sigaltstack` | Set/get alternate signal stack |
| 130 | `sys_utime` | Set file last access and modification times |
| 131 | `sys_mknod` | Create a special or ordinary file |
| 132 | `sys_uselib` | Load a shared library (obsolete) |
| 133 | `sys_personality` | Set the process execution domain |
| 134 | `sys_ustat` | Get file status (obsolete) |
| 135 | `sys_statfs` | Get filesystem statistics |
| 136 | `sys_fstatfs` | Get filesystem statistics (by file descriptor) |
| 137 | `sys_sysfs` | Get filesystem type |
| 138 | `sys_getpriority` | Get program scheduling priority |
| 139 | `sys_setpriority` | Set program scheduling priority |
| 140 | `sys_sched_setparam` | Set scheduling parameters |
| 141 | `sys_sched_getparam` | Get scheduling parameters |
| 142 | `sys_sched_setscheduler` | Set scheduling policy and parameters |
| 143 | `sys_sched_getscheduler` | Get scheduling policy |
| 144 | `sys_sched_get_priority_max` | Get maximum scheduling priority |
| 145 | `sys_sched_get_priority_min` | Get minimum scheduling priority |
| 146 | `sys_sched_rr_get_interval` | Get round-robin scheduling interval |
| 147 | `sys_mlock` | Lock memory |
| 148 | `sys_munlock` | Unlock memory |
| 149 | `sys_mlockall` | Lock all memory |
| 150 | `sys_munlockall` | Unlock all memory |
| 151 | `sys_vhangup` | Virtual hangup |
| 152 | `sys_modify_ldt` | Modify local descriptor table |
| 153 | `sys_pivot_root` | Change the root filesystem |
| 154 | `sys_sysctl` | Get/set kernel parameters |
| 155 | `sys_prctl` | Set/get process attributes |
| 156 | `sys_arch_prctl` | Architecture-specific prctl |
| 157 | `sys_adjtimex` | Adjust kernel clock |
| 158 | `sys_setrlimit` | Set resource limits |
| 159 | `sys_chroot` | Change root directory |
| 160 | `sys_sync` | Synchronize filesystem |
| 161 | `sys_acct` | Enable/disable process accounting |
| 162 | `sys_settimeofday` | Set time of day |
| 163 | `sys_mount` | Mount a filesystem |
| 164 | `sys_umount2` | Unmount a filesystem |
| 165 | `sys_swapon` | Enable paging to a file or swap device |
| 166 | `sys_swapoff` | Disable paging to a file or swap device |
| 167 | `sys_reboot` | Reboot the system |
| 168 | `sys_sethostname` | Set hostname |
| 169 | `sys_setdomainname` | Set domain name |
| 170 | `sys_iopl` | Change I/O privilege level |
| 171 | `sys_ioperm` | Set I/O permission bitmap |
| 172 | `sys_create_module` | Create a kernel module (obsolete) |
| 173 | `sys_init_module` | Initialize a kernel module (obsolete) |
| 174 | `sys_delete_module` | Delete a kernel module (obsolete) |
| 175 | `sys_get_kernel_syms` | Get kernel symbol table (obsolete) |
| 176 | `sys_query_module` | Query kernel module (obsolete) |
| 177 | `sys_quotactl` | Manipulate disk quotas |
| 178 | `sys_nfsservctl` | NFS server control (obsolete) |
| 179 | `sys_getpmsg` | Get a message from a message queue (obsolete) |
| 180 | `sys_putpmsg` | Put a message to a message queue (obsolete) |
| 181 | `sys_afs_syscall` | AFS system call (obsolete) |
| 182 | `sys_tuxcall` | Tux system call (obsolete) |
| 183 | `sys_request_key` | Request a key from the kernel |
| 184 | `sys_keyctl` | Key management |
| 185 | `sys_ioprio_set` | Set I/O priority |
| 186 | `sys_ioprio_get` | Get I/O priority |
| 187 | `sys_inotify_init` | Initialize inotify |
| 188 | `sys_inotify_add_watch` | Add an inotify watch |
| 189 | `sys_inotify_rm_watch` | Remove an inotify watch |
| 190 | `sys_migrate_pages` | Migrate memory pages |
| 191 | `sys_move_pages` | Move memory pages |
| 192 | `sys_rt_tgsigqueueinfo` | Get thread group signal queue info |
| 193 | `sys_perf_event_open` | Open a performance event |
| 194 | `sys_accept4` | Accept a connection on a socket |
| 195 | `sys_recvmmsg` | Receive a message from a socket |
| 196 | `sys_wait4` | Wait for a child process to exit |
| 197 | `sys_prlimit64` | Set/get resource limits (64-bit) |
| 198 | `sys_fanotify_init` | Initialize fanotify |
| 199 | `sys_fanotify_mark` | Add/remove/modify fanotify marks |
| 200 | `sys_prlimit64` | Set/get resource limits (64-bit) |

---
### **Linux System Calls (x86)**
*(32-bit Linux uses `int 0x80` with EAX = syscall number, EBX, ECX, EDX, ESI, EDI, EBP = arguments)*

| Syscall Number | Name | Description |
|----------------|------|-------------|
| 0 | `sys_restart_syscall` | Restart a system call |
| 1 | `sys_exit` | Terminate the process |
| 2 | `sys_fork` | Create a child process |
| 3 | `sys_read` | Read from a file descriptor |
| 4 | `sys_write` | Write to a file descriptor |
| 5 | `sys_open` | Open or create a file |
| 6 | `sys_close` | Close a file descriptor |
| 7 | `sys_waitpid` | Wait for a child process to exit |
| 8 | `sys_creat` | Create or truncate a file |
| 9 | `sys_link` | Create a hard link |
| 10 | `sys_unlink` | Remove a hard link |
| 11 | `sys_execve` | Execute a program |
| 12 | `sys_chdir` | Change directory |
| 13 | `sys_time` | Get time in seconds |
| 14 | `sys_mknod` | Create a special or ordinary file |
| 15 | `sys_chmod` | Change file permissions |
| 16 | `sys_lchown` | Change file ownership (no symlink follow) |
| 17 | `sys_break` | Change data segment size (obsolete; use `brk`) |
| 18 | `sys_oldstat` | Get file status (obsolete) |
| 19 | `sys_lseek` | Seek on a file descriptor |
| 20 | `sys_getpid` | Get process ID |
| 21 | `sys_mount` | Mount a filesystem |
| 22 | `sys_umount` | Unmount a filesystem |
| 23 | `sys_setuid` | Set user ID |
| 24 | `sys_getuid` | Get user ID |
| 25 | `sys_stime` | Set time (obsolete; use `settimeofday`) |
| 26 | `sys_ptrace` | Process trace |
| 27 | `sys_alarm` | Set alarm clock |
| 28 | `sys_oldfstat` | Get file status (by file descriptor, obsolete) |
| 29 | `sys_pause` | Pause process |
| 30 | `sys_utime` | Set file last access and modification times |
| 31 | `sys_stty` | Set terminal I/O options (obsolete) |
| 32 | `sys_gtty` | Get terminal I/O options (obsolete) |
| 33 | `sys_access` | Check file accessibility |
| 34 | `sys_nice` | Change process priority |
| 35 | `sys_ftime` | Get file creation/modification times (obsolete) |
| 36 | `sys_sync` | Synchronize filesystem |
| 37 | `sys_kill` | Send a signal to a process |
| 38 | `sys_rename` | Rename a file |
| 39 | `sys_mkdir` | Create a directory |
| 40 | `sys_rmdir` | Remove a directory |
| 41 | `sys_dup` | Duplicate file descriptor |
| 42 | `sys_pipe` | Create a pipe |
| 43 | `sys_times` | Get process times |
| 44 | `sys_prof` | Enable/disable profiling (obsolete) |
| 45 | `sys_brk` | Change data segment size |
| 46 | `sys_setgid` | Set group ID |
| 47 | `sys_getgid` | Get group ID |
| 48 | `sys_signal` | Set signal handler (obsolete; use `sigaction`) |
| 49 | `sys_geteuid` | Get effective user ID |
| 50 | `sys_getegid` | Get effective group ID |
| 51 | `sys_acct` | Enable/disable process accounting |
| 52 | `sys_umount2` | Unmount a filesystem |
| 53 | `sys_lock` | Apply/remove an advisory lock (obsolete; use `flock`) |
| 54 | `sys_ioctl` | I/O control |
| 55 | `sys_fcntl` | File control |
| 56 | `sys_mpx` | (obsolete) |
| 57 | `sys_setpgid` | Set process group ID |
| 58 | `sys_ulimit` | Set file size limit (obsolete) |
| 59 | `sys_oldolduname` | Get system name (obsolete) |
| 60 | `sys_umask` | Set file mode creation mask |
| 61 | `sys_chroot` | Change root directory |
| 62 | `sys_ustat` | Get file status (obsolete) |
| 63 | `sys_dup2` | Duplicate file descriptor to a specific number |
| 64 | `sys_getppid` | Get parent process ID |
| 65 | `sys_getpgrp` | Get process group ID |
| 66 | `sys_setsid` | Set session ID |
| 67 | `sys_sigaction` | Set signal handler |
| 68 | `sys_sgetmask` | Get signal mask (obsolete; use `sigprocmask`) |
| 69 | `sys_ssetmask` | Set signal mask (obsolete; use `sigprocmask`) |
| 70 | `sys_setreuid` | Set real and/or effective user ID |
| 71 | `sys_setregid` | Set real and/or effective group ID |
| 72 | `sys_sigsuspend` | Suspend process until signal |
| 73 | `sys_sigpending` | Get pending signals |
| 74 | `sys_sethostname` | Set hostname |
| 75 | `sys_setrlimit` | Set resource limits |
| 76 | `sys_getrlimit` | Get resource limits |
| 77 | `sys_getrusage` | Get resource usage |
| 78 | `sys_gettimeofday` | Get time of day |
| 79 | `sys_settimeofday` | Set time of day |
| 80 | `sys_getgroups` | Get group list |
| 81 | `sys_setgroups` | Set group list |
| 82 | `sys_select` | Synchronous I/O multiplexing |
| 83 | `sys_symlink` | Create a symbolic link |
| 84 | `sys_oldlstat` | Get file status (no symlink follow, obsolete) |
| 85 | `sys_readlink` | Read symbolic link |
| 86 | `sys_uselib` | Load a shared library (obsolete) |
| 87 | `sys_swapon` | Enable paging to a file or swap device |
| 88 | `sys_reboot` | Reboot the system |
| 89 | `sys_readdir` | Read directory entries (obsolete; use `getdents`) |
| 90 | `sys_mmap` | Map memory |
| 91 | `sys_munmap` | Unmap memory |
| 92 | `sys_truncate` | Truncate a file |
| 93 | `sys_ftruncate` | Truncate a file (by file descriptor) |
| 94 | `sys_fchmod` | Change file permissions (by file descriptor) |
| 95 | `sys_fchown` | Change file ownership (by file descriptor) |
| 96 | `sys_getpriority` | Get program scheduling priority |
| 97 | `sys_setpriority` | Set program scheduling priority |
| 98 | `sys_profil` | Enable/disable profiling (obsolete) |
| 99 | `sys_statfs` | Get filesystem statistics |
| 100 | `sys_fstatfs` | Get filesystem statistics (by file descriptor) |
| 101 | `sys_ioperm` | Set I/O permission bitmap |
| 102 | `sys_socketcall` | Socket operations (obsolete; use individual socket calls) |
| 103 | `sys_syslog` | Read/write system log |
| 104 | `sys_setitimer` | Set interval timer |
| 105 | `sys_getitimer` | Get interval timer |
| 106 | `sys_stat` | Get file status |
| 107 | `sys_lstat` | Get file status (no symlink follow) |
| 108 | `sys_fstat` | Get file status (by file descriptor) |

---
### **Windows System Calls (x86/x86-64)**
*(Windows uses a different mechanism. For 32-bit: `int 0x2E` or `sysenter`. For 64-bit: `syscall` with RCX, RDX, R8, R9 = arguments)*

| Function | Description | Library |
|----------|-------------|---------|
| `NtCreateFile` | Create or open a file | ntdll.dll |
| `NtReadFile` | Read from a file | ntdll.dll |
| `NtWriteFile` | Write to a file | ntdll.dll |
| `NtClose` | Close a handle | ntdll.dll |
| `NtQueryInformationFile` | Query file information | ntdll.dll |
| `NtSetInformationFile` | Set file information | ntdll.dll |
| `NtCreateSection` | Create a section object | ntdll.dll |
| `NtMapViewOfSection` | Map a view of a section | ntdll.dll |
| `NtUnmapViewOfSection` | Unmap a view of a section | ntdll.dll |
| `NtAllocateVirtualMemory` | Allocate virtual memory | ntdll.dll |
| `NtFreeVirtualMemory` | Free virtual memory | ntdll.dll |
| `NtProtectVirtualMemory` | Protect virtual memory | ntdll.dll |
| `NtCreateThread` | Create a thread | ntdll.dll |
| `NtTerminateThread` | Terminate a thread | ntdll.dll |
| `NtWaitForSingleObject` | Wait for a single object | ntdll.dll |
| `NtWaitForMultipleObjects` | Wait for multiple objects | ntdll.dll |
| `NtCreateProcess` | Create a process | ntdll.dll |
| `NtTerminateProcess` | Terminate a process | ntdll.dll |
| `NtCreateProcessEx` | Create a process (extended) | ntdll.dll |
| `NtOpenProcess` | Open a process | ntdll.dll |
| `NtQuerySystemInformation` | Query system information | ntdll.dll |
| `NtQueryInformationProcess` | Query process information | ntdll.dll |
| `NtSetInformationProcess` | Set process information | ntdll.dll |
| `NtCreateThreadEx` | Create a thread (extended) | ntdll.dll |
| `NtOpenThread` | Open a thread | ntdll.dll |
| `NtQueryInformationThread` | Query thread information | ntdll.dll |
| `NtSetInformationThread` | Set thread information | ntdll.dll |
| `NtSuspendThread` | Suspend a thread | ntdll.dll |
| `NtResumeThread` | Resume a thread | ntdll.dll |
| `NtQueueApcThread` | Queue an APC to a thread | ntdll.dll |
| `NtTestAlert` | Test if thread has an alert | ntdll.dll |
| `NtAlertResumeThread` | Alert and resume a thread | ntdll.dll |
| `NtAlertThread` | Alert a thread | ntdll.dll |
| `NtGetContextThread` | Get thread context | ntdll.dll |
| `NtSetContextThread` | Set thread context | ntdll.dll |
| `NtCreateEvent` | Create an event | ntdll.dll |
| `NtOpenEvent` | Open an event | ntdll.dll |
| `NtSetEvent` | Set an event | ntdll.dll |
| `NtClearEvent` | Clear an event | ntdll.dll |
| `NtPulseEvent` | Pulse an event | ntdll.dll |
| `NtCreateSemaphore` | Create a semaphore | ntdll.dll |
| `NtOpenSemaphore` | Open a semaphore | ntdll.dll |
| `NtReleaseSemaphore` | Release a semaphore | ntdll.dll |
| `NtCreateMutex` | Create a mutex | ntdll.dll |
| `NtOpenMutex` | Open a mutex | ntdll.dll |
| `NtReleaseMutex` | Release a mutex | ntdll.dll |
| `NtCreateKeyedEvent` | Create a keyed event | ntdll.dll |
| `NtOpenKeyedEvent` | Open a keyed event | ntdll.dll |
| `NtSetKeyedEvent` | Set a keyed event | ntdll.dll |
| `NtCreateIoCompletion` | Create an I/O completion port | ntdll.dll |
| `NtCreateFile` | Create or open a file | ntdll.dll |
| `NtDeviceIoControlFile` | Device I/O control | ntdll.dll |
| `NtFsControlFile` | Filesystem control | ntdll.dll |
| `NtLockFile` | Lock a file | ntdll.dll |
| `NtUnlockFile` | Unlock a file | ntdll.dll |
| `NtCancelIoFile` | Cancel I/O on a file | ntdll.dll |
| `NtSetIoCompletion` | Set I/O completion | ntdll.dll |

---
---
---
## **6. C Library Functions Callable from Assembly**
*(Standard C library functions that can be called from assembly code)*

---

### **Standard I/O (stdio.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `printf` | Formatted output to stdout | cdecl |
| `fprintf` | Formatted output to a stream | cdecl |
| `sprintf` | Formatted output to a string | cdecl |
| `snprintf` | Formatted output to a string (safe) | cdecl |
| `scanf` | Formatted input from stdin | cdecl |
| `fscanf` | Formatted input from a stream | cdecl |
| `sscanf` | Formatted input from a string | cdecl |
| `putchar` | Output a character to stdout | cdecl |
| `puts` | Output a string to stdout | cdecl |
| `getchar` | Input a character from stdin | cdecl |
| `gets` | Input a string from stdin | cdecl |
| `fputs` | Output a string to a stream | cdecl |
| `fgets` | Input a string from a stream | cdecl |
| `fputc` | Output a character to a stream | cdecl |
| `fgetc` | Input a character from a stream | cdecl |
| `ungetc` | Push back a character to a stream | cdecl |
| `feof` | Check for end-of-file | cdecl |
| `ferror` | Check for error | cdecl |
| `clearerr` | Clear error indicators | cdecl |
| `fflush` | Flush a stream | cdecl |
| `fseek` | Reposition a stream | cdecl |
| `ftell` | Get current position in a stream | cdecl |
| `rewind` | Rewind a stream | cdecl |
| `fgetpos` | Get current position in a stream | cdecl |
| `fsetpos` | Set position in a stream | cdecl |
| `setbuf` | Set buffer for a stream | cdecl |
| `setvbuf` | Set buffering for a stream | cdecl |
| `setbuffer` | Set buffer for a stream | cdecl |
| `setlinebuf` | Set line buffering for a stream | cdecl |
| `tmpfile` | Create a temporary file | cdecl |
| `tmpnam` | Generate a temporary filename | cdecl |
| `remove` | Remove a file | cdecl |
| `rename` | Rename a file | cdecl |
| `fclose` | Close a stream | cdecl |
| `fopen` | Open a stream | cdecl |
| `freopen` | Reopen a stream with a different file | cdecl |
| `fdopen` | Associate a stream with a file descriptor | cdecl |
| `fileno` | Get file descriptor from a stream | cdecl |
| `popen` | Open a process by creating a pipe | cdecl |
| `pclose` | Close a process opened by popen | cdecl |

---
### **File I/O (stdio.h, fcntl.h, unistd.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `open` | Open a file | cdecl |
| `close` | Close a file descriptor | cdecl |
| `read` | Read from a file descriptor | cdecl |
| `write` | Write to a file descriptor | cdecl |
| `lseek` | Reposition a file offset | cdecl |
| `stat` | Get file status | cdecl |
| `fstat` | Get file status (by file descriptor) | cdecl |
| `lstat` | Get file status (no symlink follow) | cdecl |
| `access` | Check file accessibility | cdecl |
| `chmod` | Change file permissions | cdecl |
| `fchmod` | Change file permissions (by file descriptor) | cdecl |
| `chown` | Change file ownership | cdecl |
| `fchown` | Change file ownership (by file descriptor) | cdecl |
| `lchown` | Change file ownership (no symlink follow) | cdecl |
| `link` | Create a hard link | cdecl |
| `unlink` | Remove a hard link | cdecl |
| `symlink` | Create a symbolic link | cdecl |
| `readlink` | Read symbolic link | cdecl |
| `mkdir` | Create a directory | cdecl |
| `rmdir` | Remove a directory | cdecl |
| `truncate` | Truncate a file | cdecl |
| `ftruncate` | Truncate a file (by file descriptor) | cdecl |
| `fsync` | Synchronize a file | cdecl |
| `fdatasync` | Synchronize file data | cdecl |
| `sync` | Synchronize filesystem | cdecl |
| `dup` | Duplicate file descriptor | cdecl |
| `dup2` | Duplicate file descriptor to a specific number | cdecl |
| `fcntl` | File control | cdecl |
| `ioctl` | I/O control | cdecl |
| `flock` | Apply or remove an advisory lock | cdecl |
| `lockf` | Apply/remove an advisory lock (obsolete) | cdecl |

---
### **Memory Allocation (stdlib.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `malloc` | Allocate memory | cdecl |
| `calloc` | Allocate and zero memory | cdecl |
| `realloc` | Reallocate memory | cdecl |
| `free` | Free allocated memory | cdecl |
| `alloca` | Allocate memory on stack | cdecl |
| `brk` | Change data segment size | cdecl |
| `sbrk` | Increment data segment | cdecl |

---
### **String Manipulation (string.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `strlen` | Get string length | cdecl |
| `strnlen` | Get string length (safe) | cdecl |
| `strcpy` | Copy a string | cdecl |
| `strncpy` | Copy a string (safe) | cdecl |
| `strcat` | Concatenate strings | cdecl |
| `strncat` | Concatenate strings (safe) | cdecl |
| `strcmp` | Compare strings | cdecl |
| `strncmp` | Compare strings (safe) | cdecl |
| `strcasecmp` | Compare strings (case-insensitive) | cdecl |
| `strncasecmp` | Compare strings (case-insensitive, safe) | cdecl |
| `strchr` | Find character in string | cdecl |
| `strrchr` | Find last character in string | cdecl |
| `strstr` | Find substring | cdecl |
| `strnstr` | Find substring (safe) | cdecl |
| `strtok` | Tokenize a string | cdecl |
| `strtok_r` | Tokenize a string (reentrant) | cdecl |
| `memcpy` | Copy memory | cdecl |
| `memmove` | Copy memory (overlapping safe) | cdecl |
| `memset` | Fill memory | cdecl |
| `memcmp` | Compare memory | cdecl |
| `memchr` | Find character in memory | cdecl |
| `strerror` | Get error message | cdecl |
| `strerror_r` | Get error message (reentrant) | cdecl |

---
### **Character Classification and Conversion (ctype.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `isalnum` | Check if alphanumeric | cdecl |
| `isalpha` | Check if alphabetic | cdecl |
| `iscntrl` | Check if control character | cdecl |
| `isdigit` | Check if digit | cdecl |
| `isgraph` | Check if printable (excluding space) | cdecl |
| `islower` | Check if lowercase | cdecl |
| `isprint` | Check if printable (including space) | cdecl |
| `ispunct` | Check if punctuation | cdecl |
| `isspace` | Check if whitespace | cdecl |
| `isupper` | Check if uppercase | cdecl |
| `isxdigit` | Check if hexadecimal digit | cdecl |
| `tolower` | Convert to lowercase | cdecl |
| `toupper` | Convert to uppercase | cdecl |
| `toascii` | Convert to ASCII | cdecl |
| `_tolower` | Convert to lowercase (internal) | cdecl |
| `_toupper` | Convert to uppercase (internal) | cdecl |

---
### **Time and Date (time.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `time` | Get current time | cdecl |
| `difftime` | Compute difference between two times | cdecl |
| `mktime` | Convert calendar time to time_t | cdecl |
| `strftime` | Format time as a string | cdecl |
| `strptime` | Parse time from a string | cdecl |
| `ctime` | Convert time to a string | cdecl |
| `localtime` | Convert time to local time | cdecl |
| `gmtime` | Convert time to UTC | cdecl |
| `asctime` | Convert time to a string | cdecl |
| `clock` | Get processor time | cdecl |
| `sleep` | Sleep for a specified number of seconds | cdecl |
| `usleep` | Sleep for a specified number of microseconds | cdecl |
| `nanosleep` | Sleep for a specified number of nanoseconds | cdecl |

---
### **Process Control (stdlib.h, unistd.h, process.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `exit` | Terminate the process | cdecl |
| `_exit` | Terminate the process (no cleanup) | cdecl |
| `atexit` | Register a function to call at exit | cdecl |
| `at_quick_exit` | Register a function to call at quick exit | cdecl |
| `quick_exit` | Terminate the process quickly | cdecl |
| `abort` | Abort the process | cdecl |
| `system` | Execute a shell command | cdecl |
| `execve` | Execute a program | cdecl |
| `execl` | Execute a program (with argument list) | cdecl |
| `execlp` | Execute a program (with PATH search) | cdecl |
| `execle` | Execute a program (with environment) | cdecl |
| `execv` | Execute a program (with argument array) | cdecl |
| `execvp` | Execute a program (with PATH search, argument array) | cdecl |
| `fork` | Create a child process | cdecl |
| `vfork` | Create a child process (with shared address space) | cdecl |
| `getpid` | Get process ID | cdecl |
| `getppid` | Get parent process ID | cdecl |
| `getuid` | Get user ID | cdecl |
| `geteuid` | Get effective user ID | cdecl |
| `getgid` | Get group ID | cdecl |
| `getegid` | Get effective group ID | cdecl |
| `setuid` | Set user ID | cdecl |
| `seteuid` | Set effective user ID | cdecl |
| `setgid` | Set group ID | cdecl |
| `setegid` | Set effective group ID | cdecl |
| `setreuid` | Set real and effective user ID | cdecl |
| `setregid` | Set real and effective group ID | cdecl |
| `getgroups` | Get group list | cdecl |
| `setgroups` | Set group list | cdecl |
| `getpgid` | Get process group ID | cdecl |
| `setpgid` | Set process group ID | cdecl |
| `getsid` | Get session ID | cdecl |
| `setsid` | Set session ID | cdecl |
| `getpriority` | Get scheduling priority | cdecl |
| `setpriority` | Set scheduling priority | cdecl |
| `nice` | Change process priority | cdecl |
| `pause` | Wait for a signal | cdecl |
| `alarm` | Set alarm clock | cdecl |
| `sleep` | Sleep for a specified number of seconds | cdecl |
| `usleep` | Sleep for a specified number of microseconds | cdecl |
| `nanosleep` | Sleep for a specified number of nanoseconds | cdecl |

---
### **Signal Handling (signal.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `signal` | Set signal handler | cdecl |
| `sigaction` | Set signal handler (extended) | cdecl |
| `sigprocmask` | Set/get signal mask | cdecl |
| `sigpending` | Get pending signals | cdecl |
| `sigsetjmp` | Set jump point for non-local goto | cdecl |
| `siglongjmp` | Non-local goto | cdecl |
| `raise` | Send a signal to the current process | cdecl |
| `kill` | Send a signal to a process | cdecl |
| `killpg` | Send a signal to a process group | cdecl |
| `sigaltstack` | Set/get alternate signal stack | cdecl |
| `sighold` | Add a signal to the signal mask | cdecl |
| `sigrelse` | Remove a signal from the signal mask | cdecl |
| `sigignore` | Ignore a signal | cdecl |
| `sigset` | Set signal handler to default | cdecl |

---
### **Dynamic Memory Allocation (malloc.h, stdlib.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `malloc` | Allocate memory | cdecl |
| `calloc` | Allocate and zero memory | cdecl |
| `realloc` | Reallocate memory | cdecl |
| `free` | Free allocated memory | cdecl |
| `alloca` | Allocate memory on stack | cdecl |
| `brk` | Change data segment size | cdecl |
| `sbrk` | Increment data segment | cdecl |
| `memalign` | Allocate aligned memory | cdecl |
| `posix_memalign` | Allocate aligned memory (POSIX) | cdecl |
| `valloc` | Allocate page-aligned memory | cdecl |
| `pvalloc` | Allocate page-aligned memory (rounded up) | cdecl |
| `mallinfo` | Get memory allocation information | cdecl |
| `mallopt` | Set memory allocation parameters | cdecl |

---
### **Mathematical Functions (math.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `sin` | Sine | cdecl |
| `cos` | Cosine | cdecl |
| `tan` | Tangent | cdecl |
| `asin` | Arcsine | cdecl |
| `acos` | Arccosine | cdecl |
| `atan` | Arctangent | cdecl |
| `atan2` | Arctangent of y/x | cdecl |
| `sinh` | Hyperbolic sine | cdecl |
| `cosh` | Hyperbolic cosine | cdecl |
| `tanh` | Hyperbolic tangent | cdecl |
| `exp` | Exponential | cdecl |
| `exp2` | Exponential base 2 | cdecl |
| `expm1` | Exponential minus 1 | cdecl |
| `log` | Natural logarithm | cdecl |
| `log10` | Base-10 logarithm | cdecl |
| `log2` | Base-2 logarithm | cdecl |
| `log1p` | Natural log of 1+x | cdecl |
| `pow` | Power | cdecl |
| `sqrt` | Square root | cdecl |
| `cbrt` | Cube root | cdecl |
| `hypot` | Hypotenuse | cdecl |
| `fabs` | Absolute value | cdecl |
| `abs` | Absolute value (integer) | cdecl |
| `labs` | Absolute value (long) | cdecl |
| `llabs` | Absolute value (long long) | cdecl |
| `fmod` | Remainder | cdecl |
| `remainder` | IEEE remainder | cdecl |
| `remquo` | Remainder and quotient | cdecl |
| `fma` | Fused multiply-add | cdecl |
| `copysign` | Copy sign | cdecl |
| `nextafter` | Next representable value | cdecl |
| `nexttoward` | Next representable value toward | cdecl |
| `fdim` | Positive difference | cdecl |
| `fmax` | Maximum | cdecl |
| `fmin` | Minimum | cdecl |
| `fma` | Fused multiply-add | cdecl |
| `nan` | Not-a-Number | cdecl |
| `nextafter` | Next representable value | cdecl |
| `scalbn` | Scale by power of FLT_RADIX | cdecl |
| `scalbln` | Scale by power of FLT_RADIX (long double) | cdecl |
| `tgamma` | Gamma function | cdecl |
| `lgamma` | Natural log of absolute gamma | cdecl |
| `erf` | Error function | cdecl |
| `erfc` | Complementary error function | cdecl |
| `ceil` | Round up | cdecl |
| `floor` | Round down | cdecl |
| `trunc` | Round toward zero | cdecl |
| `round` | Round to nearest integer | cdecl |
| `lround` | Round to nearest integer (long) | cdecl |
| `llround` | Round to nearest integer (long long) | cdecl |
| `rint` | Round to nearest integer (rounding mode) | cdecl |
| `lrint` | Round to nearest integer (long, rounding mode) | cdecl |
| `llrint` | Round to nearest integer (long long, rounding mode) | cdecl |
| `nearbyint` | Round to nearest integer (no exception) | cdecl |
| `remainder` | IEEE remainder | cdecl |

---
### **Error Handling (errno.h, string.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `perror` | Print error message | cdecl |
| `strerror` | Get error message | cdecl |
| `strerror_r` | Get error message (reentrant) | cdecl |
| `errno` | Error number (macro) | - |

---
### **Memory and String (memory.h, string.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `memcpy` | Copy memory | cdecl |
| `memmove` | Copy memory (overlapping safe) | cdecl |
| `memcmp` | Compare memory | cdecl |
| `memset` | Fill memory | cdecl |
| `memchr` | Find character in memory | cdecl |
| `bcmp` | Compare memory (obsolete; use memcmp) | cdecl |
| `bcopy` | Copy memory (obsolete; use memmove) | cdecl |
| `bzero` | Fill memory with zeros (obsolete; use memset) | cdecl |
| `index` | Find character in string (obsolete; use strchr) | cdecl |
| `rindex` | Find last character in string (obsolete; use strrchr) | cdecl |

---
### **Directory Operations (dirent.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `opendir` | Open a directory | cdecl |
| `readdir` | Read a directory entry | cdecl |
| `readdir_r` | Read a directory entry (reentrant) | cdecl |
| `telldir` | Get directory stream position | cdecl |
| `seekdir` | Set directory stream position | cdecl |
| `rewinddir` | Reset directory stream | cdecl |
| `closedir` | Close a directory | cdecl |
| `scandir` | Scan a directory | cdecl |
| `alphasort` | Sort directory entries alphabetically | cdecl |
| `versionsort` | Sort directory entries by version | cdecl |

---
### **Networking (sys/socket.h, netinet/in.h, arpa/inet.h, netdb.h)**

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `socket` | Create a socket | cdecl |
| `bind` | Bind a socket to an address | cdecl |
| `connect` | Connect a socket | cdecl |
| `listen` | Listen for connections | cdecl |
| `accept` | Accept a connection | cdecl |
| `send` | Send data on a socket | cdecl |
| `recv` | Receive data from a socket | cdecl |
| `sendto` | Send data to a specific address | cdecl |
| `recvfrom` | Receive data from a specific address | cdecl |
| `sendmsg` | Send a message on a socket | cdecl |
| `recvmsg` | Receive a message from a socket | cdecl |
| `shutdown` | Shut down a socket | cdecl |
| `getsockname` | Get socket name | cdecl |
| `getpeername` | Get peer name | cdecl |
| `socketpair` | Create a pair of connected sockets | cdecl |
| `setsockopt` | Set socket options | cdecl |
| `getsockopt` | Get socket options | cdecl |
| `fcntl` | File control | cdecl |
| `ioctl` | I/O control | cdecl |
| `htonl` | Host to network long | cdecl |
| `htons` | Host to network short | cdecl |
| `ntohl` | Network to host long | cdecl |
| `ntohs` | Network to host short | cdecl |
| `inet_addr` | Convert IPv4 address from dotted-decimal to binary | cdecl |
| `inet_aton` | Convert IPv4 address from dotted-decimal to binary | cdecl |
| `inet_ntoa` | Convert IPv4 address from binary to dotted-decimal | cdecl |
| `inet_pton` | Convert IPv4/IPv6 address from text to binary | cdecl |
| `inet_ntop` | Convert IPv4/IPv6 address from binary to text | cdecl |
| `gethostbyname` | Get host by name | cdecl |
| `gethostbyaddr` | Get host by address | cdecl |
| `getservbyname` | Get service by name | cdecl |
| `getservbyport` | Get service by port | cdecl |
| `getprotobyname` | Get protocol by name | cdecl |
| `getprotobynumber` | Get protocol by number | cdecl |

---
### **Threading (pthread.h)**
*(POSIX threads)*

| Function | Description | Calling Convention |
|----------|-------------|-------------------|
| `pthread_create` | Create a thread | cdecl |
| `pthread_join` | Join a thread | cdecl |
| `pthread_detach` | Detach a thread | cdecl |
| `pthread_exit` | Exit a thread | cdecl |
| `pthread_cancel` | Cancel a thread | cdecl |
| `pthread_testcancel` | Test for cancellation | cdecl |
| `pthread_setcancelstate` | Set cancellation state | cdecl |
| `pthread_setcanceltype` | Set cancellation type | cdecl |
| `pthread_cleanup_push` | Push cleanup handler | cdecl |
| `pthread_cleanup_pop` | Pop cleanup handler | cdecl |
| `pthread_mutex_init` | Initialize a mutex | cdecl |
| `pthread_mutex_destroy` | Destroy a mutex | cdecl |
| `pthread_mutex_lock` | Lock a mutex | cdecl |
| `pthread_mutex_trylock` | Try to lock a mutex | cdecl |
| `pthread_mutex_unlock` | Unlock a mutex | cdecl |
| `pthread_mutex_timedlock` | Lock a mutex with timeout | cdecl |
| `pthread_cond_init` | Initialize a condition variable | cdecl |
| `pthread_cond_destroy` | Destroy a condition variable | cdecl |
| `pthread_cond_signal` | Signal a condition variable | cdecl |
| `pthread_cond_broadcast` | Broadcast a condition variable | cdecl |
| `pthread_cond_wait` | Wait on a condition variable | cdecl |
| `pthread_cond_timedwait` | Wait on a condition variable with timeout | cdecl |
| `pthread_rwlock_init` | Initialize a read-write lock | cdecl |
| `pthread_rwlock_destroy` | Destroy a read-write lock | cdecl |
| `pthread_rwlock_rdlock` | Lock a read-write lock for reading | cdecl |
| `pthread_rwlock_tryrdlock` | Try to lock a read-write lock for reading | cdecl |
| `pthread_rwlock_wrlock` | Lock a read-write lock for writing | cdecl |
| `pthread_rwlock_trywrlock` | Try to lock a read-write lock for writing | cdecl |
| `pthread_rwlock_unlock` | Unlock a read-write lock | cdecl |
| `pthread_barrier_init` | Initialize a barrier | cdecl |
| `pthread_barrier_destroy` | Destroy a barrier | cdecl |
| `pthread_barrier_wait` | Wait on a barrier | cdecl |
| `pthread_key_create` | Create a thread-specific storage key | cdecl |
| `pthread_key_delete` | Delete a thread-specific storage key | cdecl |
| `pthread_setspecific` | Set thread-specific storage | cdecl |
| `pthread_getspecific` | Get thread-specific storage | cdecl |
| `pthread_once` | Execute a function once | cdecl |

---
---
---
## **7. Assembler Directives**
*(Pseudo-ops for assemblers like NASM, GAS, MASM)*

---

### **NASM Directives (x86/x86-64)**

| Directive | Description |
|-----------|-------------|
| `section .text` | Define text (code) section |
| `section .data` | Define data section |
| `section .bss` | Define uninitialized data section |
| `section .rodata` | Define read-only data section |
| `section .comment` | Define comment section |
| `section .note` | Define note section |
| `global label` | Make a label global (visible to linker) |
| `extern label` | Declare an external label |
| `label:` | Define a label |
| `db` | Define byte(s) |
| `dw` | Define word(s) (2 bytes) |
| `dd` | Define doubleword(s) (4 bytes) |
| `dq` | Define quadword(s) (8 bytes) |
| `dt` | Define ten bytes (80-bit) |
| `resb n` | Reserve n bytes (uninitialized) |
| `resw n` | Reserve n words (uninitialized) |
| `resd n` | Reserve n doublewords (uninitialized) |
| `resq n` | Reserve n quadwords (uninitialized) |
| `rest n` | Reserve n ten-byte values (uninitialized) |
| `equ` | Define a constant |
| `times n` | Repeat the following n times |
| `incbin "file"` | Include binary file |
| `include "file"` | Include source file |
| `%include "file"` | Include source file (same as include) |
| `%define name value` | Define a single-line macro |
| `%xdefine name value` | Define a multi-line macro |
| `%undef name` | Undefine a macro |
| `%if expr` | Conditional assembly (if) |
| `%elif expr` | Conditional assembly (else if) |
| `%else` | Conditional assembly (else) |
| `%endif` | End conditional assembly |
| `%rep n` | Repeat block n times |
| `%endrep` | End repeat block |
| `%assign name expr` | Assign a value to a local variable |
| `%warning msg` | Emit a warning |
| `%error msg` | Emit an error |
| `%fatal msg` | Emit a fatal error |
| `strict` | Enable strict mode |
| `bits 16` | Set 16-bit mode |
| `bits 32` | Set 32-bit mode |
| `bits 64` | Set 64-bit mode |
| `cpu` | Specify CPU type |
| `org` | Set origin (location counter) |
| `align n` | Align to n-byte boundary |
| `align n, fill` | Align to n-byte boundary with fill byte |
| `use16` | Use 16-bit mode (same as bits 16) |
| `use32` | Use 32-bit mode (same as bits 32) |
| `use64` | Use 64-bit mode (same as bits 64) |
| `[label]` | Local label |
| `default` | Set default for certain directives |
| `segment` | Define segment (same as section) |
| `absolute` | Use absolute addressing |
| `extern` | Declare an external symbol |
| `common` | Declare a common symbol |
| `weak` | Declare a weak symbol |
| `group` | Define a group |

---
### **GAS Directives (GNU Assembler, AT&T Syntax)**

| Directive | Description |
|-----------|-------------|
| `.text` | Define text (code) section |
| `.data` | Define data section |
| `.bss` | Define uninitialized data section |
| `.rodata` | Define read-only data section |
| `.comment` | Define comment section |
| `.note` | Define note section |
| `.section name, flags` | Define a section with flags |
| `.globl symbol` | Make a symbol global |
| `.local symbol` | Make a symbol local |
| `.weak symbol` | Make a symbol weak |
| `.hidden symbol` | Make a symbol hidden |
| `.type symbol, type` | Set symbol type (function, object, etc.) |
| `.size symbol, size` | Set symbol size |
| `.equiv symbol, value` | Define an equivalent symbol |
| `.equ symbol, value` | Define a constant (same as .equiv) |
| `.set symbol, value` | Define a variable symbol |
| `.asciz "string"` | Define a null-terminated string |
| `.ascii "string"` | Define a string (no null terminator) |
| `.byte expr1, expr2, ...` | Define byte(s) |
| `.word expr1, expr2, ...` | Define word(s) (2 bytes) |
| `.long expr1, expr2, ...` | Define long(s) (4 bytes) |
| `.quad expr1, expr2, ...` | Define quadword(s) (8 bytes) |
| `.octa expr1, expr2, ...` | Define octaword(s) (16 bytes) |
| `.single expr1, expr2, ...` | Define single-precision float(s) |
| `.double expr1, expr2, ...` | Define double-precision float(s) |
| `.p2align n` | Align to 2^n-byte boundary |
| `.p2align n, fill` | Align to 2^n-byte boundary with fill byte |
| `.align n` | Align to n-byte boundary |
| `.fill n, size, value` | Fill n bytes with value (size bytes each) |
| `.space n` | Reserve n bytes (uninitialized) |
| `.skip n` | Reserve n bytes (uninitialized, same as .space) |
| `.comm symbol, size` | Declare a common symbol |
| `.lcomm symbol, size` | Declare a local common symbol |
| `.if expr` | Conditional assembly (if) |
| `.else` | Conditional assembly (else) |
| `.endif` | End conditional assembly |
| `.rept n` | Repeat block n times |
| `.endr` | End repeat block |
| `.macro name args` | Define a macro |
| `.endm` | End macro |
| `.altmacro` | Enable alternative macro syntax |
| `.noaltmacro` | Disable alternative macro syntax |
| `.include "file"` | Include source file |
| `.incbin "file"` | Include binary file |
| `.file "name"` | Set filename for error messages |
| `.line n` | Set line number for error messages |
| `.loc n m` | Set line number and filename |
| `.abort` | Abort assembly |
| `.warning "msg"` | Emit a warning |
| `.error "msg"` | Emit an error |
| `.intel_syntax` | Use Intel syntax |
| `.att_syntax` | Use AT&T syntax |
| `.arch name` | Set architecture |
| `.code16` | Use 16-bit mode |
| `.code32` | Use 32-bit mode |
| `.code64` | Use 64-bit mode |
| `.att_syntax prefix` | Use AT&T syntax with prefix |
| `.att_syntax noprefix` | Use AT&T syntax without prefix |

---
### **MASM Directives (Microsoft Macro Assembler)**

| Directive | Description |
|-----------|-------------|
| `.386` | Enable 386 instructions |
| `.386P` | Enable 386 instructions and protected mode |
| `.486` | Enable 486 instructions |
| `.486P` | Enable 486 instructions and protected mode |
| `.586` | Enable 586 instructions |
| `.586P` | Enable 586 instructions and protected mode |
| `.686` | Enable 686 instructions |
| `.686P` | Enable 686 instructions and protected mode |
| `.XMM` | Enable XMM instructions |
| `.MMX` | Enable MMX instructions |
| `.MODEL memory_model` | Set memory model (SMALL, MEDIUM, COMPACT, LARGE, FLAT, etc.) |
| `.STACK size` | Set stack size |
| `.STACK reserve, commit` | Set stack reserve and commit sizes |
| `.DATA` | Define data section |
| `.DATA?` | Define uninitialized data section |
| `.CODE` | Define code section |
| `.CONST` | Define constant data section |
| `.FARDATA` | Define far data section |
| `.FARDATA?` | Define far uninitialized data section |
| `label:` | Define a label |
| `label EQU expr` | Define a constant |
| `=expr` | Define a numeric constant |
| `DB expr1, expr2, ...` | Define byte(s) |
| `DW expr1, expr2, ...` | Define word(s) (2 bytes) |
| `DD expr1, expr2, ...` | Define doubleword(s) (4 bytes) |
| `DQ expr1, expr2, ...` | Define quadword(s) (8 bytes) |
| `DT expr1, expr2, ...` | Define ten bytes (80-bit) |
| `REPT n` | Repeat block n times |
| `ENDM` | End repeat block |
| `IF expr` | Conditional assembly (if) |
| `IFDEF name` | Conditional assembly (if defined) |
| `IFNDEF name` | Conditional assembly (if not defined) |
| `IFIDN str1, str2` | Conditional assembly (if identical) |
| `IFIDNI str1, str2` | Conditional assembly (if identical, case-insensitive) |
| `IFDIF str1, str2` | Conditional assembly (if different) |
| `IFDIFI str1, str2` | Conditional assembly (if different, case-insensitive) |
| `ELSE` | Conditional assembly (else) |
| `ELSEIF expr` | Conditional assembly (else if) |
| `ENDIF` | End conditional assembly |
| `MACRO name params` | Define a macro |
| `ENDM` | End macro |
| `LOCAL label1, label2, ...` | Define local labels |
| `INVOKE name, args` | Invoke a procedure with arguments |
| `PROC name` | Define a procedure |
| `ENDP` | End procedure |
| `PUBLIC label` | Make a label public |
| `EXTRN label:type` | Declare an external label |
| `INCLUDE filename` | Include source file |
| `INCLUDELIB libname` | Include library file |
| `LIST` | Enable listing |
| `LISTMACRO` | Enable macro expansion in listing |
| `LISTMACROALL` | Enable all macro expansions in listing |
| `NOLIST` | Disable listing |
| `NOLISTMACRO` | Disable macro expansion in listing |
| `SUBTITLE text` | Set subtitle for listing |
| `TITLE text` | Set title for listing |
| `PAGE length, width` | Set page size for listing |
| `PAGE+` | Eject page in listing |
| `.RADIX n` | Set default radix for numbers |
| `.XALL` | List all symbols in cross-reference table |
| `.XCREF` | List symbols in cross-reference table (sorted) |
| `.XLIST` | List symbols in cross-reference table |
| `.NOXREF` | Suppress cross-reference table |
| `.CREF` | Enable cross-reference listing |
| `.NOCREF` | Disable cross-reference listing |
| `COMM name:size` | Declare a common variable |
| `ORG expr` | Set location counter |
| `ALIGN n` | Align to n-byte boundary |
| `EVEN` | Align to even address |
| `ASSUME seg:reg, ...` | Set segment register assumptions |
| `SEGMENT name` | Define a segment |
| `ENDS` | End segment |
| `GROUP name` | Define a group |
| `END` | End assembly |

---
---
---
## **8. Common Macro Libraries and Utilities**

---
### **NASM Macro Library (for x86)**

| Macro | Description |
|-------|-------------|
| `%macro name n` | Define a macro with n parameters |
| `%endmacro` | End macro definition |
| `%push context` | Save macro context |
| `%pop context` | Restore macro context |
| `%local label` | Define a local label |
| `%arg n` | Access macro argument n |
| `%stacksize size` | Set local variable space |
| `%assign name expr` | Assign a value to a local variable |
| `%warning msg` | Emit a warning |
| `%error msg` | Emit an error |
| `%fatal msg` | Emit a fatal error |
| `%if expr` | Conditional assembly |
| `%elif expr` | Else if |
| `%else` | Else |
| `%endif` | End if |
| `%rep n` | Repeat block n times |
| `%endrep` | End repeat |
| `%include "file"` | Include a file |
| `%line n "file"` | Set line number and filename |

---
### **Linux Kernel Macros (for x86)**

| Macro | Description |
|-------|-------------|
| `ENTRY(name)` | Define a kernel entry point |
| `END(name)` | End a kernel entry point |
| `ENDPROC(name)` | End a procedure |
| `SYM_FUNC_START(name)` | Start a function symbol |
| `SYM_FUNC_END(name)` | End a function symbol |
| `SYM_DATA_START(name)` | Start a data symbol |
| `SYM_DATA_END(name)` | End a data symbol |
| `SYM_DATA(name, type)` | Define a data symbol |
| `SYM_CODE_START(name)` | Start a code symbol |
| `SYM_CODE_END(name)` | End a code symbol |

---
### **Common Utility Macros**

| Macro | Description | Example |
|-------|-------------|---------|
| `PUSH_ALL` | Push all general-purpose registers | `PUSH_ALL` |
| `POP_ALL` | Pop all general-purpose registers | `POP_ALL` |
| `SAVE_REGS` | Save registers to stack | `SAVE_REGS` |
| `RESTORE_REGS` | Restore registers from stack | `RESTORE_REGS` |
| `ENTER_FRAME` | Create a stack frame | `ENTER_FRAME` |
| `LEAVE_FRAME` | Remove a stack frame | `LEAVE_FRAME` |
| `PROLOGUE` | Function prologue | `PROLOGUE func` |
| `EPILOGUE` | Function epilogue | `EPILOGUE func` |
| `SYSCALL0 num` | Make a system call with 0 arguments | `SYSCALL0 60` (exit) |
| `SYSCALL1 num, arg1` | Make a system call with 1 argument | `SYSCALL1 1, 42` (write 1 byte) |
| `SYSCALL2 num, arg1, arg2` | Make a system call with 2 arguments | `SYSCALL2 1, 1, buffer` (write to stdout) |
| `SYSCALL3 num, arg1, arg2, arg3` | Make a system call with 3 arguments | `SYSCALL3 0, 0, buffer, 1` (read from stdin) |

---
---
---
## **9. Floating-Point and SIMD Instructions (x86/x86-64)**
*(Additional instructions for floating-point and SIMD operations)*

---
### **x87 FPU Instructions (Continued)**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `FPTAN` | | Compute partial tangent (ST(0) = tan(ST(0)), ST(1) = 1) |
| `FPATAN` | | Compute partial arctangent (ST(0) = arctan(ST(1)/ST(0))) |
| `FYL2X` | | Compute y * log2(x) (ST(0) = ST(1) * log2(ST(0))) |
| `FYL2XP1` | | Compute y * log2(x + 1) (ST(0) = ST(1) * log2(ST(0) + 1)) |
| `F2XM1` | | Compute 2^x - 1 (ST(0) = 2^ST(0) - 1) |
| `FSCALE` | | Scale by power of 2 (ST(0) = ST(0) * 2^ST(1)) |
| `FXTRACT` | | Extract exponent and significand (ST(0) = significand, ST(1) = exponent) |
| `FPREM` | | Partial remainder (ST(0) = ST(0) % ST(1)) |
| `FPREM1` | | IEEE partial remainder (ST(0) = ST(0) % ST(1)) |
| `FYL2X` | | Compute y * log2(x) |
| `FYL2XP1` | | Compute y * log2(x + 1) |
| `FSIN` | | Compute sine (ST(0) = sin(ST(0))) |
| `FCOS` | | Compute cosine (ST(0) = cos(ST(0))) |
| `FSINCOS` | | Compute sine and cosine (ST(0) = cos(ST(0)), ST(1) = sin(ST(0))) |
| `FRNDINT` | | Round to integer (ST(0) = round(ST(0))) |
| `FCHS` | | Change sign (ST(0) = -ST(0)) |
| `FABS` | | Absolute value (ST(0) = |ST(0)|) |
| `FTST` | | Test ST(0) against 0.0 |
| `FXAM` | | Examine ST(0) |
| `FLDENV` | mem | Load FPU environment |
| `FSTENV` | mem | Store FPU environment |
| `FSAVE` | mem | Store FPU state |
| `FRSTOR` | mem | Restore FPU state |
| `FNSTENV` | mem | Store FPU environment (no wait) |
| `FNLDENV` | mem | Load FPU environment (no wait) |
| `FNSTSW` | mem/AX | Store FPU status word |
| `FNSTCW` | mem | Store FPU control word |
| `FLDCW` | mem | Load FPU control word |

---
### **SSE3 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `ADDSUBPS` | xmm, xmm/mem | Alternating add/subtract packed single-precision |
| `ADDSUBPD` | xmm, xmm/mem | Alternating add/subtract packed double-precision |
| `HADDPS` | xmm, xmm/mem | Horizontal add packed single-precision |
| `HADDPD` | xmm, xmm/mem | Horizontal add packed double-precision |
| `HSUBPS` | xmm, xmm/mem | Horizontal subtract packed single-precision |
| `HSUBPD` | xmm, xmm/mem | Horizontal subtract packed double-precision |
| `MOVSHDUP` | xmm, xmm/mem | Move high and duplicate packed single-precision |
| `MOVSLDUP` | xmm, xmm/mem | Move low and duplicate packed single-precision |
| `MOVDDUP` | xmm, xmm/mem | Move and duplicate packed double-precision |
| `LDDQU` | xmm, mem | Load unaligned double quadword |

---
### **SSSE3 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `PSHUFB` | mm/xmm, mm/xmm/mem | Packed shuffle bytes |
| `PSIGNB` | mm/xmm, mm/xmm/mem | Packed sign bytes |
| `PSIGNW` | mm/xmm, mm/xmm/mem | Packed sign words |
| `PSIGND` | mm/xmm, mm/xmm/mem | Packed sign doublewords |
| `PALIGNR` | mm/xmm, mm/xmm/mem, imm8 | Packed align right |
| `PHADDW` | mm/xmm, mm/xmm/mem | Packed horizontal add words |
| `PHSUBW` | mm/xmm, mm/xmm/mem | Packed horizontal subtract words |
| `PHADDSW` | mm/xmm, mm/xmm/mem | Packed horizontal add signed words |
| `PHSUBSW` | mm/xmm, mm/xmm/mem | Packed horizontal subtract signed words |
| `PMADDUBSW` | mm/xmm, mm/xmm/mem | Packed multiply add unsigned byte to signed word |
| `PMAXSB` | xmm, xmm/mem | Packed maximum signed bytes |
| `PMAXSW` | xmm, xmm/mem | Packed maximum signed words |
| `PMAXSD` | xmm, xmm/mem | Packed maximum signed doublewords |
| `PMINSB` | xmm, xmm/mem | Packed minimum signed bytes |
| `PMINSW` | xmm, xmm/mem | Packed minimum signed words |
| `PMINSD` | xmm, xmm/mem | Packed minimum signed doublewords |
| `PMULHRSW` | xmm, xmm/mem | Packed multiply high with round and scale words |
| `PSHUFB` | xmm, xmm/mem | Packed shuffle bytes |
| `PSIGNB` | xmm, xmm/mem | Packed sign bytes |
| `PSIGNW` | xmm, xmm/mem | Packed sign words |
| `PSIGND` | xmm, xmm/mem | Packed sign doublewords |

---
### **SSE4.1 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `BLENDPS` | xmm, xmm/mem, imm8 | Blend packed single-precision |
| `BLENDPD` | xmm, xmm/mem, imm8 | Blend packed double-precision |
| `BLENDVPS` | xmm, xmm/mem, xmm0 | Variable blend packed single-precision |
| `BLENDVPD` | xmm, xmm/mem, xmm0 | Variable blend packed double-precision |
| `PBLENDVB` | xmm, xmm/mem, xmm0 | Variable blend packed bytes |
| `PMINSB` | xmm, xmm/mem | Packed minimum signed bytes |
| `PMAXSB` | xmm, xmm/mem | Packed maximum signed bytes |
| `PMINSW` | xmm, xmm/mem | Packed minimum signed words |
| `PMAXSW` | xmm, xmm/mem | Packed maximum signed words |
| `PMINSD` | xmm, xmm/mem | Packed minimum signed doublewords |
| `PMAXSD` | xmm, xmm/mem | Packed maximum signed doublewords |
| `PMINUW` | xmm, xmm/mem | Packed minimum unsigned words |
| `PMAXUW` | xmm, xmm/mem | Packed maximum unsigned words |
| `PMULLD` | xmm, xmm/mem | Packed multiply dwords |
| `PMULDQ` | xmm, xmm/mem | Packed multiply quadwords |
| `DMUL` | xmm, xmm/mem | Double-precision multiply |
| `DMULQ` | xmm, xmm/mem | Double-precision multiply quadwords |
| `EXTRQ` | xmm, xmm, imm8 | Extract packed quadwords |
| `INSERTPS` | xmm, xmm/mem, imm8 | Insert packed single-precision |
| `INSERTQ` | xmm, xmm/mem, imm8 | Insert packed quadwords |
| `MOVNTDQA` | xmm, mem | Non-temporal load aligned double quadword |
| `MOVNTDQ` | mem, xmm | Non-temporal store double quadword |
| `MOVNTQA` | xmm, mem | Non-temporal load aligned quadword (MMX) |
| `MOVNTQ` | mem, mm | Non-temporal store quadword (MMX) |
| `PACKUSDW` | xmm, xmm/mem | Pack unsigned with signed saturation words to dwords |
| `PBLENDVB` | xmm, xmm/mem | Packed blend variable bytes |
| `PBLENDW` | xmm, xmm/mem, imm8 | Packed blend words |
| `PMAXSB` | xmm, xmm/mem | Packed maximum signed bytes |
| `PMAXSD` | xmm, xmm/mem | Packed maximum signed doublewords |
| `PMAXUD` | xmm, xmm/mem | Packed maximum unsigned doublewords |
| `PMAXUW` | xmm, xmm/mem | Packed maximum unsigned words |
| `PMINSB` | xmm, xmm/mem | Packed minimum signed bytes |
| `PMINSD` | xmm, xmm/mem | Packed minimum signed doublewords |
| `PMINUD` | xmm, xmm/mem | Packed minimum unsigned doublewords |
| `PMINUW` | xmm, xmm/mem | Packed minimum unsigned words |
| `PMULDQ` | xmm, xmm/mem | Packed multiply dwords |
| `PMULLD` | xmm, xmm/mem | Packed multiply dwords |
| `PTEST` | xmm, xmm/mem | Packed test |
| `ROUNDPS` | xmm, xmm/mem, imm8 | Round packed single-precision |
| `ROUNDPD` | xmm, xmm/mem, imm8 | Round packed double-precision |
| `ROUNDSS` | xmm, xmm/mem, imm8 | Round scalar single-precision |
| `ROUNDSD` | xmm, xmm/mem, imm8 | Round scalar double-precision |

---
### **SSE4.2 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `CRC32` | reg, reg/mem | Compute CRC32 checksum |
| `PCMPGTQ` | xmm, xmm/mem | Packed compare greater than quadwords |
| `PCMPEQQ` | xmm, xmm/mem | Packed compare equal quadwords |
| `POPCNT` | reg, reg/mem | Count number of bits set |
| `EXTRQ` | xmm, xmm, imm8 | Extract packed quadwords |
| `INSERTQ` | xmm, xmm/mem, imm8 | Insert packed quadwords |
| `MOVNTDQA` | xmm, mem | Non-temporal load aligned double quadword |
| `MOVNTDQ` | mem, xmm | Non-temporal store double quadword |

---
### **AVX2 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `VPBROADCASTB` | xmm/ymm, mem | Broadcast byte |
| `VPBROADCASTW` | xmm/ymm, mem | Broadcast word |
| `VPBROADCASTD` | xmm/ymm, mem | Broadcast doubleword |
| `VPBROADCASTQ` | xmm/ymm, mem | Broadcast quadword |
| `VPERM2I128` | ymm, ymm, ymm/mem, imm8 | Permute 128-bit integers |
| `VPERMQ` | ymm, ymm/mem, imm8 | Permute quadwords |
| `VPERMD` | ymm, ymm, ymm/mem | Permute doublewords |
| `VPSLLVD` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift left logical doublewords |
| `VPSRLVD` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift right logical doublewords |
| `VPSRAVD` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift right arithmetic doublewords |
| `VPGATHERDD` | xmm/ymm, mem_base, xmm/ymm_index | Gather doublewords |
| `VPGATHERQD` | xmm/ymm, mem_base, xmm/ymm_index | Gather quadwords to doublewords |
| `VPGATHERDQ` | xmm/ymm, mem_base, xmm/ymm_index | Gather doublewords to quadwords |
| `VPGATHERQQ` | xmm/ymm, mem_base, xmm/ymm_index | Gather quadwords |
| `VPSLLVQ` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift left logical quadwords |
| `VPSRLVQ` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift right logical quadwords |
| `VPSRAVQ` | xmm/ymm, xmm/ymm, xmm/ymm/mem | Variable shift right arithmetic quadwords |
| `VPMASKMOV` | mem, mask, xmm/ymm | Store selected bytes from xmm/ymm to memory |
| `VPMASKMOVD` | mem, mask, xmm/ymm | Store selected doublewords from xmm/ymm to memory |
| `VPMASKMOVQ` | mem, mask, xmm/ymm | Store selected quadwords from xmm/ymm to memory |

---
### **AVX-512 Instructions**

| Instruction | Operands | Description |
|-------------|----------|-------------|
| `VPBROADCASTB` | zmm, mem | Broadcast byte to all elements in ZMM |
| `VPBROADCASTW` | zmm, mem | Broadcast word to all elements in ZMM |
| `VPBROADCASTD` | zmm, mem | Broadcast doubleword to all elements in ZMM |
| `VPBROADCASTQ` | zmm, mem | Broadcast quadword to all elements in ZMM |
| `VPBROADCASTMB2M` | k, mem | Broadcast byte to mask register |
| `VPBROADCASTMW2M` | k, mem | Broadcast word to mask register |
| `VPBROADCASTMW2M` | k, mem | Broadcast doubleword to mask register |
| `VPBROADCASTMQ2M` | k, mem | Broadcast quadword to mask register |
| `VEXPANDPS` | zmm, mask, zmm/mem | Expand packed single-precision floating-point |
| `VEXPANDPD` | zmm, mask, zmm/mem | Expand packed double-precision floating-point |
| `VCOMPRESSPS` | mem, mask, zmm | Compress packed single-precision floating-point |
| `VCOMPRESSPD` | mem, mask, zmm | Compress packed double-precision floating-point |
| `VPMOVDB2M` | k, zmm | Move doublewords from ZMM to mask register |
| `VPMOVQB2M` | k, zmm | Move quadwords from ZMM to mask register |
| `VPMOVM2B` | zmm, k | Move mask register to bytes in ZMM |
| `VPMOVM2W` | zmm, k | Move mask register to words in ZMM |
| `VPMOVM2D` | zmm, k | Move mask register to doublewords in ZMM |
| `VPMOVM2Q` | zmm, k | Move mask register to quadwords in ZMM |
| `VSCATTERDPS` | mem, mask, zmm | Scatter packed single-precision floating-point |
| `VSCATTERDPD` | mem, mask, zmm | Scatter packed double-precision floating-point |
| `VSCATTERQPS` | mem, mask, zmm | Scatter quadwords to packed single-precision floating-point |
| `VSCATTERQPD` | mem, mask, zmm | Scatter quadwords to packed double-precision floating-point |
| `VSCATTERDPS` | mem, mask, zmm | Scatter doublewords to packed single-precision floating-point |
| `VSCATTERDPD` | mem, mask, zmm | Scatter doublewords to packed double-precision floating-point |
| `VEXP2PS` | zmm, zmm/mem | Exponential base 2 of packed single-precision floating-point |
| `VEXP2PD` | zmm, zmm/mem | Exponential base 2 of packed double-precision floating-point |
| `VRCPPPS` | zmm, zmm/mem | Reciprocal of packed single-precision floating-point |
| `VRCPPPD` | zmm, zmm/mem | Reciprocal of packed double-precision floating-point |
| `VRSQRT14PS` | zmm, zmm/mem | Reciprocal square root (14-bit precision) packed single-precision |
| `VRSQRT14PD` | zmm, zmm/mem | Reciprocal square root (14-bit precision) packed double-precision |
| `VRSQRT28PS` | zmm, zmm/mem | Reciprocal square root (28-bit precision) packed single-precision |
| `VRSQRT28PD` | zmm, zmm/mem | Reciprocal square root (28-bit precision) packed double-precision |

---
---
---
## **10. Common Assembler Pseudo-Ops and Utilities**

---
### **Common Pseudo-Operations (All Assemblers)**

| Pseudo-Op | Description | Example |
|-----------|-------------|---------|
| `ORG address` | Set location counter | `ORG 0x1000` |
| `ALIGN n` | Align to n-byte boundary | `ALIGN 4` |
| `EQU symbol, value` | Define a constant | `MAX_SIZE EQU 1024` |
| `=value` | Define a numeric constant | `COUNT = 0` |
| `DB byte1, byte2, ...` | Define byte(s) | `DB 0x48, 0x65, 0x6C, 0x6C, 0x6F` |
| `DW word1, word2, ...` | Define word(s) | `DW 0x1234, 0x5678` |
| `DD dword1, dword2, ...` | Define doubleword(s) | `DD 0xDEADBEEF, 0xCAFEBABE` |
| `DQ qword1, qword2, ...` | Define quadword(s) | `DQ 0x123456789ABCDEF0` |
| `RESB n` | Reserve n bytes | `RESB 1024` |
| `RESW n` | Reserve n words | `RESW 256` |
| `RESD n` | Reserve n doublewords | `RESD 64` |
| `RESB n` | Reserve n quadwords | `RESQ 16` |
| `ASCII "string"` | Define ASCII string | `ASCII "Hello"` |
| `ASCIZ "string"` | Define null-terminated ASCII string | `ASCIZ "Hello"` |
| `INCLUDE "file"` | Include source file | `INCLUDE "macros.inc"` |
| `INCBIN "file"` | Include binary file | `INCBIN "data.bin"` |
| `MACRO name params` | Define a macro | `MACRO print_str str` |
| `ENDM` | End macro | `ENDM` |
| `IF expr` | Conditional assembly | `IF DEBUG` |
| `ELSE` | Else | `ELSE` |
| `ENDIF` | End if | `ENDIF` |
| `REPT n` | Repeat block n times | `REPT 10` |
| `ENDM` | End repeat | `ENDM` |
| `LOCAL label` | Define local label | `LOCAL .loop` |
| `GLOBL label` | Make label global | `GLOBL _start` |
| `EXTERN label` | Declare external label | `EXTERN printf` |
| `COMMON label, size` | Declare common symbol | `COMMON buffer, 1024` |

---
---
---
## **11. Summary of Calling Conventions**
*(How arguments are passed to functions in different architectures and OSes)*

---
### **x86 (32-bit) Calling Conventions**

| Convention | Registers Used | Stack Cleanup | Return Value | Notes |
|------------|----------------|---------------|--------------|-------|
| **cdecl** | None (all args on stack) | Caller | EAX | C standard. Args right-to-left. |
| **stdcall** | None (all args on stack) | Callee | EAX | Windows API. Args right-to-left. |
| **fastcall** | ECX, EDX | Caller | EAX | First two args in ECX, EDX. Rest on stack. |
| **thiscall** | ECX (this pointer) | Callee | EAX | C++ member functions. Args right-to-left. |
| **pascal** | None (all args on stack) | Callee | EAX | Args left-to-right. |
| **regparm(n)** | EAX, EDX, ECX (n=1,2,3) | Caller | EAX | Linux. First n args in registers. |

---
### **x86-64 Calling Conventions**

| Convention | Registers Used | Stack Cleanup | Return Value | Notes |
|------------|----------------|---------------|--------------|-------|
| **System V AMD64** (Linux, macOS) | RDI, RSI, RDX, RCX, R8, R9 | Caller | RAX, RDX | First 6 args in registers. Rest on stack. |
| **Microsoft x64** (Windows) | RCX, RDX, R8, R9 | Caller | RAX | First 4 args in registers. Rest on stack. |
| **Win64** | RCX, RDX, R8, R9 | Caller | RAX | Same as Microsoft x64. |
| **Linux x64** | RDI, RSI, RDX, RCX, R8, R9 | Caller | RAX, RDX | Same as System V AMD64. |

---
### **ARM Calling Conventions**

| Convention | Registers Used | Stack Cleanup | Return Value | Notes |
|------------|----------------|---------------|--------------|-------|
| **ARM (32-bit)** | R0-R3 | Caller | R0 | First 4 args in R0-R3. Rest on stack. |
| **Thumb** | R0-R3 | Caller | R0 | Same as ARM. |
| **AAPCS (ARM Architecture Procedure Call Standard)** | R0-R3 | Caller | R0 | Standard for ARM. |
| **AAPCS-VFP** | R0-R3, S0-S15 | Caller | R0, S0-S15 | Floating-point args in S0-S15. |
| **AArch64 (64-bit)** | X0-X7 | Caller | X0 | First 8 args in X0-X7. Rest on stack. |

---
### **MIPS Calling Conventions**

| Convention | Registers Used | Stack Cleanup | Return Value | Notes |
|------------|----------------|---------------|--------------|-------|
| **O32** | $4-$7 ($a0-$a3) | Caller | $2-$3 ($v0-$v1) | 32-bit. First 4 args in $a0-$a3. |
| **N32** | $4-$7 ($a0-$a3) | Caller | $2-$3 ($v0-$v1) | 64-bit. Similar to O32. |
| **N64** | $4-$11 ($a0-$a7) | Caller | $2-$3 ($v0-$v1) | 64-bit. First 8 args in $a0-$a7. |
| **EABI** | $4-$7 ($a0-$a3) | Caller | $2-$3 ($v0-$v1) | Embedded ABI. |

---
### **RISC-V Calling Conventions**

| Convention | Registers Used | Stack Cleanup | Return Value | Notes |
|------------|----------------|---------------|--------------|-------|
| **RV32I** | a0-a7 (x10-x17) | Caller | a0 (x10) | First 8 args in a0-a7. Rest on stack. |
| **RV64I** | a0-a7 (x10-x17) | Caller | a0 (x10), a1 (x11) | First 8 args in a0-a7. 128-bit return in a0:a1. |

---
---
---
## **12. Common Data Structures and Constants**

---
### **x86 Segment Registers**

| Register | Description |
|----------|-------------|
| `CS` | Code Segment |
| `DS` | Data Segment |
| `ES` | Extra Segment |
| `SS` | Stack Segment |
| `FS` | F Segment |
| `GS` | G Segment |

---
### **x86 General-Purpose Registers (32-bit)**

| Register | Description | Alternative Name |
|----------|-------------|-----------------|
| `EAX` | Accumulator | AX, AH, AL |
| `EBX` | Base | BX, BH, BL |
| `ECX` | Counter | CX, CH, CL |
| `EDX` | Data | DX, DH, DL |
| `ESI` | Source Index | SI |
| `EDI` | Destination Index | DI |
| `EBP` | Base Pointer | BP |
| `ESP` | Stack Pointer | SP |

---
### **x86 General-Purpose Registers (64-bit)**

| Register | Description | Alternative Name |
|----------|-------------|-----------------|
| `RAX` | Accumulator | EAX, AX, AH, AL |
| `RBX` | Base | EBX, BX, BH, BL |
| `RCX` | Counter | ECX, CX, CH, CL |
| `RDX` | Data | EDX, DX, DH, DL |
| `RSI` | Source Index | ESI, SI |
| `RDI` | Destination Index | EDI, DI |
| `RBP` | Base Pointer | EBP, BP |
| `RSP` | Stack Pointer | ESP, SP |
| `R8` | General-purpose | R8D, R8W, R8B |
| `R9` | General-purpose | R9D, R9W, R9B |
| `R10` | General-purpose | R10D, R10W, R10B |
| `R11` | General-purpose | R11D, R11W, R11B |
| `R12` | General-purpose | R12D, R12W, R12B |
| `R13` | General-purpose | R13D, R13W, R13B |
| `R14` | General-purpose | R14D, R14W, R14B |
| `R15` | General-purpose | R15D, R15W, R15B |

---
### **x86 Control Registers**

| Register | Description |
|----------|-------------|
| `CR0` | Control Register 0 (flags: PE, MP, EM, TS, ET, NE, WP, AM, NW, CD, PG) |
| `CR1` | Control Register 1 (reserved) |
| `CR2` | Page Fault Linear Address |
| `CR3` | Page Directory Base Register |
| `CR4` | Control Register 4 (SMEP, SMAP, PKE, etc.) |
| `CR8` | Task Priority Register (x86-64) |

---
### **x86 Debug Registers**

| Register | Description |
|----------|-------------|
| `DR0` | Debug Address Register 0 |
| `DR1` | Debug Address Register 1 |
| `DR2` | Debug Address Register 2 |
| `DR3` | Debug Address Register 3 |
| `DR4` | Debug Address Register 4 (reserved) |
| `DR5` | Debug Address Register 5 (reserved) |
| `DR6` | Debug Status Register |
| `DR7` | Debug Control Register |

---
### **x86 EFLAGS Register Flags**

| Flag | Bit | Description |
|------|-----|-------------|
| `CF` | 0 | Carry Flag |
| `PF` | 2 | Parity Flag |
| `AF` | 4 | Auxiliary Carry Flag |
| `ZF` | 6 | Zero Flag |
| `SF` | 7 | Sign Flag |
| `TF` | 8 | Trap Flag |
| `IF` | 9 | Interrupt Enable Flag |
| `DF` | 10 | Direction Flag |
| `OF` | 11 | Overflow Flag |
| `IOPL` | 12-13 | I/O Privilege Level |
| `NT` | 14 | Nested Task Flag |
| `RF` | 16 | Resume Flag |
| `VM` | 17 | Virtual-8086 Mode Flag |
| `AC` | 18 | Alignment Check Flag |
| `VIF` | 19 | Virtual Interrupt Flag |
| `VIP` | 20 | Virtual Interrupt Pending Flag |
| `ID` | 21 | Identification Flag |

---
### **ARM Registers (32-bit)**

| Register | Description | Alternative Name |
|----------|-------------|-----------------|
| `R0-R12` | General-purpose registers | |
| `R13` | Stack Pointer | SP |
| `R14` | Link Register | LR |
| `R15` | Program Counter | PC |
| `CPSR` | Current Program Status Register | |
| `SPSR` | Saved Program Status Register | |
| `APSR` | Application Program Status Register | |
| `IPSR` | Interrupt Program Status Register | |
| `EPSR` | Execution Program Status Register | |
| `IEPSR` | Interruptable Execution Program Status Register | |
| `MSP` | Main Stack Pointer | |
| `PSP` | Process Stack Pointer | |
| `MSP_LIMIT` | Main Stack Pointer Limit | |
| `PSP_LIMIT` | Process Stack Pointer Limit | |

---
### **AArch64 Registers (64-bit)**

| Register | Description | Alternative Name |
|----------|-------------|-----------------|
| `X0-X30` | General-purpose registers (64-bit) | |
| `X31` | Stack Pointer or Zero Register | SP or XZR |
| `W0-W30` | General-purpose registers (32-bit) | |
| `W31` | Zero Register | WZR |
| `PC` | Program Counter | |
| `SP` | Stack Pointer | |
| `ELR` | Exception Link Register | |
| `SPSR` | Saved Program Status Register | |
| `DAIF` | Debug, Asynchronous, Interrupt, Fiq flags | |
| `FP` | Frame Pointer | X29 |
| `LR` | Link Register | X30 |
| `NZCV` | Negative, Zero, Carry, oVerflow flags | |
| `FPSR` | Floating-Point Status Register | |
| `FPCR` | Floating-Point Control Register | |

---
### **MIPS Registers (32-bit)**

| Register | Number | Description | Alternative Name |
|----------|--------|-------------|-----------------|
| `$0` | 0 | Zero | |
| `$at` | 1 | Assembler Temporary | |
| `$v0` | 2 | Return Value 0 | |
| `$v1` | 3 | Return Value 1 | |
| `$a0` | 4 | Argument 0 | |
| `$a1` | 5 | Argument 1 | |
| `$a2` | 6 | Argument 2 | |
| `$a3` | 7 | Argument 3 | |
| `$t0` | 8 | Temporary 0 | |
| `$t1` | 9 | Temporary 1 | |
| `$t2` | 10 | Temporary 2 | |
| `$t3` | 11 | Temporary 3 | |
| `$t4` | 12 | Temporary 4 | |
| `$t5` | 13 | Temporary 5 | |
| `$t6` | 14 | Temporary 6 | |
| `$t7` | 15 | Temporary 7 | |
| `$s0` | 16 | Saved 0 | |
| `$s1` | 17 | Saved 1 | |
| `$s2` | 18 | Saved 2 | |
| `$s3` | 19 | Saved 3 | |
| `$s4` | 20 | Saved 4 | |
| `$s5` | 21 | Saved 5 | |
| `$s6` | 22 | Saved 6 | |
| `$s7` | 23 | Saved 7 | |
| `$t8` | 24 | Temporary 8 | |
| `$t9` | 25 | Temporary 9 | |
| `$k0` | 26 | Kernel 0 | |
| `$k1` | 27 | Kernel 1 | |
| `$gp` | 28 | Global Pointer | |
| `$sp` | 29 | Stack Pointer | |
| `$fp` | 30 | Frame Pointer | |
| `$ra` | 31 | Return Address | |

---
### **MIPS Registers (64-bit)**

| Register | Number | Description | Alternative Name |
|----------|--------|-------------|-----------------|
| `$0` | 0 | Zero | |
| `$at` | 1 | Assembler Temporary | |
| `$v0` | 2 | Return Value 0 | |
| `$v1` | 3 | Return Value 1 | |
| `$a0` | 4 | Argument 0 | |
| `$a1` | 5 | Argument 1 | |
| `$a2` | 6 | Argument 2 | |
| `$a3` | 7 | Argument 3 | |
| `$a4` | 8 | Argument 4 | |
| `$a5` | 9 | Argument 5 | |
| `$a6` | 10 | Argument 6 | |
| `$a7` | 11 | Argument 7 | |
| `$t0` | 12 | Temporary 0 | |
| `$t1` | 13 | Temporary 1 | |
| `$t2` | 14 | Temporary 2 | |
| `$t3` | 15 | Temporary 3 | |
| `$t4` | 16 | Temporary 4 | |
| `$t5` | 17 | Temporary 5 | |
| `$t6` | 18 | Temporary 6 | |
| `$t7` | 19 | Temporary 7 | |
| `$s0` | 20 | Saved 0 | |
| `$s1` | 21 | Saved 1 | |
| `$s2` | 22 | Saved 2 | |
| `$s3` | 23 | Saved 3 | |
| `$s4` | 24 | Saved 4 | |
| `$s5` | 25 | Saved 5 | |
| `$s6` | 26 | Saved 6 | |
| `$s7` | 27 | Saved 7 | |
| `$t8` | 28 | Temporary 8 | |
| `$t9` | 29 | Temporary 9 | |
| `$k0` | 30 | Kernel 0 | |
| `$k1` | 31 | Kernel 1 | |
| `$gp` | 28 | Global Pointer | |
| `$sp` | 29 | Stack Pointer | |
| `$fp` | 30 | Frame Pointer | |
| `$ra` | 31 | Return Address | |

---
### **RISC-V Registers (RV32I/RV64I)**

| Register | Number | Description | Alternative Name |
|----------|--------|-------------|-----------------|
| `x0` | 0 | Zero | |
| `x1` | 1 | Return Address | ra |
| `x2` | 2 | Stack Pointer | sp |
| `x3` | 3 | Global Pointer | gp |
| `x4` | 4 | Thread Pointer | tp |
| `x5-x7` | 5-7 | Temporary Registers | t0-t2 |
| `x8` | 8 | Saved Register / Frame Pointer | s0/fp |
| `x9` | 9 | Saved Register | s1 |
| `x10-x11` | 10-11 | Function Arguments / Return Values | a0-a1 |
| `x12-x17` | 12-17 | Function Arguments | a2-a7 |
| `x18-x27` | 18-27 | Saved Registers | s2-s11 |
| `x28-x31` | 28-31 | Temporary Registers | t3-t6 |

---
---
---
## **13. Common Assembler Examples**

---
### **x86-64 Linux: Hello, World! (NASM Syntax)**
```assembly
section .data
    msg db 'Hello, World!', 0xA
    len equ $ - msg

section .text
    global _start

_start:
    ; Write to stdout
    mov rax, 1          ; sys_write
    mov rdi, 1          ; fd = stdout
    mov rsi, msg        ; buffer
    mov rdx, len        ; length
    syscall

    ; Exit
    mov rax, 60         ; sys_exit
    xor rdi, rdi        ; status = 0
    syscall
```

---
### **x86-64 Linux: Hello, World! (GAS Syntax)**
```assembly
.section .data
msg:
    .ascii "Hello, World!\n"
    len = . - msg

.section .text
.global _start

_start:
    ; Write to stdout
    mov $1, %rax        ; sys_write
    mov $1, %rdi        ; fd = stdout
    mov $msg, %rsi      ; buffer
    mov $len, %rdx      ; length
    syscall

    ; Exit
    mov $60, %rax       ; sys_exit
    xor %rdi, %rdi      ; status = 0
    syscall
```

---
### **x86-64 Windows: Hello, World! (MASM Syntax)**
```assembly
.386
.model flat, stdcall
option casemap:none

include \masm32\include\windows.inc
include \masm32\include\kernel32.inc
include \masm32\include\masm32.inc
includelib \masm32\lib\kernel32.lib
includelib \masm32\lib\masm32.lib

.data
    msg db 'Hello, World!', 0Ah, 0

.code
start:
    ; Write to stdout
    invoke WriteFile, 1, addr msg, sizeof msg, 0, 0

    ; Exit
    invoke ExitProcess, 0
end start
```

---
### **ARM (32-bit): Hello, World! (GAS Syntax)**
```assembly
.data
msg:
    .asciz "Hello, World!\n"
len = . - msg

.text
.global _start

_start:
    ; Write to stdout
    mov r0, #1          ; fd = stdout
    ldr r1, =msg        ; buffer
    ldr r2, =len        ; length
    mov r7, #4          ; sys_write
    swi 0

    ; Exit
    mov r0, #0          ; status = 0
    mov r7, #1          ; sys_exit
    swi 0
```

---
### **AArch64 (64-bit): Hello, World! (GAS Syntax)**
```assembly
.data
msg:
    .ascii "Hello, World!\n"
    len = . - msg

.text
.global _start

_start:
    ; Write to stdout
    mov x0, #1          ; fd = stdout
    ldr x1, =msg        ; buffer
    ldr x2, =len        ; length
    mov w8, #64         ; sys_write
    svc #0

    ; Exit
    mov x0, #0          ; status = 0
    mov w8, #93         ; sys_exit
    svc #0
```

---
### **MIPS (32-bit): Hello, World! (GAS Syntax)**
```assembly
.data
msg:
    .asciiz "Hello, World!\n"

.text
.globl __start

__start:
    ; Write to stdout
    li $v0, 4           ; sys_write
    la $a0, msg         ; buffer
    li $a1, 14          ; length
    li $a2, 1           ; fd = stdout
    syscall

    ; Exit
    li $v0, 10          ; sys_exit
    li $a0, 0           ; status = 0
    syscall
```

---
### **RISC-V (64-bit): Hello, World! (GAS Syntax)**
```assembly
.section .data
msg:
    .ascii "Hello, World!\n"
    .equ len, . - msg

.section .text
.global _start

_start:
    ; Write to stdout
    li a7, 64          ; sys_write
    li a0, 1           ; fd = stdout
    la a1, msg         ; buffer
    li a2, len         ; length
    ecall

    ; Exit
    li a7, 93          ; sys_exit
    li a0, 0           ; status = 0
    ecall
```

---
---
---
## **14. Common Macros for Assembly Programming**

---
### **x86-64 Linux System Call Macros (NASM)**
```assembly
; Define system call macros for x86-64 Linux
%macro SYSCALL0 1
    mov rax, %1
    syscall
%endmacro

%macro SYSCALL1 2
    mov rax, %1
    mov rdi, %2
    syscall
%endmacro

%macro SYSCALL2 3
    mov rax, %1
    mov rdi, %2
    mov rsi, %3
    syscall
%endmacro

%macro SYSCALL3 4
    mov rax, %1
    mov rdi, %2
    mov rsi, %3
    mov rdx, %4
    syscall
%endmacro

%macro SYSCALL4 5
    mov rax, %1
    mov rdi, %2
    mov rsi, %3
    mov rdx, %4
    mov r10, %5
    syscall
%endmacro

%macro SYSCALL5 6
    mov rax, %1
    mov rdi, %2
    mov rsi, %3
    mov rdx, %4
    mov r10, %5
    mov r8, %6
    syscall
%endmacro

%macro SYSCALL6 7
    mov rax, %1
    mov rdi, %2
    mov rsi, %3
    mov rdx, %4
    mov r10, %5
    mov r8, %6
    mov r9, %7
    syscall
%endmacro
```

---
### **Function Prologue and Epilogue Macros (NASM)**
```assembly
; Function prologue macro
%macro PROLOGUE 1-2
    push rbp
    mov rbp, rsp
    %if %0 >= 2
        sub rsp, %2
    %endif
%endmacro

; Function epilogue macro
%macro EPILOGUE 1-2
    %if %0 >= 2
        add rsp, %2
    %endif
    pop rbp
    ret
%endmacro
```

---
### **Common x86-64 Register Saving Macros (NASM)**
```assembly
; Save all general-purpose registers
%macro PUSH_ALL 0
    push rax
    push rbx
    push rcx
    push rdx
    push rsi
    push rdi
    push rbp
    push r8
    push r9
    push r10
    push r11
    push r12
    push r13
    push r14
    push r15
%endmacro

; Restore all general-purpose registers
%macro POP_ALL 0
    pop r15
    pop r14
    pop r13
    pop r12
    pop r11
    pop r10
    pop r9
    pop r8
    pop rbp
    pop rdi
    pop rsi
    pop rdx
    pop rcx
    pop rbx
    pop rax
%endmacro

; Save registers for function calls (System V AMD64)
%macro SAVE_REGS 0
    push rbp
    push rbx
    push r12
    push r13
    push r14
    push r15
%endmacro

; Restore registers for function calls (System V AMD64)
%macro RESTORE_REGS 0
    pop r15
    pop r14
    pop r13
    pop r12
    pop rbx
    pop rbp
%endmacro
```

---
---
---
## **15. Summary of Common Tasks in Assembly**

---
### **x86-64: Function Call (System V AMD64)**
```assembly
; Caller:
mov rdi, arg1
mov rsi, arg2
mov rdx, arg3
mov rcx, arg4
mov r8, arg5
mov r9, arg6
; For additional args:
push arg7
push arg8
call function
; Clean up stack (if any args were pushed)
add rsp, 16

; Callee:
function:
    push rbp
    mov rbp, rsp
    ; Save callee-saved registers (RBX, RBP, R12-R15)
    push rbx
    push r12
    push r13
    push r14
    push r15
    ; Function body
    ; Return value in RAX (and RDX for 128-bit)
    pop r15
    pop r14
    pop r13
    pop r12
    pop rbx
    mov rsp, rbp
    pop rbp
    ret
```

---
### **x86-64: Loop Example**
```assembly
; Loop example: sum an array of 64-bit integers
; Input: RDI = array pointer, RSI = count
; Output: RAX = sum
sum_array:
    xor rax, rax        ; sum = 0
    xor rcx, rcx        ; i = 0
.loop:
    add rax, [rdi + rcx*8]  ; sum += array[i]
    inc rcx             ; i++
    cmp rcx, rsi        ; i < count?
    jl .loop            ; if less, loop
    ret
```

---
### **x86-64: Conditional Branch Example**
```assembly
; Compare two integers and set RAX to the larger
; Input: RDI = a, RSI = b
; Output: RAX = max(a, b)
max:
    cmp rdi, rsi
    jg .a_greater
    mov rax, rsi        ; b >= a, return b
    ret
.a_greater:
    mov rax, rdi        ; a > b, return a
    ret
```

---
### **ARM: Function Call (AAPCS)**
```assembly
; Caller:
mov r0, #arg1
mov r1, #arg2
mov r2, #arg3
mov r3, #arg4
; For additional args:
push {arg5, arg6}
bl function
; Clean up stack (if any args were pushed)
add sp, sp, #8

; Callee:
function:
    push {r4-r11, lr}   ; Save callee-saved registers
    ; Function body
    ; Return value in R0 (and R1 for 64-bit)
    pop {r4-r11, pc}    ; Restore registers and return
```

---
### **ARM: Loop Example**
```assembly
; Loop example: sum an array of 32-bit integers
; Input: R0 = array pointer, R1 = count
; Output: R0 = sum
sum_array:
    mov r2, #0          ; sum = 0
    mov r3, #0          ; i = 0
.loop:
    ldr r4, [r0, r3, lsl #2]  ; load array[i]
    add r2, r2, r4      ; sum += array[i]
    add r3, r3, #1      ; i++
    cmp r3, r1          ; i < count?
    blt .loop           ; if less, loop
    mov r0, r2          ; return sum
    bx lr
```

---
---
---
## **Final Notes**

1. **Architecture-Specific**: Assembly language is highly architecture-specific. The instructions and registers differ significantly between x86, ARM, MIPS, RISC-V, etc.

2. **Assembler-Specific**: Directives and syntax vary between assemblers (NASM, GAS, MASM, FASM, etc.).

3. **OS-Specific**: System calls and calling conventions depend on the operating system (Linux, Windows, macOS, etc.).

4. **No True Standard Library**: Unlike higher-level languages, assembly does not have a standard library. Instead, it relies on:
   - CPU instruction sets
   - Operating system system calls
   - C library bindings
   - Assembler directives and macros

5. **Common Tasks**: Most assembly programs interact with the OS via system calls, manipulate data in memory, and perform arithmetic/logical operations.