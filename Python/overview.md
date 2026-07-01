## **Built-in Functions**
*(Available without importing)*

| Function | Description |
|----------|-------------|
| `abs(x)` | Absolute value of a number |
| `aiter(iterable)` | Return an asynchronous iterator |
| `all(iterable)` | Return True if all elements are true |
| `any(iterable)` | Return True if any element is true |
| `anext(iterator)` | Retrieve the next item from an asynchronous iterator |
| `ascii(object)` | Return a string containing a printable representation |
| `bin(x)` | Convert an integer to a binary string |
| `bool(x)` | Return a Boolean value |
| `breakpoint()` | Enter the debugger at the call site |
| `bytearray(iterable)` | Return a new array of bytes |
| `bytes(iterable)` | Return a new bytes object |
| `callable(object)` | Check if an object is callable |
| `chr(i)` | Return the string representing a character |
| `classmethod(function)` | Transform a method into a class method |
| `compile(source, filename, mode)` | Compile source into a code object |
| `complex(real, imag)` | Create a complex number |
| `delattr(x, name)` | Delete an attribute from an object |
| `dict()` | Create a new dictionary |
| `dir(object)` | Return the list of names in the current scope |
| `divmod(a, b)` | Return the quotient and remainder of division |
| `enumerate(iterable, start)` | Return an enumerate object |
| `eval(expression)` | Evaluate a string as a Python expression |
| `exec(object)` | Execute dynamically created code |
| `filter(function, iterable)` | Construct an iterator from elements filtered |
| `float(x)` | Convert a string or number to a floating point number |
| `format(value, format_spec)` | Format a value |
| `frozenset(iterable)` | Return a new frozenset object |
| `getattr(x, name)` | Return the value of a named attribute of an object |
| `globals()` | Return the dictionary of the current global symbol table |
| `hasattr(x, name)` | Check if an object has a named attribute |
| `hash(object)` | Return the hash value of an object |
| `help(object)` | Invoke the built-in help system |
| `hex(x)` | Convert an integer to a hexadecimal string |
| `id(object)` | Return the identity of an object |
| `input(prompt)` | Read a string from standard input |
| `int(x)` | Convert a string or number to an integer |
| `isinstance(object, classinfo)` | Check if an object is an instance of a class |
| `issubclass(class, classinfo)` | Check if a class is a subclass of another |
| `iter(object)` | Return an iterator object |
| `len(object)` | Return the number of items in an object |
| `list(iterable)` | Create a new list |
| `locals()` | Return the dictionary of the current local symbol table |
| `map(function, iterable)` | Apply a function to all items in an iterable |
| `max(iterable)` | Return the largest item in an iterable |
| `memoryview(obj)` | Return a memory view of an argument |
| `min(iterable)` | Return the smallest item in an iterable |
| `next(iterator)` | Retrieve the next item from an iterator |
| `object()` | Return a new featureless object |
| `oct(x)` | Convert an integer to an octal string |
| `open(file, mode)` | Open a file |
| `ord(c)` | Return the integer representing the Unicode character |
| `pow(x, y)` | Return x raised to the power y |
| `print(*objects, sep, end, file, flush)` | Print objects to the standard output |
| `property(fget, fset, fdel, doc)` | Return a property attribute |
| `range(stop)` | Return a range object |
| `repr(object)` | Return a string containing a printable representation |
| `reversed(iterable)` | Return a reverse iterator |
| `round(number, ndigits)` | Round a number to a given precision |
| `set(iterable)` | Create a new set |
| `setattr(x, name, value)` | Set the value of a named attribute of an object |
| `slice(stop)` | Return a slice object |
| `sorted(iterable, key, reverse)` | Return a new sorted list |
| `staticmethod(function)` | Transform a method into a static method |
| `str(object)` | Return the string version of an object |
| `sum(iterable, start)` | Sum the items of an iterable |
| `super()` | Return a proxy object for delegating method calls |
| `tuple(iterable)` | Create a new tuple |
| `type(object)` | Return the type of an object |
| `vars(object)` | Return the `__dict__` attribute of an object |
| `zip(*iterables)` | Create an iterator that aggregates elements from iterables |
| `__import__(name)` | Import a module dynamically |

---

---
## **Built-in Constants**

| Constant | Description |
|----------|-------------|
| `False` | Boolean false |
| `True` | Boolean true |
| `None` | The sole value of the type `NoneType` |
| `Ellipsis` | The same as the ellipsis literal `...` |
| `__debug__` | True if Python was not started with the -O option |

---

---
## **Built-in Types**

| Type | Description |
|------|-------------|
| `bool` | Boolean value |
| `bytearray` | Mutable sequence of bytes |
| `bytes` | Immutable sequence of bytes |
| `complex` | Complex number |
| `dict` | Dictionary (key-value pairs) |
| `float` | Floating point number |
| `frozenset` | Immutable set |
| `int` | Integer |
| `list` | Mutable sequence |
| `memoryview` | Memory view of another object |
| `range` | Immutable sequence of numbers |
| `set` | Mutable unordered set |
| `slice` | Slice object |
| `str` | String |
| `tuple` | Immutable sequence |
| `type` | Type of an object |

---

---
## **Built-in Exceptions**

| Exception | Description |
|-----------|-------------|
| `BaseException` | Base class for all built-in exceptions |
| `SystemExit` | Raised by `sys.exit()` |
| `KeyboardInterrupt` | Raised when the user hits the interrupt key |
| `GeneratorExit` | Raised when a generator is closed |
| `Exception` | Base class for all non-system-exiting built-in exceptions |
| `StopIteration` | Raised when the next element of an iterator is not available |
| `StopAsyncIteration` | Raised when an asynchronous iterator is exhausted |
| `ArithmeticError` | Base class for arithmetic errors |
| `FloatingPointError` | Raised when a floating point operation fails |
| `OverflowError` | Raised when a calculation exceeds maximum limit |
| `ZeroDivisionError` | Raised when division or modulo by zero occurs |
| `AssertionError` | Raised when an `assert` statement fails |
| `AttributeError` | Raised when an attribute reference or assignment fails |
| `BufferError` | Raised when a buffer related operation cannot be performed |
| `EOFError` | Raised when the input() function hits an end-of-file condition |
| `ImportError` | Raised when an import statement fails to find a module |
| `ModuleNotFoundError` | Raised when a module could not be found |
| `LookupError` | Base class for lookup errors |
| `IndexError` | Raised when a sequence subscript is out of range |
| `KeyError` | Raised when a dictionary key is not found |
| `MemoryError` | Raised when an operation runs out of memory |
| `NameError` | Raised when a local or global name is not found |
| `OSError` | Base class for OS-related errors |
| `BlockingIOError` | Raised for I/O operations that would block |
| `ChildProcessError` | Raised when an operation on a child process fails |
| `ConnectionError` | Base class for connection-related errors |
| `BrokenPipeError` | Raised when trying to write on a pipe with no reader |
| `ConnectionAbortedError` | Raised when a connection attempt is aborted |
| `ConnectionRefusedError` | Raised when a connection is refused |
| `ConnectionResetError` | Raised when a connection is reset by the peer |
| `FileExistsError` | Raised when a file already exists |
| `FileNotFoundError` | Raised when a file or directory is requested but doesn't exist |
| `InterruptedError` | Raised when a system call is interrupted by an incoming signal |
| `IsADirectoryError` | Raised when a file operation is requested on a directory |
| `NotADirectoryError` | Raised when a directory operation is requested on something which is not a directory |
| `PermissionError` | Raised when trying to run an operation without the adequate access rights |
| `ProcessLookupError` | Raised when a given process doesn't exist |
| `TimeoutError` | Raised when a system function timed out at the system level |
| `RuntimeError` | Raised when an error does not fall under any other category |
| `RecursionError` | Raised when the maximum recursion depth is exceeded |
| `NotImplementedError` | Raised when a feature or operation is not implemented |
| `SyntaxError` | Raised when the parser encounters a syntax error |
| `IndentationError` | Base class for syntax errors related to incorrect indentation |
| `TabError` | Raised when indentation consists of inconsistent tabs and spaces |
| `SystemError` | Raised when the interpreter finds an internal error |
| `TypeError` | Raised when an operation or function is applied to an object of inappropriate type |
| `ValueError` | Raised when an operation or function receives an argument of the right type but an inappropriate value |
| `UnicodeError` | Base class for Unicode-related errors |
| `UnicodeDecodeError` | Raised when a Unicode decoding error occurs |
| `UnicodeEncodeError` | Raised when a Unicode encoding error occurs |
| `UnicodeTranslateError` | Raised when a Unicode translation error occurs |
| `Warning` | Base class for warning categories |
| `DeprecationWarning` | Base category for warnings about deprecated features |
| `PendingDeprecationWarning` | Base category for warnings about features that will be deprecated in the future |
| `RuntimeWarning` | Base category for warnings about dubious runtime behavior |
| `FutureWarning` | Base category for warnings about deprecated features when those warnings are intended for end users of applications written in Python |
| `UserWarning` | Base category for warnings generated by user code |
| `SyntaxWarning` | Base category for warnings about dubious syntax |
| `ImportWarning` | Base category for warnings triggered during the import process |
| `UnicodeWarning` | Base category for warnings related to Unicode |
| `BytesWarning` | Base category for warnings related to bytes and bytearray |
| `ResourceWarning` | Base category for warnings related to resource usage |
| `ExceptionGroup` | Base class for exceptions that are containers for other exceptions |

---

---
---
## **Standard Library Modules by Category**

---
---
### **Text Processing**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `string` | `ascii_letters`, `ascii_lowercase`, `ascii_uppercase`, `digits`, `hexdigits`, `octdigits`, `punctuation`, `whitespace`, `printable`, `Template`, `Formatter` | Common string operations and constants |
| `re` | `compile`, `search`, `match`, `fullmatch`, `findall`, `finditer`, `sub`, `subn`, `split`, `escape`, `purge`, `IGNORECASE`, `MULTILINE`, `DOTALL`, `VERBOSE`, `ASCII`, `Pattern`, `Match` | Regular expression operations |
| `difflib` | `SequenceMatcher`, `get_close_matches`, `ndiff`, `restore`, `unified_diff`, `context_diff`, `HtmlDiff`, `Differ` | Tools for comparing sequences and files |
| `textwrap` | `wrap`, `fill`, `shorten`, `indent`, `dedent`, `TextWrapper` | Text wrapping and filling |
| `unicodedata` | `name`, `decimal`, `digit`, `numeric`, `category`, `bidirectional`, `combining`, `east_asian_width`, `mirrored`, `normalize`, `lookup`, `ucd_3_2_0` | Unicode Database access |
| `stringprep` | `in_table_a1`, `in_table_b1`, `b1_set`, `c11_c12_set`, `c21_c22_set`, `c3_set`, `c4_set`, `c5_set`, `c6_set`, `c7_set`, `c8_set`, `c9_set`, `d1_set`, `d2_set`, `bidi_set`, `join_set`, `mapping_set`, `unassigned_set`, `in_table_c11_c12`, `in_table_c21_c22`, `in_table_c3`, `in_table_c4`, `in_table_c5`, `in_table_c6`, `in_table_c8`, `in_table_d1`, `in_table_d2`, `in_table_bidi`, `bidi_uis`, `bidi_character_form`, `bidi_mirroring_glyph`, `bidi_brackets`, `bidi_test`, `in_table_a1`, `in_table_b1`, `b1_set`, `c11_c12_set` | String preparation for internationalization |
| `codecs` | `open`, `encode`, `decode`, `lookup`, `register`, `unregister`, `iterencode`, `iterdecode`, `StreamReader`, `StreamWriter`, `StreamReaderWriter`, `StreamRecoder`, `Codec`, `CodecInfo`, `IncrementalEncoder`, `IncrementalDecoder`, `BOM`, `BOM_UTF8`, `BOM_UTF16`, `BOM_UTF16_BE`, `BOM_UTF16_LE`, `BOM_UTF32`, `BOM_UTF32_BE`, `BOM_UTF32_LE` | Codec registry and base classes |

---
---
### **Binary Data**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `struct` | `pack`, `unpack`, `calcsize`, `pack_into`, `unpack_from` | Convert between Python values and C structs |
| `base64` | `b64encode`, `b64decode`, `b32encode`, `b32decode`, `b16encode`, `b16decode`, `a85encode`, `a85decode`, `b85encode`, `b85decode`, `standard_b64encode`, `standard_b64decode`, `urlsafe_b64encode`, `urlsafe_b64decode` | Base64, Base32, Base16, Base85 data encoding |
| `binascii` | `a2b_base64`, `b2a_base64`, `a2b_hex`, `b2a_hex`, `a2b_qp`, `b2a_qp`, `a2b_uu`, `b2a_uu`, `crc32`, `crc_hqx`, `rlecode_hqx`, `rledecode_hqx` | ASCII-binary conversions |
| `hashlib` | `md5`, `sha1`, `sha224`, `sha256`, `sha384`, `sha512`, `sha3_224`, `sha3_256`, `sha3_384`, `sha3_512`, `blake2b`, `blake2s`, `new`, `pbkdf2_hmac`, `scrypt` | Secure hash and message digest algorithms |
| `hmac` | `new`, `digest`, `hexdigest`, `copy`, `update` | HMAC message authentication |

---
---
### **Data Types**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `datetime` | `datetime`, `date`, `time`, `timedelta`, `timezone`, `utcnow`, `now`, `today`, `fromtimestamp`, `strptime`, `strftime`, `combine`, `MINYEAR`, `MAXYEAR` | Basic date and time types |
| `calendar` | `Calendar`, `TextCalendar`, `HTMLCalendar`, `LocaleTextCalendar`, `LocaleHTMLCalendar`, `month`, `prmonth`, `weekday`, `monthrange`, `monthcalendar`, `prcal`, `timegm`, `leapdays`, `isleap` | Calendar-related functions |
| `collections` | `Counter`, `defaultdict`, `OrderedDict`, `deque`, `ChainMap`, `namedtuple`, `UserDict`, `UserList`, `UserString` | Container datatypes |
| `collections.abc` | `Callable`, `Container`, `Hashable`, `Iterable`, `Iterator`, `Generator`, `Reversible`, `Sequence`, `MutableSequence`, `ByteString`, `Set`, `MutableSet`, `Mapping`, `MutableMapping`, `MappingView`, `KeysView`, `ItemsView`, `ValuesView` | Abstract Base Classes for containers |
| `heapq` | `heappush`, `heappop`, `heappushpop`, `heapify`, `heapreplace`, `merge`, `nlargest`, `nsmallest` | Heap queue algorithm |
| `bisect` | `bisect`, `bisect_left`, `bisect_right`, `insort`, `insort_left`, `insort_right` | Maintain a list in sorted order |
| `array` | `array`, `ArrayType` | Efficient arrays of numeric values |
| `enum` | `Enum`, `IntEnum`, `Flag`, `IntFlag`, `auto`, `unique`, `property`, `name`, `value` | Enumeration support |
| `graphlib` (3.9+) | `TopologicalSorter` | Graph algorithms |
| `typing` | `Any`, `Union`, `Optional`, `List`, `Dict`, `Set`, `Tuple`, `Type`, `TypeVar`, `Generic`, `Callable`, `Sequence`, `Mapping`, `Iterable`, `Iterator`, `ClassVar`, `Final`, `Literal`, `TypedDict`, `Protocol`, `runtime_checkable`, `overload`, `NoReturn`, `NewType`, `NamedTuple`, `DefaultDict`, `Counter`, `Deque`, `ChainMap`, `OrderedDict`, `FrozenSet`, `ByteString`, `IO`, `TextIO`, `BinaryIO`, `Pattern`, `Match` | Type hints |
| `types` | `DynamicClassAttribute`, `EllipsisType`, `FrameType`, `FunctionType`, `GeneratorType`, `LambdaType`, `MethodType`, `BuiltinFunctionType`, `BuiltinMethodType`, `WrapperDescriptorType`, `MethodWrapperType`, `MethodDescriptorType`, `ClassMethodDescriptorType`, `CoroutineType`, `AsyncGeneratorType`, `AsyncIteratorType`, `AsyncIterableType`, `AwaitableType`, `NewType`, `GenericAlias`, `UnionType`, `NoneType`, `NotImplementedType` | Names for built-in types |
| `dataclasses` | `dataclass`, `field`, `Field`, `asdict`, `astuple`, `make_dataclass`, `is_dataclass`, `fields` | Data Classes |
| `copy` | `copy`, `deepcopy` | Shallow and deep copy operations |
| `pprint` | `pprint`, `pformat`, `PrettyPrinter`, `saferepr` | Data pretty printer |
| `reprlib` | `Repr`, `repr` | Alternative repr() implementation |
| `operator` | `add`, `sub`, `mul`, `matmul`, `truediv`, `floordiv`, `mod`, `pow`, `lshift`, `rshift`, `and_`, `or_`, `xor`, `inv`, `neg`, `pos`, `abs`, `invert`, `not_`, `is_`, `is_not`, `eq`, `ne`, `lt`, `le`, `gt`, `ge`, `contains`, `countOf`, `indexOf`, `concat`, `repeat`, `itemgetter`, `attrgetter`, `methodcaller`, `truth`, `not_` | Standard operators as functions |
| `functools` | `reduce`, `partial`, `partialmethod`, `wraps`, `total_ordering`, `cmp_to_key`, `lru_cache`, `singledispatch`, `singledispatchmethod`, `cached_property` | Higher-order functions and operations on callable objects |
| `itertools` | `accumulate`, `chain`, `chain.from_iterable`, `combinations`, `combinations_with_replacement`, `count`, `cycle`, `dropwhile`, `filterfalse`, `groupby`, `islice`, `permutations`, `product`, `repeat`, `starmap`, `takewhile`, `tee`, `zip_longest` | Functions creating iterators for efficient looping |
| `more_itertools` | *(Not in standard library)* | *(External package)* |
| `contextlib` | `contextmanager`, `closing`, `suppress`, `redirect_stdout`, `redirect_stderr`, `nullcontext`, `ExitStack`, `AsyncExitStack`, `chdir`, `contextlib` | Utilities for `with` statement contexts |
| `contextvars` | `ContextVar`, `Token`, `Context`, `copy_context` | Context Variables |
| `atexit` | `register`, `unregister`, `isregistered`, `_clear`, `_exithandlers` | Exit handlers |
| `traceback` | `print_exc`, `print_exception`, `print_last`, `print_stack`, `print_tb`, `format_exc`, `format_exception`, `format_tb`, `extract_tb`, `extract_stack`, `tb_lineno`, `tb_frame`, `TracebackException` | Stack trace utilities |
| `sys` | `argv`, `path`, `modules`, `displayhook`, `excepthook`, `stdin`, `stdout`, `stderr`, `exit`, `exc_info`, `exc_clear`, `getrefcount`, `getsizeof`, `intern`, `is_finalizing`, `addaudithook`, `getdlopenflags`, `setdlopenflags`, `getfilesystemencoding`, `getfilesystemencodeerrors`, `getdefaultencoding`, `getswitchinterval`, `setswitchinterval`, `getrecursionlimit`, `setrecursionlimit`, `getintmax`, `getfloatinfo`, `float_info`, `hash_randomization_seed`, `is_finalizing` | System-specific parameters and functions |
| `__main__` | | Top-level script environment |
| `warnings` | `warn`, `catch_warnings`, `simplefilter`, `filterwarnings`, `resetwarnings`, `Warnings`, `WarningMessage` | Warning control |
| `weakref` | `ref`, `proxy`, `WeakValueDictionary`, `WeakKeyDictionary`, `WeakSet`, `getweakrefcount`, `getweakrefs` | Weak references |
| `abc` | `ABC`, `abstractmethod`, `abstractclassmethod`, `abstractstaticmethod`, `abstractproperty` | Abstract Base Classes |

---
---
### **Numeric and Mathematical Modules**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `math` | `acos`, `acosh`, `asin`, `asinh`, `atan`, `atan2`, `atanh`, `ceil`, `comb`, `copysign`, `cos`, `cosh`, `degrees`, `dist`, `erf`, `erfc`, `exp`, `expm1`, `fabs`, `factorial`, `floor`, `fmod`, `frexp`, `fsum`, `gamma`, `gcd`, `hypot`, `isclose`, `isfinite`, `isinf`, `isnan`, `isqrt`, `lcm`, `ldexp`, `lgamma`, `log`, `log10`, `log1p`, `log2`, `modf`, `nextafter`, `perm`, `pow`, `prod`, `radians`, `remainder`, `sin`, `sinh`, `sqrt`, `tan`, `tanh`, `trunc`, `ulp`, `pi`, `e`, `tau`, `inf`, `nan` | Mathematical functions |
| `cmath` | `acos`, `acosh`, `asin`, `asinh`, `atan`, `atanh`, `cos`, `cosh`, `exp`, `isclose`, `isfinite`, `isinf`, `isnan`, `log`, `log10`, `phase`, `polar`, `pow`, `rect`, `sin`, `sinh`, `sqrt`, `tan`, `tanh`, `pi`, `e`, `tau`, `inf`, `nan` | Mathematical functions for complex numbers |
| `decimal` | `Decimal`, `getcontext`, `localcontext`, `BasicContext`, `ExtendedContext`, `setcontext`, `ROUND_CEILING`, `ROUND_DOWN`, `ROUND_FLOOR`, `ROUND_HALF_DOWN`, `ROUND_HALF_EVEN`, `ROUND_HALF_UP`, `ROUND_UP`, `InvalidOperation`, `DivisionByZero`, `Overflow`, `Underflow`, `Subnormal`, `Inexact`, `Rounded`, `Clamped` | Decimal floating point arithmetic |
| `fractions` | `Fraction`, `gcd`, `lcm` | Rational number arithmetic |
| `numbers` | `Number`, `Complex`, `Real`, `Rational`, `Integral` | Abstract Base Classes for numbers |
| `statistics` | `mean`, `median`, `median_low`, `median_high`, `mode`, `pstdev`, `pvariance`, `stdev`, `variance`, `harmonic_mean`, `multimode`, `quantiles`, `NormalDist` | Mathematical statistics functions |
| `random` | `random`, `seed`, `getstate`, `setstate`, `randbytes`, `choice`, `choices`, `sample`, `shuffle`, `permutation`, `randrange`, `randint`, `uniform`, `triangular`, `betavariate`, `expovariate`, `gammavariate`, `gauss`, `lognormvariate`, `normalvariate`, `vonmisesvariate`, `paretovariate`, `weibullvariate`, `SystemRandom` | Generate pseudo-random numbers |
| `statistics` | `mean`, `median`, `mode`, `stdev`, `variance`, `pstdev`, `pvariance` | Mathematical statistics functions |

---
---
### **Functional Programming**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `itertools` | `accumulate`, `chain`, `chain.from_iterable`, `combinations`, `combinations_with_replacement`, `count`, `cycle`, `dropwhile`, `filterfalse`, `groupby`, `islice`, `permutations`, `product`, `repeat`, `starmap`, `takewhile`, `tee`, `zip_longest` | Functions creating iterators for efficient looping |
| `functools` | `reduce`, `partial`, `partialmethod`, `wraps`, `total_ordering`, `cmp_to_key`, `lru_cache`, `singledispatch`, `singledispatchmethod`, `cached_property` | Higher-order functions and operations on callable objects |
| `operator` | `add`, `sub`, `mul`, `matmul`, `truediv`, `floordiv`, `mod`, `pow`, `lshift`, `rshift`, `and_`, `or_`, `xor`, `inv`, `neg`, `pos`, `abs`, `invert`, `not_`, `is_`, `is_not`, `eq`, `ne`, `lt`, `le`, `gt`, `ge`, `contains`, `countOf`, `indexOf`, `concat`, `repeat`, `itemgetter`, `attrgetter`, `methodcaller` | Standard operators as functions |

---
---
### **File and Directory Access**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `os` | `name`, `uname`, `environ`, `getenv`, `putenv`, `unsetenv`, `chdir`, `fchdir`, `getcwd`, `chmod`, `fchmod`, `chown`, `fchown`, `lchown`, `chroot`, `listdir`, `mkdir`, `makedirs`, `remove`, `rmdir`, `removedirs`, `rename`, `renames`, `replace`, `symlink`, `readlink`, `link`, `unlink`, `utime`, `stat`, `fstat`, `lstat`, `statvfs`, `fstatvfs`, `stat_result`, `walk`, `fwalk`, `open`, `fdopen`, `popen`, `close`, `read`, `write`, `pipe`, `dup`, `dup2`, `lseek`, `fsync`, `ftruncate`, `kill`, `killpg`, `getpid`, `getppid`, `getuid`, `geteuid`, `getgid`, `getegid`, `getgroups`, `setuid`, `setgid`, `setgroups`, `getpgid`, `setpgid`, `getsid`, `setsid`, `getpgrp`, `setpgrp`, `umask`, `getloadavg`, `times`, `ctermid`, `get_terminal_size`, `terminal_size`, `startfile`, `system`, `urandom`, `cpu_count`, `sched_getaffinity`, `sched_setaffinity`, `get_inheritable`, `set_inheritable`, `get_blocking`, `set_blocking`, `preexec_fn`, `register_at_fork`, `unregister_at_fork`, `O_APPEND`, `O_CREAT`, `O_EXCL`, `O_RDONLY`, `O_RDWR`, `O_WRONLY`, `O_TRUNC`, `SEEK_SET`, `SEEK_CUR`, `SEEK_END`, `path` | Miscellaneous operating system interfaces |
| `os.path` | `abspath`, `basename`, `commonpath`, `commonprefix`, `dirname`, `exists`, `expanduser`, `expandvars`, `getatime`, `getctime`, `getmtime`, `getsize`, `isabs`, `isdir`, `isfile`, `islink`, `ismount`, `join`, `normcase`, `normpath`, `realpath`, `relpath`, `samefile`, `sameopenfile`, `split`, `splitdrive`, `splitext`, `splitunc`, `stat`, `lstat`, `lexists`, `supports_unicode_filenames`, `curdir`, `pardir`, `sep`, `altsep`, `pathsep`, `defpath`, `devnull`, `extsep` | Common pathname manipulations |
| `pathlib` | `Path`, `PurePath`, `PosixPath`, `WindowsPath`, `PurePosixPath`, `PureWindowsPath` | Object-oriented filesystem paths |
| `glob` | `glob`, `iglob`, `escape` | Unix style pathname pattern expansion |
| `fnmatch` | `fnmatch`, `fnmatchcase`, `filter`, `translate` | Unix filename pattern matching |
| `fileinput` | `FileInput`, `input`, `close`, `nextfile`, `filename`, `filelineno`, `lineno`, `isfirstline`, `isstdin` | Iterate over lines from multiple input streams |
| `tempfile` | `NamedTemporaryFile`, `TemporaryFile`, `SpooledTemporaryFile`, `TemporaryDirectory`, `mkstemp`, `mkdtemp`, `mktemp`, `gettempdir`, `gettempprefix`, `tempdir`, `TMP_MAX` | Generate temporary files and directories |
| `shutil` | `copy`, `copy2`, `copyfile`, `copyfileobj`, `copymode`, `copystat`, `copytree`, `rmtree`, `move`, `chown`, `lchown`, `acl`, `get_archive_formats`, `register_archive_format`, `unregister_archive_format`, `find_archive`, `get_unpack_formats`, `register_unpack_format`, `unregister_unpack_format`, `unpack_archive`, `make_archive`, `which`, `disk_usage`, `chflags`, `lchflags`, `get_terminal_size`, `SameFileError`, `Error` | High-level file operations |
| `filecmp` | `cmp`, `cmpfiles`, `dircmp` | Compare files and directories |
| `stat` | `ST_MODE`, `ST_INO`, `ST_DEV`, `ST_NLINK`, `ST_UID`, `ST_GID`, `ST_SIZE`, `ST_ATIME`, `ST_MTIME`, `ST_CTIME`, `S_IMODE`, `S_IFMT`, `S_IFDIR`, `S_IFCHR`, `S_IFBLK`, `S_IFREG`, `S_IFLNK`, `S_IFSOCK`, `S_IFIFO`, `S_ISDIR`, `S_ISCHR`, `S_ISBLK`, `S_ISREG`, `S_ISLNK`, `S_ISFIFO`, `S_ISSOCK`, `stat`, `lstat`, `filemode`, `file_flags` | Interpret `os.stat()` results |
| `statfile` | *(Deprecated)* | *(Use `stat`)* |
| `pty` | `openpty`, `fork`, `spawn` | Pseudo-terminal utilities |
| `fcntl` | `fcntl`, `ioctl`, `flock`, `lockf`, `F_DUPFD`, `F_GETFD`, `F_SETFD`, `F_GETFL`, `F_SETFL`, `O_ACCMODE`, `O_RDONLY`, `O_WRONLY`, `O_RDWR`, `O_CREAT`, `O_EXCL`, `O_NOCTTY`, `O_TRUNC`, `O_APPEND`, `O_NONBLOCK`, `O_SYNC`, `O_DSYNC`, `FASYNC`, `O_DIRECT`, `O_LARGEFILE`, `O_NOFOLLOW`, `O_DIRECTORY` | The `fcntl` and `ioctl` system calls |
| `termios` | `tcgetattr`, `tcsetattr`, `tcflush`, `tcsendbreak`, `tcdrain`, `cfgetispeed`, `cfgetospeed`, `cfsetispeed`, `cfsetospeed`, `termios`, `TIOCGWINSZ`, `TIOCSWINSZ`, `IFLAG`, `OFLAG`, `CFLAG`, `LFLAG`, `ECHO`, `ECHOE`, `ECHOK`, `ECHONL`, `ICANON`, `ISIG`, `IEXTEN`, `TOSTOP`, `FLUSHO`, `PENDIN`, `NOFLSH`, `CSIZE`, `CS5`, `CS6`, `CS7`, `CS8`, `PARENB`, `PARODD`, `CSTOPB`, `CREAD`, `HUPCL`, `CLOCAL`, `CREAD`, `PARENB`, `PARODD`, `CMIN`, `CTIME`, `B0`, `B50`, `B75`, `B110`, `B134`, `B150`, `B200`, `B300`, `B600`, `B1200`, `B1800`, `B2400`, `B4800`, `B9600`, `B19200`, `B38400`, `EXTA`, `EXTB` | POSIX terminal control settings |
| `tty` | `setraw`, `setcbreak`, `setecho` | Terminal control functions |
| `pwd` | `getpwnam`, `getpwuid`, `getpwall` | The password database |
| `grp` | `getgrnam`, `getgrgid`, `getgrall` | The group database |

---
---
### **Data Storage**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `pickle` | `dump`, `dumps`, `load`, `loads`, `PickleError`, `UnpicklingError`, `Pickler`, `Unpickler` | Python object serialization |
| `shelve` | `Shelf`, `DbfilenameShelf`, `open` | Python object persistence |
| `marshal` | `dump`, `dumps`, `load`, `loads` | Internal Python object serialization |
| `dbm` | `open`, `whichdb`, `error` | Generic interface to DBM-style databases |
| `sqlite3` | `connect`, `Connection`, `Cursor`, `Complete`, `IntegrityError`, `DatabaseError`, `Error`, `InterfaceError`, `OperationalError`, `ProgrammingError`, `InternalError`, `NotSupportedError`, `Warning`, `Row`, `Blob`, `Date`, `DateFromTicks`, `Time`, `TimeFromTicks`, `Timestamp`, `TimestampFromTicks`, `Binary` | DB-API 2.0 interface for SQLite databases |

---
---
### **Data Compression and Archiving**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `zlib` | `adler32`, `compress`, `compress2`, `compressobj`, `crc32`, `decompress`, `decompressobj`, `ZlibError`, `MAX_WBITS`, `DEF_MEMLEVEL`, `DEF_COMPRESSION` | Low-level interface to the zlib library |
| `gzip` | `GzipFile`, `open`, `compress`, `decompress` | Support for gzip files |
| `bz2` | `BZ2File`, `BZ2Compressor`, `BZ2Decompressor`, `open`, `compress`, `decompress`, `compresslevel` | Support for bzip2 compression |
| `lzma` | `LZMAFile`, `LZMACompressor`, `LZMADecompressor`, `open`, `compress`, `decompress`, `CHECK_NONE`, `CHECK_CRC32`, `CHECK_CRC64`, `CHECK_SHA256`, `CHECK_ID_MAX`, `PRESET_DEFAULT`, `PRESET_MIN`, `PRESET_MAX`, `FILTER_LZMA1`, `FILTER_LZMA2`, `FILTER_X86`, `FILTER_IA64`, `FILTER_ARM`, `FILTER_ARMTHUMB`, `FILTER_POWERPC`, `FILTER_SPARC`, `FILTER_DELTA` | Support for LZMA compression |
| `zipfile` | `ZipFile`, `PyZipFile`, `ZipInfo`, `ZIP_STORED`, `ZIP_DEFLATED`, `ZIP_BZIP2`, `ZIP_LZMA`, `open`, `is_zipfile` | Read and write ZIP-format archive files |
| `tarfile` | `TarFile`, `TarInfo`, `open`, `is_tarfile`, `USTAR_FORMAT`, `GNU_FORMAT`, `PAX_FORMAT`, `DEFAULT_FORMAT` | Read and write tar-format archive files |

---
---
### **File Formats**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `csv` | `reader`, `writer`, `DictReader`, `DictWriter`, `Sniffer`, `QUOTE_MINIMAL`, `QUOTE_ALL`, `QUOTE_NONNUMERIC`, `QUOTE_NONE`, `Error` | CSV file reading and writing |
| `json` | `dump`, `dumps`, `load`, `loads`, `JSONDecoder`, `JSONEncoder`, `scanner` | JSON (JavaScript Object Notation) support |
| `configparser` | `ConfigParser`, `RawConfigParser`, `SafeConfigParser`, `MissingSectionHeaderError`, `DuplicateSectionError`, `DuplicateOptionError`, `NoSectionError`, `NoOptionError`, `InterpolationError`, `InterpolationMissingOptionError`, `InterpolationSyntaxError`, `ParsingError`, `DEFAULTSECT`, `read`, `read_dict`, `read_string`, `write`, `add_section`, `has_section`, `options`, `read`, `items`, `get`, `getint`, `getfloat`, `getboolean`, `set` | Configuration file parser |
| `netrc` | `netrc`, `NetrcParseError` | netrc file processing |
| `xdrlib` | `Packer`, `Unpacker`, `Error` | XDR library for packing/unpacking |
| `plistlib` | `readPlist`, `writePlist`, `readPlistFromBytes`, `writePlistToBytes`, `dumps`, `loads`, `Data`, `UID`, `InvalidFileException`, `UnknownNodeTypeException` | Generate and parse Apple .plist files |

---
---
### **Cryptographic Services**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `hashlib` | `md5`, `sha1`, `sha224`, `sha256`, `sha384`, `sha512`, `sha3_224`, `sha3_256`, `sha3_384`, `sha3_512`, `blake2b`, `blake2s`, `new`, `pbkdf2_hmac`, `scrypt`, `algorithms_available`, `algorithms_guaranteed` | Secure hash and message digest algorithms |
| `hmac` | `new`, `digest`, `hexdigest`, `copy`, `update` | HMAC message authentication |
| `secrets` | `choice`, `randbelow`, `randbits`, `token_bytes`, `token_hex`, `token_urlsafe`, `compare_digest`, `SystemRandom` | Generate cryptographically strong random numbers |

---
---
### **Generic Operating System Services**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `os` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `io` | `open`, `FileIO`, `RawIOBase`, `BufferedIOBase`, `TextIOBase`, `BytesIO`, `StringIO`, `RawIOBase`, `BufferedReader`, `BufferedWriter`, `BufferedRandom`, `BufferedRWPair`, `IncrementalNewlineDecoder`, `BlockedMapping`, `DEFAULT_BUFFER_SIZE`, `SEEK_SET`, `SEEK_CUR`, `SEEK_END` | Core tools for working with streams |
| `time` | `time`, `sleep`, `clock`, `ctime`, `gmtime`, `localtime`, `mktime`, `strftime`, `strptime`, `timezone`, `tzname`, `altzone`, `daylight`, `tzset`, `asctime`, `clock_gettime`, `clock_getres`, `clock_settime`, `CLOCK_REALTIME`, `CLOCK_MONOTONIC`, `CLOCK_MONOTONIC_RAW`, `CLOCK_PROCESS_CPUTIME_ID`, `CLOCK_THREAD_CPUTIME_ID`, `struct_time` | Time access and conversions |
| `argparse` | `ArgumentParser`, `Namespace`, `FileType`, `HelpFormatter`, `ArgumentDefaultsHelpFormatter`, `RawDescriptionHelpFormatter`, `RawTextHelpFormatter`, `MetavarTypeHelpFormatter`, `ArgumentError`, `SUPPRESS` | Command-line argument parsing |
| `getopt` | `getopt`, `gnu_getopt`, `GetoptError` | Command-line argument parsing (C-style) |
| `logging` | `getLogger`, `basicConfig`, `debug`, `info`, `warning`, `error`, `critical`, `exception`, `log`, `Logger`, `Handler`, `Formatter`, `Filter`, `LogRecord`, `StreamHandler`, `FileHandler`, `RotatingFileHandler`, `TimedRotatingFileHandler`, `NullHandler`, `MemoryHandler`, `NTEventLogHandler`, `SysLogHandler`, `SMTPHandler`, `HTTPHandler`, `SocketHandler`, `DatagramHandler`, `QueueHandler`, `QueueListener`, `BufferingHandler`, `WARNING`, `ERROR`, `CRITICAL`, `FATAL`, `NOTSET`, `DEBUG`, `INFO` | Logging system for Python |
| `logging.config` | `dictConfig`, `fileConfig`, `listen`, `stopListening` | Logging configuration |
| `logging.handlers` | `Handler`, `MemoryHandler`, `NTEventLogHandler`, `SysLogHandler`, `SMTPHandler`, `HTTPHandler`, `SocketHandler`, `DatagramHandler`, `QueueHandler`, `QueueListener`, `BufferingHandler`, `WatchedFileHandler`, `RotatingFileHandler`, `TimedRotatingFileHandler` | Logging handlers |
| `sys` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |
| `sysconfig` | `get_config_var`, `get_config_vars`, `get_path`, `get_paths`, `get_platform`, `get_python_version`, `get_scheme_names`, `is_python_build` | Provide access to Python's configuration information |
| `platform` | `platform`, `machine`, `processor`, `system`, `version`, `release`, `uname`, `java_ver`, `win32_ver`, `win32_edition`, `win32_service_pack`, `win32_processor`, `architecture`, `node`, `python_branch`, `python_compiler`, `python_build`, `python_implementation`, `python_revision`, `python_version`, `python_version_tuple` | Retrieve as much possible information about the platform |
| `resource` | `getrlimit`, `getrusage`, `setrlimit`, `prlimit`, `RLIMIT_CPU`, `RLIMIT_FSIZE`, `RLIMIT_DATA`, `RLIMIT_STACK`, `RLIMIT_CORE`, `RLIMIT_RSS`, `RLIMIT_NPROC`, `RLIMIT_NOFILE`, `RLIMIT_MEMLOCK`, `RLU_NPROC`, `RLU_NOFILE` | Resource usage information |
| `syslog` | `openlog`, `closelog`, `syslog`, `LOG_EMERG`, `LOG_ALERT`, `LOG_CRIT`, `LOG_ERR`, `LOG_WARNING`, `LOG_NOTICE`, `LOG_INFO`, `LOG_DEBUG`, `LOG_KERN`, `LOG_USER`, `LOG_MAIL`, `LOG_DAEMON`, `LOG_AUTH`, `LOG_SYSLOG`, `LOG_LPR`, `LOG_NEWS`, `LOG_UUCP`, `LOG_CRON`, `LOG_AUTHPRIV`, `LOG_LOCAL0`, `LOG_LOCAL1`, `LOG_LOCAL2`, `LOG_LOCAL3`, `LOG_LOCAL4`, `LOG_LOCAL5`, `LOG_LOCAL6`, `LOG_LOCAL7`, `LOG_NDELAY`, `LOG_ODelay`, `LOG_PID`, `LOG_PERROR`, `LOG_CONS`, `LOG_NOWAIT` | Interface to the Unix syslog library |
| `posix` | *(Deprecated; use `os`)* | *(Use `os`)* |
| `posixpath` | *(Deprecated; use `os.path`)* | *(Use `os.path`)* |
| `nt` | *(Windows-specific; use `os`)* | *(Use `os`)* |
| `ntpath` | *(Windows-specific; use `os.path`)* | *(Use `os.path`)* |
| `pwd` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `grp` | *(See File and Directory Access)* | *(See File and Directory Access)* |

---
---
### **Concurrent Execution**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `threading` | `Thread`, `Lock`, `RLock`, `Condition`, `Semaphore`, `BoundedSemaphore`, `Event`, `Timer`, `Barrier`, `active_count`, `current_thread`, `enumerate`, `get_ident`, `main_thread`, `stack_size`, `TIMEOUT_MAX` | Thread-based parallelism |
| `_thread` | `start_new_thread`, `allocate_lock`, `exit_thread`, `get_ident`, `interrupt_main`, `stack_size`, `TIMEOUT_MAX`, `LockType`, `error` | Low-level threading interface |
| `queue` | `Queue`, `LifoQueue`, `PriorityQueue`, `SimpleQueue`, `Empty`, `Full` | A synchronized queue class |
| `multiprocessing` | `Process`, `Pool`, `Connection`, `Queue`, `Pipe`, `Lock`, `RLock`, `Semaphore`, `BoundedSemaphore`, `Condition`, `Event`, `Barrier`, `Value`, `Array`, `Manager`, `active_children`, `cpu_count`, `freeze_support`, `get_all_start_methods`, `get_context`, `get_start_method`, `set_start_method`, `spawn`, `fork`, `forkserver`, `TimeoutError` | Process-based parallelism |
| `multiprocessing.dummy` | *(Deprecated; use `multiprocessing`)* | *(Use `multiprocessing`)* |
| `multiprocessing.pool` | `Pool`, `AsyncResult`, `MapResult`, `ApplyResult` | Process pools |
| `concurrent.futures` | `ThreadPoolExecutor`, `ProcessPoolExecutor`, `Executor`, `Future`, `as_completed`, `wait`, `FirstCompleted`, `AllCompleted`, `TimeoutError`, `BrokenProcessPool`, `ProcessPoolError` | High-level interface for asynchronously executing callables |
| `subprocess` | `run`, `Popen`, `call`, `check_call`, `check_output`, `run`, `DEVNULL`, `PIPE`, `STDOUT`, `SubprocessError`, `CalledProcessError`, `TimeoutExpired` | Subprocess management |
| `signal` | `signal`, `pthread_sigmask`, `sigwait`, `sigwaitinfo`, `sigaltstack`, `pthread_kill`, `kill`, `killpg`, `alarm`, `setitimer`, `getitimer`, `pause`, `sigpending`, `sigprocmask`, `sigblock`, `sigsetmask`, `sigsuspend`, `siginterrupt`, `SIG_DFL`, `SIG_IGN`, `SIGERR`, `NSIG`, `SIGABRT`, `SIGALRM`, `SIGBUS`, `SIGCHLD`, `SIGCONT`, `SIGFPE`, `SIGHUP`, `SIGILL`, `SIGINT`, `SIGIO`, `SIGIOT`, `SIGKILL`, `SIGPIPE`, `SIGPOLL`, `SIGPROF`, `SIGPWR`, `SIGQUIT`, `SIGRTMIN`, `SIGRTMAX`, `SIGSEGV`, `SIGSTKSZ`, `SIGTERM`, `SIGTRAP`, `SIGTSTP`, `SIGTTIN`, `SIGTTOU`, `SIGURG`, `SIGUSR1`, `SIGUSR2`, `SIGVTALRM`, `SIGWINCH`, `SIGXCPU`, `SIGXFSZ`, `SIGXRES`, `Sigmasks`, `ItimerError`, `default_int_handler`, `fwalk` | Set handlers for asynchronous events |
| `sched` | `scheduler`, `sched_param`, `SCHED_OTHER`, `SCHED_FIFO`, `SCHED_RR`, `SCHED_BATCH`, `SCHED_IDLE`, `SCHED_RESET_ON_FORK`, `set_scheduler`, `get_scheduler`, `sched_yield`, `sched_get_priority_min`, `sched_get_priority_max`, `sched_rr_get_interval` | Event scheduler |

---
---
### **Networking and Interprocess Communication**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `socket` | `socket`, `SocketType`, `SocketKind`, `AF_UNIX`, `AF_INET`, `AF_INET6`, `AF_IPX`, `AF_APPLETALK`, `AF_NETLINK`, `AF_TIPC`, `AF_BLUETOOTH`, `AF_ALG`, `AF_VSOCK`, `AF_XDP`, `SOCK_STREAM`, `SOCK_DGRAM`, `SOCK_RAW`, `SOCK_RDM`, `SOCK_SEQPACKET`, `SOCK_DCCP`, `SOCK_PACKET`, `IPPROTO_IP`, `IPPROTO_ICMP`, `IPPROTO_ICMPV6`, `IPPROTO_RAW`, `IPPROTO_TCP`, `IPPROTO_UDP`, `IPPROTO_DCCP`, `IPPROTO_IPV6`, `IPPROTO_ROUTING`, `IPPROTO_FRAGMENT`, `IPPROTO_ESP`, `IPPROTO_AH`, `IPPROTO_SCTP`, `IPPROTO_UDPLITE`, `IPPROTO_RAW`, `IPPROTO_MPTCP`, `SO_DEBUG`, `SO_REUSEADDR`, `SO_REUSEPORT`, `SO_DONTROUTE`, `SO_BROADCAST`, `SO_LINGER`, `SO_OOBINLINE`, `SO_SNDBUF`, `SO_RCVBUF`, `SO_SNDLOWAT`, `SO_RCVLOWAT`, `SO_SNDTIMEO`, `SO_RCVTIMEO`, `SO_TYPE`, `SO_ERROR`, `SO_DONTTRUNC`, `SO_PROTOCOL`, `SO_DOMAIN`, `SO_NOSIGPIPE`, `SO_NO_CHECK`, `SO_PRIORITY`, `SO_BSDCOMPAT`, `SO_PASSCRED`, `SO_PEERCRED`, `SO_RCVGID`, `SO_SECGID`, `SO_SNDGID`, `SO_SECGID`, `SO_BINDTODEVICE`, `SO_ATTACH_FILTER`, `SO_DETACH_FILTER`, `SO_GET_FILTER`, `SO_PEERNAME`, `SO_TIMESTAMP`, `SCM_RIGHTS`, `accept`, `bind`, `connect`, `connect_ex`, `fileno`, `getblocking`, `getpeername`, `getsockname`, `getsockopt`, `listen`, `makefile`, `recv`, `recvfrom`, `recvfrom_into`, `recv_into`, `send`, `sendall`, `sendto`, `setblocking`, `setsockopt`, `shutdown`, `socketpair`, `getaddrinfo`, `getnameinfo`, `getservbyname`, `getservbyport`, `htons`, `htonl`, `ntohs`, `ntohl`, `inet_aton`, `inet_ntoa`, `inet_pton`, `inet_ntop`, `CMSG_LEN`, `CMSG_SPACE`, `getdefaulttimeout`, `setdefaulttimeout`, `create_connection`, `getfqdn`, `herror`, `hstrerror`, `inet_aton`, `inet_ntoa`, `inet_pton`, `inet_ntop`, `ntohs`, `ntohl`, `htons`, `htonl`, `socketpair`, `gethostbyname`, `gethostbyname_ex`, `gethostbyaddr`, `gethostbyaddr_ex`, `getservbyname`, `getservbyport`, `getprotobyname`, `getprotobynumber`, `getnameinfo`, `getaddrinfo`, `AI_PASSIVE`, `AI_CANONNAME`, `AI_NUMERICHOST`, `AI_NUMERICSERV`, `AI_ALL`, `AI_ADDRCONFIG`, `AI_V4MAPPED`, `AI_DEFAULT`, `NI_NUMERICHOST`, `NI_NAMEREQD`, `NI_NUMERICSERV`, `NI_DGRAM`, `NI_NAMEREQD`, `NI_NUMERICHOST`, `NI_NUMERICSERV`, `EAI_ADDRFAMILY`, `EAI_AGAIN`, `EAI_BADFLAGS`, `EAI_FAIL`, `EAI_FAMILY`, `EAI_MEMORY`, `EAI_NODATA`, `EAI_NONAME`, `EAI_OVERFLOW`, `EAI_PROTOCOL`, `EAI_SERVICE`, `EAI_SOCKTYPE`, `EAI_SYSTEM`, `GAIError`, `timeout`, `gethostname`, `sethostname`, `if_nameindex`, `if_indextoname`, `if_nametoindex`, `IFF_UP`, `IFF_BROADCAST`, `IFF_LOOPBACK`, `IFF_POINTOPOINT`, `IFF_MULTICAST`, `socket`, `getaddrinfo`, `getnameinfo` | Low-level networking interface |
| `ssl` | `SSLContext`, `SSLSession`, `SSLSocket`, `SSLWantReadError`, `SSLWantWriteError`, `SSLError`, `SSLErrorNumber`, `SSLZeroReturnError`, `SSLWantReadError`, `SSLWantWriteError`, `SSLSyscallError`, `SSLEOFError`, `SSLError`, `PROTOCOL_TLS`, `PROTOCOL_TLSv1`, `PROTOCOL_TLSv1_1`, `PROTOCOL_TLSv1_2`, `PROTOCOL_SSLv23`, `PROTOCOL_SSLv3`, `PROTOCOL_SSLv2`, `CERT_NONE`, `CERT_OPTIONAL`, `CERT_REQUIRED`, `VERIFY_DEFAULT`, `VERIFY_CRL_CHECK_CHAIN`, `VERIFY_CRL_CHECK_LEAF`, `VERIFY_DEFAULT`, `VERIFY_IGNORE`, `OP_NO_SSLv2`, `OP_NO_SSLv3`, `OP_NO_TLSv1`, `OP_NO_TLSv1_1`, `OP_NO_TLSv1_2`, `OP_NO_COMPRESSION`, `OP_SINGLE_ECDH_USE`, `OP_SINGLE_DH_USE`, `OP_EPHEMERAL_RSA`, `OP_LEGACY_SERVER_CONNECT`, `OP_NO_TICKET`, `OP_ALL`, `wrap_socket`, `match_hostname`, `cert_time_to_seconds`, `get_default_verify_paths`, `get_server_certificate`, `DER_cert_to_PEM_cert`, `PEM_cert_to_DER_cert`, `DER_key_to_PEM_key`, `PEM_key_to_DER_key`, `get_protocol_name` | TLS/SSL wrapper for socket objects |
| `select` | `select`, `poll`, `epoll`, `kqueue`, `devpoll`, `PIPE_BUF` | Waiting for I/O completion |
| `selectors` | `BaseSelector`, `SelectorKey`, `PollSelector`, `EpollSelector`, `DevpollSelector`, `KqueueSelector`, `SelectSelector`, `DefaultSelector` | High-level I/O multiplexing |
| `asyncio` | `coroutine`, `get_event_loop`, `set_event_loop`, `new_event_loop`, `get_event_loop_policy`, `set_event_loop_policy`, `get_child_watcher`, `set_child_watcher`, `get_default_executor`, `set_default_executor`, `all_tasks`, `current_task`, `sleep`, `create_task`, `ensure_future`, `gather`, `wait`, `as_completed`, `shield`, `timeout`, `wait_for`, `to_thread`, `run_coroutine_threadsafe`, `Future`, `Task`, `Event`, `Condition`, `Semaphore`, `BoundedSemaphore`, `Lock`, `RLock`, `Barrier`, `Queue`, `PriorityQueue`, `LifoQueue`, `StreamReader`, `StreamWriter`, `open_connection`, `start_server`, `open_unix_connection`, `start_unix_server`, `SubprocessProtocol`, `Process`, `create_subprocess_exec`, `create_subprocess_shell`, `RunTimeError`, `InvalidStateError`, `CancelledError`, `TimeoutError`, `IncompleteReadError`, `LimitOverrunError`, `Protocol`, `Transport`, `BaseEventLoop`, `AbstractEventLoop`, `SelectorEventLoop`, `UVLoop`, `ProactorEventLoop` | Asynchronous I/O |
| `asyncore` | `dispatcher`, `dispatcher_with_send`, `loop`, `poll`, `poll2`, `create_socket`, `close_all`, `read`, `write`, `readwrite` | Asynchronous socket handler |
| `asynchat` | `async_chat`, `asyncore`, `fifo`, `simple_producer`, `simple_consumer` | Asynchronous chat protocol handler |
| `socketserver` | `BaseServer`, `TCPServer`, `UDPServer`, `UnixStreamServer`, `UnixDatagramServer`, `ForkingMixIn`, `ForkingTCPServer`, `ForkingUDPServer`, `ThreadingMixIn`, `ThreadingTCPServer`, `ThreadingUDPServer`, `BaseRequestHandler`, `StreamRequestHandler`, `DatagramRequestHandler` | Framework for network servers |
| `xmlrpc` | *(Deprecated; use `xmlrpc.client` and `xmlrpc.server`)* | *(Use `xmlrpc.client` and `xmlrpc.server`)* |
| `xmlrpc.client` | `ServerProxy`, `MultiCall`, `Fault`, `ProtocolError`, `ResponseError`, `Binary`, `DateTime`, `Boolean`, `Double`, `Int`, `Long`, `String` | XML-RPC client access |
| `xmlrpc.server` | `SimpleXMLRPCServer`, `SimpleXMLRPCRequestHandler`, `DocXMLRPCServer`, `CGIXMLRPCRequestHandler`, `XMLRPCHandler`, `resolve_dotted_attribute` | Basic XML-RPC server |
| `ipaddress` | `ip_address`, `ip_network`, `ip_interface`, `IPv4Address`, `IPv6Address`, `IPv4Network`, `IPv6Network`, `IPv4Interface`, `IPv6Interface`, `AddressValueError`, `NetmaskValueError`, `summarize_address_range`, `collapse_addresses`, `get_mixed_type_key`, `IPv6Multicast` | IPv4/IPv6 manipulation library |
| `uuid` | `UUID`, `uuid1`, `uuid3`, `uuid4`, `uuid5`, `NAMESPACE_DNS`, `NAMESPACE_URL`, `NAMESPACE_OID`, `NAMESPACE_X500`, `RESERVED_NCS`, `RESERVED_RFC_4122`, `RESERVED_MICROSOFT`, `RESERVED_FUTURE`, `getnode`, `UUID` | UUID objects and generation functions |

---
---
### **Internet Data Handling**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `urllib` | *(Split into submodules)* | *(Use `urllib.request`, `urllib.parse`, etc.)* |
| `urllib.request` | `urlopen`, `Request`, `OpenerDirector`, `HTTPHandler`, `HTTPRedirectHandler`, `HTTPCookieProcessor`, `ProxyHandler`, `HTTPDefaultErrorHandler`, `HTTPErrorProcessor`, `HTTPResponse`, `HTTPError`, `URLError`, `ContentTooShortError`, `HTTPPasswordMgr`, `HTTPPasswordMgrWithDefaultRealm`, `AbstractBasicAuthHandler`, `ProxyBasicAuthHandler`, `ProxyDigestAuthHandler`, `AbstractDigestAuthHandler`, `HTTPDigestAuthHandler`, `BaseHandler`, `build_opener`, `install_opener`, `pathname2url`, `url2pathname`, `getproxies`, `getproxies_environment`, `proxy_bypass`, `proxy_bypass_environment`, `urlretrieve`, `urlcleanup`, `URLopener`, `FancyURLopener` | Extensible library for opening URLs |
| `urllib.response` | `addbase`, `addclose`, `addinfo`, `addinfourl` | Response classes used by `urllib` |
| `urllib.parse` | `urlparse`, `urlunparse`, `urlsplit`, `urlunsplit`, `urljoin`, `urldefrag`, `parse_qs`, `parse_qsl`, `urlencode`, `quote`, `quote_plus`, `unquote`, `unquote_plus`, `urlcleanup`, `spliturl`, `splithost`, `splitnport`, `splituser`, `splitpasswd`, `url2pathname`, `pathname2url`, `uses_netloc`, `uses_params`, `uses_query`, `uses_fragment`, `urlparse`, `ParseResult`, `SplitResult` | Parse URLs into components |
| `urllib.error` | `URLError`, `HTTPError`, `ContentTooShortError` | Exception classes raised by `urllib.request` |
| `urllib.robotparser` | `RobotFileParser`, `urllib.robotparser` | Parser for robots.txt |
| `http` | `HTTPStatus` | HTTP status codes |
| `http.client` | `HTTPConnection`, `HTTPSConnection`, `HTTPResponse`, `HTTPException`, `BadStatusLine`, `LineTooLong`, `InvalidURL`, `UnknownProtocol`, `UnknownTransferEncoding`, `UnimplementedFileMode`, `IncompleteRead`, `ImproperConnectionState`, `CannotSendHeader`, `CannotSendRequest`, `ResponseNotReady`, `RequestNotReady`, `HTTPConnectionPool`, `HTTPSConnectionPool`, `parse_headers`, `read_headers` | HTTP protocol client |
| `http.server` | `BaseHTTPRequestHandler`, `HTTPServer`, `ThreadingHTTPServer`, `ForkingHTTPServer`, `ThreadingMixIn`, `ForkingMixIn`, `SimpleHTTPRequestHandler`, `CGIHTTPRequestHandler` | HTTP server classes |
| `http.cookies` | `Cookie`, `SimpleCookie`, `BaseCookie`, `SerialCookie`, `SmartCookie`, `CookieError`, `OutputFormatter`, `CookieJar`, `DefaultCookiePolicy`, `CookiePolicy` | HTTP Cookie handling |
| `http.cookiejar` | `CookieJar`, `FileCookieJar`, `MozillaCookieJar`, `LWPCookieJar`, `Cookie`, `CookiePolicy`, `DefaultCookiePolicy`, `CookieJar`, `load`, `save`, `make_cookies`, `extract_cookies`, `add_cookie_header`, `request_host`, `set_policy`, `set_cookie`, `set_cookie_if_ok`, `reject_cookie`, `clear`, `clear_session_cookies` | HTTP client cookie handling |
| `ftplib` | `FTP`, `FTP_TLS`, `all_errors`, `error_temp`, `error_perm`, `error_reply`, `error_proto`, `parse150`, `parse226`, `parse227`, `parse228`, `parse229`, `parse257` | FTP protocol client |
| `poplib` | `POP3`, `POP3_SSL`, `all_errors`, `error_proto` | POP3 protocol client |
| `imaplib` | `IMAP4`, `IMAP4_SSL`, `IMAP4_stream`, `all_errors`, `error`, `abort`, `readonly` | IMAP4 protocol client |
| `nntplib` | `NNTP`, `all_errors`, `error_temp`, `error_perm`, `error_reply`, `error_proto` | NNTP protocol client |
| `smtplib` | `SMTP`, `SMTP_SSL`, `LMTP`, `all_errors`, `SMTPException`, `SMTPServerDisconnected`, `SMTPResponseException`, `SMTPSenderRefused`, `SMTPRecipientsRefused`, `SMTPDataError`, `SMTPConnectError`, `SMTPAuthenticationError`, `SMTPNotSupportedError`, `SMTPResponseError`, `debuglevel`, `default_port`, `CRAMMD5_AUTH_AVAILABLE` | SMTP protocol client |
| `telnetlib` | `Telnet`, `IAC`, `DONT`, `DO`, `WONT`, `WILL`, `SE`, `NOP`, `DM`, `BRK`, `IP`, `AO`, `AYT`, `EC`, `EL`, `GA`, `SB`, `WILL`, `WONT`, `DO`, `DONT`, `theNULL` | Telnet protocol client |
| `socketserver` | *(See Networking and Interprocess Communication)* | *(See Networking and Interprocess Communication)* |
| `xmlrpc.client` | *(See Networking and Interprocess Communication)* | *(See Networking and Interprocess Communication)* |
| `xmlrpc.server` | *(See Networking and Interprocess Communication)* | *(See Networking and Interprocess Communication)* |
| `cgi` | `FieldStorage`, `FormContent`, `FormContentDict`, `MiniFieldStorage`, `SvFormContentDict`, `parse`, `parse_multipart`, `parse_header`, `escape`, `print_environ`, `print_environ_usage`, `print_directory`, `print_form`, `test`, `log` | Common Gateway Interface support |
| `cgitb` | `enable`, `disable`, `reset`, `handler`, `text`, `html`, `Hook` | Traceback manager for CGI programs |
| `wsgiref` | `WSGIRequestHandler`, `WSGIServer`, `simple_server`, `handlers`, `util`, `validate`, `demo_app`, `setup_testing_defaults` | WSGI Utilities and Reference Implementation |

---
---
### **Structured Markup Processing Tools**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `html` | `escape`, `unescape` | HTML support |
| `html.parser` | `HTMLParser`, `HTMLParserError` | Simple HTML and XHTML parser |
| `html.entities` | `name2codepoint`, `codepoint2name`, `entitydefs` | Definitions of HTML general entities |
| `xml` | *(Package)* | *(Package containing XML modules)* |
| `xml.etree` | *(Package)* | *(Package containing ElementTree modules)* |
| `xml.etree.ElementTree` | `Element`, `SubElement`, `Comment`, `ProcessingInstruction`, `ElementTree`, `parse`, `fromstring`, `tostring`, `XML`, `XMLParser`, `TreeBuilder`, `XMLTreeBuilder`, `canonicalize`, `indent`, `QName`, `iselement`, `iterparse`, `iter`, `find`, `findall`, `findtext`, `iterfind` | ElementTree API for XML |
| `xml.dom` | *(Package)* | *(Package containing DOM modules)* |
| `xml.dom.minidom` | `Document`, `DocumentFragment`, `DocumentType`, `Element`, `Attr`, `Text`, `Comment`, `ProcessingInstruction`, `CDATASection`, `Entity`, `EntityReference`, `Notation`, `parse`, `parseString`, `getDOMImplementation`, `Node`, `NodeList`, `NamedNodeMap`, `DOMImplementation`, `DOMException` | Lightweight DOM implementation |
| `xml.dom.pulldom` | `PullDom`, `SAX2DOM`, `PullParser`, `default_bufsize` | Support for building a DOM tree from a SAX2 stream |
| `xml.sax` | `parse`, `parseString`, `make_parser`, `getFeature`, `setFeature`, `HandlerBase`, `ContentHandler`, `ErrorHandler`, `DTDHandler`, `EntityResolver`, `InputSource`, `Locator`, `Attributes`, `AttributesNS`, `AttributesImpl`, `AttributesNSImpl`, `SAXException`, `SAXParseException`, `SAXNotRecognizedException`, `SAXNotSupportedException`, `XMLReader`, `IncrementalParser`, `Parser`, `SAXParserFactory` | SAX2 (Simple API for XML) parser |
| `xml.sax.handler` | `feature_external_ges`, `feature_external_pes`, `feature_string_interning`, `property_dom_node`, `property_xml_string`, `property_declaration_handler`, `property_lexical_handler`, `all_features`, `all_properties` | SAX handler base classes |
| `xml.sax.saxutils` | `escape`, `unescape`, `quoteattr`, `XMLFilterBase`, `XMLGenerator`, `prepare_input_source`, `InputSource` | SAX utilities |
| `xml.sax.xmlreader` | `Attributes`, `AttributesImpl`, `AttributesNS`, `AttributesNSImpl`, `ContentHandler`, `DTDHandler`, `EntityResolver`, `ErrorHandler`, `InputSource`, `Locator`, `Parser`, `IncrementalParser`, `SAXException`, `SAXNotRecognizedException`, `SAXNotSupportedException`, `XMLReader`, `XMLReaderFactory` | Interface for SAX2 XML readers |
| `xml.parsers` | *(Package)* | *(Package containing parser modules)* |
| `xml.parsers.expat` | `ParserCreate`, `ExpatError`, `xmlparser`, `ErrorString`, `errors`, `ExpatError`, `model`, `xmlparser`, `ExternEntityParserCreate`, `XMLParserType` | Low-level Expat interface |

---
---
### **Internet Protocols and Support**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `webbrowser` | `open`, `open_new`, `open_new_tab`, `get`, `register`, `unregister`, `Browser` | Easy-to-use controller for web browsers |
| `cgi` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `cgitb` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `wsgiref` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `urllib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `http` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `ftplib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `poplib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `imaplib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `nntplib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `smtplib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `telnetlib` | *(See Internet Data Handling)* | *(See Internet Data Handling)* |
| `socketserver` | *(See Networking and Interprocess Communication)* | *(See Networking and Interprocess Communication)* |
| `xmlrpc` | *(See Networking and Interprocess Communication)* | *(See Networking and Interprocess Communication)* |
| `json` | *(See File Formats)* | *(See File Formats)* |
| `mailcap` | `findmatch`, `getcaps`, `mailcap` | Mailcap file handling |
| `mimetypes` | `guess_type`, `guess_extension`, `init`, `add_type`, `MimeTypes` | Mapping of filenames to MIME types |
| `netrc` | *(See File Formats)* | *(See File Formats)* |
| `nis` | `cat`, `getpwnam`, `getpwuid`, `getgrnam`, `getgrgid`, `match`, `maps`, `get_default_domain`, `set_default_domain`, `get_local_domain`, `get_local_host`, `get_nis_domain`, `get_nis_host`, `get_nis_map`, `get_nis_object`, `nis_error`, `NISError` | Interface to Sun's NIS (Yellow Pages) |
| `rpc` | *(Deprecated)* | *(Use other modules)* |

---
---
### **Software Packaging and Distribution**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `distutils` | *(Package; deprecated in 3.10, removed in 3.12)* | *(Use `setuptools` or `packaging`)* |
| `ensurepip` | `version`, `bootstrap`, `_uninstall` | Bootstrapping the `pip` installer |
| `pip` | *(External package; not part of stdlib)* | *(External package)* |
| `venv` | `create`, `EnvBuilder`, `EnvVar` | Creation of virtual environments |
| `zipapp` | `create_archive`, `get_interpreter` | Manage executable Python zip archives |
| `__phello__` | *(Easter egg)* | *(Easter egg)* |

---
---
### **Python Runtime Services**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `sys` | `argv`, `path`, `modules`, `displayhook`, `excepthook`, `stdin`, `stdout`, `stderr`, `exit`, `exc_info`, `exc_clear`, `getrefcount`, `getsizeof`, `intern`, `is_finalizing`, `addaudithook`, `getdlopenflags`, `setdlopenflags`, `getfilesystemencoding`, `getfilesystemencodeerrors`, `getdefaultencoding`, `getswitchinterval`, `setswitchinterval`, `getrecursionlimit`, `setrecursionlimit`, `getintmax`, `getfloatinfo`, `float_info`, `hash_randomization_seed`, `is_finalizing` | System-specific parameters and functions |
| `sysconfig` | `get_config_var`, `get_config_vars`, `get_path`, `get_paths`, `get_platform`, `get_python_version`, `get_scheme_names`, `is_python_build` | Provide access to Python's configuration information |
| `builtins` | *(See Built-in Functions)* | *(See Built-in Functions)* |
| `__main__` | | Top-level script environment |
| `gc` | `enable`, `disable`, `isenabled`, `collect`, `set_debug`, `get_debug`, `get_count`, `get_stats`, `get_threshold`, `set_threshold`, `get_objects`, `callbacks`, `collecting`, `stop_world`, `CallbackError` | Interface to the cycle detector |
| `inspect` | `getmembers`, `getdoc`, `getfile`, `getmodule`, `getmro`, `getclasstree`, `getouterframes`, `currentframe`, `stack`, `trace`, `isroutine`, `ismethod`, `isfunction`, `isgenerator`, `isgeneratorfunction`, `iscoroutine`, `iscoroutinefunction`, `isawaitable`, `isclass`, `isabstract`, `ismodule`, `isbuiltin`, `isframe`, `istraceback`, `iscode`, `isdatadescriptor`, `getattr_static`, `hasattr_static`, `signature`, `Parameter`, `Signature`, `BoundArguments`, `getcallargs`, `formatargvalues`, `formatargspec`, `ArgSpec`, `getfullargspec`, `getargvalues`, `argvalspec`, `ClassFoundException`, `BlockFinder` | Get information about live objects |
| `dis` | `dis`, `disco`, `distb`, `dump`, `code_info`, `show_code`, `Bytecode`, `Instruction`, `OpcodeInfo` | Disassembler for Python bytecode |
| `traceback` | `print_exc`, `print_exception`, `print_last`, `print_stack`, `print_tb`, `format_exc`, `format_exception`, `format_tb`, `extract_tb`, `extract_stack`, `tb_lineno`, `tb_frame`, `TracebackException` | Stack trace utilities |
| `__future__` | `all_feature_names`, `print_function`, `unicode_literals`, `absolute_import`, `division`, `generators`, `nested_scopes`, `with_statement`, `annotations` | Future statement definitions |
| `copy` | *(See Data Types)* | *(See Data Types)* |
| `pprint` | *(See Data Types)* | *(See Data Types)* |
| `reprlib` | *(See Data Types)* | *(See Data Types)* |
| `abc` | *(See Data Types)* | *(See Data Types)* |

---
---
### **Custom Python Interpreters**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `code` | `InteractiveConsole`, `InteractiveInterpreter`, `compile_command`, `softspace` | Base classes for the read-eval-print loop |
| `codeop` | `compile_command`, `CommandCompiler`, `PyCF_DONT_IMPLY_DEDENT` | Compile Python code |
| `codecs` | *(See Binary Data)* | *(See Binary Data)* |
| `compileall` | `compile_dir`, `compile_file`, `compile_path`, `PY_SOURCE`, `PY_COMPILED`, `all` | Tools for compiling all Python files in a directory |
| `py_compile` | `compile`, `main`, `PyCompileError` | Compile Python source files |

---
---
### **Restricted Execution**
*(Mostly removed or deprecated in Python 3)*

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `rexec` | *(Removed)* | *(Removed in Python 3)* |
| `Bastion` | *(Removed)* | *(Removed in Python 3)* |

---
---
### **Importing Modules**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `importlib` | `import_module`, `reload`, `invalidate_caches`, `find_loader`, `find_spec`, `util`, `machinery`, `metadata`, `resources` | The implementation of import |
| `importlib.abc` | `Finder`, `Loader`, `MetaPathFinder`, `PathEntryFinder`, `FileFinder`, `NamespaceLoader`, `ExecutionLoader`, `InspectLoader`, `ResourceReader` | Abstract base classes for import |
| `importlib.machinery` | `ModuleSpec`, `PathFinder`, `FileFinder`, `ExtensionFileLoader`, `SourceFileLoader`, `SourcelessFileLoader`, `NamespaceLoader`, `WindowsRegistryFinder`, `FrozenImporter`, `BuiltinImporter` | Import machinery |
| `importlib.metadata` | `distribution`, `requires`, `version`, `entry_points`, `files`, `PackageNotFoundError`, `DistributionNotFoundError` | Metadata for installed Python distribution packages |
| `importlib.resources` | `files`, `as_file`, `path`, `open_binary`, `open_text`, `open_resource`, `read_binary`, `read_text`, `contents`, `is_resource`, `ResourceReader`, `Package`, `ResourcePackage` | Resource reading and access |
| `importlib.util` | `spec_from_loader`, `spec_from_file_location`, `module_from_spec`, `resolve_name`, `find_spec`, `cache_from_source`, `source_from_cache`, `decode_source`, `MAGIC_NUMBER` | Utilities for import |
| `pkgutil` | `get_data`, `get_loader`, `find_loader`, `iter_modules`, `iter_importers`, `walk_packages`, `imp`, `get_importer`, `read_pkg`, `write_pkg`, `extend_path`, `declare_namespace`, `ModuleInfo`, `Provider` | Package utilities |
| `runpy` | `run_module`, `run_path`, `_run_code`, `_run_module_code` | Locate and execute Python modules |
| `site` | `getsitepackages`, `addsitedir`, `removesitedir`, `getusersitepackages`, `getuserbase`, `USER_SITE`, `USER_BASE`, `ENABLE_USER_SITE`, `check_enableusersite`, `addpackage`, `getmodulename`, `check_path` | Site-specific configuration path setup |

---
---
### **Python Language Services**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `ast` | `parse`, `literal_eval`, `dump`, `NodeVisitor`, `NodeTransformer`, `Module`, `Interactive`, `Expression`, `FunctionDef`, `ClassDef`, `Return`, `Delete`, `Assign`, `AugAssign`, `For`, `AsyncFor`, `While`, `If`, `With`, `AsyncWith`, `Raise`, `Try`, `Assert`, `Import`, `ImportFrom`, `Global`, `Nonlocal`, `Expr`, `BoolOp`, `BinOp`, `UnaryOp`, `Lambda`, `IfExp`, `Dict`, `Set`, `ListComp`, `SetComp`, `DictComp`, `GeneratorExp`, `Await`, `Yield`, `YieldFrom`, `Compare`, `Call`, `Keyword`, `Starred`, `Name`, `Load`, `Store`, `Del`, `Starred`, `NameConstant`, `Ellipsis`, `Num`, `Str`, `Bytes`, `NameConstant`, `Ellipsis`, `Attribute`, `Subscript`, `Starred`, `Name`, `Load`, `Store`, `Del`, `AugLoad`, `AugStore`, `Param`, `arg`, `keyword`, `alias`, `AST` | Abstract Syntax Trees |
| `symtable` | `symtable`, `SymbolTableFactory`, `Class`, `Function`, `Block`, `Scope`, `LookupError` | Interface to the compiler's symbol tables |
| `token` | `tok_name`, `ISEOF`, `ENDMARKER`, `NAME`, `NUMBER`, `STRING`, `NEWLINE`, `INDENT`, `DEDENT`, `LPAR`, `RPAR`, `LSQB`, `RSQB`, `COLON`, `COMMA`, `SEMI`, `PLUS`, `MINUS`, `STAR`, `SLASH`, `VDIV`, `MOD`, `AMPER`, `VBAR`, `CARET`, `LEFTSHIFT`, `RIGHTSHIFT`, `DOUBLESTAR`, `PLUSEQUAL`, `MINEQUAL`, `STAREQUAL`, `SLASHEQUAL`, `PERCENTEQUAL`, `AMPEREQUAL`, `VBAREQUAL`, `CARETEQUAL`, `LEFTSHIFTEQUAL`, `RIGHTSHIFTEQUAL`, `DOUBLESTAREQUAL`, `DOUBLEEQUAL`, `EQUAL`, `NOTEQUAL`, `LESS`, `LESSEQUAL`, `GREATER`, `GREATEREQUAL`, `AT`, `ATEQUAL`, `RARROW`, `ELLIPSES`, `COLONEQUAL`, `OP`, `AWAIT`, `ASYNC`, `TYPE_IGNORE`, `TYPE_COMMENT`, `SOFT_KEYWORD`, `fstring_start`, `fstring_middle`, `fstring_end`, `COMMENT`, `NL`, `ENCODING`, `N_TOKENS`, `NT_OFFSET` | Constants representing internal tokens |
| `keyword` | `iskeyword`, `issoftkeyword`, `kwlist`, `softkwlist` | Check for Python keywords |
| `tokenize` | `generate_tokens`, `untokenize`, `TokenInfo`, `STRING`, `NUMBER`, `NAME`, `COMMENT`, `NL`, `ENCODING`, `ERRORTOKEN`, `N_TOKENS`, `ISEOF`, `ENDMARKER`, `tokenize` | Tokenizer for Python source |
| `tabnanny` | `check`, `NannyNag`, `IndentationError` | Tool for detecting inconsistent indentation |
| `pyclbr` | `readmodule`, `readmodule_ex`, `Class`, `Function`, `getmembers`, `getmembers_ex` | Python class browser support |
| `py_compile` | *(See Custom Python Interpreters)* | *(See Custom Python Interpreters)* |
| `compileall` | *(See Custom Python Interpreters)* | *(See Custom Python Interpreters)* |
| `dis` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |

---
---
### **System and Shell Interface**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `os` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `os.path` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `pathlib` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `glob` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `fnmatch` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `fileinput` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `subprocess` | *(See Concurrent Execution)* | *(See Concurrent Execution)* |
| `shlex` | `split`, `quote`, `shlex` | Simple lexical analysis for Unix shell-like syntaxes |
| `shutil` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `tempfile` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `pwd` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `grp` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `sys` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |
| `platform` | *(See Generic Operating System Services)* | *(See Generic Operating System Services)* |
| `resource` | *(See Generic Operating System Services)* | *(See Generic Operating System Services)* |
| `syslog` | *(See Generic Operating System Services)* | *(See Generic Operating System Services)* |
| `posix` | *(Deprecated; use `os`)* | *(Use `os`)* |
| `posixpath` | *(Deprecated; use `os.path`)* | *(Use `os.path`)* |
| `nt` | *(Windows-specific; use `os`)* | *(Use `os`)* |
| `ntpath` | *(Windows-specific; use `os.path`)* | *(Use `os.path`)* |
| `fcntl` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `termios` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `tty` | *(See File and Directory Access)* | *(See File and Directory Access)* |
| `pty` | *(See File and Directory Access)* | *(See File and Directory Access)* |

---
---
### **Debugging and Profiling**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `pdb` | `Pdb`, `run`, `runcall`, `set_trace`, `post_mortem`, `pm`, `runctx`, `restart`, `cl`, `clear`, `commands`, `condition`, `continue`, `debug`, `disable`, `display`, `down`, `enable`, `exit`, `h`, `help`, `ignore`, `interact`, `j`, `jump`, `l`, `list`, `ll`, `longlist`, `n`, `next`, `p`, `pp`, `print`, `q`, `quit`, `r`, `return`, `s`, `step`, `u`, `up`, `w`, `where`, `BdbQuit`, `PdbError` | The Python debugger |
| `pdb` | *(Same as above)* | *(Same as above)* |
| `profile` | `Profile`, `run`, `runctx`, `Stats`, `print_stats`, `pstats` | Python profiler |
| `pstats` | `Stats`, `SortKey` | Statistics object for use with the profile module |
| `timeit` | `Timer`, `timeit`, `repeat`, `default_timer`, `default_number`, `default_repeat` | Measure execution time of small code snippets |
| `trace` | `Trace`, `Counts`, `CoverageResults` | Trace or track Python statement execution |
| `tracemalloc` | `start`, `stop`, `is_tracing`, `get_traced_memory`, `get_object_traceback`, `get_traceback`, `clear_traces`, `reset_peak`, `take_snapshot`, `Snapshot`, `DomainFilter`, `Filter` | Trace memory allocations |
| `sys` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |
| `inspect` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |
| `dis` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |
| `gc` | *(See Python Runtime Services)* | *(See Python Runtime Services)* |

---
---
### **Development Tools**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `unittest` | `TestCase`, `TestSuite`, `TestLoader`, `TextTestRunner`, `TextTestResult`, `TestProgram`, `main`, `defaultTestLoader`, `TestLoader`, `FunctionTestCase`, `skip`, `skipIf`, `skipUnless`, `expectedFailure`, `assertEqual`, `assertNotEqual`, `assertTrue`, `assertFalse`, `assertIs`, `assertIsNot`, `assertIsNone`, `assertIsNotNone`, `assertIn`, `assertNotIn`, `assertIsInstance`, `assertNotIsInstance`, `assertAlmostEqual`, `assertNotAlmostEqual`, `assertGreater`, `assertGreaterEqual`, `assertLess`, `assertLessEqual`, `assertRegex`, `assertNotRegex`, `assertCountEqual`, `assertMultiLineEqual`, `assertSequenceEqual`, `assertListEqual`, `assertTupleEqual`, `assertSetEqual`, `assertDictEqual`, `assertDictContainsSubset`, `assertRaises`, `assertRaisesRegex`, `assertWarns`, `assertWarnsRegex`, `fail`, `error`, `expectingFailure`, `cleanup`, `addCleanup`, `doCleanups`, `setUp`, `tearDown`, `setUpClass`, `tearDownClass`, `setUpModule`, `tearDownModule`, `classSetUp`, `classTearDown`, `moduleSetUp`, `moduleTearDown` | Unit testing framework |
| `unittest.mock` | `Mock`, `MagicMock`, `patch`, `patch.object`, `patch.dict`, `patch.multiple`, `call`, `create_autospec`, `ANY`, `FILNO`, `sentries`, `mock_open`, `PropertyMock`, `NonCallableMock`, `NonCallableMagicMock`, `CallableMixin`, `BaseSpec`, `_Missing`, `spec`, `spec_set`, `MockSpec`, `FunctionSpec` | Mock object library |
| `doctest` | `testmod`, `testfile`, `DocTestParser`, `DocTestRunner`, `OutputChecker`, `DocTest`, `Example`, `skip`, `master`, `TestResults`, `NORMALIZE_WHITESPACE`, `ELLIPSIS`, `IGNORE_EXCEPTION_DETAIL`, `REPORT_UDIFF`, `REPORT_CDIFF`, `REPORT_NDIFF`, `REPORT_ONLY_FIRST_FAILURE`, `DONT_ACCEPT_TRUE_FOR_1`, `DONT_ACCEPT_BLANKLINE` | Test interactive Python examples |
| `pdb` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |
| `profile` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |
| `pstats` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |
| `timeit` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |
| `trace` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |
| `tracemalloc` | *(See Debugging and Profiling)* | *(See Debugging and Profiling)* |

---
---
### **Unicode Support**

| Module | Key Components | Description |
|--------|-----------------|-------------|
| `codecs` | *(See Binary Data)* | *(See Binary Data)* |
| `encodings` | `aliases`, `codecs`, `mbcs` | Codec registry and base classes |
| `encodings.ascii` | `IncrementalEncoder`, `IncrementalDecoder`, `StreamReader`, `StreamWriter` | ASCII codec |
| `encodings.base64_codec` | `base64_encode`, `base64_decode` | Base64 codec |
| `encodings.big5` | `IncrementalEncoder`, `IncrementalDecoder` | Big5 codec |
| `encodings.big5hkscs` | `IncrementalEncoder`, `IncrementalDecoder` | Big5-HKSCS codec |
| `encodings.bz2_codec` | `BZ2StreamReader`, `BZ2StreamWriter` | BZ2 codec |
| `encodings.charmap` | `CharmapCodec`, `charmap_encode`, `charmap_decode` | Character mapping codec |
| `encodings.cp037` | `IncrementalEncoder`, `IncrementalDecoder` | EBCDIC CP-US, CP-CA, CP-NL, CP-ROECE, CP-YU codec |
| `encodings.cp1006` | `IncrementalEncoder`, `IncrementalDecoder`