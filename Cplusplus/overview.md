## **Core Headers & Components**

---

### **I/O Streams**
**Header:** `<iostream>`, `<fstream>`, `<sstream>`, `<iomanip>`
| Component | Description |
|-----------|-------------|
| `cin`, `cout`, `cerr`, `clog` | Standard input/output/error streams |
| `wcin`, `wcout`, `werr`, `wlog` | Wide-character streams |
| `ifstream`, `ofstream`, `fstream` | File input/output streams |
| `istringstream`, `ostringstream`, `stringstream` | String-based streams |
| `setw(n)`, `setprecision(n)`, `setfill(c)` | Formatting manipulators |
| `boolalpha`, `noboolalpha`, `hex`, `dec`, `oct` | Base/boolean manipulators |
| `endl`, `flush` | Stream control |

---

### **Containers**
**Headers:** `<vector>`, `<list>`, `<deque>`, `<array>`, `<forward_list>`, `<set>`, `<map>`, `<unordered_set>`, `<unordered_map>`, `<stack>`, `<queue>`, `<span>`

| **Category**       | **Containers** | **Description** |
|--------------------|----------------|-----------------|
| **Sequence**       | `vector<T>` | Dynamic array |
|                    | `list<T>` | Doubly-linked list |
|                    | `deque<T>` | Double-ended queue |
|                    | `array<T,N>` | Fixed-size array |
|                    | `forward_list<T>` | Singly-linked list |
| **Associative**    | `set<T>` | Ordered unique elements |
|                    | `multiset<T>` | Ordered elements (duplicates allowed) |
|                    | `map<K,V>` | Ordered key-value pairs |
|                    | `multimap<K,V>` | Ordered key-value pairs (duplicate keys allowed) |
| **Unordered**      | `unordered_set<T>` | Hash-based unique elements |
|                    | `unordered_multiset<T>` | Hash-based elements (duplicates allowed) |
|                    | `unordered_map<K,V>` | Hash-based key-value pairs |
|                    | `unordered_multimap<K,V>` | Hash-based key-value pairs (duplicate keys allowed) |
| **Adapters**       | `stack<T>` | LIFO stack (uses `deque` by default) |
|                    | `queue<T>` | FIFO queue (uses `deque` by default) |
|                    | `priority_queue<T>` | Max-heap (uses `vector` by default) |
| **Views**          | `span<T>` (C++20) | Non-owning view of a contiguous sequence |

---

---

### **Algorithms**
**Headers:** `<algorithm>`, `<numeric>`

| **Category**       | **Functions** | **Description** |
|--------------------|---------------|-----------------|
| **Sorting**        | `sort`, `stable_sort` | Sort a range |
|                    | `partial_sort` | Sort first N elements |
|                    | `nth_element` | Partially sort to position N |
| **Searching**      | `find`, `find_if` | Find element/match |
|                    | `binary_search` | Check if element exists (sorted range) |
|                    | `lower_bound`, `upper_bound` | Find insertion point |
| **Modifying**      | `copy`, `move` | Copy/move elements |
|                    | `transform` | Apply function to range |
|                    | `replace`, `replace_if` | Replace elements |
|                    | `remove`, `remove_if` | Remove elements (moves to end) |
|                    | `unique` | Remove consecutive duplicates |
| **Reordering**     | `reverse`, `rotate` | Reverse/rotate range |
|                    | `shuffle` | Randomly shuffle range |
|                    | `next_permutation`, `prev_permutation` | Generate permutations |
| **Numeric**        | `accumulate` | Sum/accumulate values |
|                    | `partial_sum` | Compute partial sums |
|                    | `inner_product` | Dot product of two ranges |
|                    | `gcd`, `lcm` (C++17) | Greatest common divisor / Least common multiple |
| **Min/Max**        | `min`, `max`, `minmax` | Find min/max |
|                    | `min_element`, `max_element` | Find min/max in range |
| **Heap**           | `make_heap`, `push_heap`, `pop_heap`, `sort_heap` | Heap operations |
| **Set Operations**| `set_union`, `set_intersection`, `set_difference`, `set_symmetric_difference` | Set operations (sorted ranges) |
| **Comparisons**    | `equal`, `lexicographical_compare`, `mismatch` | Compare ranges |

---

---

### **Strings**
**Headers:** `<string>`, `<string_view>`, `<charconv>` (C++17)

| **Component** | **Description** |
|---------------|-----------------|
| `std::string` | Dynamic string |
| `std::wstring`, `std::u16string`, `std::u32string` | Wide/Unicode strings |
| `std::string_view` (C++17) | Non-owning string view |
| `substr`, `find`, `rfind` | Substring/search |
| `append`, `replace`, `insert`, `erase` | Modification |
| `compare`, `starts_with`, `ends_with` (C++20) | Comparison |
| `to_string`, `stoi`, `stol`, `stoll`, `stoul`, `stoull` | String <-> numeric conversions |
| `from_chars`, `to_chars` (C++17) | Fast numeric <-> string conversions |

---

---

### **Memory Management**
**Headers:** `<memory>`, `<new>`

| **Component** | **Description** |
|---------------|-----------------|
| **Smart Pointers** | |
| `unique_ptr<T>` | Exclusive ownership |
| `shared_ptr<T>` | Shared ownership |
| `weak_ptr<T>` | Non-owning observer for `shared_ptr` |
| `make_unique<T>(args...)`, `make_shared<T>(args...)` | Factory functions |
| `static_pointer_cast`, `dynamic_pointer_cast`, `const_pointer_cast` | Pointer casts |
| **Allocators** | |
| `allocator<T>` | Default allocator |
| `allocator_traits` | Allocator traits |
| **Raw Memory** | |
| `align_val_t`, `launder` (C++17) | Alignment utilities |
| **Exceptions** | |
| `bad_alloc` | Thrown on allocation failure |
| `nothrow` | Allocation without exceptions |

---

---

### **Concurrency & Threading**
**Headers:** `<thread>`, `<mutex>`, `<condition_variable>`, `<future>`, `<atomic>`

| **Category** | **Component** | **Description** |
|--------------|---------------|-----------------|
| **Threads** | `std::thread` | Thread management |
| | `this_thread::get_id()`, `yield()`, `sleep_for()`, `sleep_until()` | Thread utilities |
| **Mutexes** | `mutex`, `timed_mutex` | Basic mutexes |
| | `recursive_mutex`, `recursive_timed_mutex` | Reentrant mutexes |
| | `shared_mutex` (C++17), `shared_timed_mutex` (C++14) | Reader-writer mutexes |
| **Locks** | `lock_guard<T>` | RAII lock (basic) |
| | `unique_lock<T>` | RAII lock (flexible) |
| | `shared_lock<T>` (C++14) | Shared (reader) lock |
| | `scoped_lock` (C++17) | Deadlock-avoiding lock for multiple mutexes |
| **Condition Variables** | `condition_variable`, `condition_variable_any` | Thread synchronization |
| **Futures** | `promise<T>`, `future<T>`, `shared_future<T>` | Asynchronous results |
| | `async` | Run function asynchronously |
| | `packaged_task<T>` | Wrap a callable for async execution |
| **Atomics** | `atomic<T>`, `atomic_flag` | Atomic variables |
| | `atomic_ref<T>` (C++20) | Atomic reference to non-atomic object |
| | `memory_order_relaxed`, `memory_order_consume`, `memory_order_acquire`, `memory_order_release`, `memory_order_acq_rel`, `memory_order_seq_cst` | Memory ordering |

---
---
### **Utilities**
**Headers:** `<utility>`, `<tuple>`, `<optional>`, `<variant>`, `<any>`, `<functional>`, `<chrono>`, `<ratio>`

| **Category** | **Component** | **Description** |
|--------------|---------------|-----------------|
| **Pairs & Tuples** | `pair<T1, T2>`, `make_pair` | Pair of values |
| | `tuple<...>`, `make_tuple`, `tie`, `get<N>` | Fixed-size collection of heterogeneous values |
| **Optional & Variant** | `optional<T>` (C++17) | Maybe/monadic value |
| | `variant<T...>` (C++17) | Type-safe union |
| | `holds_alternative`, `get<T>`, `visit` | Variant utilities |
| | `any` (C++17) | Type-erased value |
| **Function Objects** | `function<R(Args...)>` | Polymorphic function wrapper |
| | `bind`, `ref`, `cref`, `mem_fn` | Function binding |
| **Time** | `chrono::duration`, `chrono::time_point` | Time durations and points |
| | `system_clock`, `steady_clock`, `high_resolution_clock` | Clocks |
| | `seconds`, `milliseconds`, `microseconds`, `nanoseconds` | Duration units |
| | `time_t`, `tm` (from `<ctime>`) | C-style time |
| **Ratio** | `ratio<Num, Den>`, `milli`, `micro`, `nano`, `kilo`, `mega` | Compile-time rational numbers |

---
---
### **Numerics**
**Headers:** `<random>`, `<complex>`, `<cmath>`, `<numeric>`, `<cstdlib>`

| **Category** | **Component** | **Description** |
|--------------|---------------|-----------------|
| **Random Numbers** | `random_device` | Non-deterministic random number generator |
| | `mt19937`, `mt19937_64` | Mersenne Twister engines |
| | `minstd_rand`, `rand` | Linear congruential engine |
| | `uniform_int_distribution<T>` | Uniform integer distribution |
| | `uniform_real_distribution<T>` | Uniform real distribution |
| | `normal_distribution<T>` | Normal (Gaussian) distribution |
| | `bernoulli_distribution` | Boolean distribution |
| | `poisson_distribution`, `binomial_distribution`, etc. | Other distributions |
| **Complex Numbers** | `complex<T>`, `polar<T>` | Complex number support |
| | `real`, `imag`, `abs`, `arg`, `conj`, `norm` | Complex operations |
| **Math Functions** | `sqrt`, `pow`, `exp`, `log`, `log10`, `log2` | Exponential/logarithmic |
| | `sin`, `cos`, `tan`, `asin`, `acos`, `atan`, `atan2` | Trigonometric |
| | `sinh`, `cosh`, `tanh` | Hyperbolic |
| | `ceil`, `floor`, `round`, `trunc` | Rounding |
| | `fmod`, `remainder`, `fabs` | Modulo/absolute |
| | `hypot`, `fma` | Hypotenuse/fused multiply-add |

---
---
### **Filesystem** (C++17)
**Header:** `<filesystem>`

| **Component** | **Description** |
|---------------|-----------------|
| `path` | Filesystem path manipulation |
| `directory_entry` | Directory entry info |
| `directory_iterator`, `recursive_directory_iterator` | Directory traversal |
| `file_status`, `file_type` | File status/type |
| `space_info` | Filesystem space info |
| **Functions** | |
| `exists`, `is_directory`, `is_regular_file`, `is_symlink` | Path checks |
| `file_size`, `last_write_time`, `last_access_time` | File metadata |
| `create_directory`, `create_directories` | Directory creation |
| `remove`, `remove_all` | File/directory removal |
| `rename`, `copy`, `copy_file` | File operations |
| `equivalent`, `canonical`, `absolute`, `relative` | Path utilities |
| `current_path`, `temp_directory_path` | System paths |

---
---
### **Regular Expressions**
**Header:** `<regex>`

| **Component** | **Description** |
|---------------|-----------------|
| `regex`, `wregex` | Regular expression objects |
| `smatch`, `cmatch`, `ssubmatch`, `csubmatch` | Match result containers |
| **Functions** | |
| `regex_match` | Full string match |
| `regex_search` | Partial string match |
| `regex_replace` | Replace matches |
| `regex_iterator`, `regex_token_iterator` | Iterate over matches |
| **Flags** | |
| `regex_constants::icase`, `regex_constants::nosubs` | Matching options |

---
---
### **Type Support**
**Headers:** `<typeinfo>`, `<type_traits>`, `<limits>`

| **Category** | **Component** | **Description** |
|--------------|---------------|-----------------|
| **Type Info** | `typeid`, `type_info` | Runtime type information |
| | `type_info::name()`, `type_info::hash_code()` | Type metadata |
| **Type Traits** | `is_same<T, U>`, `is_integral<T>`, `is_floating_point<T>` | Type checks |
| | `is_arithmetic<T>`, `is_class<T>`, `is_enum<T>` | Category checks |
| | `is_const<T>`, `is_volatile<T>`, `is_reference<T>` | CV-qualifier checks |
| | `enable_if<Cond, T>`, `conditional<Cond, T, F>` | Conditional types |
| | `remove_reference<T>`, `add_const<T>`, `remove_pointer<T>` | Type transformations |
| | `decay<T>`, `common_type<T...>`, `result_of<F(Args...)>` | Advanced transformations |
| **Limits** | `numeric_limits<T>::min()`, `max()`, `digits`, `is_signed` | Numeric type properties |

---
---
### **Error Handling**
**Headers:** `<exception>`, `<stdexcept>`, `<system_error>`

| **Component** | **Description** |
|---------------|-----------------|
| `exception` | Base class for all standard exceptions |
| `bad_exception` | Thrown by `unexpected()` |
| **Logic Errors** | `logic_error` (base) |
| | `invalid_argument`, `domain_error`, `length_error`, `out_of_range` | Specific logic errors |
| **Runtime Errors** | `runtime_error` (base) |
| | `range_error`, `overflow_error`, `underflow_error` | Specific runtime errors |
| **System Errors** | `system_error` | System-level errors |
| | `error_code`, `error_condition` | Error code/condition objects |
| | `make_error_code`, `make_error_condition` | Factory functions |
| | `generic_category()`, `system_category()` | Error categories |

---
---
---
## **C++20 Additions**

| **Header** | **Components** | **Description** |
|------------|----------------|-----------------|
| `<coroutine>` | `coroutine_handle`, `suspend_always`, `suspend_never` | Coroutine support |
| `<ranges>` | `view`, `range`, `subrange`, `views::filter`, `views::transform` | Range-based operations |
| `<concepts>` | `concept`, `requires`, `requires_expression` | Constraints/Concepts |
| `<format>` | `format`, `vformat`, `format_to`, `vformat_to` | Type-safe formatting |
| `<source_location>` | `source_location` | Compile-time source location |
| `<bit>` | `bit_cast`, `countl_zero`, `countr_zero`, `popcount`, `bit_ceil`, `bit_floor` | Bit manipulation |
| `<compare>` | `strong_ordering`, `weak_ordering`, `partial_ordering`, `<=>` | Three-way comparison |
| `<span>` | `span<T>` | Non-owning view of contiguous sequences |
| `<syncstream>` | `syncstream`, `osyncstream` | Synchronized output streams |

---
---
## **C++23 Additions (Partial)**

| **Header** | **Components** | **Description** |
|------------|----------------|-----------------|
| `<print>` | `print`, `println` | Formatted output to stdout |
| `<mdspan>` | `mdspan` | Multidimensional array view |
| `<stop_token>` | `stop_token`, `stop_source`, `stop_callback` | Cooperative cancellation |
| `<stacktrace>` | `stacktrace`, `stacktrace_entry` | Stack trace capture |
| `<generator>` | `generator<T>` | Coroutine-based generator |
| `<expected>` | `expected<T, E>` | Either a value or an error (like Rust's Result) |