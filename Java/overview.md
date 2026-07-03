## java.lang Package

| Code | Description |
|------|-------------|
| `Object` | Root of the Java class hierarchy. All classes inherit from Object. Provides methods like `toString()`, `equals()`, `hashCode()`, `getClass()`, `clone()`, `notify()`, `notifyAll()`, and `wait()`. |
| `String` | Immutable sequence of characters. Provides methods for string manipulation, comparison, and conversion. |
| `String(char[] value)` | Constructs a new String from a character array. |
| `String(byte[] bytes)` | Constructs a new String from a byte array using the platform's default charset. |
| `String(byte[] bytes, String charsetName)` | Constructs a new String from a byte array using the specified charset. |
| `String.valueOf(Object obj)` | Returns the string representation of the Object argument. |
| `String.format(String format, Object... args)` | Returns a formatted string using the specified format string and arguments. |
| `String.join(CharSequence delimiter, CharSequence... elements)` | Returns a new String composed of copies of the CharSequence elements joined together with a copy of the specified delimiter. |
| `StringBuilder` | Mutable sequence of characters. Provides methods like `append()`, `insert()`, `delete()`, `replace()`, `reverse()`, and `toString()`. |
| `StringBuffer` | Thread-safe mutable sequence of characters. Similar to StringBuilder but synchronized. |
| `Integer` | Wrapper class for the primitive type int. Provides methods like `parseInt()`, `valueOf()`, `toString()`, and constants like `MIN_VALUE` and `MAX_VALUE`. |
| `Long` | Wrapper class for the primitive type long. |
| `Float` | Wrapper class for the primitive type float. |
| `Double` | Wrapper class for the primitive type double. |
| `Boolean` | Wrapper class for the primitive type boolean. Provides methods like `parseBoolean()` and `valueOf()`. |
| `Byte` | Wrapper class for the primitive type byte. |
| `Character` | Wrapper class for the primitive type char. Provides methods like `isLetter()`, `isDigit()`, `isWhitespace()`, and `toUpperCase()`. |
| `Short` | Wrapper class for the primitive type short. |
| `Number` | Abstract superclass for all numeric wrapper classes. Provides methods like `intValue()`, `longValue()`, `floatValue()`, and `doubleValue()`. |
| `Math` | Provides mathematical functions and constants. Methods include `abs()`, `ceil()`, `floor()`, `round()`, `max()`, `min()`, `pow()`, `sqrt()`, `sin()`, `cos()`, `tan()`, `log()`, `exp()`, and `random()`. Constants include `E` and `PI`. |
| `StrictMath` | Provides mathematical functions with strict semantics. Similar to Math but with guaranteed reproducibility. |
| `System` | Provides access to system resources and properties. Fields include `in`, `out`, and `err`. Methods include `currentTimeMillis()`, `nanoTime()`, `arraycopy()`, `exit()`, `gc()`, and `getProperty()`. |
| `Runtime` | Provides access to the Java runtime system. Methods include `getRuntime()`, `exec()`, `exit()`, `gc()`, `freeMemory()`, `totalMemory()`, `maxMemory()`, and `addShutdownHook()`. |
| `Class<T>` | Represents a class or interface at runtime. Provides methods like `getName()`, `getSimpleName()`, `getSuperclass()`, `getInterfaces()`, `getMethods()`, `getFields()`, `getConstructors()`, `newInstance()`, `forName()`, and `getClassLoader()`. |
| `ClassLoader` | Responsible for loading classes. Provides methods like `loadClass()`, `findClass()`, `defineClass()`, `getParent()`, and `getResources()`. |
| `Thread` | Represents a thread of execution. Provides methods like `start()`, `run()`, `stop()`, `suspend()`, `resume()`, `sleep()`, `join()`, `yield()`, `setPriority()`, `getPriority()`, and `interrupt()`. |
| `Runnable` | Interface for classes whose instances are intended to be executed by a thread. Requires implementation of the `run()` method. |
| `ThreadGroup` | Represents a group of threads. Provides methods for managing thread groups. |
| `Throwable` | Root of the Java exception hierarchy. Provides methods like `getMessage()`, `getCause()`, `printStackTrace()`, and `fillInStackTrace()`. |
| `Exception` | Root of the Java exception hierarchy. |
| `RuntimeException` | Root of the Java unchecked exception hierarchy. |
| `Error` | Root of the Java error hierarchy. |
| `IllegalArgumentException` | Thrown to indicate that a method has been passed an illegal or inappropriate argument. |
| `IllegalStateException` | Thrown to indicate that a method has been invoked at an illegal or inappropriate time. |
| `NullPointerException` | Thrown when an application attempts to use null in a case where an object is required. |
| `IndexOutOfBoundsException` | Thrown to indicate that an index of some sort is out of range. |
| `ArrayIndexOutOfBoundsException` | Thrown to indicate that an array has been accessed with an illegal index. |
| `StringIndexOutOfBoundsException` | Thrown by String methods to indicate that an index is out of range. |
| `ClassCastException` | Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance. |
| `UnsupportedOperationException` | Thrown to indicate that the requested operation is not supported. |
| `SecurityManager` | Provides a security policy for applications. |
| `Package` | Contains version information about the implementation and specification of a Java package. |
| `Void` | Placeholder class for the Java keyword void. |
| `Comparable<T>` | Interface for classes whose instances can be compared for natural ordering. Requires implementation of the `compareTo()` method. |
| `Iterable<T>` | Interface for classes whose instances can be iterated over. Requires implementation of the `iterator()` method. |
| `AutoCloseable` | Interface for classes whose instances can be closed. Requires implementation of the `close()` method. |
| `Cloneable` | Interface for classes whose instances can be cloned. |
| `Serializable` | Interface for classes whose instances can be serialized. |
| `SuppressWarnings` | Annotation to suppress warnings. |
| `Override` | Annotation to indicate that a method is intended to override a method in a superclass. |
| `Deprecated` | Annotation to indicate that a program element is deprecated. |
| `SafeVarargs` | Annotation to assert that the use of varargs in a method or constructor is safe. |
| `FunctionalInterface` | Annotation to indicate that an interface is intended to be a functional interface. |

---
## java.util Package

| Code | Description |
|------|-------------|
| `Collection<E>` | Root interface for all collections. Provides methods like `add()`, `addAll()`, `remove()`, `removeAll()`, `retainAll()`, `clear()`, `contains()`, `containsAll()`, `isEmpty()`, `size()`, `iterator()`, `toArray()`, `stream()`, and `parallelStream()`. |
| `List<E>` | Interface for ordered collections (sequences). Provides methods like `get()`, `set()`, `indexOf()`, `lastIndexOf()`, `subList()`, and `listIterator()`. |
| `ArrayList<E>` | Resizable array implementation of the List interface. Provides methods for dynamic array manipulation. |
| `LinkedList<E>` | Doubly-linked list implementation of the List and Deque interfaces. Provides methods for efficient insertion and removal at both ends. |
| `Vector<E>` | Thread-safe resizable array implementation. Similar to ArrayList but synchronized. |
| `Stack<E>` | Last-in-first-out (LIFO) stack of objects. Extends Vector with methods like `push()`, `pop()`, `peek()`, and `empty()`. |
| `Queue<E>` | Interface for queues. Provides methods like `offer()`, `poll()`, `peek()`, and `remove()`. |
| `Deque<E>` | Interface for double-ended queues. Provides methods for insertion and removal at both ends. |
| `PriorityQueue<E>` | Priority queue implementation. Orders elements according to their natural ordering or a provided Comparator. |
| `ArrayDeque<E>` | Resizable array implementation of the Deque interface. More efficient than LinkedList for most operations. |
| `Set<E>` | Interface for collections that contain no duplicate elements. |
| `HashSet<E>` | Hash table implementation of the Set interface. Provides O(1) time complexity for basic operations. |
| `LinkedHashSet<E>` | Hash table and linked list implementation of the Set interface. Maintains insertion order. |
| `TreeSet<E>` | Red-black tree implementation of the Set interface. Maintains elements in sorted order. |
| `SortedSet<E>` | Interface for sets that maintain their elements in sorted order. |
| `NavigableSet<E>` | Interface for sets that support navigation operations like `lower()`, `floor()`, `ceiling()`, and `higher()`. |
| `Map<K,V>` | Interface for mappings from keys to values. Provides methods like `put()`, `get()`, `remove()`, `containsKey()`, `containsValue()`, `keySet()`, `values()`, `entrySet()`, `size()`, and `isEmpty()`. |
| `HashMap<K,V>` | Hash table implementation of the Map interface. Provides O(1) time complexity for basic operations. |
| `LinkedHashMap<K,V>` | Hash table and linked list implementation of the Map interface. Maintains insertion order or access order. |
| `TreeMap<K,V>` | Red-black tree implementation of the Map interface. Maintains keys in sorted order. |
| `SortedMap<K,V>` | Interface for maps that maintain their keys in sorted order. |
| `NavigableMap<K,V>` | Interface for maps that support navigation operations. |
| `Hashtable<K,V>` | Thread-safe hash table implementation. Similar to HashMap but synchronized. |
| `Properties` | Hashtable subclass for storing and retrieving string key-value pairs. Used for configuration files. |
| `Iterator<E>` | Interface for iterating over collections. Provides methods like `hasNext()`, `next()`, and `remove()`. |
| `ListIterator<E>` | Interface for iterating over lists in both directions. Provides methods like `hasPrevious()`, `previous()`, `nextIndex()`, and `previousIndex()`. |
| `Enumeration<E>` | Legacy interface for iterating over collections. Provides methods like `hasMoreElements()` and `nextElement()`. |
| `Arrays` | Utility class for array operations. Provides methods like `sort()`, `binarySearch()`, `fill()`, `copyOf()`, `asList()`, `toString()`, `deepToString()`, `equals()`, `deepEquals()`, `hashCode()`, and `stream()`. |
| `Collections` | Utility class for collection operations. Provides methods like `sort()`, `binarySearch()`, `reverse()`, `shuffle()`, `fill()`, `copy()`, `addAll()`, `frequency()`, `disjoint()`, `max()`, `min()`, `synchronizedList()`, `synchronizedMap()`, `synchronizedSet()`, `unmodifiableList()`, `unmodifiableMap()`, and `unmodifiableSet()`. |
| `Comparator<T>` | Interface for comparing two objects. Requires implementation of the `compare()` method. Provides methods like `reversed()`, `thenComparing()`, and `naturalOrder()`. |
| `Comparators` | Utility class for Comparator operations. Provides methods like `naturalOrder()`, `reverseOrder()`, and `nullsFirst()`. |
| `Objects` | Utility class for object operations. Provides methods like `equals()`, `deepEquals()`, `hashCode()`, `hash()`, `toString()`, `requireNonNull()`, and `isNull()`. |
| `Random` | Generates pseudo-random numbers. Provides methods like `nextInt()`, `nextLong()`, `nextFloat()`, `nextDouble()`, `nextBoolean()`, `nextBytes()`, and `setSeed()`. |
| `UUID` | Represents an immutable universally unique identifier. Provides methods like `randomUUID()`, `fromString()`, `toString()`, `getMostSignificantBits()`, and `getLeastSignificantBits()`. |
| `Optional<T>` | Container object for values that may be null. Provides methods like `isPresent()`, `get()`, `orElse()`, `orElseGet()`, `orElseThrow()`, `ifPresent()`, `filter()`, `map()`, and `flatMap()`. |
| `OptionalInt` | Container object for int values that may be null. |
| `OptionalLong` | Container object for long values that may be null. |
| `OptionalDouble` | Container object for double values that may be null. |
| `Scanner` | Scanner for parsing primitive types and strings from input. Provides methods like `next()`, `nextInt()`, `nextLine()`, `hasNext()`, `useDelimiter()`, and `useLocale()`. |
| `StringTokenizer` | Legacy class for breaking strings into tokens. |
| `Tokenizer` | Tokenizer for breaking strings into tokens. |
| `Locale` | Represents a geographical, political, or cultural region. Provides methods like `getDefault()`, `getCountry()`, `getLanguage()`, and `getDisplayName()`. |
| `Currency` | Represents a currency. Provides methods like `getInstance()`, `getCurrencyCode()`, and `getSymbol()`. |
| `TimeZone` | Represents a time zone. Provides methods like `getDefault()`, `getTimeZone()`, and `getDisplayName()`. |
| `Calendar` | Abstract class for converting between dates and time fields. Provides methods like `getInstance()`, `get()`, `set()`, `add()`, `roll()`, and `getTime()`. |
| `GregorianCalendar` | Concrete subclass of Calendar for the Gregorian calendar. |
| `Date` | Represents a specific instant in time. Provides methods like `getTime()`, `setTime()`, `before()`, `after()`, and `compareTo()`. |
| `SimpleTimeZone` | Concrete subclass of TimeZone for Gregorian time zones. |
| `Timer` | Facility for threads to schedule tasks for future execution. Provides methods like `schedule()`, `scheduleAtFixedRate()`, `cancel()`, and `purge()`. |
| `TimerTask` | Task that can be scheduled for one-time or repeated execution by a Timer. Requires implementation of the `run()` method. |
| `Observable` | Observable object that can be subscribed to by observers. Provides methods like `addObserver()`, `deleteObserver()`, `notifyObservers()`, and `setChanged()`. |
| `Observer` | Interface for receiving notifications from an Observable. Requires implementation of the `update()` method. |
| `ResourceBundle` | Provides access to locale-specific resources. Provides methods like `getBundle()`, `getString()`, `getObject()`, and `getKeys()`. |
| `ResourceBundle.Control` | Control class for customizing ResourceBundle loading. |
| `PropertyResourceBundle` | ResourceBundle subclass for property files. |
| `ListResourceBundle` | ResourceBundle subclass for lists of key-value pairs. |
| `ServiceLoader<S>` | Facility for loading service providers. Provides methods like `load()`, `reload()`, and `iterator()`. |
| `Formatter` | Base class for formatters. |
| `Format` | Abstract base class for formatters. |
| `MessageFormat` | Formats messages with locale-specific patterns. |
| `DateFormat` | Abstract class for date/time formatting. Provides methods like `getInstance()`, `getDateInstance()`, `getTimeInstance()`, `getDateTimeInstance()`, `format()`, and `parse()`. |
| `SimpleDateFormat` | Concrete class for formatting and parsing dates. |
| `NumberFormat` | Abstract class for number formatting. Provides methods like `getInstance()`, `getNumberInstance()`, `getCurrencyInstance()`, `getPercentInstance()`, `format()`, and `parse()`. |
| `DecimalFormat` | Concrete class for formatting decimal numbers. |
| `ChoiceFormat` | Formats numbers as words. |
| `Collator` | Performs locale-sensitive string comparison. Provides methods like `getInstance()`, `compare()`, and `equals()`. |
| `Currency` | Represents a currency. |
| `Formattable` | Interface for objects that can be formatted. |
| `ParsePosition` | Tracks the current position during parsing. |
| `AttributedCharacterIterator` | Interface for character iterators with attribute information. |
| `AttributedString` | String with attributes. |
| `Annotation` | Interface for annotation types. |
| `EventObject` | Root class for all event classes. |
| `EventListener` | Interface for event listeners. |

---
## java.io Package

| Code | Description |
|------|-------------|
| `InputStream` | Abstract class for reading bytes from a stream. Provides methods like `read()`, `read(byte[] b)`, `skip()`, `available()`, `close()`, `mark()`, `reset()`, and `markSupported()`. |
| `FileInputStream` | InputStream for reading bytes from a file. |
| `ByteArrayInputStream` | InputStream that reads from a byte array. |
| `PipedInputStream` | InputStream for reading from a piped output stream. |
| `FilterInputStream` | Abstract class for filtering input streams. |
| `BufferedInputStream` | InputStream with buffering for efficient reading. |
| `DataInputStream` | InputStream for reading primitive data types. Provides methods like `readBoolean()`, `readByte()`, `readChar()`, `readShort()`, `readInt()`, `readLong()`, `readFloat()`, `readDouble()`, and `readUTF()`. |
| `ObjectInputStream` | InputStream for deserializing objects. Provides methods like `readObject()`, `readBoolean()`, `readByte()`, `readChar()`, etc. |
| `PushbackInputStream` | InputStream with the ability to push back a byte. |
| `SequenceInputStream` | InputStream that concatenates multiple input streams. |
| `OutputStream` | Abstract class for writing bytes to a stream. Provides methods like `write(int b)`, `write(byte[] b)`, `flush()`, and `close()`. |
| `FileOutputStream` | OutputStream for writing bytes to a file. |
| `ByteArrayOutputStream` | OutputStream that writes to a byte array. |
| `PipedOutputStream` | OutputStream for writing to a piped input stream. |
| `FilterOutputStream` | Abstract class for filtering output streams. |
| `BufferedOutputStream` | OutputStream with buffering for efficient writing. |
| `DataOutputStream` | OutputStream for writing primitive data types. Provides methods like `writeBoolean()`, `writeByte()`, `writeChar()`, `writeShort()`, `writeInt()`, `writeLong()`, `writeFloat()`, `writeDouble()`, and `writeUTF()`. |
| `ObjectOutputStream` | OutputStream for serializing objects. Provides methods like `writeObject()`, `writeBoolean()`, `writeByte()`, `writeChar()`, etc. |
| `PrintStream` | OutputStream for printing formatted representations of objects. Provides methods like `print()`, `println()`, and `printf()`. |
| `File` | Represents a file or directory pathname. Provides methods like `exists()`, `isFile()`, `isDirectory()`, `canRead()`, `canWrite()`, `canExecute()`, `length()`, `lastModified()`, `delete()`, `mkdir()`, `mkdirs()`, `renameTo()`, `list()`, `listFiles()`, and `createNewFile()`. |
| `FileDescriptor` | Represents a file descriptor for open files or sockets. |
| `FilenameFilter` | Interface for filtering filenames. Requires implementation of the `accept()` method. |
| `FileFilter` | Interface for filtering files. Requires implementation of the `accept()` method. |
| `RandomAccessFile` | Supports both reading and writing to a random access file. Provides methods like `read()`, `write()`, `seek()`, `getFilePointer()`, `length()`, and `setLength()`. |
| `Reader` | Abstract class for reading character streams. Provides methods like `read()`, `read(char[] cbuf)`, `skip()`, `ready()`, `mark()`, `reset()`, `markSupported()`, and `close()`. |
| `FileReader` | Reader for reading character files. |
| `CharArrayReader` | Reader that reads from a character array. |
| `PipedReader` | Reader for reading from a piped writer. |
| `FilterReader` | Abstract class for filtering character streams. |
| `BufferedReader` | Reader with buffering for efficient reading. Provides methods like `readLine()`. |
| `InputStreamReader` | Bridge from byte streams to character streams. |
| `FileReader` | Convenience class for reading character files. |
| `PushbackReader` | Reader with the ability to push back a character. |
| `StringReader` | Reader that reads from a string. |
| `Writer` | Abstract class for writing character streams. Provides methods like `write(int c)`, `write(char[] cbuf)`, `write(String str)`, `append()`, `flush()`, and `close()`. |
| `FileWriter` | Writer for writing character files. |
| `CharArrayWriter` | Writer that writes to a character array. |
| `PipedWriter` | Writer for writing to a piped reader. |
| `FilterWriter` | Abstract class for filtering character streams. |
| `BufferedWriter` | Writer with buffering for efficient writing. Provides methods like `newLine()`. |
| `OutputStreamWriter` | Bridge from character streams to byte streams. |
| `PrintWriter` | Writer for printing formatted representations of objects. Provides methods like `print()`, `println()`, and `printf()`. |
| `StringWriter` | Writer that writes to a string. |
| `Console` | Provides access to the character-based console device. Provides methods like `printf()`, `format()`, and `reader()`. |
| `Serializable` | Interface for classes whose instances can be serialized. |
| `Externalizable` | Interface for classes that control their own serialization. |
| `ObjectStreamClass` | Serialization descriptor for classes. |
| `StreamCorruptedException` | Thrown when control information in the object stream is inconsistent. |
| `InvalidClassException` | Thrown when the serialization runtime detects a class incompatibility. |
| `InvalidObjectException` | Thrown when the serialization runtime detects a problem with a class. |
| `NotActiveException` | Thrown when serialization or deserialization is not active. |
| `NotSerializableException` | Thrown when an instance is required to have a serializable interface. |
| `OptionalDataException` | Thrown when primitive data is read instead of objects. |
| `StreamCorruptedException` | Thrown when control information in the object stream is inconsistent. |
| `WriteAbortedException` | Thrown when an exception was thrown during a write operation. |

---
## java.nio Package

| Code | Description |
|------|-------------|
| `Buffer` | Abstract class for buffers. Provides methods like `capacity()`, `position()`, `limit()`, `mark()`, `reset()`, `clear()`, `flip()`, `rewind()`, `remaining()`, `hasRemaining()`, `isReadOnly()`, and `isDirect()`. |
| `ByteBuffer` | Buffer for bytes. Provides methods like `get()`, `put()`, `getChar()`, `putChar()`, `getShort()`, `putShort()`, `getInt()`, `putInt()`, `getLong()`, `putLong()`, `getFloat()`, `putFloat()`, `getDouble()`, `putDouble()`, `asCharBuffer()`, `asShortBuffer()`, `asIntBuffer()`, `asLongBuffer()`, `asFloatBuffer()`, and `asDoubleBuffer()`. |
| `CharBuffer` | Buffer for characters. |
| `DoubleBuffer` | Buffer for double values. |
| `FloatBuffer` | Buffer for float values. |
| `IntBuffer` | Buffer for int values. |
| `LongBuffer` | Buffer for long values. |
| `ShortBuffer` | Buffer for short values. |
| `MappedByteBuffer` | Direct byte buffer whose content is a memory-mapped file. |
| `DirectByteBuffer` | Direct byte buffer. |
| `HeapByteBuffer` | Heap-allocated byte buffer. |
| `ByteOrder` | Defines endianness. Provides constants like `BIG_ENDIAN` and `LITTLE_ENDIAN`. |
| `CharSet` | Named mapping between characters and bytes. Provides methods like `forName()`, `availableCharsets()`, `canEncode()`, `encode()`, `decode()`, `newEncoder()`, and `newDecoder()`. |
| `CharsetEncoder` | Encodes characters into bytes. Provides methods like `canEncode()`, `encode()`, `flush()`, and `reset()`. |
| `CharsetDecoder` | Decodes bytes into characters. Provides methods like `canDecode()`, `decode()`, `flush()`, and `reset()`. |
| `CodingErrorAction` | Action to take when a coding error occurs. |
| `CharsetProvider` | Service-provider class for charsets. |
| `StandardCharsets` | Constants for standard charsets. Provides constants like `US_ASCII`, `ISO_8859_1`, `UTF_8`, `UTF_16`, `UTF_16BE`, and `UTF_16LE`. |
| `Path` | Represents a path in the file system. Provides methods like `getFileSystem()`, `getRoot()`, `getFileName()`, `getParent()`, `getNameCount()`, `getName()`, `subpath()`, `normalize()`, `resolve()`, `resolveSibling()`, `relativize()`, `toUri()`, `toAbsolutePath()`, `toFile()`, `toRealPath()`, `startsWith()`, `endsWith()`, and `iterator()`. |
| `Paths` | Utility class for Path operations. Provides methods like `get()`. |
| `FileSystem` | Represents a file system. Provides methods like `getPath()`, `getRootDirectories()`, `getFileStores()`, `getSeparator()`, `getPathMatcher()`, `newWatchService()`, and `provider()`. |
| `FileSystems` | Utility class for FileSystem operations. Provides methods like `getDefault()`, `newFileSystem()`, and `getFileSystem()`. |
| `FileStore` | Represents a storage mechanism for files. |
| `WatchService` | Service for watching file system events. Provides methods like `poll()`, `take()`, and `close()`. |
| `WatchKey` | Token representing the registration of a watchable object with a WatchService. Provides methods like `pollEvents()`, `reset()`, `cancel()`, `isValid()`, and `watchable()`. |
| `WatchEvent<T>` | Represents an event or a repeated event for an object that is registered with a WatchService. |
| `WatchEvent.Kind<T>` | Enumeration of event kinds. Provides constants like `OVERFLOW`, `ENTRY_CREATE`, `ENTRY_DELETE`, and `ENTRY_MODIFY`. |
| `WatchEvent.Modifier` | Enumeration of event modifiers. |
| `FileVisitor<T>` | Interface for visiting files. Requires implementation of methods like `preVisitDirectory()`, `postVisitDirectory()`, `visitFile()`, and `visitFileFailed()`. |
| `SimpleFileVisitor<T>` | Simple implementation of FileVisitor. |
| `FileAttribute<T>` | Interface for file attributes. |
| `FileAttributeView` | Interface for file attribute views. |
| `BasicFileAttributeView` | File attribute view for basic file attributes. |
| `BasicFileAttributes` | Basic file attributes. Provides methods like `lastModifiedTime()`, `lastAccessTime()`, `creationTime()`, `size()`, `isRegularFile()`, `isDirectory()`, `isSymbolicLink()`, `isOther()`, and `fileKey()`. |
| `DosFileAttributeView` | File attribute view for DOS file attributes. |
| `DosFileAttributes` | DOS file attributes. |
| `PosixFileAttributeView` | File attribute view for POSIX file attributes. |
| `PosixFileAttributes` | POSIX file attributes. Provides methods like `owner()`, `group()`, and `permissions()`. |
| `PosixFilePermission` | Enumeration of POSIX file permissions. Provides constants like `OWNER_READ`, `OWNER_WRITE`, `OWNER_EXECUTE`, `GROUP_READ`, etc. |
| `PosixFilePermissions` | POSIX file permissions. Provides methods like `asFileAttribute()`, `toString()`, and `fromString()`. |
| `LinkOption` | Enumeration of link options. Provides constants like `NOFOLLOW_LINKS`. |
| `CopyOption` | Interface for copy options. |
| `StandardCopyOption` | Enumeration of standard copy options. Provides constants like `REPLACE_EXISTING`, `COPY_ATTRIBUTES`, and `NOFOLLOW_LINKS`. |
| `StandardOpenOption` | Enumeration of standard open options. Provides constants like `READ`, `WRITE`, `APPEND`, `TRUNCATE_EXISTING`, `CREATE`, `CREATE_NEW`, `DELETE_ON_CLOSE`, and `SPARSE`. |
| `OpenOption` | Interface for open options. |
| `DirectoryStream<T>` | Interface for iterating over the entries in a directory. |
| `DirectoryStream.Filter<T>` | Interface for filtering directory stream entries. |
| `FileTreeWalker` | Utility for walking a file tree. |
| `SecureDirectoryStream<T>` | Directory stream with support for secure directory operations. |
| `Channel` | Interface for channels that can be asynchronously closed and interrupted. |
| `InterruptibleChannel` | Interface for channels that can be asynchronously closed and interrupted. |
| `SelectableChannel` | Interface for channels that can be multiplexed via a Selector. |
| `ServerSocketChannel` | Selectable channel for server sockets. |
| `SocketChannel` | Selectable channel for stream-oriented connecting sockets. |
| `DatagramChannel` | Selectable channel for datagram-oriented sockets. |
| `Pipe.SinkChannel` | Writable channel for pipes. |
| `Pipe.SourceChannel` | Readable channel for pipes. |
| `Selector` | Selector for multiplexed, non-blocking I/O operations. Provides methods like `open()`, `close()`, `isOpen()`, `provider()`, `keys()`, `selectedKeys()`, `select()`, `select(long timeout)`, `wakeup()`, and `register()`. |
| `SelectionKey` | Token representing the registration of a SelectableChannel with a Selector. Provides methods like `isValid()`, `cancel()`, `readyOps()`, `interestOps()`, `selector()`, `channel()`, `attach()`, `attachment()`, and `isReadable()`, `isWritable()`, `isConnectable()`, `isAcceptable()`. |
| `SelectionKey.OP_READ` | Operation set bit for read operations. |
| `SelectionKey.OP_WRITE` | Operation set bit for write operations. |
| `SelectionKey.OP_CONNECT` | Operation set bit for connect operations. |
| `SelectionKey.OP_ACCEPT` | Operation set bit for accept operations. |
| `SelectorProvider` | Factory for selectors. |
| `Pipe` | Pair of channels that implement a unidirectional pipe. |
| `FileChannel` | File channel for reading, writing, mapping, and manipulating a file. Provides methods like `open()`, `read()`, `write()`, `position()`, `size()`, `truncate()`, `force()`, `lock()`, `tryLock()`, `map()`, and `transferFrom()`, `transferTo()`. |
| `FileLock` | Token for file region locks. Provides methods like `isValid()`, `overlaps()`, `release()`, and `channel()`. |
| `MappedByteBuffer` | Direct byte buffer whose content is a memory-mapped file. |
| `Channel` | Interface for channels. |
| `GatheringByteChannel` | Interface for channels that can gather bytes from a buffer into a channel. |
| `ScatteringByteChannel` | Interface for channels that can scatter bytes from a channel into a buffer. |
| `ByteChannel` | Interface for channels that can read and write bytes. |
| `ReadableByteChannel` | Interface for channels that can read bytes. |
| `WritableByteChannel` | Interface for channels that can write bytes. |
| `SeekableByteChannel` | Interface for channels that maintain a position and allow the position to be changed. |

---
## java.time Package

| Code | Description |
|------|-------------|
| `Instant` | Represents an instantaneous point in time. Provides methods like `now()`, `ofEpochSecond()`, `ofEpochMilli()`, `parse()`, `toEpochMilli()`, `plus()`, `minus()`, `plusNanos()`, `isAfter()`, `isBefore()`, and `compareTo()`. |
| `LocalDate` | Represents a date (year, month, day) without a time-zone. Provides methods like `now()`, `of()`, `parse()`, `toEpochDay()`, `plusDays()`, `minusDays()`, `plusWeeks()`, `minusWeeks()`, `plusMonths()`, `minusMonths()`, `plusYears()`, `minusYears()`, `withDayOfMonth()`, `withDayOfYear()`, `withMonth()`, `withYear()`, `isLeapYear()`, `isBefore()`, `isAfter()`, `isEqual()`, and `compareTo()`. |
| `LocalTime` | Represents a time (hour, minute, second, nanosecond) without a date or time-zone. Provides methods like `now()`, `of()`, `parse()`, `toSecondOfDay()`, `toNanoOfDay()`, `plusHours()`, `minusHours()`, `plusMinutes()`, `minusMinutes()`, `plusSeconds()`, `minusSeconds()`, `plusNanos()`, `minusNanos()`, `withHour()`, `withMinute()`, `withSecond()`, `withNano()`, `isBefore()`, `isAfter()`, `isEqual()`, and `compareTo()`. |
| `LocalDateTime` | Represents a date-time (date and time) without a time-zone. Provides methods like `now()`, `of()`, `parse()`, `toInstant()`, `toEpochSecond()`, `plusDays()`, `minusDays()`, `plusHours()`, `minusHours()`, etc. |
| `ZonedDateTime` | Represents a date-time with a time-zone. Provides methods like `now()`, `of()`, `parse()`, `toInstant()`, `toLocalDateTime()`, `toOffsetDateTime()`, `withZoneSameInstant()`, `withZoneSameLocal()`, `plusDays()`, `minusDays()`, etc. |
| `OffsetDateTime` | Represents a date-time with an offset from UTC/Greenwich. Provides methods like `now()`, `of()`, `parse()`, `toInstant()`, `toLocalDateTime()`, `toZonedDateTime()`, `withOffsetSameInstant()`, `withOffsetSameLocal()`, `plusDays()`, etc. |
| `OffsetTime` | Represents a time with an offset from UTC/Greenwich. |
| `ZoneOffset` | Represents a time-zone offset from UTC/Greenwich. Provides constants like `UTC` and methods like `of()`, `ofHours()`, `ofHoursMinutes()`, `ofTotalSeconds()`, `parse()`, `getTotalSeconds()`, `getId()`, and `getRules()`. |
| `ZoneId` | Represents a time-zone ID. Provides methods like `of()`, `ofOffset()`, `systemDefault()`, `getAvailableZoneIds()`, `getRules()`, and `normalize()`. |
| `ZoneRegion` | Represents a time-zone region. |
| `ZoneRules` | Rules defining how a time-zone offset varies. |
| `DayOfWeek` | Enumeration of the days of the week. Provides constants like `MONDAY`, `TUESDAY`, etc., and methods like `of()`, `valueOf()`, `plus()`, `minus()`, and `getValue()`. |
| `Month` | Enumeration of the months of the year. Provides constants like `JANUARY`, `FEBRUARY`, etc., and methods like `of()`, `valueOf()`, `plus()`, `minus()`, and `getValue()`. |
| `Year` | Represents a year. |
| `YearMonth` | Represents a year-month. |
| `MonthDay` | Represents a month-day. |
| `Era` | Enumeration of eras. Provides constants like `BCE` and `CE`. |
| `ChronoLocalDate` | Interface for date objects without a time-zone. |
| `ChronoLocalDateTime` | Interface for date-time objects without a time-zone. |
| `ChronoZonedDateTime` | Interface for date-time objects with a time-zone. |
| `Chronology` | Interface for calendar systems. |
| `ChronoField` | Enumeration of fields for date-time objects. Provides constants like `NANO_OF_SECOND`, `NANO_OF_DAY`, `MICRO_OF_SECOND`, `MICRO_OF_DAY`, `MILLI_OF_SECOND`, `MILLI_OF_DAY`, `SECOND_OF_MINUTE`, `SECOND_OF_DAY`, `MINUTE_OF_HOUR`, `MINUTE_OF_DAY`, `HOUR_OF_AMPM`, `CLOCK_HOUR_OF_AMPM`, `HOUR_OF_DAY`, `CLOCK_HOUR_OF_DAY`, `AMPM_OF_DAY`, `DAY_OF_WEEK`, `ALIGNED_DAY_OF_WEEK_IN_MONTH`, `ALIGNED_DAY_OF_WEEK_IN_YEAR`, `DAY_OF_MONTH`, `DAY_OF_YEAR`, `EPOCH_DAY`, `ALIGNED_WEEK_OF_MONTH`, `ALIGNED_WEEK_OF_YEAR`, `MONTH_OF_YEAR`, `PROLEPTIC_MONTH`, `YEAR_OF_ERA`, `YEAR`, `ERA`, `INSTANT_SECONDS`, and `OFFSET_SECONDS`. |
| `ChronoUnit` | Enumeration of units for date-time objects. Provides constants like `NANOS`, `MICROS`, `MILLIS`, `SECONDS`, `MINUTES`, `HOURS`, `HALF_DAYS`, `DAYS`, `WEEKS`, `MONTHS`, `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA`, and `ERAS`. |
| `Temporal` | Interface for temporal objects. |
| `TemporalAccessor` | Interface for accessing temporal objects. |
| `TemporalAdjuster` | Interface for adjusting temporal objects. |
| `TemporalAmount` | Interface for amounts of time. |
| `TemporalField` | Interface for fields of temporal objects. |
| `TemporalQuery<R>` | Interface for querying temporal objects. |
| `TemporalUnit` | Interface for units of time. |
| `ValueRange` | Represents a range of values. |
| `DateTimeException` | Exception thrown for date-time errors. |
| `DateTimeParseException` | Exception thrown for date-time parsing errors. |
| `DateTimeFormatter` | Formatter for date-time objects. Provides methods like `ofPattern()`, `ofLocalizedDate()`, `ofLocalizedTime()`, `ofLocalizedDateTime()`, `parse()`, `format()`, `withLocale()`, `withChronology()`, `withZone()`, and `withResolverStyle()`. |
| `DateTimeFormatterBuilder` | Builder for DateTimeFormatter. |
| `DecimalStyle` | Style for decimal numbers. |
| `FormatStyle` | Enumeration of format styles. Provides constants like `SHORT`, `MEDIUM`, `LONG`, and `FULL`. |
| `ResolverStyle` | Enumeration of resolver styles. Provides constants like `SMART`, `STRICT`, `LENIENT`, and `THROW_ON_CONFLICT`. |
| `SignStyle` | Enumeration of sign styles. Provides constants like `POSITIVE`, `NEGATIVE`, `EXCEEDS_PAD`, and `ALWAYS`. |
| `TextStyle` | Enumeration of text styles. Provides constants like `FULL`, `SHORT`, and `NARROW`. |
| `Duration` | Represents a duration of time. Provides methods like `of()`, `ofMillis()`, `ofSeconds()`, `ofMinutes()`, `ofHours()`, `ofDays()`, `parse()`, `toMillis()`, `toSeconds()`, `toMinutes()`, `toHours()`, `toDays()`, `plus()`, `minus()`, `multipliedBy()`, `dividedBy()`, `negated()`, `abs()`, `isZero()`, `isNegative()`, and `compareTo()`. |
| `Period` | Represents a period of time in terms of years, months, and days. Provides methods like `of()`, `ofYears()`, `ofMonths()`, `ofDays()`, `ofWeeks()`, `parse()`, `toTotalMonths()`, `getYears()`, `getMonths()`, `getDays()`, `plus()`, `minus()`, `multipliedBy()`, `negated()`, `abs()`, `isZero()`, `isNegative()`, and `compareTo()`. |
| `YearMonth` | Represents a year-month. |
| `MonthDay` | Represents a month-day. |
| `Clock` | Provides access to the current instant, date, and time using a time-zone. Provides methods like `systemUTC()`, `systemDefaultZone()`, `system()`, `fixed()`, `offset()`, `tick()`, `tickMinutes()`, `tickSeconds()`, `tickMillis()`, `withZone()`, and `getZone()`. |
| `TimeZone` | Legacy class for representing a time zone. |

---
## java.util.concurrent Package

| Code | Description |
|------|-------------|
| `Executor` | Interface for executing tasks. Provides a single method: `execute(Runnable command)`. |
| `ExecutorService` | Interface for an Executor that provides methods to manage termination and methods to produce Future objects. Provides methods like `shutdown()`, `shutdownNow()`, `isShutdown()`, `isTerminated()`, `awaitTermination()`, `submit()`, `invokeAll()`, `invokeAny()`, and `newTaskFor()`. |
| `ScheduledExecutorService` | ExecutorService that can schedule commands to run after a given delay, or to execute periodically. Provides methods like `schedule()`, `scheduleAtFixedRate()`, and `scheduleWithFixedDelay()`. |
| `ThreadPoolExecutor` | Thread pool implementation of ExecutorService. Provides methods for configuring the thread pool, such as `setCorePoolSize()`, `setMaximumPoolSize()`, `setKeepAliveTime()`, and `setRejectedExecutionHandler()`. |
| `ForkJoinPool` | ExecutorService for running ForkJoinTasks. Provides methods like `commonPool()`, `submit()`, and `invoke()`. |
| `ForkJoinTask<V>` | Abstract base class for ForkJoinPool tasks. Provides methods like `fork()`, `join()`, `get()`, `isDone()`, `isCompletedAbnormally()`, and `isCancelled()`. |
| `RecursiveTask<V>` | ForkJoinTask that returns a result. Requires implementation of the `compute()` method. |
| `RecursiveAction` | ForkJoinTask that does not return a result. Requires implementation of the `compute()` method. |
| `Callable<V>` | Interface for tasks that return a result. Requires implementation of the `call()` method. |
| `Future<V>` | Interface for the result of an asynchronous computation. Provides methods like `get()`, `get(long timeout, TimeUnit unit)`, `cancel()`, `isCancelled()`, and `isDone()`. |
| `RunnableFuture<V>` | Interface for a Runnable that also returns a result. |
| `CompletableFuture<T>` | CompletionStage that may be explicitly completed. Provides methods like `supplyAsync()`, `runAsync()`, `thenApply()`, `thenAccept()`, `thenRun()`, `thenCombine()`, `thenAcceptBoth()`, `runAfterBoth()`, `thenCompose()`, `acceptEither()`, `runAfterEither()`, `exceptionally()`, `whenComplete()`, `complete()`, `completeExceptionally()`, `join()`, `get()`, `isDone()`, `isCompletedExceptionally()`, and `obtrudeValue()`. |
| `CompletionStage<T>` | Interface for a stage of a possibly asynchronous computation. Provides methods like `thenApply()`, `thenAccept()`, `thenRun()`, `thenCombine()`, `thenAcceptBoth()`, `runAfterBoth()`, `thenCompose()`, `acceptEither()`, `runAfterEither()`, `exceptionally()`, and `whenComplete()`. |
| `CompletionException` | Exception thrown when an exception is encountered during the completion of a CompletionStage. |
| `Lock` | Interface for locks. Provides methods like `lock()`, `lockInterruptibly()`, `tryLock()`, `tryLock(long timeout, TimeUnit unit)`, `unlock()`, and `newCondition()`. |
| `ReentrantLock` | Lock implementation that supports reentrancy. Provides methods like `isLocked()`, `isHeldByCurrentThread()`, `getHoldCount()`, `getQueueLength()`, `hasQueuedThreads()`, `hasQueuedThread()`, `hasWaiters()`, `getWaitQueueLength()`, and `isFair()`. |
| `ReadWriteLock` | Interface for read-write locks. Provides methods like `readLock()` and `writeLock()`. |
| `ReentrantReadWriteLock` | ReadWriteLock implementation that supports reentrancy. |
| `StampedLock` | Lock implementation that supports three modes: read, write, and optimistic read. |
| `Condition` | Interface for condition variables. Provides methods like `await()`, `await(long time, TimeUnit unit)`, `awaitNanos(long nanosTimeout)`, `awaitUninterruptibly()`, `awaitUntil(Date deadline)`, `signal()`, and `signalAll()`. |
| `Semaphore` | Counting semaphore. Provides methods like `acquire()`, `acquire(int permits)`, `acquireUninterruptibly()`, `tryAcquire()`, `tryAcquire(int permits)`, `tryAcquire(long timeout, TimeUnit unit)`, `tryAcquire(int permits, long timeout, TimeUnit unit)`, `release()`, `release(int permits)`, `availablePermits()`, `drainPermits()`, `reducePermits(int reduction)`, `isFair()`, `hasQueuedThreads()`, `getQueueLength()`, and `getQueuedThreads()`. |
| `CountDownLatch` | Synchronization aid that allows one or more threads to wait until a set of operations being performed in other threads completes. Provides methods like `await()`, `await(long timeout, TimeUnit unit)`, `countDown()`, `getCount()`, and `toString()`. |
| `CyclicBarrier` | Synchronization aid that allows a set of threads to all wait for each other to reach a common barrier point. Provides methods like `await()`, `await(long timeout, TimeUnit unit)`, `isBroken()`, `reset()`, and `getNumberWaiting()`. |
| `Phaser` | Synchronization aid that allows coordination of phases, or steps, among a set of threads. |
| `Exchanger<V>` | Synchronization aid that allows two threads to exchange objects. Provides methods like `exchange(V x)` and `exchange(V x, long timeout, TimeUnit unit)`. |
| `BlockingQueue<E>` | Interface for queues that support blocking operations. Provides methods like `put()`, `offer(E e, long timeout, TimeUnit unit)`, `take()`, `poll(long timeout, TimeUnit unit)`, `remainingCapacity()`, `remove(Object o)`, `contains(Object o)`, and `drainTo(Collection<? super E> c)`. |
| `ArrayBlockingQueue<E>` | Bounded blocking queue backed by an array. |
| `LinkedBlockingQueue<E>` | Optionally bounded blocking queue backed by linked nodes. |
| `PriorityBlockingQueue<E>` | Unbounded blocking queue that uses the same ordering rules as PriorityQueue. |
| `DelayQueue<E extends Delayed>` | Unbounded blocking queue of Delayed elements, in which an element can only be taken when its delay has expired. |
| `SynchronousQueue<E>` | Blocking queue that does not store elements. |
| `LinkedTransferQueue<E>` | Unbounded transfer queue based on linked nodes. |
| `TransferQueue<E>` | Interface for queues that support transfer operations. |
| `BlockingDeque<E>` | Interface for double-ended queues that support blocking operations. |
| `LinkedBlockingDeque<E>` | Unbounded blocking deque backed by linked nodes. |
| `ConcurrentMap<K,V>` | Interface for maps that support concurrent access. |
| `ConcurrentHashMap<K,V>` | Hash table implementation of ConcurrentMap. Provides methods like `putIfAbsent()`, `remove(Object key, Object value)`, `replace(K key, V oldValue, V newValue)`, `replace(K key, V value)`, `computeIfAbsent()`, `computeIfPresent()`, `compute()`, `merge()`, `forEach()`, `replaceAll()`, and `search()`. |
| `ConcurrentNavigableMap<K,V>` | Interface for concurrent navigable maps. |
| `ConcurrentSkipListMap<K,V>` | ConcurrentNavigableMap implementation based on a skip list. |
| `ConcurrentSkipListSet<E>` | ConcurrentNavigableSet implementation based on a ConcurrentSkipListMap. |
| `CopyOnWriteArrayList<E>` | Thread-safe variant of ArrayList in which all mutative operations are implemented by making a fresh copy of the underlying array. |
| `CopyOnWriteArraySet<E>` | Set implementation backed by a CopyOnWriteArrayList. |
| `ThreadLocal<T>` | Provides thread-local variables. Provides methods like `get()`, `set()`, `remove()`, and `initialValue()`. |
| `InheritableThreadLocal<T>` | ThreadLocal subclass that inherits values from parent threads. |
| `ThreadFactory` | Interface for creating threads. Requires implementation of the `newThread()` method. |
| `Executors` | Utility class for creating ExecutorService instances. Provides methods like `newFixedThreadPool()`, `newCachedThreadPool()`, `newSingleThreadExecutor()`, `newScheduledThreadPool()`, `newSingleThreadScheduledExecutor()`, `unconfigurableExecutorService()`, `unconfigurableScheduledExecutorService()`, `defaultThreadFactory()`, `privilegedThreadFactory()`, and `callable()`. |
| `TimeUnit` | Enumeration of time units. Provides constants like `NANOSECONDS`, `MICROSECONDS`, `MILLIS`, `SECONDS`, `MINUTES`, `HOURS`, and `DAYS`. Provides methods like `convert()`, `toMillis()`, `toSeconds()`, `toMinutes()`, `toHours()`, `toDays()`, `sleep()`, and `timedJoin()`. |
| `Callable<V>` | Interface for tasks that return a result. |
| `CompletionService<V>` | Service that decouples the production of new asynchronous tasks from the consumption of the results of completed tasks. |
| `ExecutorCompletionService<V>` | ExecutorService implementation of CompletionService. |
| `ForkJoinWorkerThread` | Thread managed by a ForkJoinPool. |
| `ForkJoinPool.ForkJoinWorkerThreadFactory` | Factory for ForkJoinWorkerThread instances. |
| `ForkJoinTask<V>` | Abstract base class for ForkJoinPool tasks. |
| `RecursiveTask<V>` | ForkJoinTask that returns a result. |
| `RecursiveAction` | ForkJoinTask that does not return a result. |
| `CountedCompleter<T>` | ForkJoinTask that maintains a completion count. |
| `DoubleAdder` | One or more variables that together maintain an initially zero double sum. |
| `DoubleAccumulator` | One or more variables that together maintain a running double value. |
| `LongAdder` | One or more variables that together maintain an initially zero long sum. |
| `LongAccumulator` | One or more variables that together maintain a running long value. |
| `Striped64` | Abstract base class for classes that maintain dynamic variables. |
| `ThreadLocalRandom` | Random number generator for a single thread. Provides methods like `current()`, `nextInt()`, `nextLong()`, `nextDouble()`, and `nextBoolean()`. |
| `AtomicBoolean` | Atomic boolean variable. Provides methods like `get()`, `set()`, `compareAndSet()`, and `weakCompareAndSet()`. |
| `AtomicInteger` | Atomic integer variable. Provides methods like `get()`, `set()`, `compareAndSet()`, `weakCompareAndSet()`, `getAndSet()`, `getAndIncrement()`, `getAndDecrement()`, `getAndAdd()`, `incrementAndGet()`, `decrementAndGet()`, `addAndGet()`, `getAndUpdate()`, `updateAndGet()`, `getAndAccumulate()`, and `accumulateAndGet()`. |
| `AtomicLong` | Atomic long variable. Similar to AtomicInteger but for long values. |
| `AtomicReference<V>` | Atomic reference variable. Provides methods like `get()`, `set()`, `compareAndSet()`, `weakCompareAndSet()`, `getAndSet()`, `getAndUpdate()`, `updateAndGet()`, `getAndAccumulate()`, and `accumulateAndGet()`. |
| `AtomicReferenceFieldUpdater<T,V>` | Reflection-based utility for atomically updating fields. |
| `AtomicIntegerFieldUpdater<T>` | Reflection-based utility for atomically updating integer fields. |
| `AtomicLongFieldUpdater<T>` | Reflection-based utility for atomically updating long fields. |
| `AtomicMarkableReference<V>` | Atomic reference variable with a mark bit. |
| `AtomicStampedReference<V>` | Atomic reference variable with an integer stamp. |
| `LongAdder` | One or more variables that together maintain an initially zero long sum. |
| `DoubleAdder` | One or more variables that together maintain an initially zero double sum. |
| `LongAccumulator` | One or more variables that together maintain a running long value. |
| `DoubleAccumulator` | One or more variables that together maintain a running double value. |

---
## java.sql Package

| Code | Description |
|------|-------------|
| `DriverManager` | Manages JDBC drivers. Provides methods like `getConnection()`, `getDrivers()`, `registerDriver()`, `deregisterDriver()`, and `setLoginTimeout()`. |
| `Connection` | Connection to a database. Provides methods like `createStatement()`, `prepareStatement()`, `prepareCall()`, `nativeSQL()`, `setAutoCommit()`, `commit()`, `rollback()`, `close()`, `isClosed()`, `getMetaData()`, `isValid()`, `setReadOnly()`, `isReadOnly()`, `setCatalog()`, `getCatalog()`, `setTransactionIsolation()`, `getTransactionIsolation()`, `getWarnings()`, `clearWarnings()`, `createArrayOf()`, `createBlob()`, `createClob()`, `createNClob()`, `createSQLXML()`, `createStruct()`, `getClientInfo()`, `setClientInfo()`, `getTypeMap()`, `setTypeMap()`, `setHoldability()`, `getHoldability()`, `setSavepoint()`, `releaseSavepoint()`, `rollback(Savepoint savepoint)`, and `createStatement(int resultSetType, int resultSetConcurrency)`. |
| `DatabaseMetaData` | Information about the database. Provides methods like `getURL()`, `getUserName()`, `getDatabaseProductName()`, `getDatabaseProductVersion()`, `getDriverName()`, `getDriverVersion()`, `getDriverMajorVersion()`, `getDriverMinorVersion()`, `isReadOnly()`, `supportsTransactions()`, `supportsSavepoints()`, `supportsResultSetType()`, `supportsResultSetConcurrency()`, `ownUpdatesAreVisible()`, `ownDeletesAreVisible()`, `ownInsertsAreVisible()`, `othersUpdatesAreVisible()`, `othersDeletesAreVisible()`, `othersInsertsAreVisible()`, `updatesAreDetected()`, `deletesAreDetected()`, `insertsAreDetected()`, `supportsBatchUpdates()`, `getDatabaseMajorVersion()`, `getDatabaseMinorVersion()`, `getJDBCMajorVersion()`, `getJDBCMinorVersion()`, `getMaxConnections()`, `getMaxTablesInSelect()`, `getMaxColumnsInTable()`, `getMaxRowSize()`, `doesMaxRowSizeIncludeBlobs()`, `getMaxStatementLength()`, `getMaxStatements()`, `getMaxLogicalLobSize()`, `getMaxColumnsInGroupBy()`, `getMaxColumnsInIndex()`, `getMaxColumnsInOrderBy()`, `getMaxUserNameLength()`, `getMaxProcedureNameLength()`, `getMaxCatalogNameLength()`, `getMaxTableNameLength()`, `getMaxTableNameLength()`, `getMaxSchemaNameLength()`, `getSQLKeywords()`, `getNumericFunctions()`, `getStringFunctions()`, `getSystemFunctions()`, `getTimeDateFunctions()`, `getSearchStringEscape()`, `getExtraNameCharacters()`, `supportsAlterTableWithAddColumn()`, `supportsAlterTableWithDropColumn()`, `supportsColumnAliasing()`, `nullPlusNonNullIsNull()`, `supportsConvert()`, `supportsConvert(int fromType, int toType)`, `supportsTableCorrelationNames()`, `supportsDifferentTableCorrelationNames()`, `supportsExpressionsInOrderBy()`, `supportsOrderByUnrelated()`, `supportsGroupBy()`, `supportsGroupByBeyondSelect()`, `supportsGroupByUnrelated()`, `supportsIntegrityEnhancementFacility()`, `supportsOuterJoins()`, `supportsFullOuterJoins()`, `supportsLimitedOuterJoins()`, `getSchemaTerm()`, `getProcedureTerm()`, `getCatalogTerm()`, `isCatalogAtStart()`, `getCatalogSeparator()`, `supportsSchemasInDataManipulation()`, `supportsSchemasInProcedureCalls()`, `supportsSchemasInTableDefinitions()`, `supportsSchemasInIndexDefinitions()`, `supportsSchemasInPrivilegeDefinitions()`, `supportsCatalogsInDataManipulation()`, `supportsCatalogsInProcedureCalls()`, `supportsCatalogsInTableDefinitions()`, `supportsCatalogsInIndexDefinitions()`, `supportsCatalogsInPrivilegeDefinitions()`, `supportsPositionedDelete()`, `supportsPositionedUpdate()`, `supportsSelectWithLimitOffset()`, `supportsVendorSpecificSyntax()`, `getIdentifierQuoteString()`, `getSQLStateType()`, `getLocatorsUpdateCopy()`, `supportsStatementPooling()`, `supportsStoredFunctionsUsingCallSyntax()`, `supportsStoredProcedures()`, `supportsTableCorrelationNames()`, `supportsTransactionIsolationLevel()`, `supportsTransactions()`, `supportsUnion()`, `supportsUnionAll()`, `getURL()`, `getUserName()`, and `getMaxLogicalLobSize()`. |
| `Statement` | SQL statement for executing queries. Provides methods like `executeQuery()`, `executeUpdate()`, `execute()`, `close()`, `isClosed()`, `getMaxFieldSize()`, `setMaxFieldSize()`, `getMaxRows()`, `setMaxRows()`, `setEscapeProcessing()`, `getEscapeProcessing()`, `setQueryTimeout()`, `getQueryTimeout()`, `cancel()`, `isPoolable()`, `setPoolable()`, `addBatch()`, `clearBatch()`, `executeBatch()`, `getConnection()`, `getFetchDirection()`, `setFetchDirection()`, `getFetchSize()`, `setFetchSize()`, `getResultSetConcurrency()`, `getResultSetType()`, `getResultSetHoldability()`, `isWrapperFor()`, and `unwrap()`. |
| `PreparedStatement` | Precompiled SQL statement. Provides methods like `executeQuery()`, `executeUpdate()`, `execute()`, `setNull()`, `setBoolean()`, `setByte()`, `setShort()`, `setInt()`, `setLong()`, `setFloat()`, `setDouble()`, `setBigDecimal()`, `setString()`, `setBytes()`, `setDate()`, `setTime()`, `setTimestamp()`, `setAsciiStream()`, `setUnicodeStream()`, `setBinaryStream()`, `setObject()`, `setCharacterStream()`, `setRef()`, `setBlob()`, `setClob()`, `setArray()`, `setURL()`, `setRowId()`, `setNString()`, `setNCharacterStream()`, `setNClob()`, `setNBlob()`, `addBatch()`, `clearBatch()`, `executeBatch()`, `getMetaData()`, `getParameterMetaData()`, `getResultSet()`, `getUpdateCount()`, `isClosed()`, `getWarnings()`, `clearWarnings()`, `setNull(int parameterIndex, int sqlType)`, `setBoolean(int parameterIndex, boolean x)`, etc. |
| `CallableStatement` | SQL stored procedure call. Provides methods like `registerOutParameter()`, `getBoolean()`, `getByte()`, `getShort()`, `getInt()`, `getLong()`, `getFloat()`, `getDouble()`, `getBigDecimal()`, `getString()`, `getBytes()`, `getDate()`, `getTime()`, `getTimestamp()`, `getObject()`, `getRef()`, `getBlob()`, `getClob()`, `getArray()`, `getURL()`, `getRowId()`, `getNString()`, `getNCharacterStream()`, `getNClob()`, `getNBlob()`, `wasNull()`, `getBigDecimal(int parameterIndex, int scale)`, `getBlob(int i)`, `getClob(int i)`, etc. |
| `ResultSet` | Table of data representing a database result set. Provides methods like `next()`, `close()`, `wasNull()`, `getString()`, `getBoolean()`, `getByte()`, `getShort()`, `getInt()`, `getLong()`, `getFloat()`, `getDouble()`, `getBigDecimal()`, `getBytes()`, `getDate()`, `getTime()`, `getTimestamp()`, `getAsciiStream()`, `getUnicodeStream()`, `getBinaryStream()`, `getObject()`, `getRef()`, `getBlob()`, `getClob()`, `getArray()`, `getURL()`, `getRowId()`, `getNString()`, `getNCharacterStream()`, `getNClob()`, `getNBlob()`, `getMetaData()`, `getStatement()`, `getWarnings()`, `clearWarnings()`, `getCursorName()`, `getFetchDirection()`, `setFetchDirection()`, `getFetchSize()`, `setFetchSize()`, `getType()`, `isFirst()`, `isLast()`, `isBeforeFirst()`, `isAfterLast()`, `first()`, `last()`, `absolute()`, `relative()`, `previous()`, `setInt()`, `setString()`, `setBoolean()`, `setByte()`, `setShort()`, `setLong()`, `setFloat()`, `setDouble()`, `setBigDecimal()`, `setBytes()`, `setDate()`, `setTime()`, `setTimestamp()`, `setAsciiStream()`, `setUnicodeStream()`, `setBinaryStream()`, `setObject()`, `setCharacterStream()`, `setRef()`, `setBlob()`, `setClob()`, `setArray()`, `setURL()`, `setRowId()`, `setNString()`, `setNCharacterStream()`, `setNClob()`, `setNBlob()`, `updateNull()`, `updateBoolean()`, `updateByte()`, `updateShort()`, `updateInt()`, `updateLong()`, `updateFloat()`, `updateDouble()`, `updateBigDecimal()`, `updateString()`, `updateBytes()`, `updateDate()`, `updateTime()`, `updateTimestamp()`, `updateAsciiStream()`, `updateUnicodeStream()`, `updateBinaryStream()`, `updateObject()`, `updateCharacterStream()`, `updateRef()`, `updateBlob()`, `updateClob()`, `updateArray()`, `updateURL()`, `updateRowId()`, `updateNString()`, `updateNCharacterStream()`, `updateNClob()`, `updateNBlob()`, `deleteRow()`, `refreshRow()`, `cancelRowUpdates()`, `insertRow()`, `updateRow()`, `moveToInsertRow()`, `moveToCurrentRow()`, `getHoldability()`, `isClosed()`, `setFetchSize()`, `getFetchSize()`, `getType()`, `getConcurrency()`, and `rowUpdated()`, `rowInserted()`, `rowDeleted()`. |
| `ResultSetMetaData` | Metadata about a ResultSet. Provides methods like `getColumnCount()`, `getColumnLabel()`, `getColumnName()`, `getSchemaName()`, `getCatalogName()`, `getTableName()`, `getColumnType()`, `getColumnTypeName()`, `getPrecision()`, `getScale()`, `isNullable()`, `isAutoIncrement()`, `isCaseSensitive()`, `isSearchable()`, `isCurrency()`, `isSigned()`, `getColumnDisplaySize()`, `getColumnClassName()`, `isReadOnly()`, `isWritable()`, `isDefinitelyWritable()`, and `unwrapper()`. |
| `ParameterMetaData` | Metadata about the parameters of a PreparedStatement. |
| `Savepoint` | Represents a savepoint in a database transaction. |
| `SQLWarning` | Warning issued by the database. |
| `SQLException` | Exception thrown for database access errors. Provides methods like `getSQLState()`, `getErrorCode()`, `getNextException()`, `setNextException()`, and `iterator()`. |
| `SQLNonTransientException` | Exception thrown for non-transient database access errors. |
| `SQLTransientException` | Exception thrown for transient database access errors. |
| `SQLRecoverableException` | Exception thrown for recoverable database access errors. |
| `SQLSyntaxErrorException` | Exception thrown for SQL syntax errors. |
| `SQLTimeoutException` | Exception thrown for database access timeouts. |
| `SQLTransactionRollbackException` | Exception thrown when a transaction is rolled back. |
| `SQLDataException` | Exception thrown for SQL data errors. |
| `SQLIntegrityConstraintViolationException` | Exception thrown for SQL integrity constraint violations. |
| `SQLInvalidAuthorizationSpecException` | Exception thrown for invalid authorization specifications. |
| `SQLNonTransientConnectionException` | Exception thrown for non-transient connection errors. |
| `SQLTransientConnectionException` | Exception thrown for transient connection errors. |
| `DataTruncation` | Exception thrown for data truncation errors. |
| `BatchUpdateException` | Exception thrown for batch update errors. |
| `Types` | Constants for SQL types. Provides constants like `NULL`, `SMALLINT`, `INTEGER`, `BIGINT`, `REAL`, `FLOAT`, `DOUBLE`, `DECIMAL`, `NUMERIC`, `CHAR`, `VARCHAR`, `LONGVARCHAR`, `DATE`, `TIME`, `TIMESTAMP`, `BINARY`, `VARBINARY`, `LONGVARBINARY`, `BOOLEAN`, `TINYINT`, `BIT`, `BLOB`, `CLOB`, `ARRAY`, `STRUCT`, `REF`, `DATALINK`, `JAVA_OBJECT`, `ROWID`, `NCHAR`, `NVARCHAR`, `LONGNVARCHAR`, `NCLOB`, `SQLXML`, `TIME_WITH_TIMEZONE`, `TIMESTAMP_WITH_TIMEZONE`, and `OTHER`. |
| `Driver` | Interface for JDBC drivers. |
| `DriverPropertyInfo` | Information about driver properties. |
| `SQLPermission` | Permission for SQL operations. |
| `RowId` | Represents a row ID. |
| `NClob` | Represents a SQL NCLob. |
| `SQLXML` | Represents a SQL XML. |
| `Struct` | Represents a SQL structured type. |
| `Array` | Represents a SQL array. |
| `Blob` | Represents a SQL Blob. |
| `Clob` | Represents a SQL Clob. |
| `Ref` | Represents a SQL Ref. |

---

## java.net Package

| Code | Description |
|------|-------------|
| `URL` | Represents a Uniform Resource Locator. Provides methods like `getProtocol()`, `getHost()`, `getPort()`, `getPath()`, `getFile()`, `getRef()`, `getQuery()`, `getAuthority()`, `getUserInfo()`, `openConnection()`, `openStream()`, `getContent()`, and `sameFile()`. |
| `URLConnection` | Abstract class for representing a connection to a URL. Provides methods like `connect()`, `getInputStream()`, `getOutputStream()`, `getContent()`, `getContentLength()`, `getContentType()`, `getContentEncoding()`, `getExpiration()`, `getDate()`, `getLastModified()`, `getHeaderField()`, `getHeaderFieldKey()`, `getHeaderFields()`, `setDoInput()`, `setDoOutput()`, `setIfModifiedSince()`, `setUseCaches()`, `setRequestProperty()`, `addRequestProperty()`, `getRequestProperty()`, `getRequestProperties()`, `setConnectTimeout()`, `getConnectTimeout()`, `setReadTimeout()`, and `getReadTimeout()`. |
| `HttpURLConnection` | URLConnection for HTTP. Provides methods like `setRequestMethod()`, `getRequestMethod()`, `getResponseCode()`, `getResponseMessage()`, `getErrorStream()`, `setInstanceFollowRedirects()`, `getInstanceFollowRedirects()`, `setFixedLengthStreamingMode()`, `getFixedLengthStreamingMode()`, `setChunkedStreamingMode()`, `getChunkedStreamingMode()`, `getHeaderFieldLong()`, `getHeaderFieldInt()`, `getHeaderFieldDate()`, `setIfModifiedSince()`, `getIfModifiedSince()`, `getPermission()`, and `disconnect()`. |
| `HttpsURLConnection` | URLConnection for HTTPS. |
| `JarURLConnection` | URLConnection for JAR files. |
| `FileNameMap` | Interface for mapping filenames to content types. |
| `MimeType` | Represents a MIME type. |
| `ContentHandler` | Interface for content handlers. |
| `ContentHandlerFactory` | Interface for content handler factories. |
| `URLEncoder` | Utility class for encoding URLs. Provides methods like `encode()`. |
| `URLDecoder` | Utility class for decoding URLs. Provides methods like `decode()`. |
| `URI` | Represents a Uniform Resource Identifier. Provides methods like `parse()`, `create()`, `resolve()`, `relativize()`, `normalize()`, `getScheme()`, `getSchemeSpecificPart()`, `getAuthority()`, `getUserInfo()`, `getHost()`, `getPort()`, `getPath()`, `getQuery()`, `getFragment()`, `getRawSchemeSpecificPart()`, `getRawAuthority()`, `getRawUserInfo()`, `getRawHost()`, `getRawPath()`, `getRawQuery()`, `getRawFragment()`, `isOpaque()`, `isAbsolute()`, `isPathAbsolute()`, and `compareTo()`. |
| `URISyntaxException` | Exception thrown for URI syntax errors. |
| `Socket` | Implements client sockets. Provides methods like `connect()`, `bind()`, `getInetAddress()`, `getPort()`, `getLocalAddress()`, `getLocalPort()`, `getInputStream()`, `getOutputStream()`, `setTcpNoDelay()`, `getTcpNoDelay()`, `setSoLinger()`, `getSoLinger()`, `setOOBInline()`, `getOOBInline()`, `setSendBufferSize()`, `getSendBufferSize()`, `setReceiveBufferSize()`, `getReceiveBufferSize()`, `setKeepAlive()`, `getKeepAlive()`, `setTrafficClass()`, `getTrafficClass()`, `setReuseAddress()`, `getReuseAddress()`, `close()`, `shutdownInput()`, `shutdownOutput()`, `isClosed()`, `isConnected()`, `isBound()`, `isInputShutdown()`, and `isOutputShutdown()`. |
| `ServerSocket` | Implements server sockets. Provides methods like `bind()`, `getInetAddress()`, `getLocalPort()`, `accept()`, `close()`, `isBound()`, `isClosed()`, `setSoTimeout()`, `getSoTimeout()`, `setReceiveBufferSize()`, `getReceiveBufferSize()`, `setReuseAddress()`, and `getReuseAddress()`. |
| `SocketAddress` | Interface for socket addresses. |
| `InetSocketAddress` | Socket address implementation for IP sockets. |
| `InetAddress` | Represents an IP address. Provides methods like `getByName()`, `getByAddress()`, `getAllByName()`, `getLocalHost()`, `getHostName()`, `getHostAddress()`, `getAddress()`, `getCanonicalHostName()`, `isMulticastAddress()`, `isAnyLocalAddress()`, `isLoopbackAddress()`, `isLinkLocalAddress()`, `isSiteLocalAddress()`, `isMCGlobal()`, `isMCNodeLocal()`, `isMCLinkLocal()`, `isMCSiteLocal()`, `isMCOrgLocal()`, `getByAddress(byte[] addr)`, and `hashCode()`. |
| `Inet4Address` | IP version 4 address implementation. |
| `Inet6Address` | IP version 6 address implementation. |
| `NetworkInterface` | Represents a network interface. Provides methods like `getByName()`, `getByIndex()`, `getByInetAddress()`, `getNetworkInterfaces()`, `getName()`, `getDisplayName()`, `getIndex()`, `getHardwareAddress()`, `getMTU()`, `isUp()`, `isLoopback()`, `isPointToPoint()`, `isVirtual()`, `supportsMulticast()`, `getInetAddresses()`, `getInterfaceAddresses()`, `isMulticast()`, and `getSubInterfaces()`. |
| `InterfaceAddress` | Represents a network interface address. |
| `SocketOptions` | Options for sockets. |
| `SocketImpl` | Implementation of sockets. |
| `ServerSocketFactory` | Factory for server sockets. |
| `SocketFactory` | Factory for sockets. |
| `Proxy` | Represents a proxy settings. Provides methods like `NO_PROXY`, `getDefault()`, `setDefault()`, and `getType()`. |
| `Proxy.Type` | Enumeration of proxy types. Provides constants like `DIRECT`, `HTTP`, and `SOCKS`. |
| `Authenticator` | Authenticator for HTTP connections. |
| `PasswordAuthentication` | Password authentication information. |
| `CookieHandler` | Interface for cookie handlers. |
| `CookieManager` | Cookie manager for HTTP state management. |
| `HttpCookie` | Represents an HTTP cookie. |
| `HttpUrlConnection` | Deprecated. Use HttpURLConnection instead. |
| `DatagramSocket` | Implements datagram sockets. Provides methods like `send()`, `receive()`, `connect()`, `disconnect()`, `isConnected()`, `isBound()`, `getLocalAddress()`, `getLocalPort()`, `getLocalSocketAddress()`, `getRemoteSocketAddress()`, `setBroadcast()`, `getBroadcast()`, `setSoTimeout()`, `getSoTimeout()`, `setSendBufferSize()`, `getSendBufferSize()`, `setReceiveBufferSize()`, `getReceiveBufferSize()`, and `close()`. |
| `DatagramPacket` | Represents a datagram packet. Provides methods like `getData()`, `getOffset()`, `getLength()`, `getPort()`, `getAddress()`, `getSocketAddress()`, `setData()`, `setOffset()`, `setLength()`, `setPort()`, `setAddress()`, and `setSocketAddress()`. |
| `MulticastSocket` | DatagramSocket for multicast. |
| `SocketPermission` | Permission for socket operations. |
| `NetPermission` | Permission for network operations. |

---

## java.math Package

| Code | Description |
|------|-------------|
| `BigInteger` | Immutable arbitrary-precision integer. Provides methods for arithmetic operations, bit manipulation, comparison, and conversion. |
| `BigInteger(String val)` | Constructs a BigInteger from a string representation. |
| `BigInteger(byte[] val)` | Constructs a BigInteger from a byte array. |
| `BigInteger.valueOf(long val)` | Returns a BigInteger with the specified value. |
| `BigInteger.TEN` | Constant for BigInteger value 10. |
| `BigInteger.ZERO` | Constant for BigInteger value 0. |
| `BigInteger.ONE` | Constant for BigInteger value 1. |
| `BigInteger.TWO` | Constant for BigInteger value 2. |
| `add(BigInteger val)` | Returns a BigInteger whose value is this + val. |
| `subtract(BigInteger val)` | Returns a BigInteger whose value is this - val. |
| `multiply(BigInteger val)` | Returns a BigInteger whose value is this * val. |
| `divide(BigInteger val)` | Returns a BigInteger whose value is this / val. |
| `divideAndRemainder(BigInteger val)` | Returns an array of two BigIntegers containing this / val followed by this % val. |
| `remainder(BigInteger val)` | Returns a BigInteger whose value is this % val. |
| `pow(int exponent)` | Returns a BigInteger whose value is this^exponent. |
| `negate()` | Returns a BigInteger whose value is -this. |
| `abs()` | Returns the absolute value of this BigInteger. |
| `mod(BigInteger m)` | Returns a BigInteger whose value is this mod m. |
| `modPow(BigInteger exponent, BigInteger m)` | Returns a BigInteger whose value is this^exponent mod m. |
| `modInverse(BigInteger m)` | Returns the modular multiplicative inverse of this BigInteger. |
| `gcd(BigInteger val)` | Returns the greatest common divisor of this BigInteger and val. |
| `compareTo(BigInteger val)` | Compares this BigInteger with the specified BigInteger. |
| `equals(Object x)` | Compares this BigInteger with the specified Object for equality. |
| `min(BigInteger val)` | Returns the minimum of this BigInteger and val. |
| `max(BigInteger val)` | Returns the maximum of this BigInteger and val. |
| `intValue()` | Returns the value of this BigInteger as an int. |
| `longValue()` | Returns the value of this BigInteger as a long. |
| `floatValue()` | Returns the value of this BigInteger as a float. |
| `doubleValue()` | Returns the value of this BigInteger as a double. |
| `toByteArray()` | Returns a byte array containing the two's-complement binary representation of this BigInteger. |
| `toString()` | Returns the decimal string representation of this BigInteger. |
| `toString(int radix)` | Returns the string representation of this BigInteger in the specified radix. |
| `BigDecimal` | Immutable arbitrary-precision decimal number. Provides methods for arithmetic operations, rounding, comparison, and conversion. |
| `BigDecimal(String val)` | Constructs a BigDecimal from a string representation. |
| `BigDecimal(double val)` | Constructs a BigDecimal from a double. |
| `BigDecimal(long val)` | Constructs a BigDecimal from a long. |
| `BigDecimal(BigInteger val)` | Constructs a BigDecimal from a BigInteger. |
| `BigDecimal.valueOf(long val)` | Returns a BigDecimal with the specified value. |
| `BigDecimal.valueOf(double val)` | Returns a BigDecimal with the specified value. |
| `BigDecimal.TEN` | Constant for BigDecimal value 10. |
| `BigDecimal.ZERO` | Constant for BigDecimal value 0. |
| `BigDecimal.ONE` | Constant for BigDecimal value 1. |
| `BigDecimal.ROUND_UP` | Rounding mode for rounding away from zero. |
| `BigDecimal.ROUND_DOWN` | Rounding mode for rounding towards zero. |
| `BigDecimal.ROUND_CEILING` | Rounding mode for rounding towards positive infinity. |
| `BigDecimal.ROUND_FLOOR` | Rounding mode for rounding towards negative infinity. |
| `BigDecimal.ROUND_HALF_UP` | Rounding mode for rounding towards nearest neighbor, or up if equidistant. |
| `BigDecimal.ROUND_HALF_DOWN` | Rounding mode for rounding towards nearest neighbor, or down if equidistant. |
| `BigDecimal.ROUND_HALF_EVEN` | Rounding mode for rounding towards nearest neighbor, or to even neighbor if equidistant. |
| `BigDecimal.ROUND_UNNECESSARY` | Rounding mode for asserting that no rounding is necessary. |
| `add(BigDecimal augend)` | Returns a BigDecimal whose value is this + augend. |
| `subtract(BigDecimal subtrahend)` | Returns a BigDecimal whose value is this - subtrahend. |
| `multiply(BigDecimal multiplicand)` | Returns a BigDecimal whose value is this * multiplicand. |
| `divide(BigDecimal divisor)` | Returns a BigDecimal whose value is this / divisor. |
| `divide(BigDecimal divisor, int scale, int roundingMode)` | Returns a BigDecimal whose value is this / divisor, with rounding according to the specified rounding mode. |
| `divideAndRemainder(BigDecimal divisor)` | Returns an array of two BigDecimals containing this / divisor followed by this % divisor. |
| `remainder(BigDecimal divisor)` | Returns a BigDecimal whose value is this % divisor. |
| `pow(int n)` | Returns a BigDecimal whose value is this^n. |
| `abs()` | Returns the absolute value of this BigDecimal. |
| `negate()` | Returns a BigDecimal whose value is -this. |
| `round(MathContext mc)` | Returns a BigDecimal rounded according to the specified MathContext. |
| `setScale(int newScale)` | Returns a BigDecimal with the specified scale. |
| `setScale(int newScale, int roundingMode)` | Returns a BigDecimal with the specified scale and rounding mode. |
| `compareTo(BigDecimal val)` | Compares this BigDecimal with the specified BigDecimal. |
| `equals(Object x)` | Compares this BigDecimal with the specified Object for equality. |
| `min(BigDecimal val)` | Returns the minimum of this BigDecimal and val. |
| `max(BigDecimal val)` | Returns the maximum of this BigDecimal and val. |
| `intValue()` | Returns the value of this BigDecimal as an int. |
| `longValue()` | Returns the value of this BigDecimal as a long. |
| `floatValue()` | Returns the value of this BigDecimal as a float. |
| `doubleValue()` | Returns the value of this BigDecimal as a double. |
| `toBigInteger()` | Returns the value of this BigDecimal as a BigInteger. |
| `toPlainString()` | Returns the string representation of this BigDecimal without an exponent. |
| `toString()` | Returns the string representation of this BigDecimal. |
| `MathContext` | Immutability and precision settings for BigDecimal operations. |
| `MathContext(int precision)` | Constructs a MathContext with the specified precision. |
| `MathContext(int precision, RoundingMode roundingMode)` | Constructs a MathContext with the specified precision and rounding mode. |
| `MathContext.DECIMAL128` | MathContext with 128-bit precision. |
| `MathContext.DECIMAL64` | MathContext with 64-bit precision. |
| `MathContext.DECIMAL32` | MathContext with 32-bit precision. |
| `MathContext.UNLIMITED` | MathContext with unlimited precision. |
| `RoundingMode` | Enumeration of rounding modes. Provides constants like `UP`, `DOWN`, `CEILING`, `FLOOR`, `HALF_UP`, `HALF_DOWN`, `HALF_EVEN`, and `UNNECESSARY`. |
| `BigIntegerMutabilityException` | Exception thrown for attempts to mutate BigIntegers. |

---

# Spring Framework Reference

---

## Core Spring Container

| Code | Description |
|------|-------------|
| `@Component` | Stereotype annotation for any Spring-managed component. |
| `@Repository` | Stereotype annotation for the persistence layer. |
| `@Service` | Stereotype annotation for the service layer. |
| `@Controller` | Stereotype annotation for the presentation layer (web controllers). |
| `@RestController` | Convenience annotation for creating RESTful controllers. Combines @Controller and @ResponseBody. |
| `@Configuration` | Indicates that a class declares one or more @Bean methods. |
| `@Bean` | Indicates that a method produces a bean to be managed by Spring. |
| `@Autowired` | Marks a constructor, field, setter method, or config method as to be autowired by Spring's dependency injection mechanism. |
| `@Qualifier` | Used to specify which bean to autowire when there are multiple candidates. |
| `@Primary` | Indicates that a bean should be given preference when multiple candidates are qualified to autowire a single-valued dependency. |
| `@Lazy` | Indicates whether a bean is to be lazily initialized. |
| `@DependsOn` | Specifies bean dependencies. |
| `@Scope` | Specifies the scope of a bean. |
| `@Value` | Used for injecting values into bean properties. |
| `@PropertySource` | Adds a property source to Spring's Environment. |
| `@PropertySources` | Allows for declaring multiple @PropertySource annotations. |
| `@ComponentScan` | Configures component scanning directives. |
| `@ComponentScans` | Allows for declaring multiple @ComponentScan annotations. |
| `@Import` | Imports additional configuration classes. |
| `@ImportResource` | Imports an XML configuration file. |
| `@Conditional` | Conditional bean creation based on some condition. |
| `@ConditionalOnClass` | Condition that only matches when the specified classes are on the classpath. |
| `@ConditionalOnMissingClass` | Condition that only matches when the specified classes are not on the classpath. |
| `@ConditionalOnBean` | Condition that only matches when the specified beans already exist. |
| `@ConditionalOnMissingBean` | Condition that only matches when the specified beans do not already exist. |
| `@ConditionalOnProperty` | Condition that only matches when the specified properties have specific values. |
| `@ConditionalOnResource` | Condition that only matches when the specified resources exist. |
| `@ConditionalOnWebApplication` | Condition that only matches when the application is a web application. |
| `@ConditionalOnNotWebApplication` | Condition that only matches when the application is not a web application. |
| `@ConditionalOnExpression` | Condition that only matches when the specified SpEL expression evaluates to true. |
| `@Order` | Defines the order of a bean. |
| `@Priority` | Indicates the priority of a bean. |
| `ApplicationContext` | Central interface for providing configuration for an application. |
| `ApplicationContext.getBean(String name)` | Retrieves the bean with the specified name. |
| `ApplicationContext.getBean(Class<T> requiredType)` | Retrieves the bean of the specified type. |
| `ApplicationContext.getBean(String name, Class<T> requiredType)` | Retrieves the bean with the specified name and type. |
| `ApplicationContext.getBeansOfType(Class<T> type)` | Retrieves all beans of the specified type. |
| `ApplicationContext.getBeansWithAnnotation(Class<? extends Annotation> annotationType)` | Retrieves all beans with the specified annotation. |
| `ApplicationContext.containsBean(String name)` | Checks if a bean with the specified name exists. |
| `ApplicationContext.isSingleton(String name)` | Checks if the bean with the specified name is a singleton. |
| `ApplicationContext.isPrototype(String name)` | Checks if the bean with the specified name is a prototype. |
| `ApplicationContext.isTypeMatch(String name, Class<?> targetType)` | Checks if the bean with the specified name matches the specified type. |
| `ApplicationContext.getClassLoader()` | Returns the class loader used by the application context. |
| `ApplicationContext.getParent()` | Returns the parent application context. |
| `ApplicationContext.getDisplayName()` | Returns the display name of the application context. |
| `ApplicationContext.getId()` | Returns the unique id of the application context. |
| `ApplicationContext.getApplicationName()` | Returns the application name. |
| `ApplicationContext.getBeansWithAnnotation(Class<? extends Annotation> annotationType)` | Retrieves all beans with the specified annotation. |
| `ApplicationContext.getBeanDefinitionNames()` | Returns the names of all beans defined in the application context. |
| `ApplicationContext.getBeanDefinitionCount()` | Returns the number of beans defined in the application context. |
| `ApplicationContext.refresh()` | Refreshes the application context. |
| `ApplicationContext.close()` | Closes the application context. |
| `ApplicationContext.registerShutdownHook()` | Registers a shutdown hook for the application context. |
| `AnnotationConfigApplicationContext` | Standalone application context for annotation-based configuration. |
| `ClassPathXmlApplicationContext` | Standalone XML application context for standalone XML configuration files. |
| `FileSystemXmlApplicationContext` | Standalone XML application context for file system XML configuration files. |
| `WebApplicationContext` | Interface for application contexts that run in a web environment. |
| `XmlWebApplicationContext` | WebApplicationContext implementation for XML configuration files. |
| `AnnotationConfigWebApplicationContext` | WebApplicationContext implementation for annotation-based configuration. |
| `BeanFactory` | Root interface for accessing a Spring bean container. |
| `BeanFactory.getBean(String name)` | Retrieves the bean with the specified name. |
| `BeanFactory.getBean(Class<T> requiredType)` | Retrieves the bean of the specified type. |
| `BeanFactory.getBean(String name, Class<T> requiredType)` | Retrieves the bean with the specified name and type. |
| `BeanFactory.containsBean(String name)` | Checks if a bean with the specified name exists. |
| `BeanFactory.isSingleton(String name)` | Checks if the bean with the specified name is a singleton. |
| `BeanFactory.isPrototype(String name)` | Checks if the bean with the specified name is a prototype. |
| `BeanFactory.isTypeMatch(String name, Class<?> targetType)` | Checks if the bean with the specified name matches the specified type. |
| `BeanFactory.getAliases(String name)` | Returns the aliases for the specified bean name. |
| `ListableBeanFactory` | Interface for bean factories that can enumerate all their beans. |
| `ListableBeanFactory.getBeanNamesForType(Class<?> type)` | Returns the names of all beans of the specified type. |
| `ListableBeanFactory.getBeanNamesForAnnotation(Class<? extends Annotation> annotationType)` | Returns the names of all beans with the specified annotation. |
| `ListableBeanFactory.getBeansOfType(Class<T> type)` | Returns all beans of the specified type. |
| `ListableBeanFactory.getBeansWithAnnotation(Class<? extends Annotation> annotationType)` | Returns all beans with the specified annotation. |
| `HierarchicalBeanFactory` | Interface for bean factories that can be part of a hierarchy. |
| `HierarchicalBeanFactory.getParentBeanFactory()` | Returns the parent bean factory. |
| `ConfigurableBeanFactory` | Interface for configurable bean factories. |
| `ConfigurableBeanFactory.setBeanClassLoader(ClassLoader beanClassLoader)` | Sets the class loader for the bean factory. |
| `ConfigurableBeanFactory.addBeanPostProcessor(BeanPostProcessor beanPostProcessor)` | Adds a bean post processor. |
| `ConfigurableBeanFactory.addPropertyEditorRegistrar(PropertyEditorRegistrar registrar)` | Adds a property editor registrar. |
| `ConfigurableBeanFactory.setParentBeanFactory(BeanFactory parentBeanFactory)` | Sets the parent bean factory. |
| `ConfigurableBeanFactory.setBeanExpressionResolver(BeanExpressionResolver resolver)` | Sets the bean expression resolver. |
| `ConfigurableBeanFactory.setBeanExpressionContext(BeanExpressionContext beanExpressionContext)` | Sets the bean expression context. |
| `AutowireCapableBeanFactory` | Interface for bean factories that can autowire beans. |
| `AutowireCapableBeanFactory.autowireBean(Object existingBean)` | Autowires the specified bean. |
| `AutowireCapableBeanFactory.autowireBeanProperties(Object existingBean, int autowireMode, boolean dependencyCheck)` | Autowires the specified bean properties. |
| `AutowireCapableBeanFactory.autowire(Object bean, int autowireMode, boolean dependencyCheck)` | Autowires the specified bean. |
| `AutowireCapableBeanFactory.createBean(Class<T> beanClass)` | Creates a bean of the specified class. |
| `BeanDefinition` | Interface for bean definitions. |
| `BeanDefinition.getBeanClassName()` | Returns the name of the bean class. |
| `BeanDefinition.getScope()` | Returns the scope of the bean. |
| `BeanDefinition.isSingleton()` | Checks if the bean is a singleton. |
| `BeanDefinition.isPrototype()` | Checks if the bean is a prototype. |
| `BeanDefinition.isLazyInit()` | Checks if the bean is lazily initialized. |
| `BeanDefinition.getDependsOn()` | Returns the names of the beans that this bean depends on. |
| `BeanDefinition.getPropertyValues()` | Returns the property values for the bean. |
| `BeanDefinition.getConstructorArgumentValues()` | Returns the constructor argument values for the bean. |
| `BeanDefinition.setBeanClassName(String beanClassName)` | Sets the name of the bean class. |
| `BeanDefinition.setScope(String scope)` | Sets the scope of the bean. |
| `BeanDefinition.setLazyInit(boolean lazyInit)` | Sets whether the bean is lazily initialized. |
| `BeanDefinition.setDependsOn(String... dependsOn)` | Sets the names of the beans that this bean depends on. |
| `BeanDefinition.setPrimary(boolean primary)` | Sets whether the bean is primary. |
| `BeanDefinition.setAbstract(boolean abstractFlag)` | Sets whether the bean is abstract. |
| `GenericBeanDefinition` | Generic BeanDefinition implementation. |
| `RootBeanDefinition` | Root BeanDefinition implementation. |
| `ChildBeanDefinition` | Child BeanDefinition implementation. |
| `AbstractBeanDefinition` | Abstract BeanDefinition implementation. |
| `BeanDefinitionReader` | Interface for reading bean definitions. |
| `BeanDefinitionRegistry` | Interface for registering bean definitions. |
| `BeanDefinitionRegistry.registerBeanDefinition(String beanName, BeanDefinition beanDefinition)` | Registers a bean definition. |
| `BeanDefinitionRegistry.removeBeanDefinition(String beanName)` | Removes a bean definition. |
| `BeanDefinitionRegistry.getBeanDefinition(String beanName)` | Retrieves a bean definition. |
| `BeanDefinitionRegistry.containsBeanDefinition(String beanName)` | Checks if a bean definition exists. |
| `BeanDefinitionRegistry.getBeanDefinitionNames()` | Returns the names of all bean definitions. |
| `BeanDefinitionRegistry.getBeanDefinitionCount()` | Returns the number of bean definitions. |
| `DefaultListableBeanFactory` | Default implementation of ListableBeanFactory and BeanDefinitionRegistry. |
| `BeanExpressionResolver` | Interface for resolving bean expressions. |
| `BeanExpressionContext` | Context for resolving bean expressions. |
| `BeanPostProcessor` | Interface for post-processing beans. |
| `BeanPostProcessor.postProcessBeforeInitialization(Object bean, String beanName)` | Post-processes the specified bean before initialization. |
| `BeanPostProcessor.postProcessAfterInitialization(Object bean, String beanName)` | Post-processes the specified bean after initialization. |
| `BeanFactoryPostProcessor` | Interface for post-processing bean factories. |
| `BeanFactoryPostProcessor.postProcessBeanFactory(ConfigurableListableBeanFactory beanFactory)` | Post-processes the specified bean factory. |
| `PropertyEditorRegistrar` | Interface for registering property editors. |
| `PropertyEditorRegistrar.registerCustomEditors(PropertyEditorRegistry registry)` | Registers custom property editors. |
| `InstantiationAwareBeanPostProcessor` | Interface for bean post processors that are aware of instantiation. |
| `SmartInstantiationAwareBeanPostProcessor` | Interface for smart instantiation-aware bean post processors. |
| `MergedBeanDefinitionPostProcessor` | Interface for post-processing merged bean definitions. |

---
## Spring Data Access

| Code | Description |
|------|-------------|
| `@Repository` | Stereotype annotation for the persistence layer. |
| `@RepositoryDefinition` | Meta-annotation for custom repository annotations. |
| `JdbcTemplate` | Class for executing SQL queries, updates, and stored procedure calls. |
| `JdbcTemplate.query(String sql, RowCallbackHandler rch)` | Executes the specified SQL query and processes the ResultSet with the specified RowCallbackHandler. |
| `JdbcTemplate.query(String sql, ResultSetExtractor<T> rse)` | Executes the specified SQL query and extracts the results with the specified ResultSetExtractor. |
| `JdbcTemplate.queryForObject(String sql, RowMapper<T> rowMapper)` | Executes the specified SQL query and maps the results to an object using the specified RowMapper. |
| `JdbcTemplate.queryForList(String sql, RowMapper<T> rowMapper)` | Executes the specified SQL query and maps the results to a list using the specified RowMapper. |
| `JdbcTemplate.queryForMap(String sql)` | Executes the specified SQL query and returns a Map of column name to value. |
| `JdbcTemplate.update(String sql)` | Executes the specified SQL update, insert, or delete. |
| `JdbcTemplate.update(String sql, Object... args)` | Executes the specified SQL update, insert, or delete with the specified arguments. |
| `JdbcTemplate.batchUpdate(String sql, BatchPreparedStatementSetter pss)` | Executes a batch update using the specified PreparedStatementSetter. |
| `JdbcTemplate.execute(ConnectionCallback<T> action)` | Executes a connection callback. |
| `JdbcTemplate.execute(StatementCallback<T> action)` | Executes a statement callback. |
| `JdbcTemplate.execute(PreparedStatementCallback<T> action)` | Executes a prepared statement callback. |
| `NamedParameterJdbcTemplate` | Class for executing SQL queries, updates, and stored procedure calls with named parameters. |
| `NamedParameterJdbcTemplate.query(String sql, Map<String, ?> paramMap, RowMapper<T> rowMapper)` | Executes the specified SQL query with the specified named parameters and maps the results using the specified RowMapper. |
| `NamedParameterJdbcTemplate.update(String sql, Map<String, ?> paramMap)` | Executes the specified SQL update with the specified named parameters. |
| `RowMapper<T>` | Interface for mapping rows of a ResultSet to objects. |
| `RowMapper<T>.mapRow(ResultSet rs, int rowNum)` | Maps the current row of the ResultSet to an object. |
| `ResultSetExtractor<T>` | Interface for extracting results from a ResultSet. |
| `ResultSetExtractor<T>.extractData(ResultSet rs)` | Extracts data from the ResultSet. |
| `RowCallbackHandler` | Interface for processing rows of a ResultSet. |
| `RowCallbackHandler.processRow(ResultSet rs)` | Processes the current row of the ResultSet. |
| `SqlParameterValue` | Class for representing a SQL parameter value. |
| `SqlLobValue` | Class for representing a SQL LOB value. |
| `SqlTypeValue` | Class for representing a SQL type value. |
| `DataSourceUtils` | Utility class for DataSource operations. |
| `DataSourceUtils.getConnection(DataSource dataSource)` | Gets a connection from the specified DataSource. |
| `DataSourceUtils.releaseConnection(Connection con, DataSource dataSource)` | Releases the specified connection back to the DataSource. |
| `TransactionTemplate` | Class for programmatic transaction management. |
| `TransactionTemplate.execute(TransactionCallback<T> action)` | Executes the specified callback within a transaction. |
| `TransactionCallback<T>` | Interface for transaction callbacks. |
| `TransactionCallback<T>.doInTransaction(TransactionStatus status)` | Executes the callback within a transaction. |
| `PlatformTransactionManager` | Interface for transaction managers. |
| `PlatformTransactionManager.getTransaction(TransactionDefinition definition)` | Gets a transaction for the specified definition. |
| `PlatformTransactionManager.commit(TransactionStatus status)` | Commits the specified transaction. |
| `PlatformTransactionManager.rollback(TransactionStatus status)` | Rolls back the specified transaction. |
| `TransactionDefinition` | Interface for transaction definitions. |
| `TransactionDefinition.PROPAGATION_REQUIRED` | Propagation behavior for required transactions. |
| `TransactionDefinition.PROPAGATION_REQUIRES_NEW` | Propagation behavior for requires new transactions. |
| `TransactionDefinition.PROPAGATION_NESTED` | Propagation behavior for nested transactions. |
| `TransactionDefinition.PROPAGATION_MANDATORY` | Propagation behavior for mandatory transactions. |
| `TransactionDefinition.PROPAGATION_NEVER` | Propagation behavior for never transactions. |
| `TransactionDefinition.PROPAGATION_NOT_SUPPORTED` | Propagation behavior for not supported transactions. |
| `TransactionDefinition.PROPAGATION_SUPPORTS` | Propagation behavior for supports transactions. |
| `TransactionDefinition.ISOLATION_DEFAULT` | Isolation level for default transactions. |
| `TransactionDefinition.ISOLATION_READ_UNCOMMITTED` | Isolation level for read uncommitted transactions. |
| `TransactionDefinition.ISOLATION_READ_COMMITTED` | Isolation level for read committed transactions. |
| `TransactionDefinition.ISOLATION_REPEATABLE_READ` | Isolation level for repeatable read transactions. |
| `TransactionDefinition.ISOLATION_SERIALIZABLE` | Isolation level for serializable transactions. |
| `TransactionDefinition.TIMEOUT_DEFAULT` | Timeout for default transactions. |
| `TransactionStatus` | Interface for transaction status. |
| `TransactionStatus.isCompleted()` | Checks if the transaction is completed. |
| `TransactionStatus.isRollbackOnly()` | Checks if the transaction is marked as rollback-only. |
| `TransactionStatus.isNewTransaction()` | Checks if the transaction is new. |
| `TransactionStatus.hasSavepoint()` | Checks if the transaction has a savepoint. |
| `TransactionSynchronization` | Interface for transaction synchronization. |
| `TransactionSynchronization.beforeCommit(boolean readOnly)` | Called before the transaction is committed. |
| `TransactionSynchronization.beforeCompletion()` | Called before the transaction is completed. |
| `TransactionSynchronization.afterCommit()` | Called after the transaction is committed. |
| `TransactionSynchronization.afterCompletion(int status)` | Called after the transaction is completed. |
| `DataSourceTransactionManager` | PlatformTransactionManager implementation for DataSource. |
| `JpaTransactionManager` | PlatformTransactionManager implementation for JPA. |
| `HibernateTransactionManager` | PlatformTransactionManager implementation for Hibernate. |
| `JtaTransactionManager` | PlatformTransactionManager implementation for JTA. |

---
## Spring Web MVC

| Code | Description |
|------|-------------|
| `@Controller` | Stereotype annotation for the presentation layer (web controllers). |
| `@RestController` | Convenience annotation for creating RESTful controllers. Combines @Controller and @ResponseBody. |
| `@RequestMapping` | Annotation for mapping web requests to handler methods. |
| `@RequestMapping(value = "/path", method = RequestMethod.GET)` | Maps GET requests for /path to the annotated method. |
| `@RequestMapping(value = "/path", method = {RequestMethod.GET, RequestMethod.POST})` | Maps GET and POST requests for /path to the annotated method. |
| `@GetMapping` | Shortcut for @RequestMapping with method = RequestMethod.GET. |
| `@PostMapping` | Shortcut for @RequestMapping with method = RequestMethod.POST. |
| `@PutMapping` | Shortcut for @RequestMapping with method = RequestMethod.PUT. |
| `@DeleteMapping` | Shortcut for @RequestMapping with method = RequestMethod.DELETE. |
| `@PatchMapping` | Shortcut for @RequestMapping with method = RequestMethod.PATCH. |
| `@RequestParam` | Binds a method parameter to a request parameter. |
| `@RequestParam(value = "name", required = false, defaultValue = "default")` | Binds the request parameter name to the method parameter. |
| `@PathVariable` | Binds a method parameter to a URI template variable. |
| `@PathVariable(value = "name")` | Binds the URI template variable name to the method parameter. |
| `@RequestBody` | Binds a method parameter to the body of the web request. |
| `@ResponseBody` | Indicates that the return value of a method should be bound to the web response body. |
| `@ResponseStatus` | Configures the HTTP status code for the response. |
| `@ResponseStatus(value = HttpStatus.OK)` | Sets the HTTP status code to 200 (OK). |
| `@ExceptionHandler` | Annotation for exception handling methods. |
| `@ExceptionHandler({IOException.class, SQLException.class})` | Handles exceptions of the specified types. |
| `@ModelAttribute` | Binds a method parameter or return value to a model attribute. |
| `@SessionAttribute` | Binds a method parameter to a session attribute. |
| `@SessionAttributes` | Specifies the session attributes to use in the controller. |
| `@InitBinder` | Annotation for methods that initialize the WebDataBinder. |
| `@CookieValue` | Binds a method parameter to the value of an HTTP cookie. |
| `@RequestHeader` | Binds a method parameter to a request header. |
| `DispatcherServlet` | Front controller for Spring Web MVC. |
| `DispatcherServlet.setContextConfigLocation(String configLocation)` | Sets the context configuration location. |
| `DispatcherServlet.setNamespace(String namespace)` | Sets the namespace for the DispatcherServlet. |
| `DispatcherServlet.setServletName(String servletName)` | Sets the servlet name. |
| `DispatcherServlet.setDispatchOptionsRequest(boolean dispatchOptionsRequest)` | Sets whether to dispatch OPTIONS requests. |
| `DispatcherServlet.setDispatchTraceRequest(boolean dispatchTraceRequest)` | Sets whether to dispatch TRACE requests. |
| `DispatcherServlet.setThrowExceptionIfNoHandlerFound(boolean throwExceptionIfNoHandlerFound)` | Sets whether to throw an exception if no handler is found. |
| `WebApplicationContext` | Interface for application contexts that run in a web environment. |
| `WebApplicationContextUtils` | Utility class for WebApplicationContext operations. |
| `RequestMappingHandlerMapping` | Implementation of HandlerMapping for @RequestMapping methods. |
| `RequestMappingHandlerAdapter` | Implementation of HandlerAdapter for @RequestMapping methods. |
| `HandlerMapping` | Interface for mapping requests to handlers. |
| `HandlerMapping.getHandler(HttpServletRequest request)` | Returns the handler for the specified request. |
| `HandlerAdapter` | Interface for adapting handlers. |
| `HandlerAdapter.supports(Object handler)` | Checks if the specified handler is supported. |
| `HandlerAdapter.handle(HttpServletRequest request, HttpServletResponse response, Object handler)` | Handles the specified request with the specified handler. |
| `HandlerInterceptor` | Interface for handler interceptors. |
| `HandlerInterceptor.preHandle(HttpServletRequest request, HttpServletResponse response, Object handler)` | Called before the handler is executed. |
| `HandlerInterceptor.postHandle(HttpServletRequest request, HttpServletResponse response, Object handler, ModelAndView modelAndView)` | Called after the handler is executed. |
| `HandlerInterceptor.afterCompletion(HttpServletRequest request, HttpServletResponse response, Object handler, Exception ex)` | Called after the request is completed. |
| `WebRequestInterceptor` | Interface for web request interceptors. |
| `AsyncHandlerInterceptor` | Interface for asynchronous handler interceptors. |
| `ViewResolver` | Interface for resolving views. |
| `ViewResolver.resolveViewName(String viewName, Locale locale)` | Resolves the specified view name to a View. |
| `View` | Interface for views. |
| `View.render(Map<String, ?> model, HttpServletRequest request, HttpServletResponse response)` | Renders the view. |
| `ModelAndView` | Container for a model and a view. |
| `ModelAndView(String viewName)` | Creates a ModelAndView with the specified view name. |
| `ModelAndView(String viewName, Map<String, ?> model)` | Creates a ModelAndView with the specified view name and model. |
| `ModelAndView(String viewName, String modelName, Object modelObject)` | Creates a ModelAndView with the specified view name, model name, and model object. |
| `ModelAndView.addObject(String attributeName, Object attributeValue)` | Adds an object to the model. |
| `ModelAndView.addAllObjects(Map<String, ?> modelMap)` | Adds all objects from the specified map to the model. |
| `ModelAndView.setViewName(String viewName)` | Sets the view name. |
| `ModelAndView.setView(View view)` | Sets the view. |
| `ModelAndView.getModel()` | Returns the model. |
| `ModelAndView.getModelMap()` | Returns the model as a ModelMap. |
| `ModelAndView.getViewName()` | Returns the view name. |
| `ModelAndView.getView()` | Returns the view. |
| `RedirectAttributes` | Interface for redirect attributes. |
| `RedirectAttributes.addAttribute(String attributeName, Object attributeValue)` | Adds an attribute to be included in the redirect URL. |
| `RedirectAttributes.addFlashAttribute(String attributeName, Object attributeValue)` | Adds a flash attribute to be included in the redirect. |
| `FlashMap` | Class for managing flash attributes. |
| `BindingResult` | Interface for binding results. |
| `BindingResult.reject(String errorCode)` | Rejects the current object with the specified error code. |
| `BindingResult.reject(String errorCode, String defaultMessage)` | Rejects the current object with the specified error code and default message. |
| `BindingResult.rejectValue(String field, String errorCode)` | Rejects the specified field with the specified error code. |
| `BindingResult.rejectValue(String field, String errorCode, String defaultMessage)` | Rejects the specified field with the specified error code and default message. |
| `BindingResult.addError(ObjectError error)` | Adds an object error. |
| `BindingResult.addError(FieldError error)` | Adds a field error. |
| `BindingResult.hasErrors()` | Checks if there are any errors. |
| `BindingResult.getAllErrors()` | Returns all errors. |
| `BindingResult.getFieldErrors()` | Returns all field errors. |
| `BindingResult.getGlobalErrors()` | Returns all global errors. |
| `BindingResult.getErrorCount()` | Returns the number of errors. |
| `DataBinder` | Class for binding data to objects. |
| `DataBinder.bind(Object target)` | Binds data to the specified target object. |
| `DataBinder.setBindingResult(BindingResult bindingResult)` | Sets the binding result. |
| `WebDataBinder` | DataBinder subclass for web binding. |
| `ServletRequestDataBinder` | WebDataBinder subclass for servlet request binding. |
| `Validator` | Interface for validators. |
| `Validator.supports(Class<?> clazz)` | Checks if the validator supports the specified class. |
| `Validator.validate(Object target, Errors errors)` | Validates the specified target object. |
| `SmartValidator` | Interface for smart validators. |
| `Errors` | Interface for errors. |
| `ObjectError` | Class for object errors. |
| `FieldError` | Class for field errors. |
| `HttpMessageConverter<T>` | Interface for HTTP message converters. |
| `HttpMessageConverter<T>.canRead(Class<?> clazz, MediaType mediaType)` | Checks if the converter can read the specified class and media type. |
| `HttpMessageConverter<T>.canWrite(Class<?> clazz, MediaType mediaType)` | Checks if the converter can write the specified class and media type. |
| `HttpMessageConverter<T>.read(Class<? extends T> clazz, HttpInputMessage inputMessage)` | Reads the specified class from the input message. |
| `HttpMessageConverter<T>.write(T t, MediaType contentType, HttpOutputMessage outputMessage)` | Writes the specified object to the output message. |
| `MappingJackson2HttpMessageConverter` | HttpMessageConverter implementation for Jackson 2. |
| `StringHttpMessageConverter` | HttpMessageConverter implementation for strings. |
| `FormHttpMessageConverter` | HttpMessageConverter implementation for form data. |
| `MultipartResolver` | Interface for multipart resolvers. |
| `CommonsMultipartResolver` | MultipartResolver implementation for Commons FileUpload. |
| `StandardServletMultipartResolver` | MultipartResolver implementation for Servlet 3.0. |
| `MultipartFile` | Interface for multipart files. |
| `CommonsMultipartFile` | MultipartFile implementation for Commons FileUpload. |
| `MockMultipartFile` | Mock implementation of MultipartFile. |
| `LocaleResolver` | Interface for locale resolvers. |
| `LocaleContextResolver` | Interface for locale context resolvers. |
| `AcceptHeaderLocaleResolver` | LocaleResolver implementation for Accept-Header. |
| `CookieLocaleResolver` | LocaleResolver implementation for cookies. |
| `SessionLocaleResolver` | LocaleResolver implementation for sessions. |
| `FixedLocaleResolver` | LocaleResolver implementation for a fixed locale. |
| `ThemeResolver` | Interface for theme resolvers. |
| `FixedThemeResolver` | ThemeResolver implementation for a fixed theme. |
| `SessionThemeResolver` | ThemeResolver implementation for sessions. |
| `CookieThemeResolver` | ThemeResolver implementation for cookies. |
| `RequestContextHolder` | Holder for the current request context. |
| `RequestContextHolder.setRequestAttributes(RequestAttributes requestAttributes)` | Sets the current request attributes. |
| `RequestContextHolder.getRequestAttributes()` | Returns the current request attributes. |
| `RequestContextHolder.resetRequestAttributes()` | Resets the current request attributes. |
| `RequestAttributes` | Interface for request attributes. |
| `ServletRequestAttributes` | RequestAttributes implementation for servlet requests. |
| `RequestContext` | Class for the current request context. |

---
## Spring WebFlux

| Code | Description |
|------|-------------|
| `@Controller` | Stereotype annotation for the presentation layer (web controllers). |
| `@RestController` | Convenience annotation for creating RESTful controllers. |
| `@RequestMapping` | Annotation for mapping web requests to handler methods. |
| `@GetMapping` | Shortcut for @RequestMapping with method = RequestMethod.GET. |
| `@PostMapping` | Shortcut for @RequestMapping with method = RequestMethod.POST. |
| `@PutMapping` | Shortcut for @RequestMapping with method = RequestMethod.PUT. |
| `@DeleteMapping` | Shortcut for @RequestMapping with method = RequestMethod.DELETE. |
| `@PatchMapping` | Shortcut for @RequestMapping with method = RequestMethod.PATCH. |
| `@RequestParam` | Binds a method parameter to a request parameter. |
| `@PathVariable` | Binds a method parameter to a URI template variable. |
| `@RequestBody` | Binds a method parameter to the body of the web request. |
| `@ResponseBody` | Indicates that the return value of a method should be bound to the web response body. |
| `@ResponseStatus` | Configures the HTTP status code for the response. |
| `@ExceptionHandler` | Annotation for exception handling methods. |
| `WebClient` | Non-blocking, reactive client for making HTTP requests. |
| `WebClient.create()` | Creates a new WebClient. |
| `WebClient.create(String baseUrl)` | Creates a new WebClient with the specified base URL. |
| `WebClient.Builder` | Builder for WebClient. |
| `WebClient.Builder.baseUrl(String baseUrl)` | Sets the base URL for the WebClient. |
| `WebClient.Builder.defaultHeader(String headerName, String... headerValues)` | Sets default headers for the WebClient. |
| `WebClient.Builder.defaultCookie(String name, String value)` | Sets default cookies for the WebClient. |
| `WebClient.Builder.defaultUriVariables(Map<String, ?> uriVariables)` | Sets default URI variables for the WebClient. |
| `WebClient.Builder.build()` | Builds the WebClient. |
| `WebClient.get()` | Prepares a GET request. |
| `WebClient.post()` | Prepares a POST request. |
| `WebClient.put()` | Prepares a PUT request. |
| `WebClient.delete()` | Prepares a DELETE request. |
| `WebClient.head()` | Prepares a HEAD request. |
| `WebClient.patch()` | Prepares a PATCH request. |
| `WebClient.options()` | Prepares an OPTIONS request. |
| `WebClient.RequestBodySpec` | Interface for specifying the request body. |
| `WebClient.RequestBodySpec.bodyValue(Object body)` | Sets the request body. |
| `WebClient.RequestBodySpec.body(BodyInserter<?, ?> inserter)` | Sets the request body inserter. |
| `WebClient.RequestHeadersSpec` | Interface for specifying request headers. |
| `WebClient.RequestHeadersSpec.header(String headerName, String... headerValues)` | Sets request headers. |
| `WebClient.RequestHeadersSpec.cookie(String name, String value)` | Sets request cookies. |
| `WebClient.RequestHeadersSpec.uri(String uri)` | Sets the request URI. |
| `WebClient.RequestHeadersSpec.uri(URI uri)` | Sets the request URI. |
| `WebClient.RequestHeadersSpec.uri(Function<UriSpec, URI> uriFunction)` | Sets the request URI using a function. |
| `WebClient.RequestHeadersSpec.retrieve()` | Retrieves the response. |
| `WebClient.RequestHeadersSpec.exchange()` | Exchanges the request and response. |
| `WebClient.ResponseSpec` | Interface for specifying response handling. |
| `WebClient.ResponseSpec.bodyToMono(Class<T> elementClass)` | Extracts the response body to a Mono. |
| `WebClient.ResponseSpec.bodyToFlux(Class<T> elementClass)` | Extracts the response body to a Flux. |
| `WebClient.ResponseSpec.toBodilessEntity()` | Retrieves the response as a bodiless entity. |
| `WebClient.ResponseSpec.toEntity(Class<T> entityClass)` | Retrieves the response as an entity. |
| `WebClient.ResponseSpec.toEntityList(Class<T> entityClass)` | Retrieves the response as a list of entities. |
| `WebClient.UriSpec` | Interface for specifying URIs. |
| `WebClient.UriSpec.uri(String uri)` | Sets the URI. |
| `WebClient.UriSpec.uri(URI uri)` | Sets the URI. |
| `WebClient.UriSpec.uri(Function<UriSpec, URI> uriFunction)` | Sets the URI using a function. |
| `WebClient.BodyInserter<T, S>` | Interface for inserting request bodies. |
| `WebClient.BodyInserters` | Utility class for BodyInserter instances. |
| `WebClient.BodyInserters.fromObject(Object body)` | Creates a BodyInserter from an object. |
| `WebClient.BodyInserters.fromPublisher(Publisher<? extends DataBuffer> publisher, Class<?> elementClass)` | Creates a BodyInserter from a publisher. |
| `WebClient.BodyInserters.fromDataBuffers(Flux<DataBuffer> dataBuffers)` | Creates a BodyInserter from a Flux of DataBuffer. |
| `WebClient.BodyInserters.fromResource(Resource resource)` | Creates a BodyInserter from a Resource. |
| `WebClient.BodyInserters.empty()` | Creates an empty BodyInserter. |
| `RouterFunction<T>` | Interface for router functions. |
| `RouterFunctions` | Utility class for RouterFunction instances. |
| `RouterFunctions.route(RequestPredicate predicate, HandlerFunction<T> handler)` | Creates a router function with the specified predicate and handler. |
| `RouterFunctions.route(ServerRequest.Predicate predicate, HandlerFunction<T> handler)` | Creates a router function with the specified predicate and handler. |
| `RouterFunctions.nest(PathPattern pathPattern, RouterFunction<T> nested)` | Creates a nested router function. |
| `RouterFunctions.nest(ServerRequest.Predicate predicate, RouterFunction<T> nested)` | Creates a nested router function with the specified predicate. |
| `RouterFunctions.filter(HandlerFilterFunction<T, T> filter, RouterFunction<T> router)` | Creates a filtered router function. |
| `RouterFunctions.resources(String locationPattern, Resource... locations)` | Creates a router function for static resources. |
| `RouterFunctions.resources(String locationPattern, String... locations)` | Creates a router function for static resources. |
| `HandlerFunction<T>` | Interface for handler functions. |
| `ServerRequest` | Interface for server requests. |
| `ServerRequest.headers()` | Returns the headers of the request. |
| `ServerRequest.method()` | Returns the HTTP method of the request. |
| `ServerRequest.path()` | Returns the path of the request. |
| `ServerRequest.queryParam(String name)` | Returns the query parameter with the specified name. |
| `ServerRequest.queryParams()` | Returns all query parameters. |
| `ServerRequest.formData()` | Returns the form data of the request. |
| `ServerRequest.multipartData()` | Returns the multipart data of the request. |
| `ServerRequest.bodyToMono(Class<T> elementClass)` | Extracts the request body to a Mono. |
| `ServerRequest.bodyToFlux(Class<T> elementClass)` | Extracts the request body to a Flux. |
| `ServerResponse` | Interface for server responses. |
| `ServerResponse.ok()` | Creates a 200 OK response. |
| `ServerResponse.created(URI location)` | Creates a 201 Created response with the specified location. |
| `ServerResponse.accepted()` | Creates a 202 Accepted response. |
| `ServerResponse.noContent()` | Creates a 204 No Content response. |
| `ServerResponse.badRequest()` | Creates a 400 Bad Request response. |
| `ServerResponse.notFound()` | Creates a 404 Not Found response. |
| `ServerResponse.status(HttpStatus status)` | Creates a response with the specified HTTP status. |
| `ServerResponse.bodyValue(Object body)` | Sets the response body. |
| `ServerResponse.body(Mono<? extends T> body)` | Sets the response body to a Mono. |
| `ServerResponse.body(Flux<? extends T> body)` | Sets the response body to a Flux. |
| `ServerResponse.headers(Consumer<HttpHeaders> headersConsumer)` | Sets the response headers. |
| `ServerResponse.cookie(String name, String value)` | Sets a response cookie. |
| `ServerResponse.writeTo(ServerWebExchange exchange, Context context)` | Writes the response to the exchange. |
| `HandlerFilterFunction<T, R>` | Interface for handler filter functions. |
| `ServerWebExchange` | Interface for server web exchanges. |
| `ServerWebExchange.getRequest()` | Returns the request. |
| `ServerWebExchange.getResponse()` | Returns the response. |
| `ServerWebExchange.getAttributes()` | Returns the attributes. |
| `ServerWebExchange.getSession()` | Returns the session. |
| `ServerWebExchange.getFormData()` | Returns the form data. |
| `ServerWebExchange.getMultipartData()` | Returns the multipart data. |
| `ServerWebExchange.getPrincipal()` | Returns the principal. |
| `ServerWebExchange.isNotModified()` | Checks if the exchange is not modified. |
| `ServerWebExchange.checkNotModified(Void result)` | Checks if the exchange is not modified. |
| `ReactiveAdapterRegistry` | Registry for reactive adapters. |
| `ReactiveAdapter` | Interface for reactive adapters. |

---
## Spring Data

| Code | Description |
|------|-------------|
| `@Repository` | Stereotype annotation for the persistence layer. |
| `@RepositoryDefinition` | Meta-annotation for custom repository annotations. |
| `Repository<T, ID>` | Interface for generic CRUD operations on a repository for a specific type. |
| `CrudRepository<T, ID>` | Interface for generic CRUD operations on a repository for a specific type. Provides methods like `save()`, `saveAll()`, `findById()`, `existsById()`, `findAll()`, `findAllById()`, `count()`, `deleteById()`, `delete()`, `deleteAll()`, `deleteAllById()`, and `deleteAll()`. |
| `PagingAndSortingRepository<T, ID>` | Interface for pagination and sorting operations. Provides methods like `findAll(Pageable pageable)` and `findAll(Sort sort)`. |
| `JpaRepository<T, ID>` | JPA-specific extension of Repository. Provides methods like `saveAndFlush()`, `deleteInBatch()`, `deleteAllInBatch()`, and `getOne()`. |
| `@Entity` | Specifies that the class is an entity. |
| `@Table` | Specifies the primary table for the annotated entity. |
| `@Id` | Specifies the primary key of an entity. |
| `@GeneratedValue` | Specifies the generation strategy for the primary key. |
| `@Column` | Specifies a mapped column for a persistent property or field. |
| `@Transient` | Specifies that the property or field is not persistent. |
| `@OneToOne` | Specifies a one-to-one association. |
| `@OneToMany` | Specifies a one-to-many association. |
| `@ManyToOne` | Specifies a many-to-one association. |
| `@ManyToMany` | Specifies a many-to-many association. |
| `@JoinColumn` | Specifies a column for joining an entity association or element collection. |
| `@JoinTable` | Specifies a join table for associations. |
| `@OrderBy` | Specifies the ordering of elements in a collection. |
| `@NamedQuery` | Specifies a named query for an entity. |
| `@NamedQueries` | Specifies multiple named queries for an entity. |
| `@Query` | Specifies a query for a repository method. |
| `@Modifying` | Indicates that a query method should be treated as a modifying query. |
| `@Transactional` | Describes transaction attributes on a method or class. |
| `@EnableJpaRepositories` | Enables JPA repositories. |
| `@EntityScan` | Configures the base packages to scan for entity classes. |
| `@EnableTransactionManagement` | Enables Spring's annotation-driven transaction management. |
| `JpaTransactionManager` | PlatformTransactionManager implementation for JPA. |
| `HibernateTransactionManager` | PlatformTransactionManager implementation for Hibernate. |
| `DataSourceTransactionManager` | PlatformTransactionManager implementation for DataSource. |
| `SimpleJpaRepository<T, ID>` | Simple JPA repository implementation. |
| `JpaRepositoryFactory` | Factory for creating JPA repositories. |
| `JpaRepositoryFactoryBean<T, ID, R>` | Factory bean for creating JPA repositories. |
| `EntityManager` | JPA EntityManager. |
| `EntityManagerFactory` | JPA EntityManagerFactory. |
| `PersistenceContext` | JPA PersistenceContext. |
| `PersistenceUnitInfo` | JPA PersistenceUnitInfo. |
| `PersistenceProvider` | JPA PersistenceProvider. |
| `Query` | JPA Query. |
| `TypedQuery<T>` | JPA TypedQuery. |
| `CriteriaQuery<T>` | JPA CriteriaQuery. |
| `CriteriaBuilder` | JPA CriteriaBuilder. |
| `Metamodel` | JPA Metamodel. |
| `EntityType<T>` | JPA EntityType. |
| `SingularAttribute<T, X>` | JPA SingularAttribute. |
| `PluralAttribute<T, C, E>` | JPA PluralAttribute. |
| `Join<T, X>` | JPA Join. |
| `From<T, X>` | JPA From. |
| `Selection<T>` | JPA Selection. |
| `Expression<T>` | JPA Expression. |
| `Predicate` | JPA Predicate. |
| `Order` | JPA Order. |
| `Page<T>` | Interface for pagination information. |
| `PageImpl<T>` | Implementation of Page. |
| `Pageable` | Interface for pagination parameters. |
| `PageRequest` | Implementation of Pageable. |
| `Sort` | Class for sorting parameters. |
| `Sort.Direction` | Enumeration of sort directions. Provides constants like `ASC` and `DESC`. |
| `Sort.Order` | Class for sort orders. |
| `Specifications<T>` | Utility class for JPA specifications. |
| `Specification<T>` | Interface for JPA specifications. |
| `Specification<T>.and(Specification<T> other)` | Combines this specification with another using AND. |
| `Specification<T>.or(Specification<T> other)` | Combines this specification with another using OR. |
| `Specification<T>.not(Specification<T> other)` | Negates this specification. |
| `Specification<T>.where(Predicate predicate)` | Creates a specification from a predicate. |
| `JpaSpecificationExecutor<T>` | Interface for executing JPA specifications. |
| `JpaSpecificationExecutor<T>.findAll(Specification<T> spec)` | Finds all entities matching the specification. |
| `JpaSpecificationExecutor<T>.findOne(Specification<T> spec)` | Finds one entity matching the specification. |
| `JpaSpecificationExecutor<T>.count(Specification<T> spec)` | Counts entities matching the specification. |

---
## Spring Boot

| Code | Description |
|------|-------------|
| `@SpringBootApplication` | Convenience annotation for Spring Boot applications. Combines @Configuration, @EnableAutoConfiguration, and @ComponentScan. |
| `@EnableAutoConfiguration` | Enables Spring Boot's auto-configuration mechanism. |
| `@Configuration` | Indicates that a class declares one or more @Bean methods. |
| `@ComponentScan` | Configures component scanning directives. |
| `@SpringBootConfiguration` | Configuration annotation for Spring Boot. |
| `@ConditionalOnClass` | Condition that only matches when the specified classes are on the classpath. |
| `@ConditionalOnMissingClass` | Condition that only matches when the specified classes are not on the classpath. |
| `@ConditionalOnBean` | Condition that only matches when the specified beans already exist. |
| `@ConditionalOnMissingBean` | Condition that only matches when the specified beans do not already exist. |
| `@ConditionalOnProperty` | Condition that only matches when the specified properties have specific values. |
| `@ConditionalOnResource` | Condition that only matches when the specified resources exist. |
| `@ConditionalOnWebApplication` | Condition that only matches when the application is a web application. |
| `@ConditionalOnNotWebApplication` | Condition that only matches when the application is not a web application. |
| `@ConditionalOnExpression` | Condition that only matches when the specified SpEL expression evaluates to true. |
| `@ConditionalOnJava` | Condition that only matches when the Java version matches. |
| `@ConditionalOnJndi` | Condition that only matches when the specified JNDI location exists. |
| `@AutoConfigureAfter` | Condition that only matches when the specified auto-configuration classes have been processed. |
| `@AutoConfigureBefore` | Condition that only matches when the specified auto-configuration classes have not been processed. |
| `@EnableConfigurationProperties` | Enables support for @ConfigurationProperties annotated beans. |
| `@ConfigurationProperties` | Annotation for externalized configuration. |
| `@ConfigurationProperties(prefix = "myprops")` | Binds external configuration to the annotated class with the specified prefix. |
| `@ConfigurationProperties(prefix = "myprops", ignoreUnknownFields = false)` | Binds external configuration to the annotated class with the specified prefix and ignores unknown fields. |
| `@ConfigurationProperties(prefix = "myprops", ignoreInvalidFields = false)` | Binds external configuration to the annotated class with the specified prefix and ignores invalid fields. |
| `@NestedConfigurationProperty` | Indicates that a field or method is a nested configuration property. |
| `@Value` | Used for injecting values into bean properties. |
| `@Value("${property.name}")` | Injects the value of the property with the specified name. |
| `@Value("${property.name:defaultValue}")` | Injects the value of the property with the specified name or the default value. |
| `@Value("#{expression}")` | Injects the result of the specified SpEL expression. |
| `SpringApplication` | Class for bootstrapping a Spring application from Java main methods. |
| `SpringApplication.run(Class<?> primarySource, String... args)` | Runs the Spring application. |
| `SpringApplication.run(Class<?>[] primarySources, String... args)` | Runs the Spring application with the specified primary sources. |
| `SpringApplicationBuilder` | Builder for SpringApplication. |
| `SpringApplicationBuilder(SpringApplication application)` | Creates a new SpringApplicationBuilder. |
| `SpringApplicationBuilder.sources(Class<?>... primarySources)` | Sets the primary sources. |
| `SpringApplicationBuilder.run(String... args)` | Runs the Spring application. |
| `SpringApplicationEvent` | Base class for SpringApplication events. |
| `SpringApplicationEvent.getApplication()` | Returns the SpringApplication. |
| `SpringApplicationEvent.getArgs()` | Returns the application arguments. |
| `ApplicationStartingEvent` | Event published when an ApplicationContext is starting. |
| `ApplicationEnvironmentPreparedEvent` | Event published when an Environment is prepared. |
| `ApplicationContextInitializedEvent` | Event published when an ApplicationContext is initialized. |
| `ApplicationPreparedEvent` | Event published when an ApplicationContext is prepared. |
| `ContextRefreshedEvent` | Event published when an ApplicationContext is refreshed. |
| `ContextStartedEvent` | Event published when an ApplicationContext is started. |
| `ContextStoppedEvent` | Event published when an ApplicationContext is stopped. |
| `ContextClosedEvent` | Event published when an ApplicationContext is closed. |
| `FailureAnalyzers` | Utility class for failure analyzers. |
| `FailureAnalyzer` | Interface for failure analyzers. |
| `FailureAnalyzer.analyze(Throwable failure)` | Analyzes the specified failure. |
| `FailureAnalysis` | Class for failure analysis results. |
| `Banner` | Interface for printing banners. |
| `Banner.printBanner(Environment environment, Class<?> sourceClass, PrintStream out)` | Prints the banner. |
| `ResourceBanner` | Banner implementation for resources. |
| `ImageBanner` | Banner implementation for images. |
| `SpringApplicationBannerPrinter` | Printer for SpringApplication banners. |
| `DefaultBanner` | Default banner implementation. |
| `StaticLogoBanner` | Banner implementation for static logos. |
| `AnsiColor` | Enumeration of ANSI colors. |
| `AnsiStyle` | Class for ANSI styles. |
| `AnsiOutput` | Class for ANSI output. |
| `AnsiOutput.setEnabled(Enabled enabled)` | Sets whether ANSI output is enabled. |
| `AnsiOutput.setConsoleAvailable(boolean consoleAvailable)` | Sets whether the console is available. |
| `SpringApplicationRunListeners` | Listeners for SpringApplication run events. |
| `SpringApplicationRunListener` | Interface for SpringApplication run listeners. |
| `SpringApplicationRunListener.starting()` | Called when the application is starting. |
| `SpringApplicationRunListener.environmentPrepared(ConfigurableEnvironment environment)` | Called when the environment is prepared. |
| `SpringApplicationRunListener.contextPrepared(ConfigurableApplicationContext context)` | Called when the context is prepared. |
| `SpringApplicationRunListener.contextLoaded(ConfigurableApplicationContext context)` | Called when the context is loaded. |
| `SpringApplicationRunListener.started(ConfigurableApplicationContext context)` | Called when the context is started. |
| `SpringApplicationRunListener.running(ConfigurableApplicationContext context)` | Called when the application is running. |
| `SpringApplicationRunListener.failed(ConfigurableApplicationContext context, Throwable exception)` | Called when the application fails. |
| `EventPublishingRunListener` | Run listener for publishing events. |
| `LoggingApplicationListener` | Application listener for logging. |
| `ClasspathLoggingApplicationListener` | Application listener for classpath logging. |
| `BackgroundPreinitializer` | Preinitializer for background tasks. |
| `DeferredLoggingApplicationListener` | Application listener for deferred logging. |
| `LiquibaseServiceLocatorApplicationListener` | Application listener for Liquibase service locator. |
| `MainApplicationClass` | Class for the main application class. |

---
## Spring Security

| Code | Description |
|------|-------------|
| `@EnableWebSecurity` | Enables web security for a Spring application. |
| `@EnableGlobalMethodSecurity` | Enables global method security. |
| `@EnableGlobalAuthentication` | Enables global authentication. |
| `@Configuration` | Indicates that a class declares one or more @Bean methods. |
| `WebSecurityConfigurerAdapter` | Convenience class for creating a WebSecurityConfigurer instance. |
| `WebSecurityConfigurerAdapter.configure(HttpSecurity http)` | Configures the HttpSecurity. |
| `HttpSecurity` | Configuration class for HTTP security. |
| `HttpSecurity.authorizeRequests()` | Configures authorization for requests. |
| `HttpSecurity.authorizeRequests().antMatchers(String... antPatterns)` | Configures authorization for the specified ant patterns. |
| `HttpSecurity.authorizeRequests().antMatchers(HttpMethod method, String... antPatterns)` | Configures authorization for the specified HTTP method and ant patterns. |
| `HttpSecurity.authorizeRequests().anyRequest()` | Configures authorization for any request. |
| `HttpSecurity.authorizeRequests().authenticated()` | Requires authentication for the configured requests. |
| `HttpSecurity.authorizeRequests().permitAll()` | Permits all requests. |
| `HttpSecurity.authorizeRequests().denyAll()` | Denies all requests. |
| `HttpSecurity.authorizeRequests().hasRole(String role)` | Requires the specified role for the configured requests. |
| `HttpSecurity.authorizeRequests().hasAnyRole(String... roles)` | Requires any of the specified roles for the configured requests. |
| `HttpSecurity.authorizeRequests().hasAuthority(String authority)` | Requires the specified authority for the configured requests. |
| `HttpSecurity.authorizeRequests().hasAnyAuthority(String... authorities)` | Requires any of the specified authorities for the configured requests. |
| `HttpSecurity.authorizeRequests().access(String expression)` | Requires the specified access expression for the configured requests. |
| `HttpSecurity.authorizeRequests().mvcMatchers(String... patterns)` | Configures authorization for the specified MVC patterns. |
| `HttpSecurity.authorizeRequests().regexMatchers(String regex, String httpMethod)` | Configures authorization for the specified regex pattern and HTTP method. |
| `HttpSecurity.formLogin()` | Configures form login. |
| `HttpSecurity.formLogin().loginPage(String loginPage)` | Sets the login page URL. |
| `HttpSecurity.formLogin().loginProcessingUrl(String loginProcessingUrl)` | Sets the login processing URL. |
| `HttpSecurity.formLogin().defaultSuccessUrl(String defaultSuccessUrl)` | Sets the default success URL. |
| `HttpSecurity.formLogin().failureUrl(String failureUrl)` | Sets the failure URL. |
| `HttpSecurity.formLogin().usernameParameter(String usernameParameter)` | Sets the username parameter name. |
| `HttpSecurity.formLogin().passwordParameter(String passwordParameter)` | Sets the password parameter name. |
| `HttpSecurity.logout()` | Configures logout. |
| `HttpSecurity.logout().logoutUrl(String logoutUrl)` | Sets the logout URL. |
| `HttpSecurity.logout().logoutSuccessUrl(String logoutSuccessUrl)` | Sets the logout success URL. |
| `HttpSecurity.logout().invalidateHttpSession(boolean invalidateHttpSession)` | Sets whether to invalidate the HTTP session. |
| `HttpSecurity.logout().deleteCookies(String... cookieNamesToClear)` | Sets the cookies to delete. |
| `HttpSecurity.csrf()` | Configures CSRF protection. |
| `HttpSecurity.csrf().disable()` | Disables CSRF protection. |
| `HttpSecurity.csrf().csrfTokenRepository(CsrfTokenRepository csrfTokenRepository)` | Sets the CSRF token repository. |
| `HttpSecurity.rememberMe()` | Configures remember-me authentication. |
| `HttpSecurity.rememberMe().key(String key)` | Sets the remember-me key. |
| `HttpSecurity.rememberMe().tokenValiditySeconds(int tokenValiditySeconds)` | Sets the remember-me token validity in seconds. |
| `HttpSecurity.rememberMe().rememberMeParameter(String rememberMeParameter)` | Sets the remember-me parameter name. |
| `HttpSecurity.rememberMe().rememberMeCookieName(String rememberMeCookieName)` | Sets the remember-me cookie name. |
| `HttpSecurity.exceptionHandling()` | Configures exception handling. |
| `HttpSecurity.exceptionHandling().accessDeniedPage(String accessDeniedPage)` | Sets the access denied page. |
| `HttpSecurity.exceptionHandling().accessDeniedHandler(AccessDeniedHandler accessDeniedHandler)` | Sets the access denied handler. |
| `HttpSecurity.sessionManagement()` | Configures session management. |
| `HttpSecurity.sessionManagement().sessionCreationPolicy(SessionCreationPolicy sessionCreationPolicy)` | Sets the session creation policy. |
| `HttpSecurity.sessionManagement().maximumSessions(int maximumSessions)` | Sets the maximum number of sessions. |
| `HttpSecurity.sessionManagement().sessionFixation().newSession()` | Configures session fixation with new sessions. |
| `HttpSecurity.sessionManagement().sessionFixation().migrateSession()` | Configures session fixation with session migration. |
| `HttpSecurity.sessionManagement().sessionFixation().none()` | Disables session fixation. |
| `HttpSecurity.headers()` | Configures security headers. |
| `HttpSecurity.headers().contentSecurityPolicy(String policy)` | Sets the Content Security Policy header. |
| `HttpSecurity.headers().addHeaderWriter(HeaderWriter headerWriter)` | Adds a header writer. |
| `HttpSecurity.requestCache()` | Configures request caching. |
| `HttpSecurity.requestCache().requestCache(RequestCache requestCache)` | Sets the request cache. |
| `HttpSecurity.portMapper()` | Configures port mapping. |
| `HttpSecurity.portMapper().addPortMapping(int httpPort, int httpsPort)` | Adds a port mapping. |
| `HttpSecurity.jeep()` | Configures JEEP support. |
| `HttpSecurity.x509()` | Configures X.509 authentication. |
| `HttpSecurity.requiresChannel()` | Configures channel security. |
| `HttpSecurity.requiresChannel().anyRequest()` | Configures channel security for any request. |
| `HttpSecurity.requiresChannel().requiresSecure()` | Requires secure channels. |
| `HttpSecurity.requiresChannel().requiresInsecure()` | Requires insecure channels. |
| `AuthenticationManager` | Interface for authentication managers. |
| `AuthenticationManager.authenticate(Authentication authentication)` | Authenticates the specified authentication. |
| `ProviderManager` | Implementation of AuthenticationManager. |
| `AuthenticationProvider` | Interface for authentication providers. |
| `AuthenticationProvider.authenticate(Authentication authentication)` | Authenticates the specified authentication. |
| `AuthenticationProvider.supports(Class<?> authentication)` | Checks if the authentication provider supports the specified authentication type. |
| `DaoAuthenticationProvider` | AuthenticationProvider implementation for DAO authentication. |
| `InMemoryAuthenticationProvider` | AuthenticationProvider implementation for in-memory authentication. |
| `LdapAuthenticationProvider` | AuthenticationProvider implementation for LDAP authentication. |
| `Authentication` | Interface for authentication tokens. |
| `Authentication.getPrincipal()` | Returns the principal. |
| `Authentication.getCredentials()` | Returns the credentials. |
| `Authentication.getAuthorities()` | Returns the authorities. |
| `Authentication.getDetails()` | Returns the details. |
| `Authentication.isAuthenticated()` | Checks if the authentication is authenticated. |
| `Authentication.setAuthenticated(boolean isAuthenticated)` | Sets whether the authentication is authenticated. |
| `UsernamePasswordAuthenticationToken` | Authentication implementation for username/password authentication. |
| `RememberMeAuthenticationToken` | Authentication implementation for remember-me authentication. |
| `AnonymousAuthenticationToken` | Authentication implementation for anonymous authentication. |
| `SecurityContext` | Holder for the current security context. |
| `SecurityContextHolder` | Holder for the current SecurityContext. |
| `SecurityContextHolder.getContext()` | Returns the current SecurityContext. |
| `SecurityContextHolder.setContext(SecurityContext context)` | Sets the current SecurityContext. |
| `SecurityContextHolder.clearContext()` | Clears the current SecurityContext. |
| `SecurityContextHolder.setStrategyName(String strategyName)` | Sets the strategy name. |
| `SecurityContextHolder.MODE_GLOBAL` | Global strategy for SecurityContextHolder. |
| `SecurityContextHolder.MODE_INHERITABLETHREADLOCAL` | InheritableThreadLocal strategy for SecurityContextHolder. |
| `SecurityContextHolder.MODE_THREADLOCAL` | ThreadLocal strategy for SecurityContextHolder. |
| `SecurityContext.getAuthentication()` | Returns the current Authentication. |
| `SecurityContext.setAuthentication(Authentication authentication)` | Sets the current Authentication. |
| `UserDetails` | Interface for user details. |
| `UserDetails.getUsername()` | Returns the username. |
| `UserDetails.getPassword()` | Returns the password. |
| `UserDetails.getAuthorities()` | Returns the authorities. |
| `UserDetails.isAccountNonExpired()` | Checks if the account is non-expired. |
| `UserDetails.isAccountNonLocked()` | Checks if the account is non-locked. |
| `UserDetails.isCredentialsNonExpired()` | Checks if the credentials are non-expired. |
| `UserDetails.isEnabled()` | Checks if the user is enabled. |
| `User` | UserDetails implementation. |
| `User.withUsername(String username)` | Creates a User with the specified username. |
| `User.password(String password)` | Sets the password. |
| `User.roles(String... roles)` | Sets the roles. |
| `User.authorities(Collection<? extends GrantedAuthority> authorities)` | Sets the authorities. |
| `User.accountExpired(boolean accountExpired)` | Sets whether the account is expired. |
| `User.accountLocked(boolean accountLocked)` | Sets whether the account is locked. |
| `User.credentialsExpired(boolean credentialsExpired)` | Sets whether the credentials are expired. |
| `User.disabled(boolean disabled)` | Sets whether the user is disabled. |
| `User.build()` | Builds the User. |
| `GrantedAuthority` | Interface for granted authorities. |
| `GrantedAuthority.getAuthority()` | Returns the authority. |
| `SimpleGrantedAuthority` | GrantedAuthority implementation. |
| `SimpleGrantedAuthority(String role)` | Creates a SimpleGrantedAuthority with the specified role. |
| `PasswordEncoder` | Interface for password encoders. |
| `PasswordEncoder.encode(CharSequence rawPassword)` | Encodes the specified password. |
| `PasswordEncoder.matches(CharSequence rawPassword, String encodedPassword)` | Checks if the specified password matches the encoded password. |
| `BCryptPasswordEncoder` | PasswordEncoder implementation for BCrypt. |
| `StandardPasswordEncoder` | PasswordEncoder implementation for standard encoding. |
| `Pbkdf2PasswordEncoder` | PasswordEncoder implementation for PBKDF2. |
| `SCryptPasswordEncoder` | PasswordEncoder implementation for SCrypt. |
| `NoOpPasswordEncoder` | PasswordEncoder implementation for no encoding. |
| `DelegatingPasswordEncoder` | PasswordEncoder implementation that delegates to other encoders. |
| `UserDetailsService` | Interface for user details services. |
| `UserDetailsService.loadUserByUsername(String username)` | Loads the user by username. |
| `InMemoryUserDetailsManager` | UserDetailsService implementation for in-memory user details. |
| `JdbcUserDetailsManager` | UserDetailsService implementation for JDBC user details. |
| `LdapUserDetailsManager` | UserDetailsService implementation for LDAP user details. |
| `UserDetailsManager` | Interface for user details managers. |
| `UserDetailsManager.createUser(UserDetails user)` | Creates a user. |
| `UserDetailsManager.updateUser(UserDetails user)` | Updates a user. |
| `UserDetailsManager.deleteUser(String username)` | Deletes a user. |
| `UserDetailsManager.changePassword(String oldPassword, String newPassword)` | Changes the password. |
| `UserDetailsManager.userExists(String username)` | Checks if a user exists. |
| `AccessDecisionManager` | Interface for access decision managers. |
| `AccessDecisionManager.decide(Authentication authentication, Object object, Collection<ConfigAttribute> configAttributes)` | Decides whether access is granted. |
| `AffirmativeBased` | AccessDecisionManager implementation that grants access if any voter votes affirmatively. |
| `ConsensusBased` | AccessDecisionManager implementation that grants access if the consensus is affirmative. |
| `UnanimousBased` | AccessDecisionManager implementation that grants access only if all voters vote affirmatively. |
| `AccessDecisionVoter<S>` | Interface for access decision voters. |
| `AccessDecisionVoter<S>.vote(Authentication authentication, S object, Collection<ConfigAttribute> attributes)` | Votes on whether access should be granted. |
| `AccessDecisionVoter<S>.supports(ConfigAttribute attribute)` | Checks if the voter supports the specified attribute. |
| `AccessDecisionVoter<S>.supports(Class<?> clazz)` | Checks if the voter supports the specified class. |
| `RoleVoter` | AccessDecisionVoter implementation for role-based voting. |
| `AuthenticatedVoter` | AccessDecisionVoter implementation for authenticated voting. |
| `WebExpressionVoter` | AccessDecisionVoter implementation for web expression voting. |
| `AfterInvocationProviderManager` | Manager for after invocation providers. |
| `AfterInvocationManager` | Interface for after invocation managers. |
| `AfterInvocationManager.decide(Authentication authentication, Object object, Collection<ConfigAttribute> configAttributes, Object returnedObject)` | Decides whether to grant access after invocation. |
| `ConfigAttribute` | Interface for configuration attributes. |
| `ConfigAttribute.getAttribute()` | Returns the attribute. |
| `SecurityConfig` | ConfigAttribute implementation. |
| `SecurityConfig(String attribute)` | Creates a SecurityConfig with the specified attribute. |
| `InterceptUrlRegistry` | Registry for intercept URLs. |
| `InterceptUrlRegistry.addInterceptor(ChannelProcessingFilter filter)` | Adds a channel processing filter. |
| `FilterSecurityInterceptor` | Security interceptor for filters. |
| `AbstractSecurityInterceptor` | Abstract security interceptor. |
| `MethodSecurityInterceptor` | Security interceptor for methods. |
| `RunAsManager` | Manager for run-as authentication. |
| `RunAsManager.setRunAsAuthenticationProvider(RunAsAuthenticationProvider runAsAuthenticationProvider)` | Sets the run-as authentication provider. |
| `RunAsAuthenticationProvider` | Interface for run-as authentication providers. |
| `AuthenticationTrustResolver` | Interface for authentication trust resolvers. |
| `AuthenticationTrustResolver.isAnonymous(Authentication authentication)` | Checks if the authentication is anonymous. |
| `AuthenticationTrustResolver.isRememberMe(Authentication authentication)` | Checks if the authentication is remember-me. |
| `AuthenticationTrustResolver.isFullyAuthenticated(Authentication authentication)` | Checks if the authentication is fully authenticated. |
| `PermissionEvaluator` | Interface for permission evaluators. |
| `PermissionEvaluator.hasPermission(Authentication authentication, Object targetDomainObject, Object permission)` | Checks if the authentication has the specified permission. |
| `DefaultPermissionEvaluator` | Default PermissionEvaluator implementation. |
| `AclPermissionEvaluator` | PermissionEvaluator implementation for ACLs. |
| `MethodSecurityExpressionHandler` | Interface for method security expression handlers. |
| `DefaultMethodSecurityExpressionHandler` | Default MethodSecurityExpressionHandler implementation. |
| `MethodSecurityExpressionOperations` | Interface for method security expression operations. |