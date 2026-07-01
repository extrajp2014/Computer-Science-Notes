Core Scala types always available without explicit imports.

| Code | Description |
|------|-------------|
| `Any` | Root of the Scala class hierarchy |
| `AnyVal` | Root class of all value types |
| `AnyRef` | Root class of all reference types |
| `App` | Trait to turn objects into executable programs |
| `Array[T]` | Mutable, indexed collections of values |
| `Boolean` | Boolean primitive type |
| `Byte` | 8-bit signed integer |
| `Char` | 16-bit unsigned integer |
| `Double` | 64-bit IEEE-754 floating point |
| `Float` | 32-bit IEEE-754 floating point |
| `Int` | 32-bit signed integer |
| `Long` | 64-bit signed integer |
| `Short` | 16-bit signed integer |
| `Unit` | Type of no-value results |
| `Null` | Type of null references |
| `Nothing` | Bottom type, subtype of every type |
| `Option[A]` | Container for optional values (Some/None) |
| `Some[A]` | Represents existing values in Option |
| `None` | Represents non-existing values in Option |
| `Either[A,B]` | Represents a value of one of two possible types |
| `TupleN` | Tuples of arity 1-22 |
| `FunctionN` | Function types of arity 0-22 |
| `String` | Type alias for java.lang.String |
| `Symbol` | Interned string for identifiers |
| `Predef` | Object containing standard definitions |
| `Console` | Object for console I/O operations |
| `BigInt` | Arbitrary-precision integers |
| `BigDecimal` | Arbitrary-precision decimals |
| `Enumeration` | Defines finite sets of values |
| `Proxy` | Trait for proxy objects |
| `DelayedInit` | Trait for delayed initialization |
| `Dynamic` | Marker trait for dynamic invocations |
| `Equals` | Interface for equality operations |
| `Product` | Interface for product types |
| `SerialVersionUID` | Annotation for serial version UID |

---

## scala.collection

Scala's collections framework.

### scala.collection.immutable

| Code | Description |
|------|-------------|
| `List[A]` | Immutable linked list |
| `Nil` | Empty List |
| `::[A]` | Cons cell for List construction |
| `Vector[A]` | Immutable indexed sequence |
| `Range` | Immutable sequence of integers |
| `Seq[A]` | Base trait for sequences |
| `IndexedSeq[A]` | Base trait for indexed sequences |
| `LinearSeq[A]` | Base trait for linear sequences |
| `Set[A]` | Base trait for immutable sets |
| `HashSet[A]` | Immutable hash set |
| `TreeSet[A]` | Immutable sorted set |
| `Map[K,V]` | Base trait for immutable maps |
| `HashMap[K,V]` | Immutable hash map |
| `TreeMap[K,V]` | Immutable sorted map |
| `Stack[A]` | Immutable stack |
| `Queue[A]` | Immutable queue |
| `Stream[A]` | Lazy list |

### scala.collection.mutable

| Code | Description |
|------|-------------|
| `ArrayBuffer[A]` | Mutable indexed sequence backed by array |
| `ListBuffer[A]` | Mutable list |
| `StringBuilder` | Mutable string builder |
| `ArraySeq[A]` | Mutable sequence wrapper for arrays |
| `MutableList[A]` | Mutable linked list |
| `HashSet[A]` | Mutable hash set |
| `HashMap[K,V]` | Mutable hash map |
| `WeakHashMap[K,V]` | Mutable hash map with weak keys |
| `LinkedHashMap[K,V]` | Mutable hash map preserving insertion order |
| `LinkedHashSet[A]` | Mutable hash set preserving insertion order |
| `Queue[A]` | Mutable queue |
| `ArrayStack[A]` | Mutable stack backed by array |
| `Stack[A]` | Mutable stack |
| `Buffer[A]` | Base trait for mutable sequences |
| `IndexedBuffer[A]` | Base trait for mutable indexed sequences |
| `Set[A]` | Base trait for mutable sets |
| `Map[K,V]` | Base trait for mutable maps |
| `Iterable[A]` | Base trait for mutable iterables |

### scala.collection.concurrent

| Code | Description |
|------|-------------|
| `TrieMap[K,V]` | Concurrent hash map based on concurrent tries |
| `Map[A,B]` | Base trait for concurrent maps |

---
---
## scala.concurrent

Primitives for concurrent and parallel programming.

| Code | Description |
|------|-------------|
| `Future[T]` | Represents a value which may be available at some point |
| `Promise[T]` | Writable, async computation |
| `Await` | Companion object for blocking operations |
| `ExecutionContext` | Executes tasks asynchronously |
| `duration.Duration` | Duration representation |
| `duration.FiniteDuration` | Finite duration |
| `duration.DurationInt` | Duration DSL |
| `duration.DurationLong` | Duration DSL |
| `duration.DurationDouble` | Duration DSL |
| `Blocking` | Context for blocking operations |
| `CanAwait` | Typeclass for await operations |
| `Channel[T]` | Communication channel |
| `ForkJoinPool` | Fork-join thread pool |
| `ForkJoinTask` | Fork-join task |
| `ForkJoinWorkerThread` | Fork-join worker thread |
| `JavaConversions` | Conversions between Scala and Java concurrency types |
| `SyncVar[T]` | Synchronized variable |
| `SyncChannel[T]` | Synchronized channel |

---
---
## scala.io

Input and output operations.

| Code | Description |
|------|-------------|
| `Source` | Represents a source of characters |
| `BufferedSource` | Buffered character source |
| `LineNumberReader` | Reader with line numbers |
| `StreamTokenizer` | Tokenizer for input streams |
| `AnsiColor` | ANSI color codes |
| `Codec` | Character encoding codec |
| `File` | Rich wrapper for java.io.File |
| `Path` | Rich wrapper for java.nio.file.Path |
| `Process` | External process execution |
| `StdIn` | Standard input |
| `StdOut` | Standard output |
| `StdErr` | Standard error |
| `Using` | Resource management utility |

---
---
## scala.math

Mathematical functions and numeric types.

| Code | Description |
|------|-------------|
| `BigDecimal` | Arbitrary-precision decimal |
| `BigInt` | Arbitrary-precision integer |
| `Equiv[T]` | Typeclass for equivalence |
| `Fractional[T]` | Typeclass for fractional numeric types |
| `Integral[T]` | Typeclass for integral numeric types |
| `Numeric[T]` | Typeclass for numeric types |
| `Ordered[T]` | Typeclass for ordered types |
| `Ordering[T]` | Typeclass for total orderings |
| `PartiallyOrdered[T]` | Typeclass for partial orderings |
| `Random` | Random number generation |
| `ScalaNumericAnyConversions` | Numeric conversions |
| `ScalaNumericConversions` | Numeric conversions |
| `Specializable` | Marker for specializable groups |
| `SpecializableGroup` | Specializable group operations |

### Math Functions

| Code | Description |
|------|-------------|
| `abs` | Absolute value |
| `acos` | Arc cosine |
| `asin` | Arc sine |
| `atan` | Arc tangent |
| `atan2` | Arc tangent of quotient |
| `cbrt` | Cube root |
| `ceil` | Ceiling |
| `cos` | Cosine |
| `cosh` | Hyperbolic cosine |
| `exp` | Exponential |
| `expM1` | Exponential minus 1 |
| `floor` | Floor |
| `log` | Natural logarithm |
| `log10` | Base-10 logarithm |
| `log1P` | Natural logarithm of 1 plus argument |
| `max` | Maximum of two values |
| `min` | Minimum of two values |
| `pow` | Power |
| `random` | Random number |
| `rint` | Round to nearest integer |
| `round` | Round |
| `sin` | Sine |
| `sinh` | Hyperbolic sine |
| `sqrt` | Square root |
| `tan` | Tangent |
| `tanh` | Hyperbolic tangent |
| `toDegrees` | Convert radians to degrees |
| `toRadians` | Convert degrees to radians |

---
---
## scala.sys

Interaction with the virtual machine and operating system.

| Code | Description |
|------|-------------|
| `BooleanProp` | Boolean system property |
| `ByteProp` | Byte system property |
| `CharProp` | Character system property |
| `DoubleProp` | Double system property |
| `FloatProp` | Float system property |
| `IntProp` | Integer system property |
| `LongProp` | Long system property |
| `Prop[T]` | Generic system property |
| `ShortProp` | Short system property |
| `StringProp` | String system property |
| `addShutdownHook` | Register shutdown hook |
| `error` | Print error message |
| `exit` | Exit the JVM |
| `process` | Object for process operations |
| `props` | System properties |
| `ShutdownHookThread` | Shutdown hook thread |
| `SystemProperties` | System properties utility |

---
---
## scala.util

Utility classes and objects.

### scala.util.matching

| Code | Description |
|------|-------------|
| `Regex` | Regular expression |
| `Pattern` | Compiled regular expression pattern |
| `Match` | Match result |
| `MatchData` | Match data |
| `MatchIterator` | Match iterator |

### scala.util.control

| Code | Description |
|------|-------------|
| `Breaks` | Break control |
| `ControlThrowable` | Control throwable |
| `Exception` | Exception utilities |
| `NonFatal` | Non-fatal exception extraction |
| `NoStackTrace` | Marker for no stack trace |
| `TailCalls` | Tail call optimization |
| `Try` | Represents a computation that may fail |
| `Success[T]` | Successful computation result |
| `Failure[T]` | Failed computation result |

### scala.util.hashing

| Code | Description |
|------|-------------|
| `BytesHash` | Hash for byte arrays |
| `MurmurHash3` | MurmurHash3 implementation |
| `Hashing[T]` | Typeclass for hashing |

### scala.util.parsing

| Code | Description |
|------|-------------|
| `Parser` | Parser combinator |
| `Parsers` | Parser combinators |
| `Combinators` | Parser combinators |
| `Input` | Parser input |
| `Reader` | Parser reader |
| `CharArrayReader` | Character array reader |
| `StringReader` | String reader |

---
---
## scala.annotation

Annotations.

| Code | Description |
|------|-------------|
| `elidable` | Marks definition for conditional compilation |
| `implicitNotFound` | Custom error message for implicit not found |
| `implicitAmbiguous` | Custom error message for ambiguous implicits |
| `migration` | Migration annotation |
| `nowarn` | Suppress warnings |
| `serializable` | Serialization annotation |
| `SerialVersionUID` | Serial version UID annotation |
| `static` | Static annotation |
| `switch` | Switch annotation |
| `tailrec` | Tail recursion annotation |
| `throws` | Throws annotation |
| `unchecked` | Unchecked annotation |
| `varargs` | Variable arguments annotation |
| `volatile` | Volatile annotation |
| `transient` | Transient annotation |
| `native` | Native annotation |
| `bridge` | Bridge annotation |
| `deprecated` | Deprecated annotation |
| `deprecatedName` | Deprecated name annotation |
| `deprecatedInheritance` | Deprecated inheritance annotation |
| `deprecatedOverriding` | Deprecated overriding annotation |
| `BeanProperty` | Bean property annotation |
| `BooleanBeanProperty` | Boolean bean property annotation |

---
---
## scala.reflect

Reflection API.

| Code | Description |
|------|-------------|
| `ClassTag[T]` | Type tag for runtime class information |
| `Manifest[T]` | Type tag for runtime type information |
| `OptManifest[T]` | Optional manifest |
| `NoManifest` | No manifest available |
| `ClassManifest[T]` | Class manifest |
| `api` | Reflection API |
| `macros` | Macro support |
| `runtime` | Runtime reflection |

---
---
## scala.compat

Compatibility utilities.

| Code | Description |
|------|-------------|
| `Platform` | Platform-specific utilities |
| `java8Compat` | Java 8 compatibility |
| `Platform.EOL` | End-of-line character |

---
---
## scala.jdk

JDK interoperability utilities.

| Code | Description |
|------|-------------|
| `CollectionConverters` | Collection conversions |
| `OptionConverters` | Option conversions |
| `StreamConverters` | Stream conversions |
| `DurationConverters` | Duration conversions |
| `FunctionConverters` | Function conversions |
| `Accumulator` | JDK Stream accumulator |
| `javaapi` | Java-friendly API |

---
---
## scala.ref

Reference types.

| Code | Description |
|------|-------------|
| `Reference[T]` | Base type for references |
| `SoftReference[T]` | Soft reference |
| `WeakReference[T]` | Weak reference |
| `PhantomReference[T]` | Phantom reference |

---
---
## scala.beans

Bean utilities.

| Code | Description |
|------|-------------|
| `BeanDescription` | Bean description |
| `BeanDisplayName` | Bean display name |
| `BeanInfo` | Bean information |
| `BeanInfoSkip` | Skip bean information |
| `BooleanBeanProperty` | Boolean bean property |
| `ScalaBeanProperty` | Scala bean property |

---
---
## scala.util

Additional utility classes.

| Code | Description |
|------|-------------|
| `Random` | Random number generator |
| `Try[T]` | Computation that may fail |
| `Success[T]` | Successful computation |
| `Failure[T]` | Failed computation |
| `Either[T1,T2]` | Disjunct union |
| `Left[T]` | Left projection of Either |
| `Right[T]` | Right projection of Either |
| `Properties` | Properties utility |
| `Sorting` | Sorting algorithms |
| `Hashing` | Hashing utilities |
| `DynamicVariable` | Dynamic variable |
| `Lazy` | Lazy initialization |
| `LazyVal` | Lazy value |
| `Chain[T]` | Chain of values |