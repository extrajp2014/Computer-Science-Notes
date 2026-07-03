## Core Types and Traits

### Primitive Types

| Code | Description |
|------|-------------|
| `i8` | 8-bit signed integer |
| `i16` | 16-bit signed integer |
| `i32` | 32-bit signed integer |
| `i64` | 64-bit signed integer |
| `i128` | 128-bit signed integer |
| `isize` | Pointer-sized signed integer |
| `u8` | 8-bit unsigned integer |
| `u16` | 16-bit unsigned integer |
| `u32` | 32-bit unsigned integer |
| `u64` | 64-bit unsigned integer |
| `u128` | 128-bit unsigned integer |
| `usize` | Pointer-sized unsigned integer |
| `f32` | 32-bit floating point (IEEE 754-2008) |
| `f64` | 64-bit floating point (IEEE 754-2008) |
| `bool` | Boolean type (`true` or `false`) |
| `char` | 32-bit Unicode scalar value |
| `()` | Unit type, denotes no meaningful value |

### Smart Pointers

| Code | Description |
|------|-------------|
| `Box<T>` | Heap-allocated value of type `T` |
| `Rc<T>` | Reference-counted pointer for shared ownership |
| `Arc<T>` | Atomic reference-counted pointer for thread-safe shared ownership |
| `Cow<'a, B>` | Clone-on-write smart pointer, either borrowed or owned data |
| `Ref<T>` | Immutable reference to data in a `RefCell` |
| `RefMut<T>` | Mutable reference to data in a `RefCell` |
| `RefCell<T>` | Single ownership with runtime borrow checking |

### Error Handling

| Code | Description |
|------|-------------|
| `Option<T>` | Optional value, either `Some(T)` or `None` |
| `Result<T, E>` | Result of an operation, either `Ok(T)` or `Err(E)` |
| `Option::unwrap()` | Returns the contained `Some` value, panics if `None` |
| `Option::unwrap_or(default)` | Returns the contained `Some` value or a provided default |
| `Option::map<U, F>(f: F) -> Option<U>` | Maps an `Option<T>` to `Option<U>` by applying a function |
| `Option::and_then<U, F>(f: F) -> Option<U>` | Returns `None` if `self` is `None`, otherwise applies `f` |
| `Result::unwrap()` | Returns the contained `Ok` value, panics if `Err` |
| `Result::unwrap_or(default)` | Returns the contained `Ok` value or a provided default |
| `Result::map<T, F>(f: F) -> Result<T, E>` | Maps a `Result<T, E>` to `Result<U, E>` by applying a function |
| `Result::map_err<F, E2>(f: F) -> Result<T, E2>` | Maps a `Result<T, E>` to `Result<T, E2>` by applying a function to the error |
| `Result::and_then<U, F>(f: F) -> Result<U, E>` | Returns `Err` if `self` is `Err`, otherwise applies `f` |
| `?` | Error propagation operator for `Result` and `Option` |

### Collections

| Code | Description |
|------|-------------|
| `Vec<T>` | Growable array type |
| `Vec::new()` | Creates a new, empty `Vec` |
| `Vec::with_capacity(capacity)` | Creates a new `Vec` with specified capacity |
| `Vec::push(value)` | Appends a value to the back of the `Vec` |
| `Vec::pop() -> Option<T>` | Removes and returns the last element, or `None` if empty |
| `Vec::len() -> usize` | Returns the number of elements in the `Vec` |
| `Vec::get(index) -> Option<&T>` | Returns a reference to the element at `index`, or `None` if out of bounds |
| `Vec::iter()` | Returns an iterator over immutable references to the elements |
| `Vec::iter_mut()` | Returns an iterator over mutable references to the elements |
| `Vec::into_iter()` | Consumes the `Vec` and returns an iterator over the elements |
| `String` | UTF-8 encoded, growable string |
| `String::new()` | Creates a new, empty `String` |
| `String::from(str)` | Converts a string slice to a `String` |
| `String::push_str(s)` | Appends a string slice to the `String` |
| `String::push(c)` | Appends a `char` to the `String` |
| `String::len() -> usize` | Returns the length of the `String` in bytes |
| `HashMap<K, V>` | Hash table with `K` as keys and `V` as values |
| `HashMap::new()` | Creates a new, empty `HashMap` |
| `HashMap::insert(k, v)` | Inserts a key-value pair into the `HashMap` |
| `HashMap::get(&k) -> Option<&V>` | Returns a reference to the value associated with `k`, or `None` if not found |
| `HashMap::remove(&k) -> Option<V>` | Removes and returns the value associated with `k`, or `None` if not found |
| `HashSet<T>` | Hash set of type `T` |
| `HashSet::new()` | Creates a new, empty `HashSet` |
| `HashSet::insert(value)` | Inserts a value into the `HashSet` |
| `HashSet::contains(&value) -> bool` | Returns `true` if the `HashSet` contains `value` |
| `LinkedList<T>` | Doubly-linked list |
| `VecDeque<T>` | Double-ended queue |
| `BinaryHeap<T>` | Priority queue |
| `BTreeMap<K, V>` | B-tree based map |
| `BTreeSet<T>` | B-tree based set |

### Strings and Text

| Code | Description |
|------|-------------|
| `str` | Immutable UTF-8 string slice |
| `&str` | Reference to a string slice |
| `String` | Owned, growable UTF-8 string |
| `OsStr` | Platform-native string (OS-specific) |
| `OsString` | Owned, growable platform-native string |
| `CString` | Null-terminated UTF-8 string for FFI |
| `CStr` | Borrowed null-terminated UTF-8 string for FFI |
| `str::len() -> usize` | Returns the length of the string in bytes |
| `str::is_empty() -> bool` | Returns `true` if the string is empty |
| `str::chars()` | Returns an iterator over the `char`s in the string |
| `str::bytes()` | Returns an iterator over the bytes in the string |
| `str::split_whitespace()` | Returns an iterator over substrings split by whitespace |
| `str::split<'a, P>(pattern: P) -> Split<'a, P>` | Returns an iterator over substrings split by a pattern |
| `str::trim()` | Returns the string with leading and trailing whitespace removed |
| `str::starts_with(prefix) -> bool` | Returns `true` if the string starts with `prefix` |
| `str::ends_with(suffix) -> bool` | Returns `true` if the string ends with `suffix` |
| `str::contains(substring) -> bool` | Returns `true` if the string contains `substring` |
| `str::replace<'a>(from: &str, to: &str) -> String` | Replaces all occurrences of `from` with `to` |
| `str::to_uppercase()` | Returns the string in uppercase |
| `str::to_lowercase()` | Returns the string in lowercase |
| `format!("{}", value)` | Formats a value into a `String` |
| `println!("{}", value)` | Prints a value to stdout with a newline |
| `eprintln!("{}", value)` | Prints a value to stderr with a newline |

---

## Input/Output

### Standard I/O

| Code | Description |
|------|-------------|
| `println!()` | Macro to print to stdout with a newline |
| `print!()` | Macro to print to stdout without a newline |
| `eprintln!()` | Macro to print to stderr with a newline |
| `eprint!()` | Macro to print to stderr without a newline |
| `std::io::stdin()` | Returns a handle to the standard input stream |
| `std::io::stdout()` | Returns a handle to the standard output stream |
| `std::io::stderr()` | Returns a handle to the standard error stream |
| `std::io::Read` | Trait for reading bytes |
| `std::io::Write` | Trait for writing bytes |
| `std::io::Seek` | Trait for seeking within a stream |
| `std::io::BufRead` | Trait for buffered reading |
| `std::io::BufReader<R>` | Wrapper around a reader that adds buffering |
| `std::io::BufWriter<W>` | Wrapper around a writer that adds buffering |
| `std::io::Cursor<T>` | Wrapper around a seekable type that implements `Read` and `Write` |
| `std::io::copy(&mut reader, &mut writer) -> io::Result<u64>` | Copies all bytes from `reader` to `writer` |
| `std::io::Read::read(&mut self, buf: &mut [u8]) -> Result<usize>` | Reads bytes into `buf` |
| `std::io::Read::read_to_string(&mut self, buf: &mut String) -> Result<usize>` | Reads all bytes into `buf` as a string |
| `std::io::Write::write(&mut self, buf: &[u8]) -> Result<usize>` | Writes bytes from `buf` |
| `std::io::Write::writeln!(&mut self, fmt: Arguments) -> Result<()>` | Writes formatted data with a newline |

### Filesystem

| Code | Description |
|------|-------------|
| `std::fs::File` | File handle |
| `std::fs::OpenOptions` | Options for opening a file |
| `File::open(path) -> Result<File>` | Opens a file in read-only mode |
| `File::create(path) -> Result<File>` | Creates a new file |
| `OpenOptions::new().read(true).write(true).open(path)` | Opens a file with read and write permissions |
| `std::fs::read(path) -> Result<Vec<u8>>` | Reads the entire contents of a file into a byte vector |
| `std::fs::read_to_string(path) -> Result<String>` | Reads the entire contents of a file into a string |
| `std::fs::write(path, contents) -> Result<()>` | Writes a byte slice to a file |
| `std::fs::metadata(path) -> Result<Metadata>` | Returns the metadata for a file |
| `std::fs::create_dir(path) -> Result<()>` | Creates a new directory |
| `std::fs::create_dir_all(path) -> Result<()>` | Creates a new directory and all its parent directories |
| `std::fs::remove_file(path) -> Result<()>` | Removes a file |
| `std::fs::remove_dir(path) -> Result<()>` | Removes an empty directory |
| `std::fs::remove_dir_all(path) -> Result<()>` | Removes a directory and all its contents |
| `std::fs::rename(from, to) -> Result<()>` | Renames a file or directory |
| `std::fs::copy(from, to) -> Result<u64>` | Copies the contents of one file to another |
| `std::fs::read_dir(path) -> Result<ReadDir>` | Returns an iterator over the entries in a directory |
| `Metadata::is_file() -> bool` | Returns `true` if the metadata is for a file |
| `Metadata::is_dir() -> bool` | Returns `true` if the metadata is for a directory |
| `Metadata::len() -> u64` | Returns the size of the file in bytes |
| `Metadata::modified() -> Result<SystemTime>` | Returns the time the file was last modified |

### Path Handling

| Code | Description |
|------|-------------|
| `std::path::Path` | Immutable path |
| `std::path::PathBuf` | Owned, mutable path |
| `Path::new(path: &str) -> &Path` | Creates a new `Path` from a string |
| `PathBuf::from(path: &str) -> PathBuf` | Creates a new `PathBuf` from a string |
| `Path::join(path: &str) -> PathBuf` | Joins a path component to the current path |
| `Path::parent() -> Option<&Path>` | Returns the parent directory of the path |
| `Path::file_name() -> Option<&OsStr>` | Returns the file name of the path |
| `Path::extension() -> Option<&OsStr>` | Returns the extension of the path |
| `Path::is_absolute() -> bool` | Returns `true` if the path is absolute |
| `Path::is_relative() -> bool` | Returns `true` if the path is relative |
| `Path::exists() -> bool` | Returns `true` if the path exists |
| `Path::is_file() -> bool` | Returns `true` if the path is a file |
| `Path::is_dir() -> bool` | Returns `true` if the path is a directory |
| `Path::canonicalize() -> Result<PathBuf>` | Returns the canonical form of the path |
| `Path::read_dir() -> Result<ReadDir>` | Returns an iterator over the entries in the directory |

---

## Concurrency

### Threads

| Code | Description |
|------|-------------|
| `std::thread` | Module for working with threads |
| `std::thread::spawn<F, T>(f: F) -> JoinHandle<T>` | Spawns a new thread and returns a handle to it |
| `std::thread::JoinHandle<T>` | Handle to a thread, used to join the thread and retrieve its result |
| `JoinHandle::join() -> Result<T>` | Waits for the thread to finish and returns its result |
| `std::thread::current()` | Returns a handle to the current thread |
| `std::thread::id()` | Returns the ID of the current thread |
| `std::thread::sleep(duration: Duration)` | Suspends the current thread for the specified duration |
| `std::thread::yield_now()` | Yields execution to the thread scheduler |
| `std::thread::available_parallelism() -> Result<usize>` | Returns an estimate of the number of threads the system can run concurrently |

### Channels

| Code | Description |
|------|-------------|
| `std::sync::mpsc` | Module for multi-producer, single-consumer channels |
| `std::sync::mpsc::channel<T>() -> (Sender<T>, Receiver<T>)` | Creates a new channel for sending and receiving values of type `T` |
| `std::sync::mpsc::Sender<T>` | Sending end of a channel |
| `std::sync::mpsc::Receiver<T>` | Receiving end of a channel |
| `Sender::send(value: T) -> Result<()>` | Sends a value to the channel |
| `Receiver::recv() -> Result<T>` | Receives a value from the channel |
| `Receiver::try_recv() -> Result<T>` | Attempts to receive a value from the channel without blocking |
| `std::sync::mpsc::sync_channel<T>(bound: usize) -> (SyncSender<T>, Receiver<T>)` | Creates a new synchronous channel with a bounded buffer |

### Synchronization Primitives

| Code | Description |
|------|-------------|
| `std::sync::Mutex<T>` | Mutual exclusion lock for thread-safe access to data |
| `Mutex::new(value: T) -> Mutex<T>` | Creates a new `Mutex` protecting the given value |
| `Mutex::lock() -> LockResult<MutexGuard<T>>` | Locks the `Mutex` and returns a guard |
| `std::sync::MutexGuard<T>` | RAII guard for a locked `Mutex` |
| `std::sync::RwLock<T>` | Reader-writer lock for thread-safe read and write access |
| `RwLock::new(value: T) -> RwLock<T>` | Creates a new `RwLock` protecting the given value |
| `RwLock::read() -> LockResult<RwLockReadGuard<T>>` | Locks the `RwLock` for reading |
| `RwLock::write() -> LockResult<RwLockWriteGuard<T>>` | Locks the `RwLock` for writing |
| `std::sync::Condvar` | Condition variable for thread synchronization |
| `Condvar::new() -> Condvar` | Creates a new `Condvar` |
| `Condvar::wait(guard: &mut MutexGuard<T>) -> LockResult<MutexGuard<T>>` | Waits on the condition variable |
| `Condvar::notify_one()` | Wakes up one blocked thread |
| `Condvar::notify_all()` | Wakes up all blocked threads |
| `std::sync::Barrier` | Synchronization primitive for coordinating threads |
| `Barrier::new(n: usize) -> Barrier` | Creates a new `Barrier` for `n` threads |
| `Barrier::wait() -> Result<()>` | Blocks until all threads have reached the barrier |
| `std::sync::Once` | One-time initialization primitive |
| `Once::new() -> Once` | Creates a new `Once` |
| `Once::call_once(closure: OnceLock)` | Performs one-time initialization |
| `std::sync::OnceLock<T>` | Thread-safe one-time initialization for a value |
| `OnceLock::new() -> OnceLock<T>` | Creates a new `OnceLock` |
| `OnceLock::get() -> Option<&T>` | Returns a reference to the initialized value, or `None` if not initialized |
| `OnceLock::set(value: T) -> Result<(), T>` | Initializes the `OnceLock` with the given value |

### Atomic Types

| Code | Description |
|------|-------------|
| `std::sync::atomic::AtomicBool` | Atomic boolean type |
| `std::sync::atomic::AtomicI8` | Atomic 8-bit signed integer |
| `std::sync::atomic::AtomicI16` | Atomic 16-bit signed integer |
| `std::sync::atomic::AtomicI32` | Atomic 32-bit signed integer |
| `std::sync::atomic::AtomicI64` | Atomic 64-bit signed integer |
| `std::sync::atomic::AtomicIsize` | Atomic pointer-sized signed integer |
| `std::sync::atomic::AtomicU8` | Atomic 8-bit unsigned integer |
| `std::sync::atomic::AtomicU16` | Atomic 16-bit unsigned integer |
| `std::sync::atomic::AtomicU32` | Atomic 32-bit unsigned integer |
| `std::sync::atomic::AtomicU64` | Atomic 64-bit unsigned integer |
| `std::sync::atomic::AtomicUsize` | Atomic pointer-sized unsigned integer |
| `std::sync::atomic::AtomicPtr<T>` | Atomic raw pointer type |
| `AtomicBool::new(value: bool) -> AtomicBool` | Creates a new `AtomicBool` with the given value |
| `AtomicBool::load(order: Ordering) -> bool` | Loads the current value with the specified memory ordering |
| `AtomicBool::store(value: bool, order: Ordering)` | Stores the given value with the specified memory ordering |
| `AtomicBool::compare_exchange(old: bool, new: bool, success: Ordering, failure: Ordering) -> Result<bool, bool>` | Compares and exchanges the value |
| `AtomicBool::fetch_and(value: bool, order: Ordering) -> bool` | Performs a bitwise AND operation |
| `AtomicBool::fetch_or(value: bool, order: Ordering) -> bool` | Performs a bitwise OR operation |
| `AtomicBool::fetch_xor(value: bool, order: Ordering) -> bool` | Performs a bitwise XOR operation |
| `std::sync::atomic::Ordering` | Memory ordering for atomic operations |
| `Ordering::Relaxed` | No ordering constraints |
| `Ordering::Release` | Release ordering |
| `Ordering::Acquire` | Acquire ordering |
| `Ordering::AcqRel` | Acquire-release ordering |
| `Ordering::SeqCst` | Sequentially consistent ordering |

---

## Time and Durations

| Code | Description |
|------|-------------|
| `std::time::Duration` | Span of time, typically used for timeouts and intervals |
| `Duration::new(secs: u64, nanos: u32) -> Duration` | Creates a new `Duration` with the given seconds and nanoseconds |
| `Duration::from_secs(secs: u64) -> Duration` | Creates a new `Duration` from seconds |
| `Duration::from_millis(millis: u64) -> Duration` | Creates a new `Duration` from milliseconds |
| `Duration::from_micros(micros: u64) -> Duration` | Creates a new `Duration` from microseconds |
| `Duration::from_nanos(nanos: u64) -> Duration` | Creates a new `Duration` from nanoseconds |
| `Duration::as_secs() -> u64` | Returns the number of whole seconds |
| `Duration::subsec_nanos() -> u32` | Returns the number of nanoseconds beyond the whole seconds |
| `Duration::checked_add(rhs: Duration) -> Option<Duration>` | Adds two `Duration`s, returning `None` if overflow occurs |
| `Duration::checked_sub(rhs: Duration) -> Option<Duration>` | Subtracts two `Duration`s, returning `None` if underflow occurs |
| `std::time::Instant` | Measurement of a monotonically non-decreasing clock |
| `Instant::now() -> Instant` | Returns an `Instant` representing the current time |
| `Instant::elapsed() -> Duration` | Returns the duration since the `Instant` was created |
| `Instant::duration_since(earlier: Instant) -> Duration` | Returns the duration between two `Instant`s |
| `Instant::checked_duration_since(earlier: Instant) -> Option<Duration>` | Returns the duration between two `Instant`s, or `None` if `earlier` is later |
| `std::time::SystemTime` | Measurement of the system clock |
| `SystemTime::now() -> SystemTime` | Returns a `SystemTime` representing the current time |
| `SystemTime::duration_since(earlier: SystemTime) -> Result<Duration>` | Returns the duration between two `SystemTime`s |
| `SystemTime::elapsed() -> Result<Duration>` | Returns the duration since the `SystemTime` was created |
| `SystemTime::from_unix_timestamp(secs: i64) -> Result<SystemTime>` | Creates a `SystemTime` from a Unix timestamp |
| `SystemTime::into_unix_timestamp() -> Result<i64>` | Converts the `SystemTime` to a Unix timestamp |

---

## Memory Management

### Allocation

| Code | Description |
|------|-------------|
| `Box::new(value: T) -> Box<T>` | Allocates a value on the heap and returns a `Box` pointing to it |
| `Box::into_raw(b: Box<T>) -> *mut T` | Consumes the `Box` and returns a raw pointer to the allocated value |
| `Box::from_raw(ptr: *mut T) -> Box<T>` | Converts a raw pointer into a `Box` |
| `std::alloc::alloc(layout: Layout) -> *mut u8` | Allocates memory with the given layout |
| `std::alloc::dealloc(ptr: *mut u8, layout: Layout)` | Deallocates memory allocated with `alloc` |
| `std::alloc::realloc(ptr: *mut u8, layout: Layout, new_size: usize) -> *mut u8` | Reallocates memory to a new size |
| `std::alloc::Layout` | Description of a memory layout |
| `Layout::from_size_align(size: usize, align: usize) -> Result<Layout>` | Creates a new `Layout` with the given size and alignment |
| `Layout::size() -> usize` | Returns the size of the layout |
| `Layout::align() -> usize` | Returns the alignment of the layout |

### Pointers

| Code | Description |
|------|-------------|
| `*const T` | Immutable raw pointer |
| `*mut T` | Mutable raw pointer |
| `std::ptr::null<T>() -> *const T` | Returns a null pointer |
| `std::ptr::null_mut<T>() -> *mut T` | Returns a nullable mutable pointer |
| `std::ptr::read(ptr: *const T) -> T` | Reads the value at `ptr` and returns it |
| `std::ptr::write(ptr: *mut T, value: T)` | Writes `value` to `ptr` |
| `std::ptr::replace(ptr: *mut T, src: T) -> T` | Replaces the value at `ptr` with `src` and returns the old value |
| `std::ptr::swap(ptr1: *mut T, ptr2: *mut T)` | Swaps the values at `ptr1` and `ptr2` |
| `std::ptr::drop_in_place(ptr: *mut T)` | Drops the value at `ptr` without deallocating the memory |
| `std::ptr::NonNull<T>` | Non-null pointer wrapper |
| `NonNull::new(ptr: *mut T) -> Option<NonNull<T>>` | Creates a new `NonNull` if `ptr` is not null |
| `NonNull::as_ptr() -> *mut T` | Returns the underlying pointer |

---

## Iterators and Collections

### Iterator Traits

| Code | Description |
|------|-------------|
| `std::iter::Iterator` | Trait for iterating over a sequence of values |
| `Iterator::next(&mut self) -> Option<Self::Item>` | Advances the iterator and returns the next value |
| `Iterator::size_hint(&self) -> (usize, Option<usize>)` | Returns the bounds on the remaining length of the iterator |
| `Iterator::count(self) -> usize` | Consumes the iterator and counts the number of elements |
| `Iterator::last(self) -> Option<Self::Item>` | Consumes the iterator and returns the last element |
| `Iterator::nth(&mut self, n: usize) -> Option<Self::Item>` | Advances the iterator by `n` elements and returns the next value |
| `Iterator::step_by(self, step: usize) -> StepBy<Self>` | Creates an iterator that steps by `step` elements at a time |
| `Iterator::chain<U>(self, other: U) -> Chain<Self, U::IntoIter>` | Creates an iterator that chains two iterators together |
| `Iterator::zip<U>(self, other: U) -> Zip<Self, U::IntoIter>` | Creates an iterator that zips two iterators together |
| `Iterator::map<B, F>(self, f: F) -> Map<Self, F>` | Creates an iterator that applies a function to each element |
| `Iterator::filter<P>(self, predicate: P) -> Filter<Self, P>` | Creates an iterator that filters elements based on a predicate |
| `Iterator::filter_map<B, F>(self, f: F) -> FilterMap<Self, F>` | Creates an iterator that filters and maps elements |
| `Iterator::flat_map<U, F>(self, f: F) -> FlatMap<Self, U::IntoIter, F>` | Creates an iterator that flattens nested iterators |
| `Iterator::flatten(self) -> Flatten<Self>` | Creates an iterator that flattens nested iterators |
| `Iterator::take(self, n: usize) -> Take<Self>` | Creates an iterator that takes the first `n` elements |
| `Iterator::skip(self, n: usize) -> Skip<Self>` | Creates an iterator that skips the first `n` elements |
| `Iterator::peekable(self) -> Peekable<Self>` | Creates an iterator that allows peeking at the next element |
| `Iterator::fuse(self) -> Fuse<Self>` | Creates an iterator that stops after the first `None` |
| `Iterator::collect<B>(self) -> B` | Transforms the iterator into a collection |
| `Iterator::partition<B, F>(self, f: F) -> (B, B)` | Partitions the iterator into two collections based on a predicate |
| `Iterator::fold<Acc, F>(self, init: Acc, f: F) -> Acc` | Folds the iterator into a single value |
| `Iterator::all<F>(self, f: F) -> bool` | Returns `true` if all elements satisfy the predicate |
| `Iterator::any<F>(self, f: F) -> bool` | Returns `true` if any element satisfies the predicate |
| `Iterator::find<P>(self, predicate: P) -> Option<Self::Item>` | Returns the first element that satisfies the predicate |
| `Iterator::position<P>(self, predicate: P) -> Option<usize>` | Returns the index of the first element that satisfies the predicate |
| `Iterator::rposition<P>(self, predicate: P) -> Option<usize>` | Returns the index of the last element that satisfies the predicate |
| `Iterator::max(self) -> Option<Self::Item>` | Returns the maximum element |
| `Iterator::min(self) -> Option<Self::Item>` | Returns the minimum element |

### Range Iterators

| Code | Description |
|------|-------------|
| `0..10` | Range from 0 (inclusive) to 10 (exclusive) |
| `0..=10` | Range from 0 (inclusive) to 10 (inclusive) |
| `(0..10).rev()` | Reversed range from 10 (exclusive) to 0 (inclusive) |
| `(0..10).step_by(2)` | Range stepping by 2 |
| `(0..10).map(\|x\| x * 2)` | Range with each element multiplied by 2 |
| `(0..10).filter(\|x\| x % 2 == 0)` | Range filtered to even numbers |
| `(0..10).take(5)` | Takes the first 5 elements of the range |
| `(0..10).skip(5)` | Skips the first 5 elements of the range |

---

## Functional Programming

### Higher-Order Functions

| Code | Description |
|------|-------------|
| `std::iter::from_fn<F>(f: F) -> FromFn<F>` | Creates an iterator from a function that returns `Option<T>` |
| `std::iter::successors(initial: Option<T>, f: F) -> Successors<F>` | Creates an iterator from an initial value and a successor function |
| `std::iter::repeat(value: T) -> Repeat<T>` | Creates an iterator that repeats a value infinitely |
| `std::iter::repeat_n(value: T, n: usize) -> std::iter::Take<std::iter::Repeat<T>>` | Creates an iterator that repeats a value `n` times |
| `std::iter::empty<T>() -> Empty<T>` | Creates an empty iterator |
| `std::iter::once<T>(value: T) -> Once<T>` | Creates an iterator that yields a single value |
| `std::iter::from_iter<T>(iter: T) -> T` | Converts an iterable into an iterator |

### Closures

| Code | Description |
|------|-------------|
| `\|x\| x + 1` | Closure that takes `x` and returns `x + 1` |
| `\|x, y\| x + y` | Closure that takes `x` and `y` and returns their sum |
| `\|x\| { let y = x * 2; y + 1 }` | Closure with a block body |
| `\|x\| x` | Closure that returns its input (identity function) |
| `move \|x\| x + 1` | Closure that takes ownership of captured variables |
| `Fn` | Trait for closures that can be called with immutable references |
| `FnMut` | Trait for closures that can be called with mutable references |
| `FnOnce` | Trait for closures that can be called once |

---

## Macros

### Built-in Macros

| Code | Description |
|------|-------------|
| `panic!()` | Panics the current thread with a message |
| `panic!("{}", message)` | Panics with a formatted message |
| `assert!(expr)` | Asserts that `expr` is `true`, panics if `false` |
| `assert!(expr, "{}", message)` | Asserts with a custom message |
| `assert_eq!(left, right)` | Asserts that `left` and `right` are equal |
| `assert_eq!(left, right, "{}", message)` | Asserts equality with a custom message |
| `assert_ne!(left, right)` | Asserts that `left` and `right` are not equal |
| `debug_assert!()` | Assertion that is only enabled in debug builds |
| `debug_assert_eq!()` | Equality assertion that is only enabled in debug builds |
| `unreachable!()` | Indicates unreachable code, panics if reached |
| `unimplemented!()` | Indicates unimplemented code, panics if reached |
| `todo!()` | Indicates code that needs to be implemented, panics if reached |
| `println!()` | Prints to stdout with a newline |
| `print!()` | Prints to stdout without a newline |
| `eprintln!()` | Prints to stderr with a newline |
| `eprint!()` | Prints to stderr without a newline |
| `format!()` | Formats a string without printing it |
| `format_args!()` | Creates a formatted string without evaluating it |
| `write!()` | Writes formatted data to a writer |
| `writeln!()` | Writes formatted data to a writer with a newline |
| `vec![]` | Creates a new `Vec` with the given elements |
| `vec![value; n]` | Creates a new `Vec` with `n` copies of `value` |
| `include_str!()` | Includes a UTF-8 string from a file at compile time |
| `include_bytes!()` | Includes a byte array from a file at compile time |
| `include!()` | Includes and evaluates a Rust file at compile time |
| `env!()` | Includes an environment variable at compile time |
| `option_env!()` | Includes an optional environment variable at compile time |
| `cfg!()` | Evaluates a configuration predicate at compile time |
| `file!()` | Expands to the current filename |
| `line!()` | Expands to the current line number |
| `column!()` | Expands to the current column number |
| `module_path!()` | Expands to the current module path |
| `function!()` | Expands to the current function name |
| `stringify!()` | Converts a macro argument to a string literal |

---

## Networking

| Code | Description |
|------|-------------|
| `std::net::TcpListener` | TCP listener for incoming connections |
| `TcpListener::bind(addr: &SocketAddr) -> Result<TcpListener>` | Binds a `TcpListener` to the given address |
| `TcpListener::accept() -> Result<(TcpStream, SocketAddr)>` | Accepts a new incoming connection |
| `TcpListener::incoming() -> Incoming` | Returns an iterator over incoming connections |
| `std::net::TcpStream` | TCP stream for reading and writing |
| `TcpStream::connect(addr: &SocketAddr) -> Result<TcpStream>` | Connects to the given address |
| `TcpStream::peer_addr() -> Result<SocketAddr>` | Returns the address of the remote peer |
| `TcpStream::local_addr() -> Result<SocketAddr>` | Returns the local address of the stream |
| `TcpStream::shutdown(how: Shutdown) -> Result<()>` | Shuts down the stream |
| `std::net::UdpSocket` | UDP socket for reading and writing |
| `UdpSocket::bind(addr: &SocketAddr) -> Result<UdpSocket>` | Binds a `UdpSocket` to the given address |
| `UdpSocket::connect(addr: &SocketAddr) -> Result<()>` | Connects the socket to the given address |
| `UdpSocket::send(buf: &[u8]) -> Result<usize>` | Sends data to the connected address |
| `UdpSocket::recv(buf: &mut [u8]) -> Result<usize>` | Receives data from the socket |
| `UdpSocket::send_to(buf: &[u8], addr: &SocketAddr) -> Result<usize>` | Sends data to the specified address |
| `UdpSocket::recv_from(buf: &mut [u8]) -> Result<(usize, SocketAddr)>` | Receives data and the address of the sender |
| `std::net::SocketAddr` | Socket address, either IPv4 or IPv6 |
| `SocketAddr::new(ip: IpAddr, port: u16) -> SocketAddr` | Creates a new `SocketAddr` |
| `std::net::IpAddr` | IP address, either IPv4 or IPv6 |
| `std::net::Ipv4Addr` | IPv4 address |
| `Ipv4Addr::new(a: u8, b: u8, c: u8, d: u8) -> Ipv4Addr` | Creates a new IPv4 address |
| `std::net::Ipv6Addr` | IPv6 address |
| `Ipv6Addr::new(a: u16, b: u16, c: u16, d: u16, e: u16, f: u16, g: u16, h: u16) -> Ipv6Addr` | Creates a new IPv6 address |

---
## Random Number Generation

| Code | Description |
|------|-------------|
| `std::rand` | Module for random number generation (note: in Rust 2021, this is typically provided by the `rand` crate) |
| `rand::random::<T>() -> T` | Generates a random value of type `T` |
| `rand::thread_rng()` | Returns a thread-local random number generator |
| `rand::Rng` | Trait for random number generators |
| `Rng::gen<T: Rand>(&mut self) -> T` | Generates a random value of type `T` |
| `Rng::gen_range<T: PartialOrd + Rand>(&mut self, range: RangeInclusive<T>) -> T` | Generates a random value in the given range |
| `rand::distributions::Uniform` | Uniform distribution |
| `rand::distributions::Normal` | Normal distribution |
| `rand::distributions::Alphanumeric` | Distribution for alphanumeric characters |
| `rand::distributions::Sample` | Trait for sampling from a distribution |

---
## Environment and Process

| Code | Description |
|------|-------------|
| `std::env` | Module for accessing environment variables and command-line arguments |
| `std::env::args() -> Args` | Returns an iterator over the command-line arguments |
| `std::env::args_os() -> ArgsOs` | Returns an iterator over the command-line arguments as `OsString` |
| `std::env::var(key: &str) -> Result<String>` | Returns the value of the environment variable `key` |
| `std::env::var_os(key: &str) -> Option<OsString>` | Returns the value of the environment variable `key` as an `OsString` |
| `std::env::set_var(key: &str, value: &str)` | Sets the environment variable `key` to `value` |
| `std::env::remove_var(key: &str)` | Removes the environment variable `key` |
| `std::env::current_dir() -> Result<PathBuf>` | Returns the current working directory |
| `std::env::set_current_dir(path: &Path) -> Result<()>` | Sets the current working directory |
| `std::env::consts::ARCH` | Target CPU architecture |
| `std::env::consts::OS` | Target operating system |
| `std::env::consts::FAMILY` | Target operating system family |
| `std::process` | Module for working with processes |
| `std::process::Command` | Builder for process configuration |
| `Command::new(program: &str) -> Command` | Creates a new `Command` for the given program |
| `Command::arg(arg: &str) -> &mut Command` | Adds an argument to the command |
| `Command::args(args: &[&str]) -> &mut Command` | Adds multiple arguments to the command |
| `Command::env(key: &str, value: &str) -> &mut Command` | Sets an environment variable for the command |
| `Command::env_remove(key: &str) -> &mut Command` | Removes an environment variable from the command |
| `Command::current_dir(dir: &Path) -> &mut Command` | Sets the current directory for the command |
| `Command::stdin(stdin: Stdio) -> &mut Command` | Sets the stdin configuration for the command |
| `Command::stdout(stdout: Stdio) -> &mut Command` | Sets the stdout configuration for the command |
| `Command::stderr(stderr: Stdio) -> &mut Command` | Sets the stderr configuration for the command |
| `Command::spawn() -> Result<Child>` | Spawns the command as a child process |
| `Command::output() -> Result<Output>` | Runs the command and returns its output |
| `Command::status() -> Result<ExitStatus>` | Runs the command and returns its exit status |
| `std::process::Child` | Child process handle |
| `Child::wait() -> Result<ExitStatus>` | Waits for the child process to exit |
| `Child::kill() -> Result<()>` | Kills the child process |
| `std::process::ExitStatus` | Exit status of a process |
| `ExitStatus::success() -> bool` | Returns `true` if the process exited successfully |
| `ExitStatus::code() -> Option<i32>` | Returns the exit code of the process |
| `std::process::Stdio` | Configuration for stdin, stdout, and stderr |
| `Stdio::inherit()` | Inherits the parent's stdin/stdout/stderr |
| `Stdio::piped()` | Creates a pipe for stdin/stdout/stderr |
| `Stdio::null()` | Redirects stdin/stdout/stderr to a null device |
| `std::process::Output` | Output of a process |
| `Output::status() -> ExitStatus` | Returns the exit status of the process |
| `Output::stdout() -> Vec<u8>` | Returns the stdout of the process |
| `Output::stderr() -> Vec<u8>` | Returns the stderr of the process |

---
## File I/O and Directories

| Code | Description |
|------|-------------|
| `std::fs::File` | File handle |
| `File::open(path: &Path) -> Result<File>` | Opens a file in read-only mode |
| `File::create(path: &Path) -> Result<File>` | Creates a new file |
| `OpenOptions::new().read(true).open(path: &Path) -> Result<File>` | Opens a file with read permissions |
| `OpenOptions::new().write(true).open(path: &Path) -> Result<File>` | Opens a file with write permissions |
| `OpenOptions::new().append(true).open(path: &Path) -> Result<File>` | Opens a file with append permissions |
| `OpenOptions::new().truncate(true).open(path: &Path) -> Result<File>` | Opens a file with truncate permissions |
| `std::fs::read(path: &Path) -> Result<Vec<u8>>` | Reads the entire contents of a file into a byte vector |
| `std::fs::read_to_string(path: &Path) -> Result<String>` | Reads the entire contents of a file into a string |
| `std::fs::write(path: &Path, contents: &[u8]) -> Result<()>` | Writes a byte slice to a file |
| `std::fs::append(path: &Path, contents: &[u8]) -> Result<()>` | Appends a byte slice to a file |
| `std::fs::metadata(path: &Path) -> Result<Metadata>` | Returns the metadata for a file |
| `std::fs::symlink_metadata(path: &Path) -> Result<Metadata>` | Returns the metadata for a file without following symlinks |
| `std::fs::create_dir(path: &Path) -> Result<()>` | Creates a new directory |
| `std::fs::create_dir_all(path: &Path) -> Result<()>` | Creates a new directory and all its parent directories |
| `std::fs::remove_file(path: &Path) -> Result<()>` | Removes a file |
| `std::fs::remove_dir(path: &Path) -> Result<()>` | Removes an empty directory |
| `std::fs::remove_dir_all(path: &Path) -> Result<()>` | Removes a directory and all its contents |
| `std::fs::rename(from: &Path, to: &Path) -> Result<()>` | Renames a file or directory |
| `std::fs::copy(from: &Path, to: &Path) -> Result<u64>` | Copies the contents of one file to another |
| `std::fs::hard_link(from: &Path, to: &Path) -> Result<()>` | Creates a hard link from `from` to `to` |
| `std::fs::soft_link(from: &Path, to: &Path) -> Result<()>` | Creates a symbolic link from `from` to `to` |
| `std::fs::read_dir(path: &Path) -> Result<ReadDir>` | Returns an iterator over the entries in a directory |
| `std::fs::read_link(path: &Path) -> Result<PathBuf>` | Reads the target of a symbolic link |
| `std::fs::canonicalize(path: &Path) -> Result<PathBuf>` | Returns the canonical form of the path |
| `std::fs::Metadata` | Metadata for a file |
| `Metadata::file_type() -> FileType` | Returns the file type |
| `Metadata::is_file() -> bool` | Returns `true` if the metadata is for a file |
| `Metadata::is_dir() -> bool` | Returns `true` if the metadata is for a directory |
| `Metadata::is_symlink() -> bool` | Returns `true` if the metadata is for a symbolic link |
| `Metadata::len() -> u64` | Returns the size of the file in bytes |
| `Metadata::permissions() -> Permissions` | Returns the permissions of the file |
| `Metadata::modified() -> Result<SystemTime>` | Returns the time the file was last modified |
| `Metadata::accessed() -> Result<SystemTime>` | Returns the time the file was last accessed |
| `Metadata::created() -> Result<SystemTime>` | Returns the time the file was created |
| `std::fs::FileType` | File type |
| `FileType::is_file() -> bool` | Returns `true` if the file type is a file |
| `FileType::is_dir() -> bool` | Returns `true` if the file type is a directory |
| `FileType::is_symlink() -> bool` | Returns `true` if the file type is a symbolic link |
| `std::fs::Permissions` | Permissions for a file |
| `Permissions::readonly() -> bool` | Returns `true` if the file is read-only |
| `Permissions::set_readonly(readonly: bool)` | Sets the read-only permission for the file |

---
## Serialization and Deserialization

| Code | Description |
|------|-------------|
| `serde` | External crate for serialization and deserialization (note: not part of the standard library but widely used) |
| `serde::Serialize` | Trait for serializing a value |
| `serde::Deserialize` | Trait for deserializing a value |
| `serde_json::to_string<T: Serialize>(value: &T) -> Result<String>` | Serializes a value to a JSON string |
| `serde_json::from_str<T: for<'a> Deserialize<'a>>(s: &str) -> Result<T>` | Deserializes a JSON string to a value |
| `serde_json::to_writer<W: Write, T: Serialize>(writer: W, value: &T) -> Result<()>` | Serializes a value to a writer as JSON |
| `serde_json::from_reader<R: Read, T: for<'a> Deserialize<'a>>(reader: R) -> Result<T>` | Deserializes JSON from a reader to a value |
| `serde_json::Value` | Enum representing a JSON value |
| `serde_json::json!` | Macro for creating `serde_json::Value` literals |

---
## Testing

| Code | Description |
|------|-------------|
| `#[test]` | Attribute to mark a function as a test |
| `#[cfg(test)]` | Attribute to include code only when running tests |
| `assert!(expr)` | Asserts that `expr` is `true` |
| `assert!(expr, "{}", message)` | Asserts with a custom message |
| `assert_eq!(left, right)` | Asserts that `left` and `right` are equal |
| `assert_eq!(left, right, "{}", message)` | Asserts equality with a custom message |
| `assert_ne!(left, right)` | Asserts that `left` and `right` are not equal |
| `panic!()` | Panics the current test |
| `std::panicking::catch_unwind<F, R>(f: F) -> Result<R>` | Catches unwinding panics and returns a `Result` |

---
## Unsafe Rust

| Code | Description |
|------|-------------|
| `unsafe` | Keyword to denote unsafe blocks, functions, or implementations |
| `unsafe fn` | Function that requires unsafe code to call |
| `unsafe impl` | Implementation that requires unsafe code |
| `unsafe { ... }` | Block of code that requires unsafe operations |
| `*ptr` | Dereferences a raw pointer |
| `&raw const T` | Immutable raw reference |
| `&raw mut T` | Mutable raw reference |
| `std::mem::transmute<T, U>(value: T) -> U` | Reinterprets the bits of `value` as type `U` |
| `std::mem::transmute_copy<T, U>(src: &T) -> U` | Copies the bits of `src` and reinterprets them as type `U` |
| `std::mem::forget<T>(value: T)` | Leaks a value without calling its destructor |
| `std::mem::ManuallyDrop<T>` | Wrapper to manually drop a value |
| `ManuallyDrop::new(value: T) -> ManuallyDrop<T>` | Creates a new `ManuallyDrop` |
| `ManuallyDrop::into_inner(self) -> ManuallyDrop<T>` | Consumes the `ManuallyDrop` and returns the inner value without dropping it |
| `ManuallyDrop::drop(&mut self)` | Drops the inner value manually |
| `std::ptr::read_unaligned(ptr: *const T) -> T` | Reads the value at `ptr` without alignment checks |
| `std::ptr::write_unaligned(ptr: *mut T, value: T)` | Writes `value` to `ptr` without alignment checks |
| `std::ptr::read_volatile(ptr: *const T) -> T` | Reads the value at `ptr` with volatile semantics |
| `std::ptr::write_volatile(ptr: *mut T, value: T)` | Writes `value` to `ptr` with volatile semantics |

---
## Traits

### Common Traits

| Code | Description |
|------|-------------|
| `std::default::Default` | Trait for types with a default value |
| `Default::default() -> Self` | Returns the default value for the type |
| `std::clone::Clone` | Trait for types that can be cloned |
| `Clone::clone(&self) -> Self` | Returns a clone of the value |
| `std::copy::Copy` | Trait for types that can be copied by bitwise copy |
| `std::fmt::Debug` | Trait for types that can be formatted for debugging |
| `Debug::fmt(&self, f: &mut Formatter<'_>) -> Result<(), std::fmt::Error>` | Formats the value for debugging |
| `std::fmt::Display` | Trait for types that can be formatted for display |
| `Display::fmt(&self, f: &mut Formatter<'_>) -> Result<(), std::fmt::Error>` | Formats the value for display |
| `std::fmt::Write` | Trait for types that can be written to |
| `Write::write_str(&mut self, s: &str) -> Result<(), std::fmt::Error>` | Writes a string to the type |
| `std::fmt::Formatter` | Type for formatting values |
| `std::eq::PartialEq` | Trait for types that can be compared for partial equality |
| `PartialEq::eq(&self, other: &Self) -> bool` | Returns `true` if `self` and `other` are equal |
| `std::eq::Eq` | Trait for types that can be compared for equality |
| `std::partial_ord::PartialOrd` | Trait for types that can be compared for partial ordering |
| `PartialOrd::partial_cmp(&self, other: &Self) -> Option<Ordering>` | Returns the ordering between `self` and `other` |
| `std::cmp::Ord` | Trait for types that can be compared for total ordering |
| `Ord::cmp(&self, other: &Self) -> Ordering` | Returns the ordering between `self` and `other` |
| `std::cmp::Ordering` | Enum representing the result of a comparison |
| `Ordering::Less` | `self` is less than `other` |
| `Ordering::Equal` | `self` is equal to `other` |
| `Ordering::Greater` | `self` is greater than `other` |
| `std::hash::Hash` | Trait for types that can be hashed |
| `Hash::hash<H: Hasher>(&self, state: &mut H)` | Hashes the value into the hasher |
| `std::hash::Hasher` | Trait for hashers |
| `std::hash::BuildHasher` | Trait for building hashers |
| `std::marker::Sized` | Trait for types with a known size at compile time |
| `std::marker::Send` | Trait for types that can be safely sent between threads |
| `std::marker::Sync` | Trait for types that can be safely shared between threads |
| `std::marker::Unpin` | Trait for types that do not require pinning |
| `std::marker::PhantomData<T>` | Zero-sized type used to mark a type as owning or borrowing data of type `T` |
| `std::marker::PhantomPinned` | Zero-sized type used to mark a type as pinned |

### Conversion Traits

| Code | Description |
|------|-------------|
| `std::convert::AsRef<T>` | Trait for cheap reference-to-reference conversions |
| `AsRef::as_ref(&self) -> &T` | Converts `self` to a reference to `T` |
| `std::convert::AsMut<T>` | Trait for cheap mutable reference-to-mutable reference conversions |
| `AsMut::as_mut(&mut self) -> &mut T` | Converts `self` to a mutable reference to `T` |
| `std::convert::Into<T>` | Trait for value-to-value conversions |
| `Into::into(self) -> T` | Converts `self` into `T` |
| `std::convert::From<T>` | Trait for value-to-value conversions (reverse of `Into`) |
| `From::from(value: T) -> Self` | Converts `value` into `Self` |
| `std::convert::TryInto<T>` | Trait for fallible value-to-value conversions |
| `TryInto::try_into(self) -> Result<T, Self::Error>` | Attempts to convert `self` into `T` |
| `std::convert::TryFrom<T>` | Trait for fallible value-to-value conversions (reverse of `TryInto`) |
| `TryFrom::try_from(value: T) -> Result<Self, Self::Error>` | Attempts to convert `value` into `Self` |
| `std::convert::FromIterator<T>` | Trait for creating a collection from an iterator |
| `FromIterator::from_iter<T: IntoIterator<Item = Self::Item>>(iter: T) -> Self` | Creates a collection from an iterator |

---
## Standard Library Modules

| Code | Description |
|------|-------------|
| `std::any` | Module for type reflection |
| `std::array` | Module for array types |
| `std::ascii` | Module for ASCII character handling |
| `std::borrow` | Module for borrowing traits |
| `std::boxed` | Module for heap allocation |
| `std::cell` | Module for interior mutability |
| `std::char` | Module for Unicode character handling |
| `std::clone` | Module for cloning traits |
| `std::cmp` | Module for comparison traits |
| `std::collections` | Module for collection types |
| `std::convert` | Module for conversion traits |
| `std::default` | Module for default values |
| `std::error` | Module for error handling |
| `std::f32` | Module for 32-bit floating point constants and functions |
| `std::f64` | Module for 64-bit floating point constants and functions |
| `std::fmt` | Module for formatting traits and types |
| `std::fs` | Module for filesystem operations |
| `std::hash` | Module for hashing traits |
| `std::i8` | Module for 8-bit signed integer constants and functions |
| `std::i16` | Module for 16-bit signed integer constants and functions |
| `std::i32` | Module for 32-bit signed integer constants and functions |
| `std::i64` | Module for 64-bit signed integer constants and functions |
| `std::i128` | Module for 128-bit signed integer constants and functions |
| `std::isize` | Module for pointer-sized signed integer constants and functions |
| `std::iter` | Module for iterator traits and types |
| `std::marker` | Module for marker traits |
| `std::mem` | Module for memory manipulation |
| `std::net` | Module for networking |
| `std::ops` | Module for operator overloading traits |
| `std::option` | Module for the `Option` type |
| `std::os` | Module for OS-specific functionality |
| `std::path` | Module for path manipulation |
| `std::prelude` | Module for the standard prelude |
| `std::process` | Module for process management |
| `std::ptr` | Module for raw pointer operations |
| `std::rc` | Module for reference counting |
| `std::result` | Module for the `Result` type |
| `std::slice` | Module for slice operations |
| `std::str` | Module for string slices |
| `std::string` | Module for the `String` type |
| `std::sync` | Module for synchronization primitives |
| `std::task` | Module for task management |
| `std::thread` | Module for thread management |
| `std::time` | Module for time handling |
| `std::u8` | Module for 8-bit unsigned integer constants and functions |
| `std::u16` | Module for 16-bit unsigned integer constants and functions |
| `std::u32` | Module for 32-bit unsigned integer constants and functions |
| `std::u64` | Module for 64-bit unsigned integer constants and functions |
| `std::u128` | Module for 128-bit unsigned integer constants and functions |
| `std::usize` | Module for pointer-sized unsigned integer constants and functions |