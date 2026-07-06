## Built-in Functions

| Code | Description |
|------|-------------|
| `append` | Append elements to a slice |
| `cap` | Return the capacity of a slice or array |
| `close` | Close a channel |
| `complex` | Create a complex number from real and imaginary parts |
| `copy` | Copy elements from one slice to another |
| `delete` | Delete an element from a map |
| `imag` | Return the imaginary part of a complex number |
| `len` | Return the length of a slice, array, string, or map |
| `make` | Allocate and initialize a slice, map, or channel |
| `new` | Allocate memory but do not initialize (zero value) |
| `panic` | Cause a runtime panic |
| `print` | Print arguments to standard output |
| `println` | Print arguments to standard output with newline |
| `real` | Return the real part of a complex number |
| `recover` | Recover from a panic |
| `delete` | Delete an element from a map |

---
## Built-in Constants

| Code | Description |
|------|-------------|
| `true` | Boolean true value |
| `false` | Boolean false value |
| `iota` | Used in const declarations to generate sequential values |
| `nil` | Zero value for pointers, interfaces, slices, maps, channels, and functions |

---
## Built-in Types

| Code | Description |
|------|-------------|
| `bool` | Boolean type (true or false) |
| `byte` | Alias for uint8 |
| `complex64` | Complex number with float32 real and imaginary parts |
| `complex128` | Complex number with float64 real and imaginary parts |
| `error` | Interface type for error handling |
| `float32` | IEEE-754 32-bit floating point number |
| `float64` | IEEE-754 64-bit floating point number |
| `int` | Platform-dependent integer type (32 or 64 bits) |
| `int8` | 8-bit signed integer |
| `int16` | 16-bit signed integer |
| `int32` | 32-bit signed integer |
| `int64` | 64-bit signed integer |
| `rune` | Alias for int32, represents a Unicode code point |
| `string` | UTF-8 encoded string type |
| `uint` | Platform-dependent unsigned integer type (32 or 64 bits) |
| `uint8` | 8-bit unsigned integer |
| `uint16` | 16-bit unsigned integer |
| `uint32` | 32-bit unsigned integer |
| `uint64` | 64-bit unsigned integer |
| `uintptr` | Unsigned integer type large enough to hold a pointer |

---
## Package archive/tar

| Code | Description |
|------|-------------|
| `tar.Reader` | Reader for tar archives |
| `tar.Writer` | Writer for tar archives |
| `tar.NewReader(r io.Reader) *Reader` | Create a new Reader from an io.Reader |
| `tar.NewWriter(w io.Writer) *Writer` | Create a new Writer to an io.Writer |
| `tar.Header` | Representation of a tar header |
| `tar.TypeReg` | Regular file type |
| `tar.TypeLink` | Hard link type |
| `tar.TypeSymlink` | Symbolic link type |
| `tar.TypeChar` | Character device type |
| `tar.TypeBlock` | Block device type |
| `tar.TypeDir` | Directory type |
| `tar.TypeFifo` | FIFO (named pipe) type |

---
## Package archive/zip

| Code | Description |
|------|-------------|
| `zip.Reader` | Reader for zip archives |
| `zip.Writer` | Writer for zip archives |
| `zip.NewReader(r io.ReaderAt, size int64) (*Reader, error)` | Create a new Reader from an io.ReaderAt |
| `zip.NewWriter(w io.Writer) *Writer` | Create a new Writer to an io.Writer |
| `zip.File` | Representation of a file in a zip archive |
| `zip.FileHeader` | Representation of a file header in a zip archive |
| `zip.FileInfo` | Return FileInfo for a FileHeader |
| `zip.RegisterCompressor(method uint16, comp Compressor)` | Register a custom compression method |
| `zip.Store` | Store compression method |
| `zip.Deflate` | Deflate compression method |

---
## Package bufio

| Code | Description |
|------|-------------|
| `bufio.Reader` | Buffered reader |
| `bufio.Writer` | Buffered writer |
| `bufio.Scanner` | Text scanner |
| `bufio.NewReader(rd io.Reader) *Reader` | Create a new buffered Reader |
| `bufio.NewReaderSize(rd io.Reader, size int) *Reader` | Create a new buffered Reader with specified size |
| `bufio.NewWriter(w io.Writer) *Writer` | Create a new buffered Writer |
| `bufio.NewWriterSize(w io.Writer, size int) *Writer` | Create a new buffered Writer with specified size |
| `bufio.NewScanner(r io.Reader) *Scanner` | Create a new Scanner |
| `Reader.Peek(n int) ([]byte, error)` | Peek at the next n bytes |
| `Reader.Read(p []byte) (n int, err error)` | Read data into p |
| `Reader.ReadByte() (byte, error)` | Read a single byte |
| `Reader.ReadBytes(delim byte) ([]byte, error)` | Read until delimiter byte |
| `Reader.ReadString(delim byte) (string, error)` | Read until delimiter byte as string |
| `Reader.ReadLine() (line []byte, prefix bool, err error)` | Read a line |
| `Reader.ReadRune() (r rune, size int, err error)` | Read a single UTF-8 encoded rune |
| `Reader.Reset(r io.Reader)` | Reset the buffer to read from r |
| `Writer.Write(p []byte) (n int, err error)` | Write data from p |
| `Writer.WriteByte(c byte) error` | Write a single byte |
| `Writer.WriteRune(r rune) (size int, err error)` | Write a single UTF-8 encoded rune |
| `Writer.WriteString(s string) (n int, err error)` | Write a string |
| `Writer.Flush() error` | Flush the buffer |
| `Writer.Reset(w io.Writer)` | Reset the buffer to write to w |
| `Scanner.Scan() bool` | Advance the scanner to the next token |
| `Scanner.Text() string` | Return the most recently scanned token |
| `Scanner.Err() error` | Return the first non-EOF error |
| `SplitFunc` | Function type for custom split functions |
| `ScanLines` | Split function for scanning lines |
| `ScanRunes` | Split function for scanning runes |
| `ScanWords` | Split function for scanning words |
| `ScanBytes` | Split function for scanning bytes |

---
## Package bytes

| Code | Description |
|------|-------------|
| `bytes.Buffer` | Variable-sized buffer of bytes |
| `bytes.NewBuffer(buf []byte) *Buffer` | Create a new Buffer with initial content |
| `bytes.NewBufferString(s string) *Buffer` | Create a new Buffer from a string |
| `Buffer.Bytes() []byte` | Return the buffer contents as a slice |
| `Buffer.String() string` | Return the buffer contents as a string |
| `Buffer.Len() int` | Return the number of bytes in the buffer |
| `Buffer.Cap() int` | Return the capacity of the buffer |
| `Buffer.Reset()` | Reset the buffer to empty |
| `Buffer.Truncate(n int)` | Truncate the buffer to n bytes |
| `Buffer.Write(p []byte) (n int, err error)` | Write data to the buffer |
| `Buffer.WriteByte(c byte) error` | Write a single byte to the buffer |
| `Buffer.WriteRune(r rune) (n int, err error)` | Write a single rune to the buffer |
| `Buffer.WriteString(s string) (n int, err error)` | Write a string to the buffer |
| `Buffer.Read(p []byte) (n int, err error)` | Read data from the buffer |
| `Buffer.ReadByte() (byte, error)` | Read a single byte from the buffer |
| `Buffer.ReadRune() (r rune, size int, err error)` | Read a single rune from the buffer |
| `Buffer.ReadBytes(delim byte) ([]byte, error)` | Read until delimiter byte |
| `Buffer.ReadString(delim byte) (string, error)` | Read until delimiter byte as string |
| `Buffer.Next(n int) []byte` | Return the next n bytes without advancing |
| `bytes.Compare(a, b []byte) int` | Compare two byte slices lexicographically |
| `bytes.Contains(b, subslice []byte) bool` | Check if subslice is within b |
| `bytes.Count(s, sep []byte) int` | Count the number of non-overlapping instances of sep in s |
| `bytes.Equal(a, b []byte) bool` | Check if two byte slices are equal |
| `bytes.Fields(s []byte) [][]byte` | Split s into fields separated by whitespace |
| `bytes.FieldsFunc(s []byte, f func(rune) bool) [][]byte` | Split s into fields using a custom function |
| `bytes.HasPrefix(s, prefix []byte) bool` | Check if s starts with prefix |
| `bytes.HasSuffix(s, suffix []byte) bool` | Check if s ends with suffix |
| `bytes.Index(s, sep []byte) int` | Return the index of the first instance of sep in s |
| `bytes.IndexAny(s []byte, chars string) int` | Return the index of the first instance of any char in s |
| `bytes.IndexByte(s []byte, c byte) int` | Return the index of the first instance of byte c in s |
| `bytes.IndexFunc(s []byte, f func(rune) bool) int` | Return the index of the first rune satisfying f |
| `bytes.IndexRune(s []byte, r rune) int` | Return the index of the first instance of rune in s |
| `bytes.Join(s [][]byte, sep []byte) []byte` | Concatenate the elements of s with sep |
| `bytes.LastIndex(s, sep []byte) int` | Return the index of the last instance of sep in s |
| `bytes.LastIndexAny(s []byte, chars string) int` | Return the index of the last instance of any char in s |
| `bytes.LastIndexByte(s []byte, c byte) int` | Return the index of the last instance of byte c in s |
| `bytes.LastIndexFunc(s []byte, f func(rune) bool) int` | Return the index of the last rune satisfying f |
| `bytes.Map(mapping func(rune) rune, s []byte) []byte` | Map each rune in s using mapping |
| `bytes.NewBuffer(buf []byte) *Buffer` | Create a new Buffer |
| `bytes.NewReader(b []byte) *bytes.Reader` | Create a new Reader from a byte slice |
| `bytes.Repeat(b []byte, count int) []byte` | Return a new byte slice with b repeated count times |
| `bytes.Replace(s, old, new []byte, n int) []byte` | Replace the first n non-overlapping instances of old with new |
| `bytes.ReplaceAll(s, old, new []byte) []byte` | Replace all instances of old with new |
| `bytes.Runes(s []byte) []rune` | Convert byte slice to rune slice |
| `bytes.Split(s, sep []byte) [][]byte` | Split s into substrings separated by sep |
| `bytes.SplitAfter(s, sep []byte) [][]byte` | Split s after each instance of sep |
| `bytes.SplitAfterN(s, sep []byte, n int) [][]byte` | Split s after each instance of sep, up to n times |
| `bytes.SplitN(s, sep []byte, n int) [][]byte` | Split s into substrings separated by sep, up to n times |
| `bytes.Title(s []byte) []byte` | Return a title-cased copy of s |
| `bytes.ToLower(s []byte) []byte` | Return a lower-cased copy of s |
| `bytes.ToLowerSpecial(c unicode.SpecialCase, s []byte) []byte` | Return a lower-cased copy of s with special case handling |
| `bytes.ToTitle(s []byte) []byte` | Return a title-cased copy of s |
| `bytes.ToTitleSpecial(c unicode.SpecialCase, s []byte) []byte` | Return a title-cased copy of s with special case handling |
| `bytes.ToUpper(s []byte) []byte` | Return an upper-cased copy of s |
| `bytes.ToUpperSpecial(c unicode.SpecialCase, s []byte) []byte` | Return an upper-cased copy of s with special case handling |
| `bytes.Trim(s []byte, cutset string) []byte` | Remove leading and trailing bytes in cutset from s |
| `bytes.TrimFunc(s []byte, f func(rune) bool) []byte` | Remove leading and trailing runes satisfying f from s |
| `bytes.TrimLeft(s []byte, cutset string) []byte` | Remove leading bytes in cutset from s |
| `bytes.TrimLeftFunc(s []byte, f func(rune) bool) []byte` | Remove leading runes satisfying f from s |
| `bytes.TrimPrefix(s, prefix []byte) []byte` | Remove leading prefix from s |
| `bytes.TrimRight(s []byte, cutset string) []byte` | Remove trailing bytes in cutset from s |
| `bytes.TrimRightFunc(s []byte, f func(rune) bool) []byte` | Remove trailing runes satisfying f from s |
| `bytes.TrimSpace(s []byte) []byte` | Remove leading and trailing whitespace from s |
| `bytes.TrimSuffix(s, suffix []byte) []byte` | Remove trailing suffix from s |

---
## Package compress/bzip2

| Code | Description |
|------|-------------|
| `bzip2.Reader` | Reader for bzip2 compressed data |
| `bzip2.Writer` | Writer for bzip2 compressed data |
| `bzip2.NewReader(r io.Reader) (*Reader, error)` | Create a new bzip2 Reader |
| `bzip2.NewWriter(w io.Writer, level *int) *Writer` | Create a new bzip2 Writer |
| `Writer.Close() error` | Close the writer and flush buffers |
| `Writer.Flush() error` | Flush the writer buffers |
| `Writer.Reset(w io.Writer)` | Reset the writer to write to w |

---
## Package compress/flate

| Code | Description |
|------|-------------|
| `flate.Reader` | Reader for deflate compressed data |
| `flate.Writer` | Writer for deflate compressed data |
| `flate.NewReader(r io.Reader) *Reader` | Create a new deflate Reader |
| `flate.NewReaderDict(r io.Reader, dict []byte) (*Reader, error)` | Create a new deflate Reader with dictionary |
| `flate.NewWriter(w io.Writer, level int) (*Writer, error)` | Create a new deflate Writer |
| `flate.NewWriterDict(w io.Writer, level int, dict []byte) (*Writer, error)` | Create a new deflate Writer with dictionary |
| `Writer.Close() error` | Close the writer and flush buffers |
| `Writer.Flush() error` | Flush the writer buffers |
| `Writer.Reset(w io.Writer)` | Reset the writer to write to w |
| `flate.CorruptInputError` | Error type for corrupt input |
| `flate.InternalError` | Error type for internal errors |
| `DefaultCompression` | Default compression level |
| `NoCompression` | No compression |
| `BestSpeed` | Best speed compression |
| `BestCompression` | Best compression |
| `HuffmanOnly` | Huffman encoding only |
| `CompressionLevel` | Type for compression level |

---
## Package compress/gzip

| Code | Description |
|------|-------------|
| `gzip.Reader` | Reader for gzip files |
| `gzip.Writer` | Writer for gzip files |
| `gzip.NewReader(r io.Reader) (*Reader, error)` | Create a new gzip Reader |
| `gzip.NewWriter(w io.Writer) *Writer` | Create a new gzip Writer |
| `gzip.NewWriterLevel(w io.Writer, level int) (*Writer, error)` | Create a new gzip Writer with compression level |
| `Reader.Close() error` | Close the reader |
| `Reader.Header` | Header of the gzip file |
| `Reader.ModTime() time.Time` | Return the modification time from the header |
| `Reader.Name` | Return the filename from the header |
| `Reader.Comment` | Return the comment from the header |
| `Reader.Extra` | Return the extra data from the header |
| `Writer.Close() error` | Close the writer and flush buffers |
| `Writer.Flush() error` | Flush the writer buffers |
| `Writer.Reset(w io.Writer)` | Reset the writer to write to w |
| `Writer.Name` | Set the filename in the header |
| `Writer.Comment` | Set the comment in the header |
| `Writer.Extra` | Set the extra data in the header |
| `Writer.ModTime` | Set the modification time in the header |
| `gzip.ErrHeader` | Error type for header errors |
| `gzip.ErrChecksum` | Error type for checksum errors |
| `DefaultCompression` | Default compression level |
| `NoCompression` | No compression |
| `BestSpeed` | Best speed compression |
| `BestCompression` | Best compression |
| `HuffmanOnly` | Huffman encoding only |

---
## Package compress/lzw

| Code | Description |
|------|-------------|
| `lzw.Reader` | Reader for LZW compressed data |
| `lzw.Writer` | Writer for LZW compressed data |
| `lzw.NewReader(r io.Reader, order Order, litWidth int) *Reader` | Create a new LZW Reader |
| `lzw.NewWriter(w io.Writer, order Order, litWidth int) *Writer` | Create a new LZW Writer |
| `Order` | Type for LZW order (LSB or MSB) |
| `LSB` | Least significant bit first |
| `MSB` | Most significant bit first |

---
## Package compress/zlib

| Code | Description |
|------|-------------|
| `zlib.Reader` | Reader for zlib compressed data |
| `zlib.Writer` | Writer for zlib compressed data |
| `zlib.NewReader(r io.Reader) *Reader` | Create a new zlib Reader |
| `zlib.NewReaderDict(r io.Reader, dict []byte) (*Reader, error)` | Create a new zlib Reader with dictionary |
| `zlib.NewWriter(w io.Writer) *Writer` | Create a new zlib Writer |
| `zlib.NewWriterLevel(w io.Writer, level int) (*Writer, error)` | Create a new zlib Writer with compression level |
| `zlib.NewWriterLevelDict(w io.Writer, level int, dict []byte) (*Writer, error)` | Create a new zlib Writer with compression level and dictionary |
| `Reader.Close() error` | Close the reader |
| `Writer.Close() error` | Close the writer and flush buffers |
| `Writer.Flush() error` | Flush the writer buffers |
| `Writer.Reset(w io.Writer)` | Reset the writer to write to w |
| `DefaultCompression` | Default compression level |
| `NoCompression` | No compression |
| `BestSpeed` | Best speed compression |
| `BestCompression` | Best compression |
| `HuffmanOnly` | Huffman encoding only |

---
## Package container/heap

| Code | Description |
|------|-------------|
| `heap.Init(h Interface)` | Initialize a heap |
| `heap.Push(h Interface, x interface{})` | Push an element onto the heap |
| `heap.Pop(h Interface) interface{}` | Pop the minimum element from the heap |
| `heap.Remove(h Interface, i int) interface{}` | Remove the element at index i from the heap |
| `heap.Fix(h Interface, i int)` | Fix the heap invariant after changing element at index i |
| `Interface` | Interface for heap operations |
| `IntHeap` | Integer heap implementation |
| `Float64Heap` | Float64 heap implementation |

---
## Package container/list

| Code | Description |
|------|-------------|
| `list.List` | Doubly linked list |
| `list.New() *List` | Create a new empty list |
| `List.Back() *Element` | Return the last element of the list |
| `List.Front() *Element` | Return the first element of the list |
| `List.Init() *List` | Initialize a list |
| `List.InsertAfter(e *Element, v interface{}) *Element` | Insert a new element after e |
| `List.InsertBefore(e *Element, v interface{}) *Element` | Insert a new element before e |
| `List.Len() int` | Return the number of elements in the list |
| `List.MoveAfter(e, mark *Element)` | Move e after mark |
| `List.MoveBefore(e, mark *Element)` | Move e before mark |
| `List.MoveToBack(e *Element)` | Move e to the back of the list |
| `List.MoveToFront(e *Element)` | Move e to the front of the list |
| `List.PushBack(v interface{}) *Element` | Add a new element at the back of the list |
| `List.PushBackList(other *List)` | Add all elements of other at the back of the list |
| `List.PushFront(v interface{}) *Element` | Add a new element at the front of the list |
| `List.PushFrontList(other *List)` | Add all elements of other at the front of the list |
| `List.Remove(e *Element) interface{}` | Remove e from the list and return its value |
| `Element` | Element of a doubly linked list |
| `Element.Next() *Element` | Return the next element |
| `Element.Prev() *Element` | Return the previous element |
| `Element.Value interface{}` | Return the value of the element |

---
## Package container/ring

| Code | Description |
|------|-------------|
| `ring.Ring` | Circular list (ring) |
| `ring.New(n int) *Ring` | Create a new ring with n elements |
| `Ring.Do(f func(interface{}))` | Call f on each element |
| `Ring.Len() int` | Return the number of elements in the ring |
| `Ring.Link(s *Ring) *Ring` | Connect two rings |
| `Ring.Move(n int) *Ring` | Move n positions forward or backward |
| `Ring.Next() *Ring` | Return the next element |
| `Ring.Prev() *Ring` | Return the previous element |
| `Ring.Value interface{}` | Return the value of the element |

---
## Package context

| Code | Description |
|------|-------------|
| `context.Context` | Context carries a deadline, a cancellation signal, and other values |
| `context.Background() Context` | Return a non-nil, empty Context |
| `context.TODO() Context` | Return a non-nil, empty Context |
| `context.WithCancel(parent Context) (ctx Context, cancel CancelFunc)` | Return a new Context with cancellation |
| `context.WithDeadline(parent Context, d time.Time) (Context, CancelFunc)` | Return a new Context with deadline |
| `context.WithDeadlineCause(parent Context, d time.Time, cause error) (Context, CancelFunc)` | Return a new Context with deadline and cause |
| `context.WithTimeout(parent Context, timeout time.Duration) (Context, CancelFunc)` | Return a new Context with timeout |
| `context.WithTimeoutCause(parent Context, timeout time.Duration, cause error) (Context, CancelFunc)` | Return a new Context with timeout and cause |
| `context.WithValue(parent Context, key, val any) Context` | Return a new Context with key-value pair |
| `context.CancelFunc` | Function type for canceling a Context |
| `context.Canceled` | Error returned when a Context is canceled |
| `context.DeadlineExceeded` | Error returned when a Context deadline is exceeded |
| `Context.Deadline() (deadline time.Time, ok bool)` | Return the deadline and whether it is set |
| `Context.Done() <-chan struct{}` | Return a channel that is closed when the Context is canceled |
| `Context.Err() error` | Return the error if the Context was canceled |
| `Context.Value(key any) any` | Return the value associated with key |

---
## Package crypto

| Code | Description |
|------|-------------|
| `crypto.RegisterHash(h Hash, f func() hash.Hash)` | Register a hash function |
| `crypto.Hash` | Type for hash functions |
| `crypto.MD5` | MD5 hash |
| `crypto.MD5_New() hash.Hash` | Return a new MD5 hash |
| `crypto.SHA1` | SHA1 hash |
| `crypto.SHA1_New() hash.Hash` | Return a new SHA1 hash |
| `crypto.SHA224` | SHA224 hash |
| `crypto.SHA224_New() hash.Hash` | Return a new SHA224 hash |
| `crypto.SHA256` | SHA256 hash |
| `crypto.SHA256_New() hash.Hash` | Return a new SHA256 hash |
| `crypto.SHA384` | SHA384 hash |
| `crypto.SHA384_New() hash.Hash` | Return a new SHA384 hash |
| `crypto.SHA512` | SHA512 hash |
| `crypto.SHA512_New() hash.Hash` | Return a new SHA512 hash |
| `crypto.SHA512_224` | SHA512/224 hash |
| `crypto.SHA512_224_New() hash.Hash` | Return a new SHA512/224 hash |
| `crypto.SHA512_256` | SHA512/256 hash |
| `crypto.SHA512_256_New() hash.Hash` | Return a new SHA512/256 hash |

---
## Package crypto/aes

| Code | Description |
|------|-------------|
| `aes.BlockSize` | Block size in bytes |
| `aes.KeySizeError` | Error for invalid key size |
| `aes.NewCipher(key []byte) (cipher.Block, error)` | Create a new AES cipher |
| `aes.NewGCM(key []byte) (cipher.AEAD, error)` | Create a new AES-GCM cipher |
| `aes.NewCTR(key []byte) (*ctr, error)` | Create a new AES-CTR stream cipher |

---
## Package crypto/cipher

| Code | Description |
|------|-------------|
| `cipher.Block` | Block cipher interface |
| `cipher.BlockMode` | Block cipher mode interface |
| `cipher.Stream` | Stream cipher interface |
| `cipher.StreamReader` | Stream reader wrapper |
| `cipher.StreamWriter` | Stream writer wrapper |
| `cipher.AEAD` | Authenticated encryption with associated data |
| `cipher.NewCBCEncrypter(block Block, iv []byte) BlockMode` | Create a new CBC encrypter |
| `cipher.NewCBCDecrypter(block Block, iv []byte) BlockMode` | Create a new CBC decrypter |
| `cipher.NewCFBEncrypter(block Block, iv []byte) Stream` | Create a new CFB encrypter |
| `cipher.NewCFBDecrypter(block Block, iv []byte) Stream` | Create a new CFB decrypter |
| `cipher.NewCTR(block Block, iv []byte) Stream` | Create a new CTR stream cipher |
| `cipher.NewECBEncrypter(block Block) BlockMode` | Create a new ECB encrypter |
| `cipher.NewECBDecrypter(block Block) BlockMode` | Create a new ECB decrypter |
| `cipher.NewGCM(block Block) (AEAD, error)` | Create a new GCM cipher |
| `cipher.NewGCMWithNonceSize(block Block, nonceSize int) (AEAD, error)` | Create a new GCM cipher with nonce size |
| `cipher.NewOFB(block Block, iv []byte) Stream` | Create a new OFB stream cipher |
| `cipher.NewReader(block BlockMode, iv []byte) *StreamReader` | Create a new stream reader |
| `cipher.NewWriter(block BlockMode, iv []byte) *StreamWriter` | Create a new stream writer |
| `cipher.PKCS7Padding` | PKCS#7 padding |
| `cipher.PKCS5Padding` | PKCS#5 padding (alias for PKCS7Padding) |
| `cipher.ISO97971Padding` | ISO9797-1 padding |

---
## Package crypto/des

| Code | Description |
|------|-------------|
| `des.BlockSize` | Block size in bytes |
| `des.KeySizeError` | Error for invalid key size |
| `des.NewCipher(key []byte) (cipher.Block, error)` | Create a new DES cipher |
| `des.NewTripleDESCipher(key []byte) (cipher.Block, error)` | Create a new Triple DES cipher |

---
## Package crypto/dsa

| Code | Description |
|------|-------------|
| `dsa.PrivateKey` | DSA private key |
| `dsa.PublicKey` | DSA public key |
| `dsa.Parameters` | DSA parameters |
| `dsa.Sign(priv *PrivateKey, hash []byte) (r, s *big.Int, err error)` | Sign a hash using DSA |
| `dsa.Verify(pub *PublicKey, hash []byte, r, s *big.Int) bool` | Verify a DSA signature |
| `dsa.GenerateParameters(params *Parameters, rand io.Reader, bits int)` | Generate DSA parameters |
| `dsa.GenerateKey(priv *PrivateKey, rand io.Reader, bits int) (*PrivateKey, error)` | Generate a DSA key |
| `dsa.MarshalPrivateKey(priv *PrivateKey) ([]byte, error)` | Marshal a DSA private key to ASN.1 |
| `dsa.ParsePrivateKey(priv []byte) (*PrivateKey, error)` | Parse a DSA private key from ASN.1 |
| `dsa.MarshalPublicKey(pub *PublicKey) ([]byte, error)` | Marshal a DSA public key to ASN.1 |
| `dsa.ParsePublicKey(pub []byte) (*PublicKey, error)` | Parse a DSA public key from ASN.1 |
| `dsa.L1024x160` | 1024-bit L, 160-bit N parameters |
| `dsa.L2048x224` | 2048-bit L, 224-bit N parameters |
| `dsa.L2048x256` | 2048-bit L, 256-bit N parameters |
| `dsa.L3072x256` | 3072-bit L, 256-bit N parameters |

---
## Package crypto/ecdsa

| Code | Description |
|------|-------------|
| `ecdsa.PrivateKey` | ECDSA private key |
| `ecdsa.PublicKey` | ECDSA public key |
| `ecdsa.Curve` | Elliptic curve |
| `ecdsa.Sign(priv *PrivateKey, hash []byte) (r, s *big.Int, err error)` | Sign a hash using ECDSA |
| `ecdsa.Verify(pub *PublicKey, hash []byte, r, s *big.Int) bool` | Verify an ECDSA signature |
| `ecdsa.GenerateKey(c elliptic.Curve, rand io.Reader) (*PrivateKey, error)` | Generate an ECDSA key |
| `ecdsa.MarshalPrivateKey(priv *PrivateKey) ([]byte, error)` | Marshal an ECDSA private key to ASN.1 |
| `ecdsa.ParsePrivateKey(priv []byte) (*PrivateKey, error)` | Parse an ECDSA private key from ASN.1 |
| `ecdsa.MarshalPublicKey(pub *PublicKey) ([]byte, error)` | Marshal an ECDSA public key to ASN.1 |
| `ecdsa.ParsePublicKey(pub []byte) (*PublicKey, error)` | Parse an ECDSA public key from ASN.1 |
| `ecdsa.P224()` | Return the P-224 curve |
| `ecdsa.P256()` | Return the P-256 curve |
| `ecdsa.P384()` | Return the P-384 curve |
| `ecdsa.P521()` | Return the P-521 curve |

---
## Package crypto/ed25519

| Code | Description |
|------|-------------|
| `ed25519.PrivateKey` | Ed25519 private key |
| `ed25519.PublicKey` | Ed25519 public key |
| `ed25519.Sign(priv PrivateKey, message []byte) []byte` | Sign a message using Ed25519 |
| `ed25519.Verify(pub PublicKey, message, sig []byte) bool` | Verify an Ed25519 signature |
| `ed25519.GenerateKey(rand io.Reader) (PublicKey, PrivateKey, error)` | Generate an Ed25519 key pair |
| `ed25519.NewKeyFromSeed(seed []byte) PrivateKey` | Create a private key from a seed |
| `ed25519.SeedSize` | Size of a seed in bytes |
| `ed25519.PrivateKeySize` | Size of a private key in bytes |
| `ed25519.PublicKeySize` | Size of a public key in bytes |
| `ed25519.SignatureSize` | Size of a signature in bytes |

---
## Package crypto/elliptic

| Code | Description |
|------|-------------|
| `elliptic.Curve` | Elliptic curve interface |
| `elliptic.P224()` | Return the P-224 curve |
| `elliptic.P256()` | Return the P-256 curve |
| `elliptic.P384()` | Return the P-384 curve |
| `elliptic.P521()` | Return the P-521 curve |
| `elliptic.Marshal(c Curve, x, y *big.Int) []byte` | Marshal a point to uncompressed form |
| `elliptic.Unmarshal(c Curve, data []byte) (x, y *big.Int)` | Unmarshal a point from uncompressed form |
| `elliptic.MarshalCompressed(c Curve, x, y *big.Int) []byte` | Marshal a point to compressed form |
| `elliptic.UnmarshalCompressed(c Curve, data []byte) (x, y *big.Int, err error)` | Unmarshal a point from compressed form |
| `elliptic.IsOnCurve(c Curve, x, y *big.Int) bool` | Check if a point is on the curve |
| `elliptic.Add(c Curve, x1, y1, x2, y2 *big.Int) (x, y *big.Int)` | Add two points on the curve |
| `elliptic.Double(c Curve, x, y *big.Int) (x, y *big.Int)` | Double a point on the curve |
| `elliptic.ScalarMult(c Curve, x, y *big.Int, k []byte) (x, y *big.Int)` | Scalar multiplication on the curve |
| `elliptic.ScalarBaseMult(c Curve, k []byte) (x, y *big.Int)` | Scalar multiplication of the base point |
| `elliptic.GenerateFieldElement(c Curve, rand io.Reader) *big.Int` | Generate a random field element |

---
## Package crypto/hmac

| Code | Description |
|------|-------------|
| `hmac.New(h func() hash.Hash, key []byte) hash.Hash` | Create a new HMAC hash |
| `hmac.Equal(a, b []byte) bool` | Compare two MACs for equality in constant time |
| `hmac.SHA1` | HMAC-SHA1 hash |
| `hmac.SHA256` | HMAC-SHA256 hash |
| `hmac.SHA384` | HMAC-SHA384 hash |
| `hmac.SHA512` | HMAC-SHA512 hash |
| `hmac.MD5` | HMAC-MD5 hash |

---
## Package crypto/md5

| Code | Description |
|------|-------------|
| `md5.New() hash.Hash` | Return a new MD5 hash |
| `md5.Sum(data []byte) [Size]byte` | Return the MD5 checksum of data |
| `md5.Size` | Size of an MD5 checksum in bytes |
| `md5.BlockSize` | Block size of MD5 in bytes |

---
## Package crypto/rand

| Code | Description |
|------|-------------|
| `rand.Reader` | Cryptographically secure random number generator |
| `rand.Int(rand io.Reader, max *big.Int) (*big.Int, error)` | Return a random big.Int in [0, max) |
| `rand.Prime(rand io.Reader, bits int) (*big.Int, error)` | Return a random prime number with the given number of bits |
| `rand.Int(rand io.Reader, max *big.Int) (*big.Int, error)` | Return a random big.Int in [0, max) |
| `rand.Int63() int64` | Return a random int64 |
| `rand.Int31() int32` | Return a random int32 |
| `rand.Uint32() uint32` | Return a random uint32 |
| `rand.Uint64() uint64` | Return a random uint64 |
| `rand.Float32() float32` | Return a random float32 in [0.0, 1.0) |
| `rand.Float64() float64` | Return a random float64 in [0.0, 1.0) |
| `rand.Perm(n int) []int` | Return a random permutation of [0, n) |
| `rand.Shuffle(n int, swap func(i, j int))` | Shuffle a slice |
| `rand.Read(b []byte) (n int, err error)` | Fill b with random bytes |
| `rand.Prime(rand io.Reader, bits int) (*big.Int, error)` | Return a random prime number |

---
## Package crypto/rc4

| Code | Description |
|------|-------------|
| `rc4.EncryptedKey` | RC4 encrypted key |
| `rc4.NewCipher(key []byte) (*Cipher, error)` | Create a new RC4 cipher |
| `Cipher.XORKeyStream(dst, src []byte)` | XORKeyStream XORs the bytes in src with the key stream and writes the result to dst |

---
## Package crypto/rsa

| Code | Description |
|------|-------------|
| `rsa.PrivateKey` | RSA private key |
| `rsa.PublicKey` | RSA public key |
| `rsa.SignPKCS1v15(rand io.Reader, priv *PrivateKey, hash crypto.Hash, digest []byte) ([]byte, error)` | Sign a hash using PKCS#1 v1.5 |
| `rsa.VerifyPKCS1v15(pub *PublicKey, hash crypto.Hash, digest, sig []byte) error` | Verify a PKCS#1 v1.5 signature |
| `rsa.SignPSS(rand io.Reader, priv *PrivateKey, hash crypto.Hash, digest []byte, opts *PSSOptions) ([]byte, error)` | Sign a hash using PSS |
| `rsa.VerifyPSS(pub *PublicKey, hash crypto.Hash, digest, sig []byte, opts *PSSOptions) error` | Verify a PSS signature |
| `rsa.EncryptPKCS1v15(rand io.Reader, pub *PublicKey, msg []byte) ([]byte, error)` | Encrypt a message using PKCS#1 v1.5 |
| `rsa.DecryptPKCS1v15(rand io.Reader, priv *PrivateKey, ciphertext []byte) ([]byte, error)` | Decrypt a PKCS#1 v1.5 encrypted message |
| `rsa.EncryptOAEP(hash crypto.Hash, rand io.Reader, pub *PublicKey, msg []byte, label []byte) ([]byte, error)` | Encrypt a message using OAEP |
| `rsa.DecryptOAEP(hash crypto.Hash, rand io.Reader, priv *PrivateKey, ciphertext, label []byte) ([]byte, error)` | Decrypt an OAEP encrypted message |
| `rsa.GenerateKey(rand io.Reader, bits int) (*PrivateKey, error)` | Generate an RSA key |
| `rsa.GenerateMultiPrimeKey(rand io.Reader, bits int, nprimes int) (*PrivateKey, error)` | Generate a multi-prime RSA key |
| `rsa.MarshalPKCS1PrivateKey(priv *PrivateKey) []byte` | Marshal a private key to PKCS#1 format |
| `rsa.ParsePKCS1PrivateKey(priv []byte) (*PrivateKey, error)` | Parse a private key from PKCS#1 format |
| `rsa.MarshalPKCS8PrivateKey(priv *PrivateKey) ([]byte, error)` | Marshal a private key to PKCS#8 format |
| `rsa.ParsePKCS8PrivateKey(priv []byte) (*PrivateKey, error)` | Parse a private key from PKCS#8 format |
| `rsa.MarshalPKCS1PublicKey(pub *PublicKey) []byte` | Marshal a public key to PKCS#1 format |
| `rsa.ParsePKCS1PublicKey(pub []byte) (*PublicKey, error)` | Parse a public key from PKCS#1 format |
| `rsa.PSSOptions` | Options for PSS signature scheme |
| `Size` | Size of an RSA key in bits |

---
## Package crypto/sha1

| Code | Description |
|------|-------------|
| `sha1.New() hash.Hash` | Return a new SHA1 hash |
| `sha1.Sum(data []byte) [Size]byte` | Return the SHA1 checksum of data |
| `sha1.Size` | Size of a SHA1 checksum in bytes |
| `sha1.BlockSize` | Block size of SHA1 in bytes |

---
## Package crypto/sha256

| Code | Description |
|------|-------------|
| `sha256.New() hash.Hash` | Return a new SHA256 hash |
| `sha256.Sum224(data []byte) [Size224]byte` | Return the SHA224 checksum of data |
| `sha256.Sum256(data []byte) [Size]byte` | Return the SHA256 checksum of data |
| `sha256.Size` | Size of a SHA256 checksum in bytes |
| `sha256.Size224` | Size of a SHA224 checksum in bytes |
| `sha256.BlockSize` | Block size of SHA256 in bytes |

---
## Package crypto/sha512

| Code | Description |
|------|-------------|
| `sha512.New() hash.Hash` | Return a new SHA512 hash |
| `sha512.New384() hash.Hash` | Return a new SHA384 hash |
| `sha512.New512_224() hash.Hash` | Return a new SHA512/224 hash |
| `sha512.New512_256() hash.Hash` | Return a new SHA512/256 hash |
| `sha512.Sum384(data []byte) [Size384]byte` | Return the SHA384 checksum of data |
| `sha512.Sum512(data []byte) [Size]byte` | Return the SHA512 checksum of data |
| `sha512.Sum512_224(data []byte) [Size224]byte` | Return the SHA512/224 checksum of data |
| `sha512.Sum512_256(data []byte) [Size256]byte` | Return the SHA512/256 checksum of data |
| `sha512.Size` | Size of a SHA512 checksum in bytes |
| `sha512.Size224` | Size of a SHA512/224 checksum in bytes |
| `sha512.Size256` | Size of a SHA512/256 checksum in bytes |
| `sha512.Size384` | Size of a SHA384 checksum in bytes |
| `sha512.BlockSize` | Block size of SHA512 in bytes |

---
## Package crypto/subtle

| Code | Description |
|------|-------------|
| `subtle.ConstantTimeByteEq(a, b uint8) int` | Compare two bytes in constant time |
| `subtle.ConstantTimeEq(a, b int32) int` | Compare two int32 in constant time |
| `subtle.ConstantTimeSelect(v, x, y int32) int32` | Select x or y based on v in constant time |
| `subtle.ConstantTimeCompare(a, b []byte) int` | Compare two byte slices in constant time |
| `subtle.ConstantTimeCopy(v int, x, y *byte)` | Copy a byte in constant time |
| `subtle.ConstantTimeCopyN(v int, x, y []byte)` | Copy n bytes in constant time |
| `subtle.XORBytes(dst, a, b []byte) int` | XOR bytes in constant time |

---
## Package crypto/tls

| Code | Description |
|------|-------------|
| `tls.Certificate` | Certificate for TLS |
| `tls.Client` | TLS client connection |
| `tls.ClientAuthType` | Client authentication type |
| `tls.Config` | Configuration for TLS |
| `tls.Conn` | TLS connection |
| `tls.ConnectionState` | Connection state |
| `tls.CurveID` | Elliptic curve identifier |
| `tls.Dial(network, addr string, config *Config) (*Conn, error)` | Dial and establish a TLS connection |
| `tls.DialWithDialer(dialer *net.Dialer, network, addr string, config *Config) (*Conn, error)` | Dial with custom dialer |
| `tls.Listen(network, laddr string, config *Config) (net.Listener, error)` | Listen for TLS connections |
| `tls.NewListener(inner net.Listener, config *Config) net.Listener` | Create a TLS listener |
| `tls.Serve(l net.Listener, config *Config) error` | Serve TLS connections |
| `tls.Accept(conn net.Conn) (*Conn, error)` | Accept a TLS connection |
| `tls.Client(netConn net.Conn, config *Config) (*Conn, error)` | Create a TLS client connection |
| `tls.Server(netConn net.Conn, config *Config) (*Conn, error)` | Create a TLS server connection |
| `tls.NewCertPool() *CertPool` | Create a new certificate pool |
| `tls.SystemCertPool() *CertPool` | Return the system certificate pool |
| `tls.X509KeyPair(certPEMBlock, keyPEMBlock []byte) (tls.Certificate, error)` | Parse a certificate and private key |
| `tls.LoadX509KeyPair(certFile, keyFile string) (Certificate, error)` | Load a certificate and private key from files |
| `tls.CertPool` | Certificate pool |
| `tls.CertPool.AppendCertsFromPEM(pemCerts []byte) bool` | Append certificates from PEM data |
| `tls.CertPool.AddCert(cert *x509.Certificate)` | Add a certificate to the pool |
| `tls.CertPool.Subjects() [][]byte` | Return the subjects of certificates in the pool |
| `tls.CipherSuite` | Cipher suite |
| `tls.CipherSuites() []*CipherSuite` | Return all cipher suites |
| `tls.CipherSuiteID` | Cipher suite ID |
| `tls.InsecureCipherSuites()` | Return insecure cipher suites |
| `tls.Version` | TLS version |
| `tls.VersionTLS10` | TLS 1.0 |
| `tls.VersionTLS11` | TLS 1.1 |
| `tls.VersionTLS12` | TLS 1.2 |
| `tls.VersionTLS13` | TLS 1.3 |

---
## Package crypto/x509

| Code | Description |
|------|-------------|
| `x509.Certificate` | X.509 certificate |
| `x509.CertificateRequest` | X.509 certificate request |
| `x509.RevocationList` | X.509 certificate revocation list |
| `x509.ParseCertificate(cert []byte) (*Certificate, error)` | Parse an X.509 certificate |
| `x509.ParseCertificates(certs []byte) ([]*Certificate, error)` | Parse multiple X.509 certificates |
| `x509.ParseCertificateRequest(csr []byte) (*CertificateRequest, error)` | Parse a PKCS#10 certificate request |
| `x509.ParseRevocationList(der []byte) (*RevocationList, error)` | Parse a revocation list |
| `x509.CreateCertificate(rand io.Reader, template, parent *Certificate, pub, priv any) (cert []byte, err error)` | Create a new certificate |
| `x509.CreateCertificateRequest(rand io.Reader, template *CertificateRequest, priv any) (csr []byte, err error)` | Create a new certificate request |
| `x509.MarshalPKCS1PrivateKey(priv *rsa.PrivateKey) []byte` | Marshal a private key to PKCS#1 format |
| `x509.ParsePKCS1PrivateKey(der []byte) (*rsa.PrivateKey, error)` | Parse a private key from PKCS#1 format |
| `x509.MarshalPKCS8PrivateKey(priv any) ([]byte, error)` | Marshal a private key to PKCS#8 format |
| `x509.ParsePKCS8PrivateKey(der []byte) (any, error)` | Parse a private key from PKCS#8 format |
| `x509.MarshalECPrivateKey(priv *ecdsa.PrivateKey) ([]byte, error)` | Marshal an EC private key |
| `x509.ParseECPrivateKey(der []byte) (*ecdsa.PrivateKey, error)` | Parse an EC private key |
| `x509.EncryptPEMBlock(rand io.Reader, blockType string, data, password []byte, pemType PEMCipher) ([]byte, error)` | Encrypt a PEM block |
| `x509.DecryptPEMBlock(block *pem.Block, password []byte) ([]byte, error)` | Decrypt a PEM block |
| `x509.IsEncryptedPEMBlock(block *pem.Block) bool` | Check if a PEM block is encrypted |
| `x509.InsecureCipherSuites()` | Return insecure cipher suites |
| `x509.SignatureAlgorithm` | Signature algorithm |
| `x509.SignatureAlgorithmFromOID(oid asn1.ObjectIdentifier) SignatureAlgorithm` | Get signature algorithm from OID |
| `x509.SystemCertPool() *CertPool` | Return the system certificate pool |
| `x509.NewCertPool() *CertPool` | Create a new certificate pool |
| `x509.CertPool` | Certificate pool |
| `x509.CertPool.AddCert(cert *Certificate)` | Add a certificate to the pool |
| `x509.CertPool.AppendCertsFromPEM(pemCerts []byte) bool` | Append certificates from PEM data |
| `x509.CertPool.Subjects() [][]byte` | Return the subjects of certificates in the pool |
| `x509.KeyUsage` | Key usage |
| `x509.ExtKeyUsage` | Extended key usage |
| `x509.UnknownExtKeyUsage` | Unknown extended key usage |
| `x509.ExtKeyUsageAny` | Any extended key usage |
| `x509.ExtKeyUsageServerAuth` | Server authentication |
| `x509.ExtKeyUsageClientAuth` | Client authentication |
| `x509.ExtKeyUsageCodeSigning` | Code signing |
| `x509.ExtKeyUsageEmailProtection` | Email protection |
| `x509.ExtKeyUsageIPSecEndSystem` | IPsec end system |
| `x509.ExtKeyUsageIPSecTunnel` | IPsec tunnel |
| `x509.ExtKeyUsageIPSecUser` | IPsec user |
| `x509.ExtKeyUsageTimeStamping` | Time stamping |
| `x509.ExtKeyUsageOCSPSigning` | OCSP signing |

---
## Package crypto/x509/pkix

| Code | Description |
|------|-------------|
| `pkix.Name` | ASN.1 representation of a Name |
| `pkix.AttributeTypeAndValue` | Attribute type and value |
| `pkix.AlgorithmIdentifier` | Algorithm identifier |
| `pkix.RDNSequence` | Relative distinguished name sequence |
| `pkix.Set` | ASN.1 SET |
| `pkix.Null` | ASN.1 NULL |

---
## Package database/sql

| Code | Description |
|------|-------------|
| `sql.DB` | Database connection pool |
| `sql.Tx` | Transaction |
| `sql.Stmt` | Prepared statement |
| `sql.Rows` | Rows returned from a query |
| `sql.Row` | Single row from a query |
| `sql.Result` | Result from an exec or query |
| `sql.Open(driverName, dataSourceName string) (*DB, error)` | Open a database connection |
| `sql.OpenDB(c driver.Connector) *DB` | Open a database connection with a connector |
| `sql.Register(driverName string, driver driver.Driver)` | Register a database driver |
| `sql.Drivers() []string` | Return the list of registered drivers |
| `DB.Ping() error` | Ping the database |
| `DB.PingContext(ctx context.Context) error` | Ping the database with context |
| `DB.Close() error` | Close the database connection |
| `DB.Exec(query string, args ...any) (Result, error)` | Execute a query without returning rows |
| `DB.ExecContext(ctx context.Context, query string, args ...any) (Result, error)` | Execute a query with context |
| `DB.Query(query string, args ...any) (*Rows, error)` | Execute a query that returns rows |
| `DB.QueryContext(ctx context.Context, query string, args ...any) (*Rows, error)` | Execute a query with context |
| `DB.QueryRow(query string, args ...any) *Row` | Execute a query that is expected to return at most one row |
| `DB.QueryRowContext(ctx context.Context, query string, args ...any) *Row` | Execute a query with context |
| `DB.Prepare(query string) (*Stmt, error)` | Prepare a statement for later execution |
| `DB.PrepareContext(ctx context.Context, query string) (*Stmt, error)` | Prepare a statement with context |
| `DB.Begin() (*Tx, error)` | Start a transaction |
| `DB.BeginTx(ctx context.Context, opts *TxOptions) (*Tx, error)` | Start a transaction with options |
| `DB.BeginContext(ctx context.Context) (*Tx, error)` | Start a transaction with context |
| `DB.Stats() *DBStats` | Return database statistics |
| `DB.SetMaxIdleConns(n int)` | Set the maximum number of idle connections |
| `DB.SetMaxOpenConns(n int)` | Set the maximum number of open connections |
| `DB.SetConnMaxLifetime(d time.Duration)` | Set the maximum lifetime of connections |
| `DB.SetConnMaxIdleTime(d time.Duration)` | Set the maximum idle time of connections |
| `DB.SetMaxIdleConns(n int)` | Set the maximum number of idle connections |
| `Tx.Commit() error` | Commit the transaction |
| `Tx.Rollback() error` | Rollback the transaction |
| `Tx.Exec(query string, args ...any) (Result, error)` | Execute a query in the transaction |
| `Tx.ExecContext(ctx context.Context, query string, args ...any) (Result, error)` | Execute a query with context |
| `Tx.Query(query string, args ...any) (*Rows, error)` | Execute a query that returns rows in the transaction |
| `Tx.QueryContext(ctx context.Context, query string, args ...any) (*Rows, error)` | Execute a query with context |
| `Tx.QueryRow(query string, args ...any) *Row` | Execute a query that returns at most one row in the transaction |
| `Tx.QueryRowContext(ctx context.Context, query string, args ...any) *Row` | Execute a query with context |
| `Tx.Prepare(query string) (*Stmt, error)` | Prepare a statement in the transaction |
| `Tx.PrepareContext(ctx context.Context, query string) (*Stmt, error)` | Prepare a statement with context |
| `Tx.Stmt(stmt *Stmt) *Stmt` | Return a transaction-specific statement |
| `Stmt.Exec(args ...any) (Result, error)` | Execute a prepared statement |
| `Stmt.ExecContext(ctx context.Context, args ...any) (Result, error)` | Execute a prepared statement with context |
| `Stmt.Query(args ...any) (*Rows, error)` | Execute a prepared statement that returns rows |
| `Stmt.QueryContext(ctx context.Context, args ...any) (*Rows, error)` | Execute a prepared statement with context |
| `Stmt.QueryRow(args ...any) *Row` | Execute a prepared statement that returns at most one row |
| `Stmt.QueryRowContext(ctx context.Context, args ...any) *Row` | Execute a prepared statement with context |
| `Stmt.Close() error` | Close the statement |
| `Rows.Next() bool` | Prepare the next result row for reading |
| `Rows.NextResultSet() bool` | Prepare the next result set for reading |
| `Rows.Scan(dest ...any) error` | Copy the columns from the current row into dest |
| `Rows.Close() error` | Close the rows |
| `Rows.Err() error` | Return the error, if any, that caused the rows to stop |
| `Rows.ColumnTypes() ([]*ColumnType, error)` | Return the column types |
| `Rows.Columns() ([]string, error)` | Return the column names |
| `Row.Scan(dest ...any) error` | Copy the columns from the matched row into dest |
| `Result.LastInsertId() (int64, error)` | Return the integer last insert id |
| `Result.RowsAffected() (int64, error)` | Return the number of rows affected |
| `NullString` | String that may be null |
| `NullInt64` | Int64 that may be null |
| `NullInt32` | Int32 that may be null |
| `NullInt16` | Int16 that may be null |
| `NullFloat64` | Float64 that may be null |
| `NullBool` | Bool that may be null |
| `NullTime` | Time that may be null |
| `NullByteSlice` | []byte that may be null |
| `IsolationLevel` | Transaction isolation level |
| `LevelDefault` | Default isolation level |
| `LevelReadUncommitted` | Read uncommitted isolation level |
| `LevelReadCommitted` | Read committed isolation level |
| `LevelRepeatableRead` | Repeatable read isolation level |
| `LevelSerializable` | Serializable isolation level |
| `LevelSnapshot` | Snapshot isolation level |
| `LevelLinearizable` | Linearizable isolation level |

---
## Package database/sql/driver

| Code | Description |
|------|-------------|
| `driver.Driver` | Interface for database drivers |
| `driver.Connector` | Interface for database connectors |
| `driver.Execer` | Interface for executing queries |
| `driver.Queryer` | Interface for executing queries that return rows |
| `driver.Stmt` | Prepared statement |
| `driver.Tx` | Transaction |
| `driver.Value` | Value that can be converted to a driver value |
| `driver.ValueConverter` | Interface for converting values |
| `driver.Rows` | Rows returned from a query |
| `driver.RowsNextResultSet` | Interface for moving to next result set |
| `driver.RowsColumnTypeDatabaseTypeName` | Interface for returning database type name |
| `driver.RowsColumnTypeLength` | Interface for returning column type length |
| `driver.RowsColumnTypeNullable` | Interface for returning if column type is nullable |
| `driver.RowsColumnTypePrecisionScale` | Interface for returning precision and scale |
| `driver.RowsColumnTypeScanType` | Interface for returning scan type |
| `driver.Result` | Result from an exec or query |
| `driver.Pinger` | Interface for pinging the database |
| `driver.Validator` | Interface for validating connections |
| `driver.Conn` | Database connection |
| `driver.ConnBeginTx` | Interface for beginning transactions |
| `driver.ConnPrepareContext` | Interface for preparing statements |
| `driver.ConnExecContext` | Interface for executing queries |
| `driver.ConnQueryContext` | Interface for executing queries that return rows |
| `driver.IsolationLevel` | Isolation level |
| `driver.DefaultParameterConverter` | Default parameter converter |

---
## Package debug/dwarf

| Code | Description |
|------|-------------|
| `dwarf.Data` | DWARF debugging data |
| `dwarf.Entry` | DWARF entry |
| `dwarf.Reader` | DWARF reader |
| `dwarf.New(r io.ReaderAt, littleEndian bool) (*Data, error)` | Create a new Data from a reader |
| `dwarf.Data.AddrSize() int` | Return the address size |
| `dwarf.Data.Reader() *Reader` | Return a new Reader |
| `dwarf.Data.LineReader() (*LineReader, error)` | Return a new LineReader |
| `dwarf.Data.Ranges() ([]*Range, error)` | Return the address ranges |
| `dwarf.Data.Types() ([]*Type, error)` | Return the type entries |
| `dwarf.Reader.SeekOffset(offset int64)` | Seek to an offset |
| `dwarf.Reader.Next() (*Entry, error)` | Read the next entry |
| `dwarf.Reader.SkipChildren() error` | Skip the children of the current entry |
| `dwarf.LineReader` | DWARF line reader |
| `dwarf.LineReader.Next(pc *uint64) (bool, error)` | Read the next line table entry |
| `dwarf.LineReader.Reset()` | Reset the line reader |
| `dwarf.LineReader.Seek(pc uint64) error` | Seek to a program counter |
| `dwarf.Range` | Address range |
| `dwarf.Type` | Type entry |
| `dwarf.Class` | Type class |
| `dwarf.Tag` | DWARF tag |
| `dwarf.Attr` | DWARF attribute |
| `dwarf.Format` | DWARF format |
| `dwarf.ErrUnknownFormat` | Error for unknown format |

---
## Package debug/elf

| Code | Description |
|------|-------------|
| `elf.File` | ELF file |
| `elf.NewFile(r io.ReaderAt) (*File, error)` | Create a new File from a reader |
| `elf.File.Close()` | Close the file |
| `elf.File.Section(name string) *Section` | Return a section by name |
| `elf.File.Symbols() ([]Symbol, error)` | Return the symbols |
| `elf.File.DynamicSymbols() ([]Symbol, error)` | Return the dynamic symbols |
| `elf.File.ImportedSymbols() ([]ImportedSymbol, error)` | Return the imported symbols |
| `elf.File.ImportedLibraries() ([]string, error)` | Return the imported libraries |
| `elf.File.Type() Type` | Return the file type |
| `elf.File.Machine() Machine` | Return the machine type |
| `elf.File.Class() Class` | Return the class |
| `elf.File.Data() Data` | Return the data encoding |
| `elf.File.Entry() uint64` | Return the entry point |
| `elf.File.DWARF() (*dwarf.Data, error)` | Return the DWARF data |
| `elf.Section` | ELF section |
| `elf.Section.Name` | Section name |
| `elf.Section.Type` | Section type |
| `elf.Section.Flags` | Section flags |
| `elf.Section.Addr` | Section address |
| `elf.Section.Offset` | Section offset |
| `elf.Section.Size` | Section size |
| `elf.Section.Data() ([]byte, error)` | Return the section data |
| `elf.Section.Open() io.ReaderAt` | Open a reader for the section |
| `elf.Symbol` | ELF symbol |
| `elf.Symbol.Name` | Symbol name |
| `elf.Symbol.Value` | Symbol value |
| `elf.Symbol.Size` | Symbol size |
| `elf.Symbol.Info` | Symbol info |
| `elf.Symbol.Other` | Symbol other |
| `elf.Symbol.Section` | Symbol section |
| `elf.ImportedSymbol` | Imported symbol |
| `elf.Prog` | ELF program header |
| `elf.Type` | ELF type |
| `elf.Machine` | ELF machine |
| `elf.Class` | ELF class |
| `elf.Data` | ELF data encoding |
| `elf.SectionType` | ELF section type |
| `elf.SectionFlag` | ELF section flag |
| `elf.SymbolBinding` | ELF symbol binding |
| `elf.SymbolType` | ELF symbol type |
| `elf.SymbolVisibility` | ELF symbol visibility |
| `elf.ProgType` | ELF program type |
| `elf.ProgFlag` | ELF program flag |
| `elf.CompressionType` | ELF compression type |

---
## Package debug/gosym

| Code | Description |
|------|-------------|
| `gosym.Table` | Go symbol table |
| `gosym.LineTable` | Line table |
| `gosym.NewTable(src io.ReaderAt, littleEndian bool) (*Table, error)` | Create a new Table from a reader |
| `gosym.Table.PCToLine(pc uint64) (file string, line int)` | Return the file and line for a program counter |
| `gosym.Table.LineToPC(file string, line int) (pc uint64, fn *Func)` | Return the program counter for a file and line |
| `gosym.Table.PCToFunc(pc uint64) *Func` | Return the function for a program counter |
| `gosym.Table.SymByAddr(addr uint64) *Sym` | Return the symbol for an address |
| `gosym.Table.LookupFunc(name string) *Func` | Return the function by name |
| `gosym.Table.LookupSym(name string) *Sym` | Return the symbol by name |
| `gosym.Func` | Function |
| `gosym.Sym` | Symbol |
| `gosym.Obj` | Object file |

---
## Package debug/macho

| Code | Description |
|------|-------------|
| `macho.File` | Mach-O file |
| `macho.NewFile(r io.ReaderAt) (*File, error)` | Create a new File from a reader |
| `macho.File.Close()` | Close the file |
| `macho.File.Type() Type` | Return the file type |
| `macho.File.Cpu() Cpu` | Return the CPU type |
| `macho.File.SubCpu() uint32` | Return the sub CPU type |
| `macho.File.Entry() uint64` | Return the entry point |
| `macho.File.DWARF() (*dwarf.Data, error)` | Return the DWARF data |
| `macho.File.Section(name string) *Section` | Return a section by name |
| `macho.File.Symbols() ([]Symbol, error)` | Return the symbols |
| `macho.File.ImportedSymbols() ([]ImportedSymbol, error)` | Return the imported symbols |
| `macho.File.ImportedLibraries() ([]string, error)` | Return the imported libraries |
| `macho.Section` | Mach-O section |
| `macho.Section.Name` | Section name |
| `macho.Section.Seg` | Section segment |
| `macho.Section.Addr` | Section address |
| `macho.Section.Size` | Section size |
| `macho.Section.Offset` | Section offset |
| `macho.Section.Align` | Section alignment |
| `macho.Section.Flags` | Section flags |
| `macho.Section.Type` | Section type |
| `macho.Section.Attributes` | Section attributes |
| `macho.Section.Reserve` | Section reserve |
| `macho.Section.Data() ([]byte, error)` | Return the section data |
| `macho.Section.Open() io.ReaderAt` | Open a reader for the section |
| `macho.Symbol` | Mach-O symbol |
| `macho.Symbol.Name` | Symbol name |
| `macho.Symbol.Value` | Symbol value |
| `macho.Symbol.Type` | Symbol type |
| `macho.Symbol.Sect` | Symbol section |
| `macho.Symbol.Desc` | Symbol description |
| `macho.ImportedSymbol` | Imported symbol |
| `macho.Segment` | Mach-O segment |
| `macho.Type` | Mach-O type |
| `macho.Cpu` | Mach-O CPU type |
| `macho.SectionType` | Mach-O section type |
| `macho.SectionAttr` | Mach-O section attribute |
| `macho.SymbolType` | Mach-O symbol type |
| `macho.LoadCmd` | Mach-O load command |
| `macho.LoadCmdType` | Mach-O load command type |

---
## Package debug/pe

| Code | Description |
|------|-------------|
| `pe.File` | PE file |
| `pe.NewFile(r io.ReaderAt) (*File, error)` | Create a new File from a reader |
| `pe.File.Close()` | Close the file |
| `pe.File.DOSHeader` | DOS header |
| `pe.File.NTHeader` | NT header |
| `pe.File.CoffHeader` | COFF header |
| `pe.File.OptionalHeader` | Optional header |
| `pe.File.SectionHeader` | Section header |
| `pe.File.Symbols` | Symbols |
| `pe.File.StringTable` | String table |
| `pe.File.Type()` Type` | Return the file type |
| `pe.File.Machine()` Machine` | Return the machine type |
| `pe.File.Entry()` uint32` | Return the entry point |
| `pe.File.ImageBase() uint64` | Return the image base |
| `pe.File.Section(name string) *Section` | Return a section by name |
| `pe.File.Symbols() ([]*Symbol, error)` | Return the symbols |
| `pe.File.ImportedSymbols() ([]*ImportedSymbol, error)` | Return the imported symbols |
| `pe.File.ImportedLibraries() ([]string, error)` | Return the imported libraries |
| `pe.File.ExportedSymbols() ([]*ExportedSymbol, error)` | Return the exported symbols |
| `pe.Section` | PE section |
| `pe.Section.Name` | Section name |
| `pe.Section.VirtualSize` | Virtual size |
| `pe.Section.VirtualAddress` | Virtual address |
| `pe.Section.Size` | Size of raw data |
| `pe.Section.Offset` | Pointer to raw data |
| `pe.Section.PointerToRelocations` | Pointer to relocation entries |
| `pe.Section.PointerToLineNumbers` | Pointer to line number entries |
| `pe.Section.NumberOfRelocations` | Number of relocation entries |
| `pe.Section.NumberOfLineNumbers` | Number of line number entries |
| `pe.Section.Characteristics` | Characteristics |
| `pe.Section.Data() ([]byte, error)` | Return the section data |
| `pe.Section.Open() io.ReaderAt` | Open a reader for the section |
| `pe.Symbol` | PE symbol |
| `pe.ImportedSymbol` | Imported symbol |
| `pe.ExportedSymbol` | Exported symbol |
| `pe.Type` | PE type |
| `pe.Machine` | PE machine |
| `pe.SectionCharacteristic` | PE section characteristic |
| `pe.SymbolType` | PE symbol type |
| `pe.SymbolClass` | PE symbol class |
| `pe.SymbolSectionNumber` | PE symbol section number |
| `pe.DataDirectoryType` | PE data directory type |

---
## Package debug/plan9obj

| Code | Description |
|------|-------------|
| `plan9obj.NewFile(r io.ReaderAt) (*File, error)` | Create a new File from a reader |
| `plan9obj.File.Close()` | Close the file |
| `plan9obj.File.Symbols() ([]*Symbol, error)` | Return the symbols |
| `plan9obj.File.Text() ([]byte, error)` | Return the text section |
| `plan9obj.Symbol` | Plan 9 symbol |
| `plan9obj.Symbol.Name` | Symbol name |
| `plan9obj.Symbol.Value` | Symbol value |
| `plan9obj.Symbol.Type` | Symbol type |

---
## Package encoding

| Code | Description |
|------|-------------|
| `encoding.BinaryMarshaler` | Interface for binary marshaling |
| `encoding.BinaryUnmarshaler` | Interface for binary unmarshaling |
| `encoding.TextMarshaler` | Interface for text marshaling |
| `encoding.TextUnmarshaler` | Interface for text unmarshaling |

---
## Package encoding/base64

| Code | Description |
|------|-------------|
| `base64.NewEncoding(encoder string)` | Create a new base64 encoding |
| `base64.StdEncoding` | Standard base64 encoding |
| `base64.URLEncoding` | URL-safe base64 encoding |
| `base64.RawStdEncoding` | Standard base64 encoding without padding |
| `base64.RawURLEncoding` | URL-safe base64 encoding without padding |
| `base64.NewEncoder(enc *Encoding, w io.Writer) io.WriteCloser` | Create a new base64 encoder |
| `base64.NewDecoder(enc *Encoding, r io.Reader) io.Reader` | Create a new base64 decoder |
| `base64.Encode(dst, src []byte)` | Encode src into dst |
| `base64.EncodeToString(src []byte) string` | Encode src to a string |
| `base64.Decode(dst, src []byte) (n int, err error)` | Decode src into dst |
| `base64.DecodeString(s string) ([]byte, error)` | Decode a string |
| `base64.CorruptInputError` | Error for corrupt input |

---
## Package encoding/base32

| Code | Description |
|------|-------------|
| `base32.NewEncoding(encoder string)` | Create a new base32 encoding |
| `base32.StdEncoding` | Standard base32 encoding |
| `base32.HexEncoding` | Hex base32 encoding |
| `base32.NewEncoder(enc *Encoding, w io.Writer) io.WriteCloser` | Create a new base32 encoder |
| `base32.NewDecoder(enc *Encoding, r io.Reader) io.Reader` | Create a new base32 decoder |
| `base32.Encode(dst, src []byte)` | Encode src into dst |
| `base32.EncodeToString(src []byte) string` | Encode src to a string |
| `base32.Decode(dst, src []byte) (n int, err error)` | Decode src into dst |
| `base32.DecodeString(s string) ([]byte, error)` | Decode a string |
| `base32.CorruptInputError` | Error for corrupt input |

---
## Package encoding/binary

| Code | Description |
|------|-------------|
| `binary.Append(varintBuf, val uint64) []byte` | Append a varint to a buffer |
| `binary.PutVarint(buf []byte, x uint64)` | Write a varint to a buffer |
| `binary.Varint(buf []byte) (uint64, int)` | Read a varint from a buffer |
| `binary.Uvarint(buf []byte) (uint64, int)` | Read an unsigned varint from a buffer |
| `binary.PutUvarint(buf []byte, x uint64)` | Write an unsigned varint to a buffer |
| `binary.Read(r io.Reader, order ByteOrder, data any) error` | Read data from a reader |
| `binary.Write(w io.Writer, order ByteOrder, data any) error` | Write data to a writer |
| `binary.Size(v any) int` | Return the size of v in bytes |
| `binary.ReadVarint(r io.ByteReader) (uint64, error)` | Read a varint from a reader |
| `binary.WriteVarint(w io.Writer, x uint64) error` | Write a varint to a writer |
| `ByteOrder` | Byte order |
| `LittleEndian` | Little-endian byte order |
| `BigEndian` | Big-endian byte order |

---
## Package encoding/csv

| Code | Description |
|------|-------------|
| `csv.Reader` | CSV reader |
| `csv.Writer` | CSV writer |
| `csv.NewReader(r io.Reader) *Reader` | Create a new CSV reader |
| `csv.NewWriter(w io.Writer) *Writer` | Create a new CSV writer |
| `Reader.Read() (record []string, err error)` | Read a record |
| `Reader.ReadAll() ([][]string, error)` | Read all records |
| `Reader.FieldsPerRecord() (int, bool)` | Return the number of fields per record |
| `Reader.HasHeader() bool` | Return whether the CSV has a header |
| `Reader.ReadHeader() ([]string, error)` | Read the header |
| `Writer.Write(record []string) error` | Write a record |
| `Writer.WriteAll(records [][]string) error` | Write all records |
| `Writer.Flush() error` | Flush the writer |
| `Writer.Error() error` | Return the first error encountered |
| `ParseError` | CSV parse error |
| `ErrTrailingComma` | Error for trailing comma |
| `ErrBareQuote` | Error for bare quote |
| `ErrQuote` | Error for quote |
| `ErrFieldCount` | Error for field count |

---
## Package encoding/gob

| Code | Description |
|------|-------------|
| `gob.NewDecoder(r io.Reader) *Decoder` | Create a new gob decoder |
| `gob.NewEncoder(w io.Writer) *Encoder` | Create a new gob encoder |
| `Decoder.Decode(e any) error` | Decode data into e |
| `Decoder.DecodeValue(v reflect.Value) error` | Decode data into v |
| `Encoder.Encode(e any) error` | Encode e |
| `Encoder.EncodeValue(v reflect.Value) error` | Encode v |
| `gob.Register(v any)` | Register a type for encoding/decoding |
| `gob.RegisterName(name string, v any)` | Register a type with a name |
| `Name` | Type name |

---
## Package encoding/hex

| Code | Description |
|------|-------------|
| `hex.NewEncoder(w io.Writer) io.Writer` | Create a new hex encoder |
| `hex.NewDecoder(r io.Reader) io.Reader` | Create a new hex decoder |
| `hex.Encode(dst, src []byte)` | Encode src into dst |
| `hex.EncodeToString(src []byte) string` | Encode src to a string |
| `hex.Decode(dst, src []byte) (n int, err error)` | Decode src into dst |
| `hex.DecodeString(s string) ([]byte, error)` | Decode a string |
| `hex.EncodedLen(n int) int` | Return the encoded length |
| `hex.DecodedLen(n int) int` | Return the decoded length |
| `InvalidByteError` | Error for invalid byte |

---
## Package encoding/json

| Code | Description |
|------|-------------|
| `json.Marshal(v any) ([]byte, error)` | Marshal v to JSON |
| `json.MarshalIndent(v any, prefix, indent string) ([]byte, error)` | Marshal v to indented JSON |
| `json.Unmarshal(data []byte, v any) error` | Unmarshal JSON data into v |
| `json.NewDecoder(r io.Reader) *Decoder` | Create a new JSON decoder |
| `json.NewEncoder(w io.Writer) *Encoder` | Create a new JSON encoder |
| `Decoder.Decode(v any) error` | Decode JSON into v |
| `Decoder.More() bool` | Return whether there is more data |
| `Encoder.Encode(v any) error` | Encode v to JSON |
| `Encoder.SetEscapeHTML(on bool)` | Set whether to escape HTML |
| `Encoder.SetIndent(prefix, indent string)` | Set the indentation |
| `json.Valid(data []byte) bool` | Check if data is valid JSON |
| `json.Compact(dst *bytes.Buffer, src []byte) error` | Compact JSON |
| `json.Indent(dst *bytes.Buffer, src []byte, prefix, indent string) error` | Indent JSON |
| `json.HTMLEscape(dst *bytes.Buffer, src []byte)` | HTML escape JSON |
| `json.Marshaler` | Interface for custom JSON marshaling |
| `json.Unmarshaler` | Interface for custom JSON unmarshaling |
| `json.RawMessage` | Raw JSON message |
| `json.Number` | JSON number |
| `SyntaxError` | JSON syntax error |
| `UnmarshalTypeError` | JSON unmarshal type error |
| `UnmarshalFieldError` | JSON unmarshal field error |
| `InvalidUnmarshalError` | JSON invalid unmarshal error |

---
## Package encoding/pem

| Code | Description |
|------|-------------|
| `pem.Encode(out io.Writer, b *Block) error` | Encode a PEM block |
| `pem.Decode(data []byte) (*Block, error)` | Decode a PEM block |
| `pem.EncodeToMemory(b *Block) []byte` | Encode a PEM block to memory |
| `Block` | PEM block |
| `Block.Type` | Block type |
| `Block.Headers` | Block headers |
| `Block.Bytes` | Block bytes |
| `Block.String() string` | Return the block as a string |

---
## Package encoding/xml

| Code | Description |
|------|-------------|
| `xml.Marshal(v any) ([]byte, error)` | Marshal v to XML |
| `xml.MarshalIndent(v any, prefix, indent string) ([]byte, error)` | Marshal v to indented XML |
| `xml.Unmarshal(data []byte, v any) error` | Unmarshal XML data into v |
| `xml.NewDecoder(r io.Reader) *Decoder` | Create a new XML decoder |
| `xml.NewEncoder(w io.Writer) *Encoder` | Create a new XML encoder |
| `Decoder.Decode(v any) error` | Decode XML into v |
| `Decoder.DecodeElement(v any, start *StartElement) error` | Decode XML element into v |
| `Encoder.Encode(v any) error` | Encode v to XML |
| `Encoder.EncodeElement(v any, start StartElement) error` | Encode v as an XML element |
| `Encoder.Flush() error` | Flush the encoder |
| `Encoder.Indent(prefix, indent string)` | Set the indentation |
| `xml.EscapeText(dst *bytes.Buffer, src []byte)` | Escape text for XML |
| `xml.Escape(dst *bytes.Buffer, src []byte)` | Escape for XML |
| `xml.Unescape(dst *bytes.Buffer, src []byte) error` | Unescape XML |
| `xml.Marshaler` | Interface for custom XML marshaling |
| `xml.Unmarshaler` | Interface for custom XML unmarshaling |
| `xml.MarshalerAttr` | Interface for custom XML marshaling with attributes |
| `xml.CharData` | Character data |
| `xml.Comment` | XML comment |
| `xml.Directive` | XML directive |
| `xml.EndElement` | XML end element |
| `xml.StartElement` | XML start element |
| `xml.SyntaxError` | XML syntax error |
| `xml.UnmarshalError` | XML unmarshal error |
| `xml.Tag` | XML tag |
| `Name` | XML name |

---
## Package errors

| Code | Description |
|------|-------------|
| `errors.New(text string) error` | Create a new error |
| `errors.Errorf(format string, a ...any) error` | Create a formatted error |
| `errors.Is(err, target error) bool` | Check if err is target |
| `errors.As(err error, target any) bool` | Check if err is of type target |
| `errors.Unwrap(err error) error` | Unwrap an error |
| `errors.Join(errs ...error) error` | Join errors into one |
| `var ErrUnsupported error` | Error for unsupported operations |
| `Op` | Error operation |

---
## Package expvar

| Code | Description |
|------|-------------|
| `expvar.Var` | Variable interface |
| `expvar.Int` | Integer variable |
| `expvar.Float` | Float variable |
| `expvar.String` | String variable |
| `expvar.Func` | Function variable |
| `expvar.Map` | Map variable |
| `expvar.NewInt(name string) *Int` | Create a new Int |
| `expvar.NewFloat(name string) *Float` | Create a new Float |
| `expvar.NewString(name string) *String` | Create a new String |
| `expvar.NewFunc(name string, f func() any) *Func` | Create a new Func |
| `expvar.NewMap(name string) *Map` | Create a new Map |
| `expvar.Publish(name string, v Var)` | Publish a variable |
| `expvar.Get(name string) Var` | Get a variable |
| `expvar.Do(f func(KeyValue))` | Do a function on all variables |
| `expvar.KeyValue` | Key-value pair |
| `expvar.Handler()` | Return the HTTP handler |

---
## Package flag

| Code | Description |
|------|-------------|
| `flag.Flag` | Flag representation |
| `flag.FlagSet` | Flag set |
| `flag.NewFlagSet(name string, errorHandling ErrorHandling) *FlagSet` | Create a new flag set |
| `flag.Parse()` | Parse command-line flags |
| `flag.NArg() int` | Return the number of arguments |
| `flag.Arg(i int) string` | Return the i-th argument |
| `flag.Args() []string` | Return the arguments |
| `flag.Bool(name string, value bool, usage string) *bool` | Define a bool flag |
| `flag.Int(name string, value int, usage string) *int` | Define an int flag |
| `flag.Int64(name string, value int64, usage string) *int64` | Define an int64 flag |
| `flag.Uint(name string, value uint, usage string) *uint` | Define a uint flag |
| `flag.Uint64(name string, value uint64, usage string) *uint64` | Define a uint64 flag |
| `flag.String(name string, value string, usage string) *string` | Define a string flag |
| `flag.Float64(name string, value float64, usage string) *float64` | Define a float64 flag |
| `flag.Duration(name string, value time.Duration, usage string) *time.Duration` | Define a duration flag |
| `flag.Var(value Value, name string, usage string)` | Define a flag with a custom value |
| `flag.Func(name, usage string, fn func(string) error)` | Define a flag with a function |
| `flag.BoolVar(p *bool, name string, value bool, usage string)` | Define a bool flag with a variable |
| `flag.IntVar(p *int, name string, value int, usage string)` | Define an int flag with a variable |
| `flag.Int64Var(p *int64, name string, value int64, usage string)` | Define an int64 flag with a variable |
| `flag.UintVar(p *uint, name string, value uint, usage string)` | Define a uint flag with a variable |
| `flag.Uint64Var(p *uint64, name string, value uint64, usage string)` | Define a uint64 flag with a variable |
| `flag.StringVar(p *string, name string, value string, usage string)` | Define a string flag with a variable |
| `flag.Float64Var(p *float64, name string, value float64, usage string)` | Define a float64 flag with a variable |
| `flag.DurationVar(p *time.Duration, name string, value time.Duration, usage string)` | Define a duration flag with a variable |
| `flag.Value` | Value interface |
| `flag.Getter` | Getter interface |
| `flag.ErrorHandling` | Error handling |
| `ContinueOnError` | Continue on error |
| `ExitOnError` | Exit on error |
| `PanicOnError` | Panic on error |
| `Usage()` | Print usage |
| `PrintDefaults()` | Print defaults |

---
## Package fmt

| Code | Description |
|------|-------------|
| `fmt.Print(a ...any) (n int, err error)` | Print arguments to standard output |
| `fmt.Println(a ...any) (n int, err error)` | Print arguments to standard output with newline |
| `fmt.Printf(format string, a ...any) (n int, err error)` | Print formatted arguments to standard output |
| `fmt.Fprint(w io.Writer, a ...any) (n int, err error)` | Print arguments to a writer |
| `fmt.Fprintln(w io.Writer, a ...any) (n int, err error)` | Print arguments to a writer with newline |
| `fmt.Fprintf(w io.Writer, format string, a ...any) (n int, err error)` | Print formatted arguments to a writer |
| `fmt.Sprint(a ...any) string` | Format arguments as a string |
| `fmt.Sprintln(a ...any) string` | Format arguments as a string with newline |
| `fmt.Sprintf(format string, a ...any) string` | Format arguments as a string |
| `fmt.Error(w io.Writer, a ...any) (n int, err error)` | Format and print an error |
| `fmt.Fscan(w io.Reader, a ...any) (n int, err error)` | Scan formatted text from a reader |
| `fmt.Fscanln(w io.Reader, a ...any) (n int, err error)` | Scan formatted text from a reader with newline |
| `fmt.Fscanf(w io.Reader, format string, a ...any) (n int, err error)` | Scan formatted text from a reader |
| `fmt.Scan(a ...any) (n int, err error)` | Scan formatted text from standard input |
| `fmt.Scanln(a ...any) (n int, err error)` | Scan formatted text from standard input with newline |
| `fmt.Scanf(format string, a ...any) (n int, err error)` | Scan formatted text from standard input |
| `fmt.Sscan(str string, a ...any) (n int, err error)` | Scan formatted text from a string |
| `fmt.Sscanln(str string, a ...any) (n int, err error)` | Scan formatted text from a string with newline |
| `fmt.Sscanf(str string, format string, a ...any) (n int, err error)` | Scan formatted text from a string |
| `fmt.Formatter` | Formatter interface |
| `fmt.Stringer` | Stringer interface |
| `fmt.GoStringer` | GoStringer interface |
| `fmt.Scanner` | Scanner interface |

---
## Package hash

| Code | Description |
|------|-------------|
| `hash.Hash` | Hash interface |
| `hash.Hash32` | 32-bit hash interface |
| `hash.Hash64` | 64-bit hash interface |
| `hash.New` | Function to create a new hash |
| `hash.Hash64Sum64(b []byte) uint64` | Return the sum64 of a hash |

---
## Package hash/adler32

| Code | Description |
|------|-------------|
| `adler32.New() hash.Hash32` | Create a new Adler-32 hash |
| `adler32.Checksum(data []byte) uint32` | Return the Adler-32 checksum of data |
| `adler32.Size` | Size of an Adler-32 checksum in bytes |

---
## Package hash/crc32

| Code | Description |
|------|-------------|
| `crc32.New(t *IEEE) hash.Hash32` | Create a new CRC-32 hash |
| `crc32.NewIEEE() hash.Hash32` | Create a new CRC-32 hash with IEEE polynomial |
| `crc32.Checksum(data []byte, tab *Table) uint32` | Return the CRC-32 checksum of data |
| `crc32.ChecksumIEEE(data []byte) uint32` | Return the CRC-32 checksum of data with IEEE polynomial |
| `crc32.IEEE` | IEEE polynomial |
| `crc32.Castagnoli` | Castagnoli polynomial |
| `crc32.Koopman` | Koopman polynomial |
| `crc32.MakeTable(poly uint32) *Table` | Create a new CRC-32 table |
| `crc32.Predefined` | Predefined polynomials |
| `crc32.Size` | Size of a CRC-32 checksum in bytes |
| `Table` | CRC-32 table |

---
## Package hash/crc64

| Code | Description |
|------|-------------|
| `crc64.New(t *Table) hash.Hash64` | Create a new CRC-64 hash |
| `crc64.Checksum(data []byte, t *Table) uint64` | Return the CRC-64 checksum of data |
| `crc64.MakeTable(poly uint64) *Table` | Create a new CRC-64 table |
| `crc64.ECMA` | ECMA polynomial |
| `crc64.ISO` | ISO polynomial |
| `crc64.Size` | Size of a CRC-64 checksum in bytes |
| `Table` | CRC-64 table |

---
## Package hash/fnv

| Code | Description |
|------|-------------|
| `fnv.New32() hash.Hash32` | Create a new 32-bit FNV-1 hash |
| `fnv.New32a() hash.Hash32` | Create a new 32-bit FNV-1a hash |
| `fnv.New64() hash.Hash64` | Create a new 64-bit FNV-1 hash |
| `fnv.New64a() hash.Hash64` | Create a new 64-bit FNV-1a hash |
| `fnv.Hash32` | 32-bit FNV-1 hash |
| `fnv.Hash32a` | 32-bit FNV-1a hash |
| `fnv.Hash64` | 64-bit FNV-1 hash |
| `fnv.Hash64a` | 64-bit FNV-1a hash |

---
## Package hash/maphash

| Code | Description |
|------|-------------|
| `maphash.Hash` | Hash for map keys |
| `maphash.MakeSeed() maphash.Seed` | Create a new random seed |
| `maphash.Seed` | Seed for hash |
| `maphash.Bytes(seed Seed, b []byte) uint64` | Return the hash of b |
| `maphash.String(seed Seed, s string) uint64` | Return the hash of s |
| `maphash.Uint32(seed Seed, i uint32) uint64` | Return the hash of i |
| `maphash.Uint64(seed Seed, i uint64) uint64` | Return the hash of i |
| `maphash.Uintptr(seed Seed, i uintptr) uint64` | Return the hash of i |
| `maphash.Uint(seed Seed, i uint) uint64` | Return the hash of i |

---
## Package html

| Code | Description |
|------|-------------|
| `html.EscapeString(s string) string` | Escape string for HTML |
| `html.UnescapeString(s string) string` | Unescape HTML entities in a string |

---
## Package html/template

| Code | Description |
|------|-------------|
| `template.Template` | HTML template |
| `template.New(name string) *Template` | Create a new template |
| `template.Must(t *Template, err error) *Template` | Check if err is non-nil and panic if so |
| `template.ParseFiles(filenames ...string) (*Template, error)` | Parse template files |
| `template.ParseGlob(pattern string) (*Template, error)` | Parse template files matching pattern |
| `template.Template.Parse(name string) (*Template, error)` | Parse a template |
| `template.Template.Funcs(funcs FuncMap) *Template` | Add functions to the template |
| `template.Template.Delims(left, right string) *Template` | Set delimiters |
| `template.Template.Execute(wr io.Writer, data any) error` | Execute the template |
| `template.Template.ExecuteTemplate(wr io.Writer, name string, data any) error` | Execute a named template |
| `template.Template.Lookup(name string) *Template` | Look up a named template |
| `template.Template.Templates() []*Template` | Return the associated templates |
| `template.Template.Name() string` | Return the name of the template |
| `template.FuncMap` | Map of functions |
| `template.Funcs(funcs FuncMap) FuncMap` | Return a new FuncMap with funcs added |
| `template.JSEscaper` | JavaScript escaper |
| `template.HTMLEscaper` | HTML escaper |
| `template.HTMLAttrEscaper` | HTML attribute escaper |
| `template.URLEscaper` | URL escaper |
| `template.CSSEscaper` | CSS escaper |
| `template.Escape` | Escape function |
| `template.JS` | JavaScript context |
| `template.JSStr` | JavaScript string context |
| `template.JSRegexp` | JavaScript regexp context |
| `template.HTML` | HTML context |
| `template.HTMLAttr` | HTML attribute context |
| `template.URL` | URL context |
| `template.CSS` | CSS context |
| `template.Safe` | Safe context |

---
## Package image

| Code | Description |
|------|-------------|
| `image.Image` | Image interface |
| `image.RGBA` | RGBA image |
| `image.NRGBA` | Non-alpha-premultiplied RGBA image |
| `image.RGBA64` | RGBA64 image |
| `image.NRGBA64` | Non-alpha-premultiplied RGBA64 image |
| `image.CMYK` | CMYK image |
| `image.Gray` | Grayscale image |
| `image.Gray16` | 16-bit grayscale image |
| `image.Paletted` | Paletted image |
| `image.Alpha` | Alpha-only image |
| `image.Alpha16` | 16-bit alpha-only image |
| `image.NewRGBA(r Rect) *RGBA` | Create a new RGBA image |
| `image.NewNRGBA(r Rect) *NRGBA` | Create a new NRGBA image |
| `image.NewRGBA64(r Rect) *RGBA64` | Create a new RGBA64 image |
| `image.NewNRGBA64(r Rect) *NRGBA64` | Create a new NRGBA64 image |
| `image.NewCMYK(r Rect) *CMYK` | Create a new CMYK image |
| `image.NewGray(r Rect) *Gray` | Create a new Gray image |
| `image.NewGray16(r Rect) *Gray16` | Create a new Gray16 image |
| `image.NewPaletted(r Rect, p color.Palette) *Paletted` | Create a new Paletted image |
| `image.NewAlpha(r Rect) *Alpha` | Create a new Alpha image |
| `image.NewAlpha16(r Rect) *Alpha16` | Create a new Alpha16 image |
| `image.Point` | 2D point |
| `image.Rectangle` | Rectangle |
| `image.Rect` | Rectangle |
| `image.ZP` | Zero point |
| `image.ZR` | Zero rectangle |
| `image.Pt(X, Y int) Point` | Create a new point |
| `image.R(X0, Y0, X1, Y1 int) Rectangle` | Create a new rectangle |
| `image.Rectangle.In(r Rectangle) bool` | Check if r is inside the rectangle |
| `image.Rectangle.Overlaps(r Rectangle) bool` | Check if r overlaps with the rectangle |
| `image.Rectangle.Intersect(r Rectangle) Rectangle` | Return the intersection of two rectangles |
| `image.Rectangle.Union(r Rectangle) Rectangle` | Return the union of two rectangles |
| `image.Rectangle.Add(p Point) Rectangle` | Add a point to the rectangle |
| `image.Rectangle.Sub(p Point) Rectangle` | Subtract a point from the rectangle |
| `image.Rectangle.Mul(k int) Rectangle` | Multiply the rectangle by k |
| `image.Rectangle.Div(k int) Rectangle` | Divide the rectangle by k |
| `image.Rectangle.Inset(dx, dy int) Rectangle` | Inset the rectangle by dx and dy |
| `image.Rectangle.Empty() bool` | Check if the rectangle is empty |
| `image.Rectangle.Size() Point` | Return the size of the rectangle |
| `image.Rectangle.Canon() Rectangle` | Return the canonical rectangle |
| `image.Rectangle.String() string` | Return the rectangle as a string |
| `image.YCbCr` | YCbCr image |
| `image.YCbCrSubsampleRatio` | YCbCr subsample ratio |
| `image.YCbCrSubsampleRatio444` | 4:4:4 subsample ratio |
| `image.YCbCrSubsampleRatio422` | 4:2:2 subsample ratio |
| `image.YCbCrSubsampleRatio420` | 4:2:0 subsample ratio |
| `image.NewYCbCr(r Rect, subsampleRatio YCbCrSubsampleRatio) *YCbCr` | Create a new YCbCr image |
| `image.Draw` | Draw interface |
| `image.Uniform` | Uniform color |
| `image.Black` | Black color |
| `image.White` | White color |
| `image.Opaque` | Opaque color |
| `image.Transparent` | Transparent color |
| `image.Op` | Porter-Duff compositing operator |
| `image.Over` | Over compositing operator |
| `image.Src` | Src compositing operator |

---
## Package image/color

| Code | Description |
|------|-------------|
| `color.Color` | Color interface |
| `color.RGBA` | RGBA color |
| `color.NRGBA` | Non-alpha-premultiplied RGBA color |
| `color.RGBA64` | RGBA64 color |
| `color.NRGBA64` | Non-alpha-premultiplied RGBA64 color |
| `color.CMYK` | CMYK color |
| `color.Gray` | Grayscale color |
| `color.Gray16` | 16-bit grayscale color |
| `color.Alpha` | Alpha color |
| `color.Alpha16` | 16-bit alpha color |
| `color.Palette` | Color palette |
| `color.NewRGBA(r, g, b, a uint8)` | Create a new RGBA color |
| `color.NewNRGBA(r, g, b, a uint8)` | Create a new NRGBA color |
| `color.NewRGBA64(r, g, b, a uint16)` | Create a new RGBA64 color |
| `color.NewNRGBA64(r, g, b, a uint16)` | Create a new NRGBA64 color |
| `color.NewCMYK(c, m, y, k uint8)` | Create a new CMYK color |
| `color.NewGray(y uint8)` | Create a new Gray color |
| `color.NewGray16(y uint16)` | Create a new Gray16 color |
| `color.NewAlpha(a uint8)` | Create a new Alpha color |
| `color.NewAlpha16(a uint16)` | Create a new Alpha16 color |
| `color.RGBA.R() uint8` | Return the red component |
| `color.RGBA.G() uint8` | Return the green component |
| `color.RGBA.B() uint8` | Return the blue component |
| `color.RGBA.A() uint8` | Return the alpha component |
| `color.YCbCr` | YCbCr color |
| `color.NewYCbCr(y, cb, cr uint8, yCbCrSubsampleRatio image.YCbCrSubsampleRatio) color.YCbCr` | Create a new YCbCr color |
| `color.YCbCr.Y() uint8` | Return the Y component |
| `color.YCbCr.Cb() uint8` | Return the Cb component |
| `color.YCbCr.Cr() uint8` | Return the Cr component |
| `color.YCbCr.YCbCr()` | Return the Y, Cb, and Cr components |
| `color.Model` | Color model interface |
| `color.ModelFunc` | Color model function |
| `color.NewPalette(p []color.Color) color.Palette` | Create a new palette |
| `color.Black` | Black color |
| `color.White` | White color |
| `color.Transparent` | Transparent color |
| `color.Opaque` | Opaque color |
| `color.RGBAModel` | RGBA color model |
| `color.NRGBAModel` | NRGBA color model |
| `color.AlphaModel` | Alpha color model |
| `color.GrayModel` | Gray color model |
| `color.CMYKModel` | CMYK color model |
| `color.YCbCrModel` | YCbCr color model |

---
## Package image/draw

| Code | Description |
|------|-------------|
| `draw.Draw(dst Image, r Rectangle, src Image, sp Point)` | Draw src onto dst |
| `draw.DrawMask(dst Image, r Rectangle, src Image, sp Point, mask Image, mp Point)` | Draw src onto dst using mask |
| `draw.DrawMaskF(dst Image, r Rectangle, src Image, sp Point, mask Image, mp Point, op Op, alpha float64)` | Draw src onto dst using mask with opacity |
| `draw.DrawF(dst Image, r Rectangle, src Image, sp Point, op Op, alpha float64)` | Draw src onto dst with opacity |
| `draw.Copy(dst Image, r Rectangle, src Image, sp Point)` | Copy src onto dst |
| `draw.DrawTriangle(dst Image, p0, p1, p2 Point, c color.Color)` | Draw a triangle |
| `draw.DrawCatmullRom(dst Image, p []Point, c color.Color)` | Draw a Catmull-Rom spline |
| `draw.DrawBezier(dst Image, p []Point, c color.Color)` | Draw a Bezier curve |
| `draw.DrawGouraudTriangle(dst Image, p0, p1, p2 Point, c0, c1, c2 color.Color)` | Draw a Gouraud-shaded triangle |
| `draw.DrawQuad(dst Image, p0, p1, p2, p3 Point, c color.Color)` | Draw a quadrilateral |
| `draw.DrawQuadBezier(dst Image, p0, p1, p2, p3 Point, c color.Color)` | Draw a quadratic Bezier curve |
| `draw.DrawCubicBezier(dst Image, p0, p1, p2, p3 Point, c color.Color)` | Draw a cubic Bezier curve |
| `draw.Scaler` | Scaler for scaling images |
| `draw.NewScaler(dst Image) *Scaler` | Create a new scaler |
| `Scaler.Scale(dst Image, r Rectangle, src Image, sr Rectangle, op Op, s Op)` | Scale src onto dst |
| `draw.Quantizer` | Quantizer for color quantization |
| `draw.NewFloydSteinberg(src Image) *FloydSteinberg` | Create a new Floyd-Steinberg quantizer |
| `draw.FloydSteinberg.Quantize(dst Image, r Rectangle)` | Quantize the image |

---
## Package image/gif

| Code | Description |
|------|-------------|
| `gif.GIF` | GIF image |
| `gif.Options` | GIF encoding options |
| `gif.Encode(w io.Writer, p *image.Paletted, o *Options) error` | Encode a paletted image to GIF |
| `gif.EncodeAll(w io.Writer, g *GIF) error` | Encode a GIF to a writer |
| `gif.Decode(r io.Reader) (*GIF, error)` | Decode a GIF from a reader |
| `gif.DecodeAll(r io.Reader) (*GIF, error)` | Decode all frames from a GIF |
| `gif.DecodeConfig(r io.Reader) (image.Config, error)` | Decode the GIF configuration |
| `GIF.Image` | Image frames |
| `GIF.Delay` | Frame delays |
| `GIF.Disposal` | Frame disposal methods |
| `GIF.LoopCount` | Loop count |
| `GIF.BackgroundIndex` | Background index |
| `GIF.PixelAspectRatio` | Pixel aspect ratio |
| `Options.NumColors` | Number of colors |
| `Options.Quantizer` | Color quantizer |
| `Options.Ditherer` | Ditherer |
| `DisposalNone` | No disposal |
| `DisposalBackground` | Dispose to background |
| `DisposalPrevious` | Dispose to previous |

---
## Package image/jpeg

| Code | Description |
|------|-------------|
| `jpeg.Options` | JPEG encoding options |
| `jpeg.Encode(w io.Writer, m image.Image, o *Options) error` | Encode an image to JPEG |
| `jpeg.EncodeConfig(w io.Writer, m image.Image, o *Options) error` | Encode an image to JPEG with config |
| `jpeg.Decode(r io.Reader) (image.Image, error)` | Decode a JPEG from a reader |
| `jpeg.DecodeConfig(r io.Reader) (image.Config, error)` | Decode the JPEG configuration |
| `Options.Quality` | JPEG quality |
| `Options.Optimize` | Optimize encoding |
| `Options.DCTMethod` | DCT method |
| `DefaultQuality` | Default JPEG quality |

---
## Package image/png

| Code | Description |
|------|-------------|
| `png.Encoder` | PNG encoder |
| `png.EncoderBufferPool` | Buffer pool for PNG encoder |
| `png.Encode(w io.Writer, m image.Image) error` | Encode an image to PNG |
| `png.Decode(r io.Reader) (image.Image, error)` | Decode a PNG from a reader |
| `png.DecodeConfig(r io.Reader) (image.Config, error)` | Decode the PNG configuration |
| `png.Encoder.CompressionLevel` | Compression level |
| `png.DefaultCompression` | Default compression level |
| `png.NoCompression` | No compression |
| `png.BestSpeed` | Best speed compression |
| `png.BestCompression` | Best compression |
| `png.ErrUnsupported` | Error for unsupported PNG |

---
## Package index/suffixarray

| Code | Description |
|------|-------------|
| `suffixarray.Index` | Suffix array index |
| `suffixarray.New(data []byte) *Index` | Create a new suffix array index |
| `Index.Find(s []byte) (int, int)` | Find the first occurrence of s |
| `Index.Lookup(s []byte) (int, bool)` | Look up s in the index |
| `Index.LongestCommonPrefix(i, j int) int` | Return the length of the longest common prefix of suffixes i and j |
| `Index.Snippet(i, start, end int) []byte` | Return the snippet of the suffix at i |
| `Index.String() string` | Return the index as a string |

---
## Package io

| Code | Description |
|------|-------------|
| `io.Reader` | Reader interface |
| `io.Writer` | Writer interface |
| `io.Closer` | Closer interface |
| `io.Seeker` | Seeker interface |
| `io.ReadCloser` | ReadCloser interface |
| `io.WriteCloser` | WriteCloser interface |
| `io.ReadWriter` | ReadWriter interface |
| `io.ReadWriteCloser` | ReadWriteCloser interface |
| `io.ReaderAt` | ReaderAt interface |
| `io.WriterAt` | WriterAt interface |
| `io.ByteReader` | ByteReader interface |
| `io.ByteWriter` | ByteWriter interface |
| `io.ByteScanner` | ByteScanner interface |
| `io.RuneReader` | RuneReader interface |
| `io.RuneScanner` | RuneScanner interface |
| `io.StringWriter` | StringWriter interface |
| `io.ReadAtLeast(r Reader, buf []byte, min int) (n int, err error)` | Read at least min bytes from r |
| `io.ReadFull(r Reader, buf []byte) (n int, err error)` | Read exactly len(buf) bytes from r |
| `io.WriteString(w Writer, s string) (n int, err error)` | Write a string to w |
| `io.Copy(dst Writer, src Reader) (written int64, err error)` | Copy from src to dst |
| `io.CopyBuffer(dst Writer, src Reader, buf []byte) (written int64, err error)` | Copy from src to dst using a buffer |
| `io.CopyN(dst Writer, src Reader, n int64) (written int64, err error)` | Copy n bytes from src to dst |
| `io.LimitReader(r Reader, n int64) Reader` | Limit the number of bytes read from r |
| `io.NopCloser(r Reader) ReadCloser` | Wrap r in a ReadCloser that does nothing on Close |
| `io.MultiReader(readers ...Reader) Reader` | Create a Reader that reads from multiple readers |
| `io.MultiWriter(writers ...Writer) Writer` | Create a Writer that writes to multiple writers |
| `io.PipeReader, PipeWriter` | Pipe for in-memory communication |
| `io.Pipe() (*PipeReader, *PipeWriter)` | Create a new pipe |
| `io.TeeReader(r Reader, w Writer) Reader` | Create a Reader that writes to w what it reads from r |
| `io.EOF` | End of file error |
| `io.ErrClosedPipe` | Closed pipe error |
| `io.ErrNoProgress` | No progress error |
| `io.ErrShortBuffer` | Short buffer error |
| `io.ErrShortWrite` | Short write error |
| `io.ErrUnexpectedEOF` | Unexpected EOF error |

---
## Package io/fs

| Code | Description |
|------|-------------|
| `fs.File` | File interface |
| `fs.DirEntry` | Directory entry |
| `fs.FileInfo` | File information |
| `fs.FileMode` | File mode |
| `fs.PathError` | Path error |
| `fs.ReadDir(name string) ([]DirEntry, error)` | Read a directory |
| `fs.ReadFile(name string) ([]byte, error)` | Read a file |
| `fs.WriteFile(name string, data []byte, perm FileMode) error` | Write a file |
| `fs.Mkdir(name string, perm FileMode) error` | Create a directory |
| `fs.MkdirAll(name string, perm FileMode) error` | Create a directory and all necessary parents |
| `fs.Remove(name string) error` | Remove a file |
| `fs.RemoveAll(path string) error` | Remove a file or directory and all its contents |
| `fs.Rename(oldpath, newpath string) error` | Rename a file |
| `fs.Chmod(name string, mode FileMode) error` | Change file mode |
| `fs.Chown(name string, uid, gid int) error` | Change file owner |
| `fs.Chtimes(name string, atime, mtime time.Time) error` | Change file access and modification times |
| `fs.Symlink(oldname, newname string) error` | Create a symbolic link |
| `fs.Readlink(name string) (string, error)` | Read a symbolic link |
| `fs.Lchown(name string, uid, gid int) error` | Change file owner (no dereference) |
| `fs.Lstat(name string) (FileInfo, error)` | Lstat a file |
| `fs.Stat(name string) (FileInfo, error)` | Stat a file |
| `fs.SameFile(fi1, fi2 FileInfo) bool` | Check if two FileInfo refer to the same file |
| `fs.WalkDir(root string, fn func(path string, d DirEntry, err error) error` | Walk a directory tree |
| `fs.Walk(root string, fn func(path string, info FileInfo, err error) error` | Walk a directory tree |
| `fs.Glob(pattern string) ([]string, error)` | Glob a pattern |
| `fs.Sub` | Sub filesystem |
| `fs.ValidPath(name string) bool` | Check if a path is valid |

---
## Package io/ioutil

| Code | Description |
|------|-------------|
| `ioutil.ReadAll(r io.Reader) ([]byte, error)` | Read all data from r |
| `ioutil.ReadFile(filename string) ([]byte, error)` | Read all data from a file |
| `ioutil.WriteFile(filename string, data []byte, perm os.FileMode) error` | Write data to a file |
| `ioutil.NopCloser(r io.Reader) io.ReadCloser` | Wrap r in a ReadCloser that does nothing on Close |
| `ioutil.TempDir(dir, prefix string) (name string, err error)` | Create a temporary directory |
| `ioutil.TempFile(dir, prefix string) (*os.File, error)` | Create a temporary file |
| `ioutil.Discard` | io.Writer that discards all writes |

---
## Package log

| Code | Description |
|------|-------------|
| `log.Logger` | Logger |
| `log.New(out io.Writer, prefix string, flag int) *Logger` | Create a new Logger |
| `log.Default()` | Return the default logger |
| `log.SetDefault(logger *Logger)` | Set the default logger |
| `log.Print(v ...any)` | Print arguments to the default logger |
| `log.Println(v ...any)` | Print arguments to the default logger with newline |
| `log.Printf(format string, v ...any)` | Print formatted arguments to the default logger |
| `log.Panic(v ...any)` | Panic with arguments to the default logger |
| `log.Panicln(v ...any)` | Panic with arguments to the default logger with newline |
| `log.Panicf(format string, v ...any)` | Panic with formatted arguments to the default logger |
| `log.Fatal(v ...any)` | Fatal with arguments to the default logger |
| `log.Fatalln(v ...any)` | Fatal with arguments to the default logger with newline |
| `log.Fatalf(format string, v ...any)` | Fatal with formatted arguments to the default logger |
| `Logger.Print(v ...any)` | Print arguments to the logger |
| `Logger.Println(v ...any)` | Print arguments to the logger with newline |
| `Logger.Printf(format string, v ...any)` | Print formatted arguments to the logger |
| `Logger.Panic(v ...any)` | Panic with arguments to the logger |
| `Logger.Panicln(v ...any)` | Panic with arguments to the logger with newline |
| `Logger.Panicf(format string, v ...any)` | Panic with formatted arguments to the logger |
| `Logger.Fatal(v ...any)` | Fatal with arguments to the logger |
| `Logger.Fatalln(v ...any)` | Fatal with arguments to the logger with newline |
| `Logger.Fatalf(format string, v ...any)` | Fatal with formatted arguments to the logger |
| `Logger.SetPrefix(prefix string)` | Set the prefix for the logger |
| `Logger.SetFlags(flag int)` | Set the flags for the logger |
| `Logger.SetOutput(w io.Writer)` | Set the output for the logger |
| `Ldate` | Date flag |
| `Ltime` | Time flag |
| `Lmicroseconds` | Microseconds flag |
| `Llongfile` | Long file flag |
| `Lshortfile` | Short file flag |
| `LUTC` | UTC flag |
| `Lmsgprefix` | Message prefix flag |
| `LstdFlags` | Standard flags |

---
## Package log/slog

| Code | Description |
|------|-------------|
| `slog.Logger` | Structured logger |
| `slog.New(h slog.Handler) *slog.Logger` | Create a new Logger |
| `slog.Default()` *slog.Logger` | Return the default logger |
| `slog.SetDefault(l *slog.Logger)` | Set the default logger |
| `slog.Log(v ...any)` | Log arguments to the default logger |
| `slog.LogAttrs(a ...any)` | Log attributes to the default logger |
| `slog.With(args ...any) *slog.Logger` | Return a new logger with the given attributes |
| `slog.WithLogger(l *slog.Logger)` | Return a context with the given logger |
| `slog.FromContext(ctx context.Context) *slog.Logger` | Return the logger from the context |
| `slog.Debug(msg string, args ...any)` | Log a debug message |
| `slog.Info(msg string, args ...any)` | Log an info message |
| `slog.Warn(msg string, args ...any)` | Log a warning message |
| `slog.Error(msg string, args ...any)` | Log an error message |
| `slog.Handler` | Handler interface |
| `slog.HandlerOptions` | Handler options |
| `slog.NewJSONHandler(w io.Writer, o *HandlerOptions) slog.Handler` | Create a new JSON handler |
| `slog.NewTextHandler(w io.Writer, o *HandlerOptions) slog.Handler` | Create a new text handler |
| `slog.Level` | Log level |
| `slog.LevelDebug` | Debug level |
| `slog.LevelInfo` | Info level |
| `slog.LevelWarn` | Warn level |
| `slog.LevelError` | Error level |
| `slog.Attr` | Attribute |
| `slog.Any(key string, v any)` | Create an Any attribute |
| `slog.Bool(key string, v bool)` | Create a Bool attribute |
| `slog.Duration(key string, v time.Duration)` | Create a Duration attribute |
| `slog.Float64(key string, v float64)` | Create a Float64 attribute |
| `slog.Int(key string, v int)` | Create an Int attribute |
| `slog.Int64(key string, v int64)` | Create an Int64 attribute |
| `slog.String(key string, v string)` | Create a String attribute |
| `slog.Time(key string, v time.Time)` | Create a Time attribute |
| `slog.Uint64(key string, v uint64)` | Create a Uint64 attribute |
| `slog.Group(key string, a ...any)` | Create a Group attribute |