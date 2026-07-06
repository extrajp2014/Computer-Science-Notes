## Core Functions

### Input and Output

| Code | Description |
|------|-------------|
| `print` | Output a list to STDOUT |
| `printf` | Output formatted text to STDOUT |
| `say` | Output a list to STDOUT with newline (requires `use 5.010;`) |
| `write` | Print a picture record to a filehandle |
| `format` | Declare a picture format for write |
| `formline` | Internal function used for formats |

### Error Handling

| Code | Description |
|------|-------------|
| `warn` | Print a warning message to STDERR |
| `die` | Throw an exception or exit |
| `croak` | Throw an exception from a called subroutine (from Carp) |
| `carp` | Warn of errors from a called subroutine (from Carp) |
| `cluck` | Throw an exception with full stack trace (from Carp) |
| `confess` | Throw an exception with full stack trace and exit (from Carp) |
| `eval` | Evaluate a string as Perl code |
| `do` | Execute a block or file |

### Module Loading

| Code | Description |
|------|-------------|
| `require` | Load a module at compile time |
| `use` | Load a module at compile time and import symbols |
| `no` | Unimport symbols from a module |
| `import` | Import symbols into current namespace |
| `unimport` | Remove imported symbols from current namespace |

### Variable and Reference Functions

| Code | Description |
|------|-------------|
| `my` | Declare a lexically-scoped variable |
| `our` | Declare a package-scoped variable |
| `local` | Create a dynamically-scoped variable |
| `state` | Declare a state variable (persistent across calls) |
| `ref` | Get the reference type |
| `bless` | Create an object |
| `defined` | Check if a variable has a value |
| `undef` | Undefine a variable |
| `exists` | Check if a hash key exists |
| `delete` | Delete a hash key |
| `tied` | Get the package class of a tied variable |
| `tie` | Bind a variable to a package class |
| `untie` | Break the binding between a variable and a package |
| `isa` | Check if an object is a subclass of a class |
| `can` | Check if an object can perform a method |
| `scalar` | Force a scalar context |
| `list` | Force a list context |

### Subroutine Functions

| Code | Description |
|------|-------------|
| `sub` | Define a subroutine |
| `caller` | Get context of the current subroutine call |
| `wantarray` | Get the context of the current subroutine call |
| `return` | Return from a subroutine |
| `goto` | Jump to a label |
| `__SUB__` | Experimental subroutine reference |

### Control Flow

| Code | Description |
|------|-------------|
| `if` | Conditional execution |
| `unless` | Execute unless condition is true |
| `else` | Alternative branch for if/unless |
| `elsif` | Alternative condition for if |
| `for` | Iterate over a list |
| `foreach` | Alias for for |
| `while` | Loop while condition is true |
| `until` | Loop until condition is true |
| `last` | Break out of a loop |
| `next` | Go to next iteration of a loop |
| `redo` | Redo current iteration of a loop |
| `continue` | Optional block executed after loop iterations |
| `given` | Start a switch statement (requires `use 5.010;`) |
| `when` | Match a case in a switch statement |
| `default` | Default case in a switch statement |
| `break` | Break out of a given/when block |

### Array Functions

| Code | Description |
|------|-------------|
| `push` | Add elements to the end of an array |
| `pop` | Remove and return the last element of an array |
| `shift` | Remove and return the first element of an array |
| `unshift` | Add elements to the beginning of an array |
| `splice` | Remove and replace elements in an array |
| `reverse` | Reverse a list |
| `sort` | Sort a list |
| `grep` | Filter a list using a pattern |
| `map` | Transform a list using a block |
| `join` | Join a list into a string |
| `split` | Split a string into a list |
| `list` | Create a list |
| `array` | Create an array |

### Hash Functions

| Code | Description |
|------|-------------|
| `keys` | Get the keys of a hash |
| `values` | Get the values of a hash |
| `each` | Iterate over a hash |
| `delete` | Remove a key from a hash |
| `exists` | Check if a key exists in a hash |

### String Functions

| Code | Description |
|------|-------------|
| `chop` | Remove the last character from a string |
| `chomp` | Remove the last newline from a string |
| `length` | Return the length of a string |
| `substr` | Get or replace a substring |
| `index` | Find the position of a substring |
| `rindex` | Find the position of a substring from the end |
| `sprintf` | Return a formatted string |
| `printf` | Print a formatted string |
| `quotemeta` | Quote metacharacters |
| `ord` | Return the numeric value of a character |
| `chr` | Return the character for a numeric value |
| `hex` | Convert a hexadecimal string to a number |
| `oct` | Convert an octal string to a number |
| `pack` | Convert a list into a binary structure |
| `unpack` | Convert a binary structure into a list |
| `uc` | Convert to uppercase |
| `ucfirst` | Convert first character to uppercase |
| `lc` | Convert to lowercase |
| `lcfirst` | Convert first character to lowercase |
| `fc` | Fold case |
| `fcfirst` | Fold case of first character |
| `concat` | Concatenate strings |
| `x` | String repetition operator |

### Regular Expression Functions

| Code | Description |
|------|-------------|
| `m//` | Pattern match operator |
| `s///` | Substitution operator |
| `qr//` | Quote a regular expression |
| `pos` | Return or set the current match position |
| `reset` | Reset search status |
| `study` | Analyze a string for optimized pattern matching |
| `split` | Split a string using a pattern |

### Numeric Functions

| Code | Description |
|------|-------------|
| `int` | Truncate to an integer |
| `abs` | Absolute value |
| `sqrt` | Square root |
| `exp` | Exponential function |
| `log` | Natural logarithm |
| `log10` | Base-10 logarithm |
| `sin` | Sine |
| `cos` | Cosine |
| `tan` | Tangent |
| `asin` | Arc sine |
| `acos` | Arc cosine |
| `atan` | Arc tangent |
| `atan2` | Arc tangent of two variables |
| `sinh` | Hyperbolic sine |
| `cosh` | Hyperbolic cosine |
| `tanh` | Hyperbolic tangent |
| `rand` | Random number |
| `srand` | Seed the random number generator |
| `hex` | Convert a hexadecimal string to a number |
| `oct` | Convert an octal string to a number |
| `bin` | Convert a binary string to a number |

### Date and Time Functions

| Code | Description |
|------|-------------|
| `time` | Return the current time in seconds since epoch |
| `localtime` | Convert time to local time |
| `gmtime` | Convert time to UTC time |
| `scalar localtime` | Return local time as a string |
| `scalar gmtime` | Return UTC time as a string |
| `mktime` | Convert local time to epoch seconds |
| `strftime` | Format local time as a string |
| `sleep` | Sleep for a number of seconds |
| `alarm` | Set an alarm |

### File Test Operators

| Code | Description |
|------|-------------|
| `-r` | File is readable by effective uid/gid |
| `-w` | File is writable by effective uid/gid |
| `-x` | File is executable by effective uid/gid |
| `-o` | File is owned by effective uid |
| `-R` | File is readable by real uid/gid |
| `-W` | File is writable by real uid/gid |
| `-X` | File is executable by real uid/gid |
| `-O` | File is owned by real uid |
| `-e` | File exists |
| `-z` | File has zero size |
| `-s` | File has non-zero size (returns size) |
| `-f` | File is a plain file |
| `-d` | File is a directory |
| `-l` | File is a symbolic link |
| `-p` | File is a named pipe (FIFO) |
| `-S` | File is a socket |
| `-b` | File is a block special file |
| `-c` | File is a character special file |
| `-u` | File has setuid bit set |
| `-g` | File has setgid bit set |
| `-k` | File has sticky bit set |
| `-t` | Filehandle is opened to a tty |
| `-T` | File is a text file |
| `-B` | File is a binary file |
| `-M` | Script start time minus file modification time, in days |
| `-A` | Current time minus file access time, in days |
| `-C` | Current time minus file inode change time, in days |

### File Operations

| Code | Description |
|------|-------------|
| `open` | Open a file or pipe |
| `close` | Close a filehandle |
| `read` | Read from a filehandle |
| `write` | Write to a filehandle |
| `sysopen` | Open a file with more control |
| `sysread` | Read from a filehandle with more control |
| `syswrite` | Write to a filehandle with more control |
| `binmode` | Set binary mode on a filehandle |
| `eof` | Test for end-of-file on a filehandle |
| `tell` | Return the current file position |
| `seek` | Move to a position in a file |
| `rewind` | Move to the beginning of a file |
| `truncate` | Truncate a file |
| `flock` | Advisory file locking |
| `ioctl` | Input/output control operations |
| `fcntl` | File control operations |
| `fileno` | Return the file descriptor for a filehandle |
| `stat` | Get file statistics |
| `lstat` | Get file statistics without following symlinks |
| `readlink` | Read the target of a symbolic link |
| `symlink` | Create a symbolic link |
| `link` | Create a hard link |
| `unlink` | Remove a file |
| `rename` | Rename a file |
| `mkdir` | Create a directory |
| `rmdir` | Remove a directory |
| `opendir` | Open a directory |
| `readdir` | Read a directory entry |
| `telldir` | Return the current position in a directory |
| `seekdir` | Move to a position in a directory |
| `rewinddir` | Rewind a directory |
| `closedir` | Close a directory |
| `glob` | Expand filenames using wildcards |
| `chdir` | Change the current working directory |
| `getcwd` | Get current working directory |
| `chmod` | Change file permissions |
| `chown` | Change file ownership |
| `umask` | Set the file creation mode mask |
| `utime` | Set file access and modification times |

### Directory Handling

| Code | Description |
|------|-------------|
| `opendir` | Open a directory handle |
| `readdir` | Read a directory entry |
| `telldir` | Return the current position in a directory |
| `seekdir` | Move to a position in a directory |
| `rewinddir` | Rewind a directory handle |
| `closedir` | Close a directory handle |

### Process Management

| Code | Description |
|------|-------------|
| `fork` | Create a new process |
| `exec` | Replace the current process with a new program |
| `system` | Execute a command and return its exit status |
| `wait` | Wait for a child process to finish |
| `waitpid` | Wait for a specific child process to finish |
| `kill` | Send a signal to a process |
| `alarm` | Set an alarm |
| `sleep` | Sleep for a number of seconds |
| `getppid` | Get parent process ID |
| `getpgrp` | Get current process group |
| `setpgrp` | Set process group |
| `getpriority` | Get current priority |
| `setpriority` | Set current priority |
| `times` | Return process times |

### User and Group Functions

| Code | Description |
|------|-------------|
| `getpwent` | Get password file entry |
| `getgrent` | Get group file entry |
| `getpwnam` | Get password file entry by name |
| `getpwuid` | Get password file entry by UID |
| `getgrnam` | Get group file entry by name |
| `getgrgid` | Get group file entry by GID |
| `endpwent` | End password file entry processing |
| `endgrent` | End group file entry processing |
| `setpwent` | Reset password file entry processing |
| `setgrent` | Reset group file entry processing |
| `getlogin` | Get login name |

### Network Functions

| Code | Description |
|------|-------------|
| `gethostbyname` | Get host information by name |
| `gethostbyaddr` | Get host information by address |
| `gethostent` | Get host entry |
| `sethostent` | Set host entry |
| `endhostent` | End host entry |
| `getnetbyname` | Get network information by name |
| `getnetbyaddr` | Get network information by address |
| `getnetent` | Get network entry |
| `setnetent` | Set network entry |
| `endnetent` | End network entry |
| `getprotobyname` | Get protocol information by name |
| `getprotobynumber` | Get protocol information by number |
| `getprotoent` | Get protocol entry |
| `setprotoent` | Set protocol entry |
| `endprotoent` | End protocol entry |
| `getservbyname` | Get service information by name |
| `getservbyport` | Get service information by port |
| `getservent` | Get service entry |
| `setservent` | Set service entry |
| `endservent` | End service entry |
| `getpeername` | Get the peer address of a socket |
| `getsockname` | Get the local address of a socket |
| `getsockopt` | Get socket options |
| `setsockopt` | Set socket options |
| `shutdown` | Shut down a socket |

### Socket Functions

| Code | Description |
|------|-------------|
| `socket` | Create a socket |
| `bind` | Bind a socket to an address |
| `connect` | Connect a socket to a remote address |
| `listen` | Listen for connections on a socket |
| `accept` | Accept a connection on a socket |
| `send` | Send data over a socket |
| `recv` | Receive data from a socket |
| `shutdown` | Shut down a socket |

### System Information

| Code | Description |
|------|-------------|
| `getc` | Get the next character from a filehandle |
| `ungetc` | Push a character back onto a filehandle |
| `readpipe` | Read the output from a pipe |
| `syscall` | Execute a system call |
| `unpack` | Convert a binary structure into a list |
| `pack` | Convert a list into a binary structure |
| `formline` | Internal function used for formats |
| `caller` | Get context of the current subroutine call |
| `wantarray` | Get the context of the current subroutine call |
| `dump` | Dump core |

---
## Pragmas

| Code | Description |
|------|-------------|
| `use strict;` | Enforce good programming practices |
| `use strict 'vars';` | Require declaration of variables |
| `use strict 'refs';` | Restrict bareword references |
| `use strict 'subs';` | Restrict bareword subroutines |
| `no strict;` | Disable strict |
| `use warnings;` | Enable warnings |
| `use warnings::register;` | Register warnings categories |
| `no warnings;` | Disable warnings |
| `use diagnostics;` | Enable verbose warnings |
| `no diagnostics;` | Disable verbose warnings |
| `use integer;` | Use integer arithmetic |
| `no integer;` | Disable integer arithmetic |
| `use bytes;` | Treat strings as bytes |
| `no bytes;` | Disable bytes |
| `use utf8;` | Enable UTF-8 in source code |
| `no utf8;` | Disable UTF-8 |
| `use feature` | Enable new features |
| `use feature ':5.10';` | Enable all features from Perl 5.10 |
| `no feature;` | Disable features |
| `use autodie;` | Replace functions with equivalents that succeed or die |
| `no autodie;` | Disable autodie |
| `use autodie qw(:all);` | Enable autodie for all functions |
| `use open` | Set default PerlIO layers for input and output |
| `no open;` | Disable open |
| `use locale;` | Use or avoid POSIX locales for built-in operations |
| `no locale;` | Disable locale |
| `use threads;` | Perl interpreter-based threads |
| `use threads::shared;` | Share data structures between threads |
| `use re` | Pragmatic module to control regex engine |
| `use re 'taint';` | Enable taint checking for regex |
| `no re;` | Disable re |
| `use overloading;` | A pragma to control overloading |
| `no overloading;` | Disable overloading |
| `use sigtrap;` | Enable simple signal handling |
| `no sigtrap;` | Disable sigtrap |
| `use sort;` | Allow user-defined sort subroutines |
| `no sort;` | Disable sort |
| `use subs;` | Predeclare sub names |
| `no subs;` | Disable subs |
| `use vars;` | Predeclare global variable names |
| `no vars;` | Disable vars |
| `use version;` | Perl extension for Version Objects |
| `no version;` | Disable version |

---
## Special Variables

### Global Special Variables

| Code | Description |
|------|-------------|
| `$_` | Default input and pattern-searching space |
| `$@` | Evaluation error |
| `$!` | System error |
| `$^E` | Extended OS error |
| `$?` | Child process exit status |
| `$<` | Real user ID |
| `$>` | Effective user ID |
| `$(` | Real group ID |
| `$)` | Effective group ID |
| `$0` | Script name |
| `$]` | Perl version |
| `$^O` | Operating system name |
| `$^T` | Taint mode flag |
| `$^W` | Warning flag |
| `$^X` | Perl executable name |
| `$^V` | Perl version as a version object |
| `$^C` | Compilation flag |
| `$^D` | Debugging flags |
| `$^F` | Maximum system file descriptor |
| `$^I` | In-place edit extension |
| `$^M` | Emergency memory pool |
| `$^P` | Perl internal debugging flag |
| `$^S` | Exception being caught |

### Pattern Matching Special Variables

| Code | Description |
|------|-------------|
| `$&` | String matched by last pattern match |
| `$'` | String before last pattern match |
| `$'` | String after last pattern match |
| `$+` | Last bracket matched by pattern match |
| `$1`, `$2`, ... | Pattern match captures |
| `@-` | Offsets of pattern match captures |
| `@+` | Offsets after pattern match captures |
| `$^R` | Last pattern match result |
| `$^N` | Most recent capture group |
| `%+` | Named capture groups |
| `%` | Named capture groups |

### I/O Special Variables

| Code | Description |
|------|-------------|
| `$/` | Input record separator |
| `$\` | Output record separator |
| `$|` | Output field separator |
| `$,` | Output field separator |
| `$"` | List separator |
| `$;` | Subscript separator |
| `$#` | Output format for numbers |
| `$%` | Page number of current output page |
| `$=` | Page length of current output page |
| `$-` | Number of lines left on current page |
| `$~` | Current report format name |
| `$^` | Current top-of-form format name |
| `@ARGV` | Command-line arguments |
| `ARGV` | Special filehandle for reading from @ARGV |
| `ARGVOUT` | Special filehandle for writing to output files |

### Array and Hash Special Variables

| Code | Description |
|------|-------------|
| `@_` | Default array for subroutine arguments |
| `@ARGV` | Command-line arguments |
| `@INC` | Include path |
| `@F` | Array of fields from last read |
| `$#` | Index of last element in an array |
| `%ENV` | Environment variables |
| `%SIG` | Signal handlers |
| `%INC` | Hash of loaded modules |

---
## Standard Modules

### File and Directory Modules

| Code | Description |
|------|-------------|
| `File::Basename` | Parse file paths into directory, filename, and suffix |
| `File::Compare` | Compare files or filehandles |
| `File::Copy` | Copy files or filehandles |
| `File::Find` | Traverse directory trees |
| `File::Glob` | Perl extension for BSD glob routine |
| `File::Path` | Create or remove directory trees |
| `File::Spec` | Portably perform operations on file names |
| `File::Spec::Functions` | Portably perform operations on file names |
| `File::Spec::Unix` | Unix-specific File::Spec methods |
| `File::Spec::Win32` | Win32-specific File::Spec methods |
| `File::Spec::Mac` | Mac-specific File::Spec methods |
| `File::Spec::OS2` | OS2-specific File::Spec methods |
| `File::Spec::VMS` | VMS-specific File::Spec methods |
| `File::Temp` | Create temporary files and directories |
| `File::stat` | By-name interface to Perl's built-in stat() functions |
| `DirHandle` | Supply object methods for directory handles |
| `Cwd` | Get pathname of current working directory |
| `Path::Class` | Cross-platform path specification manipulation |

### I/O Modules

| Code | Description |
|------|-------------|
| `IO` | Load the IO modules |
| `IO::File` | Supply object methods for filehandles |
| `IO::Pipe` | Supply object methods for pipes |
| `IO::Seekable` | Supply seek() and tell() for I/O objects |
| `IO::Select` | OO interface to select system call |
| `IO::Socket` | Object interface to socket communications |
| `IO::Socket::INET` | Object interface for AF_INET domain sockets |
| `IO::Socket::UNIX` | Object interface for AF_UNIX domain sockets |
| `IO::Poll` | OO interface to poll call |
| `IO::Dir` | Supply object methods for directory handles |
| `IO::Handle` | Supply object methods for I/O handles |
| `IO::All` | Load all IO modules |

### String and Text Modules

| Code | Description |
|------|-------------|
| `Text::Abbrev` | Create an abbreviation table from a list |
| `Text::Balanced` | Extract delimited text sequences from strings |
| `Text::ParseWords` | Parse text into an array of tokens or array of arrays |
| `Text::Soundex` | Implementation of the Soundex algorithm |
| `Text::Tabs` | Expand tabs to spaces |
| `Text::Wrap` | Line wrapping to form simple paragraphs |
| `Text::Unidecode` | US-ASCII transliterations of Unicode text |
| `String::Compare` | Compare two strings according to a collation table |
| `String::ShellQuote` | Quote strings for safe use in shells |
| `String::Escape` | Backslash escape sequences |

### Data Structure Modules

| Code | Description |
|------|-------------|
| `List::Util` | A selection of general-utility list subroutines |
| `List::MoreUtils` | Provide the stuff missing in List::Util |
| `List::Util::XS` | XS implementation of List::Util |
| `Scalar::Util` | A selection of general-utility scalar subroutines |
| `Scalar::Util::Numeric` | Numeric tests for Scalar::Util |
| `Data::Dumper` | Stringified perl data structures, suitable for both printing and eval |
| `Storable` | Persistence for Perl data structures |
| `Tie::Array` | Base class for tied arrays |
| `Tie::Hash` | Base class for tied hashes |
| `Tie::Scalar` | Base class for tied scalars |
| `Tie::StdArray` | Standard array tie |
| `Tie::StdHash` | Standard hash tie |
| `Tie::StdScalar` | Standard scalar tie |
| `Tie::SubstrHash` | Fixed-table-size, fixed-key-length hashing |
| `Tie::RefHash` | Use references as hash keys |
| `Tie::Memoize` | Add caching to functions |
| `Memoize` | Make functions faster by trading space for time |
| `Tie::Hash::NamedCapture` | Named hash captures |

### Regular Expression Modules

| Code | Description |
|------|-------------|
| `re` | Pragmatic module to control regex engine |
| `Regexp::Common` | Provide commonly requested regular expressions |
| `Regexp::Common::balanced` | Provide regexes for balanced parentheses |
| `Regexp::Common::comment` | Provide regexes for comments |
| `Regexp::Common::delimited` | Provide regexes for delimited strings |
| `Regexp::Common::lingua` | Provide regexes for language strings |
| `Regexp::Common::list` | Provide regexes for lists |
| `Regexp::Common::net` | Provide regexes for IP addresses and networks |
| `Regexp::Common::number` | Provide regexes for numbers |
| `Regexp::Common::profanity` | Provide regexes for profanity |
| `Regexp::Common::URI` | Provide regexes for URIs |
| `Regexp::Common::whitespace` | Provide regexes for whitespace |
| `Regexp::Common::zip` | Provide regexes for ZIP codes |

### Math Modules

| Code | Description |
|------|-------------|
| `Math::BigInt` | Arbitrary size integers |
| `Math::BigInt::Calc` | Pure Perl module for arbitrary precision integer arithmetic |
| `Math::BigInt::FastCalc` | Math::BigInt::Calc with some XS for more speed |
| `Math::BigInt::Lite` | Math::BigInt with some XS for more speed |
| `Math::BigFloat` | Arbitrary size floating point numbers |
| `Math::BigRat` | Arbitrary size rational numbers |
| `Math::Complex` | Complex numbers and associated mathematical functions |
| `Math::Trig` | Trigonometric functions |
| `Math::BigInt::CalcEmu` | Emulate low-level integer arithmetic |

### Date and Time Modules

| Code | Description |
|------|-------------|
| `Time::Local` | Efficiently compute time from local and GMT time |
| `Time::gmtime` | By-name interface to Perl's built-in gmtime() function |
| `Time::localtime` | By-name interface to Perl's built-in localtime() function |
| `Time::tm` | Internal object used by Time::gmtime and Time::localtime |
| `Time::Seconds` | Simple API to convert human readable time to seconds and vice versa |
| `Time::Piece` | Object oriented time objects |
| `Time::Seconds` | Simple API to convert human readable time to seconds and vice versa |
| `Time::HiRes` | High resolution alarm, sleep, and gettimeofday |
| `Benchmark` | Benchmark running times of Perl code |
| `DateTime` | Date and time object |
| `DateTime::TimeZone` | Time zone object |
| `DateTime::Duration` | Duration object |
| `DateTime::Set` | Set of DateTime objects |
| `DateTime::Span` | Span of time between two DateTime objects |
| `DateTime::Format::Builder` | Create DateTime parser classes and objects |
| `DateTime::Format::ISO8601` | Parse and format ISO8601 dates |
| `DateTime::Format::Strptime` | Parse and format strptime patterns |

### System and Process Modules

| Code | Description |
|------|-------------|
| `Getopt::Long` | Extended processing of command line options |
| `Getopt::Std` | Process single-character switches with switch clustering |
| `Pod::Usage` | Print a usage message from embedded pod documentation |
| `Pod::Text` | Convert POD data to formatted ASCII text |
| `Pod::Man` | Convert POD data to formatted *roff input |
| `Pod::Html` | Convert POD data to HTML |
| `Pod::Parser` | Base class for creating POD filters and translators |
| `Pod::InputObjects` | Objects for POD input |
| `Pod::Select` | Extract selected sections of POD from input |
| `Sys::Hostname` | Try to get the system hostname |
| `Sys::Syslog` | Perl interface to the UNIX syslog |
| `User::grent` | By-name interface to Perl's built-in getgrent() |
| `User::pwent` | By-name interface to Perl's built-in getpwent() |
| `Proc::ProcessTable` | Perl interface to the UNIX process table |
| `Proc::Simple` | Launch and control background processes |
| `Proc::Background` | Generic interface to Unix and Win32 background process management |

### Networking Modules

| Code | Description |
|------|-------------|
| `Net::Ping` | Check a remote host for reachability |
| `Net::hostent` | By-name interface to Perl's built-in gethost*() functions |
| `Net::netent` | By-name interface to Perl's built-in getnet*() functions |
| `Net::protoent` | By-name interface to Perl's built-in getproto*() functions |
| `Net::servent` | By-name interface to Perl's built-in getserv*() functions |
| `Socket` | Load the C socket.h defines and structure manipulators |
| `IO::Socket::INET` | Object interface for AF_INET domain sockets |
| `IO::Socket::UNIX` | Object interface for AF_UNIX domain sockets |
| `IO::Socket::IP` | Family-neutral IP socket supporting IPv4 and IPv6 |
| `Net::Domain` | Attempt to evaluate the internet domain name of the current host |
| `Net::FTP` | Perl FTP Client class |
| `Net::SMTP` | Simple Mail Transfer Protocol Client |
| `Net::POP3` | Post Office Protocol 3 Client |
| `Net::NNTP` | News Transport Protocol Client |
| `Net::Time` | Time server client |
| `Net::Telnet` | Interactive Telnet client |

### Database Modules

| Code | Description |
|------|-------------|
| `DBI` | Database independent interface for Perl |
| `DBD::File` | DBI driver for text files, CSV files, and other text file formats |
| `DBD::CSV` | DBI driver for CSV files |
| `DBD::SQLite` | Self-contained RDBMS in a DBI Driver |
| `DBD::Pg` | PostgreSQL driver for DBI |
| `DBD::mysql` | MySQL driver for DBI |
| `DBD::Oracle` | Oracle driver for DBI |
| `DBM_Filter` | Filter DBM keys and/or values |
| `DBM_Filter::compress` | Filter for DBM_Filter |
| `DBM_Filter::encode` | Filter for DBM_Filter |
| `DBM_Filter::int32` | Filter for DBM_Filter |
| `DBM_Filter::null` | Filter for DBM_Filter |
| `DBM_Filter::utf8` | Filter for DBM_Filter |
| `AnyDBM_File` | Provide framework for multiple DBM implementations |
| `DB_File` | Access to Berkeley DB version 1.x |
| `GDBM_File` | Tied access to gdbm files |
| `NDBM_File` | Tied access to ndbm files |
| `ODBM_File` | Tied access to odbm files |
| `SDBM_File` | Tied access to sdbm files |
| `BerkeleyDB` | Perl interface to Berkeley DB |

### Compression Modules

| Code | Description |
|------|-------------|
| `Compress::Raw::Zlib` | Low-Level Interface to zlib compression library |
| `Compress::Zlib` | Interface to zlib compression library |
| `IO::Compress::Adapter::Bzip2` | Write bzip2 compressed data |
| `IO::Compress::Adapter::Deflate` | Write RFC 1951 raw deflate compressed data |
| `IO::Compress::Adapter::Identity` | Write uncompressed data |
| `IO::Compress::Base` | Base Class for IO::Compress modules |
| `IO::Compress::Bzip2` | Write bzip2 compressed data |
| `IO::Compress::Deflate` | Write RFC 1951 raw deflate compressed data |
| `IO::Compress::Gzip` | Write gzip compressed data |
| `IO::Compress::RawDeflate` | Write RFC 1951 raw deflate compressed data |
| `IO::Compress::Zip` | Write zip compressed data |
| `IO::Uncompress::Adapter::Bunzip2` | Read bzip2 compressed data |
| `IO::Uncompress::Adapter::Identity` | Read uncompressed data |
| `IO::Uncompress::Adapter::Inflate` | Read RFC 1951 raw deflate compressed data |
| `IO::Uncompress::AnyInflate` | Read RFC 1951 raw deflate or zlib compressed data |
| `IO::Uncompress::AnyUncompress` | Uncompress zlib, gzip or bzip2 |
| `IO::Uncompress::Bunzip2` | Read bzip2 compressed data |
| `IO::Uncompress::Gunzip` | Read gzip compressed data |
| `IO::Uncompress::Inflate` | Read RFC 1951 raw deflate compressed data |
| `IO::Uncompress::RawInflate` | Read RFC 1951 raw deflate compressed data |
| `IO::Uncompress::Unzip` | Read zip compressed data |
| `Archive::Tar` | Perl module for creation and manipulation of tar files |
| `Archive::Zip` | Provide an interface to ZIP archive files |
| `Archive::Extract` | A generic archive extracting mechanism |

### Unicode and Encoding Modules

| Code | Description |
|------|-------------|
| `Encode` | Character encoding |
| `Encode::Alias` | Alias definitions to encodings |
| `Encode::Encoding` | Encoding class |
| `Encode::Supported` | List of supported encodings |
| `Encode::MIME::Header` | MIME 'B' and 'Q' header encoding/decoding |
| `Encode::Unicode` | Various Unicode Encodings |
| `Encode::UTF8` | UTF-8 encoding |
| `I18N::Langinfo` | Query locale information |
| `I18N::LangTags` | Functions for dealing with language tags |
| `Locale::Codes` | Country and currency code sets |
| `Locale::Country` | ISO codes for country identification |
| `Locale::Currency` | ISO three-letter codes for currency identification |
| `Locale::Language` | ISO two-letter codes for language identification |
| `Locale::Maketext` | Framework for localization |
| `Locale::Script` | ISO codes for script identification |
| `Unicode::Collate` | Unicode collation algorithm |
| `Unicode::Normalize` | Unicode normalization forms |
| `Unicode::UCD` | Unicode character database |
| `Unicode::GCString` | String of characters in the General Category |
| `Unicode::LineBreak` | UAX #14 Unicode Line Breaking Algorithm |
| `charnames` | Access to Unicode character names and named character sequences |

### Object-Oriented Programming Modules

| Code | Description |
|------|-------------|
| `Class::Struct` | Declare struct-like datatypes as Perl classes |
| `fields` | Compile-time class fields |
| `base` | Establish an IS-A relationship with base classes |
| `parent` | Establish an IS-A relationship with base classes at compile time |
| `lib` | Manipulate @INC at compile time |
| `overload` | Overload operators for a class |
| `Attribute::Handlers` | Simpler definition of attribute handlers |
| `Class::ISA` | Report the search path for a class's ISA tree |
| `Devel::SelfStubber` | Generate stubs for a SelfLoading class |
| `SelfLoader` | Load functions only when needed |
| `UNIVERSAL` | Base class for ALL classes (blessed references) |
| `UNIVERSAL::require` | Require a module and check for object oriented interface |
| `UNIVERSAL::isa` | Check if an object is a subclass of a class |
| `UNIVERSAL::can` | Check if an object can perform a method |
| `UNIVERSAL::VERSION` | Get the version of a module |
| `Class::Load` | A working (require Class::Name) and more |
| `Class::Load::XS` | XS implementation of Class::Load |
| `Class::Unload` | Unload a class |
| `Class::Inspector` | Get information about a class and its structure |
| `Class::MethodMaker` | Create common types of methods |
| `Class::MethodModifiers` | Provide Moose-like method modifiers |
| `Class::Tiny` | Minimalist class construction |
| `Moo` | Minimalist Object Orientation (with Moose compatibility) |
| `Moose` | A postmodern object system for Perl 5 |
| `Mouse` | Moose compatible object system |

### Testing and Debugging Modules

| Code | Description |
|------|-------------|
| `Test` | A simple framework for writing test scripts |
| `Test::Harness` | Run Perl standard test scripts with statistics |
| `Test::More` | Yet another framework for writing test scripts |
| `Test::Simple` | Basic utilities for writing tests |
| `Test::Exception` | Test exception-based code |
| `Test::Deep` | Extremely flexible deep comparisons |
| `Test::Warn` | Test methods for warnings |
| `Test::NoWarnings` | Test that no warnings are generated |
| `Test::Deep::NoTest` | Deep comparison without test context |
| `Test::LongString` | Tests for long strings |
| `Test::Memory::Cycle` | Check for memory leaks and circular references |
| `Devel::Peek` | A data debugging tool for the XS programmer |
| `Devel::SelfStubber` | Generate stubs for a SelfLoading class |
| `Dumpvalue` | Provide screen dump of Perl data structures |
| `Data::Dump` | Pretty printing of data structures |
| `Data::Dumper` | Stringified perl data structures |
| `Data::Dump::Streamer` | Perlish deconstruction of data structures |
| `Devel::Symdump` | Dump symbol names or the symbol table |
| `Devel::Size` | Find the memory usage of Perl variables |
| `Devel::Cycle` | Find memory cycles in objects |
| `Devel::Cover` | Code coverage metrics for Perl |

### Serialization Modules

| Code | Description |
|------|-------------|
| `Data::Dumper` | Stringified perl data structures |
| `Storable` | Persistence for Perl data structures |
| `FreezeThaw` | Convert Perl structures to strings and back |
| `JSON::PP` | JSON::XS compatible pure-Perl module |
| `JSON::XS` | JSON serialising / deserialising (C based) |
| `CBOR::XS` | Concise Binary Object Representation (CBOR) |
| `Sereal::Encoder` | Fast, compact, powerful binary serialization |
| `Sereal::Decoder` | Fast, compact, powerful binary deserialization |
| `YAML` | YAML Ain't Markup Language |
| `YAML::XS` | Perl extension for YAML |
| `Data::MessagePack` | MessagePack serialising / deserialising |
| `XML::Simple` | Easy API for reading and writing XML |

### Module Loading and Distribution

| Code | Description |
|------|-------------|
| `Module::CoreList` | What modules shipped with versions of Perl |
| `Module::Load` | Runtime require of both modules and files |
| `Module::Load::Conditional` | Looking up module information / loading modules conditionally |
| `Module::Loaded` | Mark modules as loaded or unloaded |
| `Module::Metadata` | Gather package and POD information from perl module files |
| `Module::Build` | Build and install Perl modules |
| `Module::Build::Compat` | Compatibility with ExtUtils::MakeMaker |
| `Module::Build::Platform::Default` | Default platform-specific behaviors |
| `Module::Build::Platform::Unix` | Unix platform-specific behaviors |
| `Module::Build::Platform::Windows` | Windows platform-specific behaviors |
| `Module::Build::Platform::VMS` | VMS platform-specific behaviors |
| `Module::Build::Platform::MacOS` | MacOS platform-specific behaviors |
| `ExtUtils::MakeMaker` | Create a module Makefile |
| `ExtUtils::Manifest` | Utilities to write and check a MANIFEST file |
| `ExtUtils::Command` | Utilities to replace common UNIX commands |
| `ExtUtils::Embed` | Utilities for embedding Perl into C/C++ applications |
| `ExtUtils::Install` | Install files from here into blib |
| `ExtUtils::Installed` | Inventory management of installed modules |
| `ExtUtils::Packlist` | Manage .packlist files |
| `ExtUtils::ParseXS` | Parse XS code into C code |
| `ExtUtils::XSSymSet` | Keep sets of symbol names |
| `Pod::Checker` | Check pod documents for syntax errors |
| `Pod::Parser` | Base class for creating POD filters and translators |
| `Pod::Simple` | Framework for parsing POD |
| `Pod::Simple::HTML` | Convert POD to HTML |
| `Pod::Simple::HTMLBatch` | Convert POD to HTML in batches |
| `Pod::Simple::LinkSection` | Represent a section of POD as a link |
| `Pod::Simple::Progress` | A Pod::Simple subclass that outputs a progress meter |
| `Pod::Simple::PullParser` | A Pod parser that does most of its work at instantiation time |
| `Pod::Simple::PullParserEndToken` | End token for Pod::Simple::PullParser |
| `Pod::Simple::PullParserStartToken` | Start token for Pod::Simple::PullParser |
| `Pod::Simple::PullParserTextToken` | Text token for Pod::Simple::PullParser |
| `Pod::Simple::Search` | Find POD documents in a directory tree |
| `Pod::Simple::SimpleTree` | A simple tree object |
| `Pod::Simple::Transcode` | Convert POD from one encoding to another |
| `Pod::Simple::TranscodeDumb` | A dumb transcode filter |
| `Pod::Simple::XHTML` | Convert POD to XHTML |
| `Pod::Simple::XMLOutStream` | A Pod::Simple subclass that outputs XML |

### Error Handling Modules

| Code | Description |
|------|-------------|
| `Carp` | Alternative warn and die for modules |
| `Carp::Heavy` | Carp guts |
| `Try::Tiny` | Minimal try/catch with proper localisation of $@ |
| `Error` | Error/exception handling in an OO-ish way |
| `Fatal` | Replace functions with equivalents which succeed or die |
| `Exception::Class` | A real exception class |
| `Exception::Class::Base` | Base class for exception classes |
| `Exception::Class::DBI` | DBI exception class |
| `Exception::Class::TryCatch` | Try/catch syntax for exceptions |
| `Throw` | A minimal class for throwing exceptions |

### Configuration and INI Modules

| Code | Description |
|------|-------------|
| `Config` | Access Perl configuration information |
| `Config::Extensions` | Hash of installed Perl extensions |
| `Config::Perl::V` | Structured data retrieval of perl -V output |
| `Config::INI` | Read and write INI files |
| `Config::INI::Reader` | Read INI files |
| `Config::INI::Writer` | Write INI files |
| `Config::Tiny` | Read/Write .ini style files with as little code as possible |
| `Config::AutoConf` | A module to implement some AutoConf macros in pure Perl |
| `Config::General` | Generic Config Module |

### Web and HTTP Modules

| Code | Description |
|------|-------------|
| `CGI` | Simple Common Gateway Interface Class |
| `CGI::Fast` | CGI Interface for Fast CGI |
| `CGI::Pretty` | Module for prettifying CGI scripts |
| `CGI::Carp` | CGI routines for writing to the HTTPD (or other) error log |
| `CGI::Cookie` | Interface to HTTP Cookies |
| `CGI::Header` | MIME message header |
| `CGI::Minimal` | Minimal CGI interface |
| `CGI::Push` | Simple Interface to Server Push |
| `CGI::Switch` | Backward-compatible dispatch mechanism for CGI scripts |
| `CGI::Util` | Internal utilities used by CGI module |
| `HTTP::Date` | Date conversion routines |
| `HTTP::Message` | HTTP message base class |
| `HTTP::Request` | HTTP request message |
| `HTTP::Response` | HTTP response message |
| `HTTP::Headers` | Class encapsulating HTTP message headers |
| `HTTP::Status` | HTTP status code handling |
| `HTTP::Negotiate` | HTTP content negotiation |
| `LWP::UserAgent` | World Wide Web UserAgent class |
| `LWP::Simple` | Simple and consistent interface to LWP |
| `LWP::MediaTypes` | Guess media type for a file |
| `LWP::Protocol` | Base class for LWP protocols |
| `LWP::Protocol::http` | HTTP protocol |
| `LWP::Protocol::https` | HTTPS protocol |
| `LWP::Protocol::ftp` | FTP protocol |
| `LWP::Protocol::file` | File protocol |
| `LWP::Protocol::mailto` | Mailto protocol |
| `LWP::Protocol::nntp` | NNTP protocol |
| `LWP::Protocol::gopher` | Gopher protocol |
| `LWP::RobotUA` | A class for well-behaved Web robots |
| `LWP::Debug` | Debugging support for LWP |
| `URI` | Uniform Resource Identifiers |
| `URI::Escape` | Escape and unescape unsafe characters |
| `URI::File` | File URIs |
| `URI::Heuristic` | Try to guess the scheme of a URI |
| `URI::HTTP` | HTTP URIs |
| `URI::HTTPS` | HTTPS URIs |
| `URI::LDAP` | LDAP URIs |
| `URI::LDAPS` | LDAPS URIs |
| `URI::mailto` | Mailto URIs |
| `URI::news` | News URIs |
| `URI::nntp` | NNTP URIs |
| `URI::QueryParam` | Additional query parameter parsing |
| `URI::Split` | Split and join URIs |
| `URI::URL` | Uniform Resource Locators |
| `URI::WithBase` | URI with base URI support |
| `WWW::RobotRules` | Parse robots.txt files |

### Email Modules

| Code | Description |
|------|-------------|
| `Mail::Cap` | Generate mailto: URLs |
| `Mail::Field` | Base class for manipulation of mail header fields |
| `Mail::Field::AddrList` | Object for keeping RFC 2822 address lists |
| `Mail::Field::Date` | Date field manipulation |
| `Mail::Field::Generic` | Generic field manipulation |
| `Mail::Header` | Manipulate mail headers |
| `Mail::Internet` | Manipulate mail messages |
| `Mail::Message` | Base class for representations of mail messages |
| `Mail::Send` | Simple, generic interface to sending mail |
| `Mail::Sendmail` | Simple platform-independent mail sending |
| `Mail::Util` | Mail utility functions |
| `MIME::Base64` | Base64 and Quoted-Printable encoding and decoding |
| `MIME::QuotedPrint` | Quoted-Printable encoding and decoding |
| `MIME::Lite` | Lightweight MIME message handling |
| `MIME::Entity` | Class for parsing and creating MIME entities |
| `MIME::Field::ParamVal` | Parameter-value pair for MIME fields |
| `MIME::Field::ContDisp` | Content-Disposition field for MIME |
| `MIME::Field::ContType` | Content-Type field for MIME |
| `MIME::Head` | MIME message header |
| `MIME::Body` | MIME message body |
| `MIME::Parser` | Parser for MIME messages |
| `MIME::Tools` | MIME tools |
| `Net::SMTP` | Simple Mail Transfer Protocol Client |

### Security Modules

| Code | Description |
|------|-------------|
| `Digest` | Base class for Digest modules |
| `Digest::file` | Compute digests of files |
| `Digest::base` | Digest base class |
| `Digest::MD5` | Perl interface to RSA's MD5 Message Digest Algorithm |
| `Digest::SHA` | Perl extension for SHA-1/224/256/384/512 |
| `Digest::SHA1` | Perl interface to SHA-1 |
| `Digest::HMAC` | Keyed-Hashing for Message Authentication |
| `Digest::HMAC_MD5` | HMAC-MD5 keyed hash algorithm |
| `Digest::HMAC_SHA1` | HMAC-SHA-1 keyed hash algorithm |
| `Crypt::PasswdMD5` | Unix MD5 password hashing |
| `Crypt::PasswdXS` | XS implementation of Unix password hashing |
| `Crypt::DES` | DES encryption |
| `Crypt::DES_EDE3` | Triple DES EDE encryption |
| `Crypt::CBC` | Cipher Block Chaining for block ciphers |
| `Crypt::ECB` | Electronic Codebook mode for block ciphers |
| `Crypt::Blowfish` | Blowfish encryption |
| `Crypt::Twofish` | Twofish encryption |
| `Crypt::Rijndael` | Rijndael encryption |
| `Crypt::AES` | AES encryption |
| `Crypt::AES_PP` | Pure Perl AES |
| `Crypt::OpenSSL::Random` | OpenSSL pseudo-random number generator |
| `Crypt::OpenSSL::RSA` | RSA encryption and signing |
| `Crypt::OpenSSL::DSA` | DSA encryption and signing |
| `Crypt::OpenSSL::DH` | Diffie-Hellman key exchange |
| `Crypt::OpenSSL::Bignum` | OpenSSL arbitrary precision integers |
| `Crypt::OpenSSL::AES` | AES encryption |
| `Crypt::OpenSSL::Blowfish` | Blowfish encryption |
| `Crypt::OpenSSL::DES` | DES encryption |
| `Crypt::OpenSSL::IDEA` | IDEA encryption |
| `Crypt::OpenSSL::RC4` | RC4 encryption |
| `Crypt::OpenSSL::RC5` | RC5 encryption |

### Miscellaneous Core Modules

| Code | Description |
|------|-------------|
| `Autoloader` | Load functions only when needed |
| `AutoSplit` | Split a package for autoloading |
| `Exporter` | Implements default import method for modules |
| `Exporter::Heavy` | Exporter guts |
| `DynaLoader` | Dynamically load C libraries into Perl code |
| `XSLoader` | Dynamically load XS modules |
| `SelfLoader` | Load functions only when needed |
| `PerlIO` | On demand loader for PerlIO layers and root class |
| `PerlIO::encoding` | Encoding layer |
| `PerlIO::mmap` | Memory mapped file |
| `PerlIO::scalar` | In-memory IO |
| `PerlIO::via` | PerlIO layer for layers tied to Perl code |
| `PerlIO::utf8_strict` | Strict UTF-8 layer |
| `Filter::Util::Call` | Perl Filter Utility |
| `Filter::Simple` | Simplified source filtering |
| `Attribute::Handlers` | Simpler definition of attribute handlers |
| `Class::ISA` | Report the search path for a class's ISA tree |
| `Symbol` | Manipulate Perl symbols and their names |
| `SelectSaver` | Save and restore selected file handles |
| `Sub::Util` | A selection of utility subroutines for working with code references |
| `Test::Harness` | Run Perl standard test scripts with statistics |
| `Test::More` | Yet another framework for writing test scripts |
| `Test::Simple` | Basic utilities for writing tests |
| `B` | The Perl Compiler |
| `B::Concise` | Walk Perl syntax tree, printing concise info about ops |
| `B::Deparse` | Perl compiler backend to produce perl code |
| `B::Lint` | Perl lint |
| `B::Showlex` | Show lexical variables |
| `B::Terse` | Walk Perl syntax tree, printing terse info about ops |
| `B::Xref` | Generate cross reference reports for Perl programs |
| `Devel::Peek` | A data debugging tool for the XS programmer |
| `Devel::DProf` | A Perl code profiler |
| `Devel::NYTProf` | Powerful feature-rich Perl source code profiler |
| `Devel::Cover` | Code coverage metrics for Perl |