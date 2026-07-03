## Core Language Features

| Code | Description |
|------|-------------|
| `Object` | Root of Ruby's class hierarchy. All classes inherit from Object. |
| `Kernel` | Module included by Object. Contains core methods like `puts`, `require`, `loop`, etc. |
| `BasicObject` | Root of Ruby's class hierarchy with minimal functionality. Used for creating minimal objects. |
| `Module` | Base class for modules. Provides methods like `module_function`, `const_get`, `const_set`, `const_defined?`, `ancestors`, `included_modules`, `included`, `extended`, `prepended`, `method_defined?`, `private_method_defined?`, `protected_method_defined?`, `public_method_defined?`, `instance_methods`, `methods`, `constants`, `const_source_location`, `autoload`, `autoload?`. |
| `Class` | Base class for classes. Inherits from Module. Provides methods like `new`, `allocate`, `superclass`, `inherited`, `method_added`, `method_removed`, `method_undefined`, `singleton_method_added`, `singleton_method_removed`, `singleton_method_undefined`. |
| `self` | Refers to the current object. |
| `nil` | Represents nothingness. Evaluates to false in a boolean context. |
| `true` | Boolean true value. |
| `false` | Boolean false value. |
| `__FILE__` | String containing the path to the current source file. |
| `__LINE__` | Integer containing the current line number in the source file. |
| `__END__` | Marks the end of the executable code; data after this line is available via the DATA constant. |
| `DATA` | File object containing data after the __END__ line. |
| `BEGIN { ... }` | Code block that runs when the program starts. |
| `END { ... }` | Code block that runs when the program ends. |
| `alias` | Creates an alias for a method. |
| `alias new_name old_name` | Creates an alias for a method. |
| `alias :new_name :old_name` | Creates an alias for a method using symbols. |
| `and` | Logical AND operator. Returns the first operand if it is false, otherwise returns the second operand. |
| `or` | Logical OR operator. Returns the first operand if it is true, otherwise returns the second operand. |
| `not` | Logical NOT operator. Returns true if the operand is false, otherwise returns false. |
| `&&` | Logical AND operator with higher precedence than `and`. |
| `||` | Logical OR operator with higher precedence than `or`. |
| `!` | Logical NOT operator with higher precedence than `not`. |
| `defined?` | Checks if an expression is defined. Returns a string describing the expression or nil if it is not defined. |
| `defined?(variable)` | Checks if a variable is defined. |
| `defined?(method)` | Checks if a method is defined. |
| `defined?(super)` | Checks if a super method is defined. |
| `defined?(yield)` | Checks if a block is passed to the current method. |
| `if condition` | Executes code if the condition is true. |
| `if condition; ...; end` | Executes code if the condition is true. |
| `if condition; ...; else; ...; end` | Executes code if the condition is true, otherwise executes the else clause. |
| `if condition; ...; elsif condition; ...; else; ...; end` | Executes code based on multiple conditions. |
| `unless condition; ...; end` | Executes code unless the condition is true. |
| `unless condition; ...; else; ...; end` | Executes code unless the condition is true, otherwise executes the else clause. |
| `case expression` | Begins a case statement. |
| `case expression; when value; ...; end` | Executes code when the expression matches the value. |
| `case expression; when value1; ...; when value2; ...; end` | Executes code when the expression matches any of the values. |
| `case expression; when value; ...; else; ...; end` | Executes code when the expression matches the value, otherwise executes the else clause. |
| `while condition; ...; end` | Executes code while the condition is true. |
| `until condition; ...; end` | Executes code until the condition is true. |
| `begin; ...; end while condition` | Post-test loop that executes code while the condition is true. |
| `begin; ...; end until condition` | Post-test loop that executes code until the condition is true. |
| `loop { ... }` | Infinite loop. |
| `break` | Exits a loop. |
| `break value` | Exits a loop and returns the value. |
| `next` | Skips to the next iteration of a loop. |
| `next value` | Skips to the next iteration of a loop and returns the value. |
| `redo` | Repeats the current iteration of a loop. |
| `retry` | Retries the loop or begin block. |
| `for variable in collection; ...; end` | Iterates over a collection. |
| `collection.each { |variable| ... }` | Iterates over a collection using a block. |
| `return` | Returns from a method. |
| `return value` | Returns from a method with a value. |
| `return value1, value2` | Returns from a method with multiple values. |
| `yield` | Yields control to the block passed to the current method. |
| `yield arg1, arg2` | Yields arguments to the block passed to the current method. |
| `super` | Calls the superclass version of the current method. |
| `super(arg1, arg2)` | Calls the superclass version of the current method with arguments. |
| `super do ... end` | Calls the superclass version of the current method with a block. |
| `super(arg1, arg2) do ... end` | Calls the superclass version of the current method with arguments and a block. |
| `begin; ...; rescue; ...; end` | Begins a rescue block for exception handling. |
| `begin; ...; rescue ExceptionClass; ...; end` | Rescues specific exception classes. |
| `begin; ...; rescue ExceptionClass => variable; ...; end` | Rescues specific exception classes and assigns the exception to a variable. |
| `begin; ...; rescue; ...; else; ...; end` | Executes the else clause if no exceptions are raised. |
| `begin; ...; rescue; ...; ensure; ...; end` | Executes the ensure clause regardless of whether an exception is raised. |
| `raise` | Raises an exception. |
| `raise ExceptionClass` | Raises an exception of a specific class. |
| `raise ExceptionClass, message` | Raises an exception with a message. |
| `raise ExceptionClass, message, backtrace` | Raises an exception with a message and backtrace. |
| `raise message` | Raises a RuntimeError with a message. |
| `fail` | Alias for raise. |
| `begin; ...; rescue; ...; retry; end` | Retries the begin block if an exception is rescued. |

---
## Built-in Classes

| Code | Description |
|------|-------------|
| `String` | Represents a sequence of bytes or characters. Provides methods for string manipulation, comparison, and conversion. |
| `Symbol` | Represents an immutable, interned string. Used as keys in hashes and for method names. |
| `Array` | Represents an ordered collection of objects. Provides methods for array manipulation, iteration, and access. |
| `Hash` | Represents a key-value store (dictionary). Provides methods for hash manipulation, iteration, and access. |
| `Numeric` | Abstract base class for numbers. Provides methods for numeric operations and comparisons. |
| `Integer` | Represents integer numbers. Provides methods for integer operations and conversions. |
| `Fixnum` | Legacy class for small integers. In Ruby 2.4+, all integers are of class Integer. |
| `Bignum` | Legacy class for large integers. In Ruby 2.4+, all integers are of class Integer. |
| `Float` | Represents floating-point numbers. Provides methods for floating-point operations and conversions. |
| `Rational` | Represents rational numbers as a fraction. Provides methods for rational operations and conversions. |
| `Complex` | Represents complex numbers. Provides methods for complex operations and conversions. |
| `BigDecimal` | Represents arbitrary-precision decimal numbers. Provides methods for decimal operations and conversions. |
| `Regexp` | Represents regular expressions. Provides methods for pattern matching and manipulation. |
| `Range` | Represents a range of values. Provides methods for range operations and iteration. |
| `Proc` | Represents a procedure object (lambda/closure). Provides methods for calling and manipulating procedures. |
| `Lambda` | Represents a lambda procedure. Similar to Proc but with stricter argument checking. |
| `Method` | Represents a bound method object. Provides methods for calling and manipulating bound methods. |
| `UnboundMethod` | Represents an unbound method object. Provides methods for binding and manipulating unbound methods. |
| `Time` | Represents a date and time. Provides methods for time operations, formatting, and conversion. |
| `Date` | Represents a calendar date. Provides methods for date operations, formatting, and conversion. |
| `DateTime` | Represents a date and time with timezone support. Provides methods for datetime operations, formatting, and conversion. |
| `Struct` | Represents a simple attribute-based class. Provides methods for creating and manipulating structs. |
| `OpenStruct` | Represents a dynamic attribute struct. Provides methods for creating and manipulating open structs. |

---
## String Methods

| Code | Description |
|------|-------------|
| `String.new` | Creates a new empty string. |
| `"#{expression}"` | String interpolation. Embeds the result of an expression into a string. |
| `%q{}` | Single-quoted string literal. Does not support interpolation. |
| `%Q{}` | Double-quoted string literal. Supports interpolation. |
| `%w{}` | Array of words. Creates an array of strings separated by whitespace. |
| `%W{}` | Array of interpolated words. Creates an array of strings with interpolation. |
| `%x{}` | Command execution. Returns the output of a shell command. |
| `%r{}` | Regular expression literal. |
| `<<` | String concatenation operator. |
| `+` | String concatenation operator. |
| `*` | String repetition operator. |
| `[]` | Character or substring access. |
| `[]=` | Character or substring assignment. |
| `ascii_only?` | Returns true if the string contains only ASCII characters. |
| `b` | Returns a copy of the string with ASCII-8BIT encoding. |
| `bytes` | Returns an array of the bytes in the string. |
| `bytesize` | Returns the length of the string in bytes. |
| `byteslice` | Returns a substring by byte index. |
| `capitalize` | Returns a copy of the string with the first character capitalized and the rest lowercase. |
| `capitalize!` | Capitalizes the first character and lowercases the rest in place. Returns nil if no changes are made. |
| `casecmp` | Case-insensitive comparison. Returns -1, 0, or 1. |
| `casecmp?` | Case-insensitive equality comparison. Returns true or false. |
| `center` | Centers the string with padding. |
| `center(width)` | Centers the string with padding to the specified width. |
| `center(width, padstr)` | Centers the string with the specified padding string. |
| `chomp` | Returns a copy of the string with the trailing newline removed. |
| `chomp!` | Removes the trailing newline in place. Returns nil if no changes are made. |
| `chop` | Returns a copy of the string with the last character removed. |
| `chop!` | Removes the last character in place. Returns nil if no changes are made. |
| `chr` | Returns the first character of the string. |
| `clear` | Removes all characters from the string. |
| `codepoints` | Returns an array of the codepoints in the string. |
| `concat` | Concatenates a string to the end of the receiver. |
| `count` | Counts the occurrences of characters. |
| `count(char)` | Counts the occurrences of a specific character. |
| `count(char1, char2, ...)` | Counts the occurrences of multiple characters. |
| `count("char1-char2")` | Counts the occurrences of characters in a range. |
| `count(^char)` | Counts the occurrences of characters not in the set. |
| `crypto` | Returns a cryptographic hash of the string. |
| `delete` | Returns a copy of the string with the specified characters removed. |
| `delete!` | Removes the specified characters in place. Returns nil if no changes are made. |
| `delete_prefix` | Returns a copy of the string with the specified prefix removed. |
| `delete_prefix!` | Removes the specified prefix in place. Returns nil if no changes are made. |
| `delete_suffix` | Returns a copy of the string with the specified suffix removed. |
| `delete_suffix!` | Removes the specified suffix in place. Returns nil if no changes are made. |
| `downcase` | Returns a copy of the string with all characters converted to lowercase. |
| `downcase!` | Converts all characters to lowercase in place. Returns nil if no changes are made. |
| `dump` | Returns a escaped version of the string. |
| `each_byte` | Iterates over each byte in the string. |
| `each_char` | Iterates over each character in the string. |
| `each_codepoint` | Iterates over each codepoint in the string. |
| `each_line` | Iterates over each line in the string. |
| `empty?` | Returns true if the string has a length of zero. |
| `end_with?` | Returns true if the string ends with the specified suffix. |
| `end_with?(suffix1, suffix2, ...)` | Returns true if the string ends with any of the specified suffixes. |
| `eql?` | Returns true if the string is equal to the specified object. |
| `force_encoding` | Forces the encoding of the string to the specified encoding. |
| `freeze` | Freezes the string. |
| `frozen?` | Returns true if the string is frozen. |
| `getbyte` | Returns the byte at the specified index. |
| `gsub` | Replaces all occurrences of a pattern with a replacement. |
| `gsub(pattern, replacement)` | Replaces all occurrences of a pattern with a replacement. |
| `gsub(pattern) { |match| ... }` | Replaces all occurrences of a pattern using a block. |
| `gsub!` | Replaces all occurrences of a pattern in place. Returns nil if no changes are made. |
| `hash` | Returns a hash value for the string. |
| `hexdigest` | Returns a hexadecimal digest of the string. |
| `include?` | Returns true if the string contains the specified substring. |
| `index` | Returns the index of the first occurrence of a substring. |
| `index(substring)` | Returns the index of the first occurrence of a substring. |
| `index(substring, offset)` | Returns the index of the first occurrence of a substring starting from the specified offset. |
| `index(regexp)` | Returns the index of the first match of a regular expression. |
| `index(regexp, offset)` | Returns the index of the first match of a regular expression starting from the specified offset. |
| `insert` | Inserts a substring at the specified index. |
| `insert(index, substring)` | Inserts a substring at the specified index. |
| `insert!` | Inserts a substring at the specified index in place. Returns nil if the index is out of range. |
| `intern` | Returns the symbol corresponding to the string. |
| `length` | Returns the length of the string. |
| `size` | Returns the length of the string. |
| `lines` | Returns an array of the lines in the string. |
| `lines(separator)` | Returns an array of the lines in the string using the specified separator. |
| `ljust` | Left-justifies the string with padding. |
| `ljust(width)` | Left-justifies the string with padding to the specified width. |
| `ljust(width, padstr)` | Left-justifies the string with the specified padding string. |
| `lstrip` | Returns a copy of the string with leading whitespace removed. |
| `lstrip!` | Removes leading whitespace in place. Returns nil if no changes are made. |
| `match` | Matches the string against a regular expression. |
| `match(pattern)` | Matches the string against a regular expression and returns a MatchData object. |
| `next` | Returns the successor of the string. |
| `next!` | Replaces the string with its successor in place. Returns nil if no changes are made. |
| `oct` | Converts the string to an integer using base 8. |
| `ord` | Returns the codepoint of the first character in the string. |
| `partition` | Partitions the string at the first occurrence of a pattern. |
| `partition(pattern)` | Partitions the string at the first occurrence of a pattern and returns an array of three elements: the part before the match, the match, and the part after the match. |
| `prepend` | Prepends a string to the beginning of the receiver. |
| `replace` | Replaces the contents of the string with the specified string. |
| `reverse` | Returns a copy of the string with the characters in reverse order. |
| `reverse!` | Reverses the string in place. Returns the string. |
| `rindex` | Returns the index of the last occurrence of a substring. |
| `rindex(substring)` | Returns the index of the last occurrence of a substring. |
| `rindex(substring, offset)` | Returns the index of the last occurrence of a substring starting from the specified offset. |
| `rindex(regexp)` | Returns the index of the last match of a regular expression. |
| `rindex(regexp, offset)` | Returns the index of the last match of a regular expression starting from the specified offset. |
| `rjust` | Right-justifies the string with padding. |
| `rjust(width)` | Right-justifies the string with padding to the specified width. |
| `rjust(width, padstr)` | Right-justifies the string with the specified padding string. |
| `rpartition` | Partitions the string at the last occurrence of a pattern. |
| `rpartition(pattern)` | Partitions the string at the last occurrence of a pattern and returns an array of three elements: the part before the match, the match, and the part after the match. |
| `rstrip` | Returns a copy of the string with trailing whitespace removed. |
| `rstrip!` | Removes trailing whitespace in place. Returns nil if no changes are made. |
| `scan` | Scans the string for occurrences of a pattern. |
| `scan(pattern)` | Scans the string for occurrences of a pattern and returns an array of matches. |
| `scan(pattern) { |match| ... }` | Scans the string for occurrences of a pattern and passes each match to a block. |
| `setbyte` | Sets the byte at the specified index. |
| `slice` | Returns a substring. |
| `slice(index)` | Returns the character at the specified index. |
| `slice(start, length)` | Returns a substring starting at the specified index with the specified length. |
| `slice(range)` | Returns a substring for the specified range. |
| `slice!(index)` | Removes and returns the character at the specified index. |
| `slice!(start, length)` | Removes and returns a substring starting at the specified index with the specified length. |
| `slice!(range)` | Removes and returns a substring for the specified range. |
| `split` | Splits the string into an array of substrings. |
| `split(pattern)` | Splits the string into an array of substrings using the specified pattern. |
| `split(pattern, limit)` | Splits the string into an array of substrings using the specified pattern and limit. |
| `squeeze` | Returns a copy of the string with consecutive duplicate characters removed. |
| `squeeze!` | Removes consecutive duplicate characters in place. Returns nil if no changes are made. |
| `start_with?` | Returns true if the string starts with the specified prefix. |
| `start_with?(prefix1, prefix2, ...)` | Returns true if the string starts with any of the specified prefixes. |
| `strip` | Returns a copy of the string with leading and trailing whitespace removed. |
| `strip!` | Removes leading and trailing whitespace in place. Returns nil if no changes are made. |
| `sub` | Replaces the first occurrence of a pattern with a replacement. |
| `sub(pattern, replacement)` | Replaces the first occurrence of a pattern with a replacement. |
| `sub(pattern) { |match| ... }` | Replaces the first occurrence of a pattern using a block. |
| `sub!` | Replaces the first occurrence of a pattern in place. Returns nil if no changes are made. |
| `succ` | Returns the successor of the string. |
| `succ!` | Replaces the string with its successor in place. Returns nil if no changes are made. |
| `sum` | Returns the sum of the bytes in the string. |
| `sum(n)` | Returns the sum of the bytes in the string modulo n. |
| `swapcase` | Returns a copy of the string with the case of each character swapped. |
| `swapcase!` | Swaps the case of each character in place. Returns nil if no changes are made. |
| `to_c` | Converts the string to a complex number. |
| `to_f` | Converts the string to a float. |
| `to_i` | Converts the string to an integer. |
| `to_i(base)` | Converts the string to an integer using the specified base. |
| `to_r` | Converts the string to a rational number. |
| `to_s` | Returns the string itself. |
| `to_sym` | Converts the string to a symbol. |
| `tr` | Replaces characters in the string. |
| `tr(from, to)` | Replaces characters in the string. |
| `tr!(from, to)` | Replaces characters in the string in place. Returns nil if no changes are made. |
| `tr_s` | Replaces and squeezes characters in the string. |
| `tr_s!(from, to)` | Replaces and squeezes characters in the string in place. Returns nil if no changes are made. |
| `unpack` | Decodes the string into an array of values. |
| `unpack(format)` | Decodes the string into an array of values using the specified format. |
| `unpack1` | Decodes the string into a single value. |
| `unpack1(format)` | Decodes the string into a single value using the specified format. |
| `upcase` | Returns a copy of the string with all characters converted to uppercase. |
| `upcase!` | Converts all characters to uppercase in place. Returns nil if no changes are made. |
| `upto` | Iterates over the string from the current string up to the specified string. |
| `upto(other) { |str| ... }` | Iterates over the string from the current string up to the specified string. |
| `valid_encoding?` | Returns true if the string has a valid encoding. |

---
## Symbol Methods

| Code | Description |
|------|-------------|
| `:symbol` | Creates a symbol. |
| `"string".to_sym` | Converts a string to a symbol. |
| `"string".intern` | Converts a string to a symbol. |
| `Symbol.all_symbols` | Returns an array of all symbols. |
| `id2name` | Returns the name of the symbol. |
| `inspect` | Returns the string representation of the symbol. |
| `to_s` | Returns the string representation of the symbol. |
| `to_proc` | Returns a Proc that calls the method represented by the symbol. |
| `match` | Matches the symbol against a regular expression. |

---
## Array Methods

| Code | Description |
|------|-------------|
| `Array.new` | Creates a new empty array. |
| `Array.new(size)` | Creates a new array with the specified size. |
| `Array.new(size, default)` | Creates a new array with the specified size and default value. |
| `Array.new { |index| ... }` | Creates a new array using a block to determine each element. |
| `[]` | Creates a new empty array. |
| `[1, 2, 3]` | Creates a new array with the specified elements. |
| `%w{word1 word2 word3}` | Creates a new array of words. |
| `%W{word1 word2 word3}` | Creates a new array of interpolated words. |
| `*` | Array repetition operator. |
| `+` | Array concatenation operator. |
| `-` | Array difference operator. |
| `<<` | Array append operator. |
| `[]` | Element access. |
| `[]=` | Element assignment. |
| `abbrev` | Returns a hash of abbreviations for the array. |
| `all?` | Returns true if all elements satisfy the condition. |
| `all? { |element| ... }` | Returns true if all elements satisfy the condition specified by the block. |
| `any?` | Returns true if any element satisfies the condition. |
| `any? { |element| ... }` | Returns true if any element satisfies the condition specified by the block. |
| `assoc` | Searches for an element that is an array whose first element matches the specified object. |
| `assoc(obj)` | Searches for an element that is an array whose first element matches the specified object. |
| `at` | Returns the element at the specified index. |
| `at(index)` | Returns the element at the specified index. |
| `bsearch` | Performs a binary search on the array. |
| `bsearch { |element| ... }` | Performs a binary search on the array using a block. |
| `bsearch_index` | Performs a binary search on the array and returns the index. |
| `bsearch_index { |element| ... }` | Performs a binary search on the array and returns the index using a block. |
| `cartesian_product` | Returns the Cartesian product of the array with the specified arrays. |
| `cartesian_product(other_arrays...)` | Returns the Cartesian product of the array with the specified arrays. |
| `cartesian_product(other_arrays...) { |element| ... }` | Returns the Cartesian product of the array with the specified arrays and passes each element to a block. |
| `casecmp` | Case-insensitive comparison. |
| `casecmp(other)` | Case-insensitive comparison with another array. |
| `chunk` | Groups consecutive elements that satisfy the condition. |
| `chunk { |element| ... }` | Groups consecutive elements that satisfy the condition specified by the block. |
| `chunk_while` | Groups consecutive elements while the condition is true. |
| `chunk_while { |before, after| ... }` | Groups consecutive elements while the condition specified by the block is true. |
| `clear` | Removes all elements from the array. |
| `clone` | Returns a shallow copy of the array. |
| `collect` | Returns a new array with the results of running the block for each element. |
| `collect { |element| ... }` | Returns a new array with the results of running the block for each element. |
| `collect!` | Replaces each element with the result of running the block for each element. Returns the array. |
| `collect! { |element| ... }` | Replaces each element with the result of running the block for each element. |
| `collect_concat` | Returns a new array with the results of running the block for each element and concatenates the results. |
| `collect_concat { |element| ... }` | Returns a new array with the results of running the block for each element and concatenates the results. |
| `combination` | Returns all combinations of the specified size. |
| `combination(n)` | Returns all combinations of the specified size. |
| `combination(n) { |elements| ... }` | Returns all combinations of the specified size and passes each combination to a block. |
| `compact` | Returns a new array with all nil elements removed. |
| `compact!` | Removes all nil elements in place. Returns nil if no changes are made. |
| `concat` | Appends elements to the end of the array. |
| `concat(other_array)` | Appends elements from another array to the end of the array. |
| `count` | Counts the number of elements that satisfy the condition. |
| `count` | Returns the number of elements. |
| `count(obj)` | Counts the number of elements equal to the specified object. |
| `count { |element| ... }` | Counts the number of elements that satisfy the condition specified by the block. |
| `cycle` | Cycles through the array indefinitely. |
| `cycle { |element| ... }` | Cycles through the array indefinitely and passes each element to a block. |
| `cycle(n)` | Cycles through the array n times. |
| `cycle(n) { |element| ... }` | Cycles through the array n times and passes each element to a block. |
| `delete` | Deletes all elements equal to the specified object. |
| `delete(obj)` | Deletes all elements equal to the specified object. |
| `delete(obj) { |element| ... }` | Deletes all elements equal to the specified object and passes each deleted element to a block. |
| `delete_at` | Deletes the element at the specified index. |
| `delete_at(index)` | Deletes the element at the specified index. |
| `delete_if` | Deletes all elements that satisfy the condition. |
| `delete_if { |element| ... }` | Deletes all elements that satisfy the condition specified by the block. |
| `dig` | Safely navigates nested data structures. |
| `dig(key1, key2, ...)` | Safely navigates nested data structures. |
| `drop` | Drops the first n elements. |
| `drop(n)` | Drops the first n elements. |
| `drop_while` | Drops elements while the condition is true. |
| `drop_while { |element| ... }` | Drops elements while the condition specified by the block is true. |
| `each` | Iterates over each element. |
| `each { |element| ... }` | Iterates over each element and passes each element to a block. |
| `each_index` | Iterates over each index. |
| `each_index { |index| ... }` | Iterates over each index and passes each index to a block. |
| `each_with_index` | Iterates over each element with its index. |
| `each_with_index { |element, index| ... }` | Iterates over each element with its index and passes each element and index to a block. |
| `each_with_object` | Iterates over each element and accumulates a result. |
| `each_with_object(obj) { |element| ... }` | Iterates over each element and accumulates a result in the specified object. |
| `empty?` | Returns true if the array has no elements. |
| `eql?` | Returns true if the array is equal to the specified object. |
| `fetch` | Returns the element at the specified index. |
| `fetch(index)` | Returns the element at the specified index. |
| `fetch(index, default)` | Returns the element at the specified index or the default value if the index is out of range. |
| `fetch(index) { |i| ... }` | Returns the element at the specified index or the result of the block if the index is out of range. |
| `fill` | Fills the array with the specified value. |
| `fill(value)` | Fills the array with the specified value. |
| `fill(value, start)` | Fills the array with the specified value starting from the specified index. |
| `fill(value, start, length)` | Fills the array with the specified value starting from the specified index for the specified length. |
| `fill(value, range)` | Fills the array with the specified value for the specified range. |
| `fill { |index| ... }` | Fills the array using a block. |
| `fill(start) { |index| ... }` | Fills the array using a block starting from the specified index. |
| `fill(start, length) { |index| ... }` | Fills the array using a block starting from the specified index for the specified length. |
| `fill(range) { |index| ... }` | Fills the array using a block for the specified range. |
| `filter` | Returns a new array containing all elements that satisfy the condition. |
| `filter { |element| ... }` | Returns a new array containing all elements that satisfy the condition specified by the block. |
| `filter!` | Replaces the array with all elements that satisfy the condition. Returns nil if no changes are made. |
| `filter! { |element| ... }` | Replaces the array with all elements that satisfy the condition specified by the block. |
| `find` | Returns the first element that satisfies the condition. |
| `find { |element| ... }` | Returns the first element that satisfies the condition specified by the block. |
| `find_all` | Returns all elements that satisfy the condition. |
| `find_all { |element| ... }` | Returns all elements that satisfy the condition specified by the block. |
| `find_index` | Returns the index of the first element that satisfies the condition. |
| `find_index { |element| ... }` | Returns the index of the first element that satisfies the condition specified by the block. |
| `find_index(obj)` | Returns the index of the first element equal to the specified object. |
| `first` | Returns the first element. |
| `first(n)` | Returns the first n elements. |
| `flat_map` | Returns a new array with the concatenated results of running the block for each element. |
| `flat_map { |element| ... }` | Returns a new array with the concatenated results of running the block for each element. |
| `flatten` | Returns a new array that is a one-dimensional flattening of the array. |
| `flatten!` | Flattens the array in place. Returns the array. |
| `flatten(level)` | Returns a new array that is a one-dimensional flattening of the array up to the specified level. |
| `flatten!(level)` | Flattens the array in place up to the specified level. Returns the array. |
| `frozen?` | Returns true if the array is frozen. |
| `group_by` | Groups the elements by the result of the block. |
| `group_by { |element| ... }` | Groups the elements by the result of the block. |
| `hash` | Returns a hash value for the array. |
| `include?` | Returns true if the array contains the specified object. |
| `index` | Returns the index of the first element equal to the specified object. |
| `index(obj)` | Returns the index of the first element equal to the specified object. |
| `index { |element| ... }` | Returns the index of the first element that satisfies the condition specified by the block. |
| `insert` | Inserts elements before the specified index. |
| `insert(index, *objects)` | Inserts elements before the specified index. |
| `inspect` | Returns a string representation of the array. |
| `intersection` | Returns a new array containing elements common to both arrays. |
| `intersection(other_array)` | Returns a new array containing elements common to both arrays. |
| `join` | Returns a string created by joining the elements with the specified separator. |
| `join(separator)` | Returns a string created by joining the elements with the specified separator. |
| `keep_if` | Keeps only the elements that satisfy the condition. |
| `keep_if { |element| ... }` | Keeps only the elements that satisfy the condition specified by the block. |
| `keep_if!` | Keeps only the elements that satisfy the condition in place. Returns nil if no changes are made. |
| `keep_if! { |element| ... }` | Keeps only the elements that satisfy the condition in place. |
| `last` | Returns the last element. |
| `last(n)` | Returns the last n elements. |
| `lazy` | Returns a lazy enumerator for the array. |
| `length` | Returns the number of elements in the array. |
| `map` | Returns a new array with the results of running the block for each element. |
| `map { |element| ... }` | Returns a new array with the results of running the block for each element. |
| `map!` | Replaces each element with the result of running the block for each element. Returns the array. |
| `map! { |element| ... }` | Replaces each element with the result of running the block for each element. |
| `max` | Returns the maximum element. |
| `max { |a, b| ... }` | Returns the maximum element using the block for comparison. |
| `max(n)` | Returns the first n maximum elements. |
| `max(n) { |a, b| ... }` | Returns the first n maximum elements using the block for comparison. |
| `max_by` | Returns the element with the maximum value. |
| `max_by { |element| ... }` | Returns the element with the maximum value specified by the block. |
| `member?` | Returns true if the array contains the specified object. |
| `min` | Returns the minimum element. |
| `min { |a, b| ... }` | Returns the minimum element using the block for comparison. |
| `min(n)` | Returns the first n minimum elements. |
| `min(n) { |a, b| ... }` | Returns the first n minimum elements using the block for comparison. |
| `min_by` | Returns the element with the minimum value. |
| `min_by { |element| ... }` | Returns the element with the minimum value specified by the block. |
| `minmax` | Returns a two-element array containing the minimum and maximum elements. |
| `minmax { |a, b| ... }` | Returns a two-element array containing the minimum and maximum elements using the block for comparison. |
| `minmax_by` | Returns a two-element array containing the elements with the minimum and maximum values. |
| `minmax_by { |element| ... }` | Returns a two-element array containing the elements with the minimum and maximum values specified by the block. |
| `none?` | Returns true if no elements satisfy the condition. |
| `none? { |element| ... }` | Returns true if no elements satisfy the condition specified by the block. |
| `one?` | Returns true if exactly one element satisfies the condition. |
| `one? { |element| ... }` | Returns true if exactly one element satisfies the condition specified by the block. |
| `pack` | Packs the contents of the array into a binary sequence. |
| `pack(template)` | Packs the contents of the array into a binary sequence using the specified template. |
| `partition` | Partitions the array into two arrays based on the condition. |
| `partition { |element| ... }` | Partitions the array into two arrays based on the condition specified by the block. |
| `permutation` | Returns all permutations of the specified size. |
| `permutation(n)` | Returns all permutations of the specified size. |
| `permutation(n) { |elements| ... }` | Returns all permutations of the specified size and passes each permutation to a block. |
| `permutation(to_shuffle)` | Returns all permutations of the array. |
| `permutation(to_shuffle) { |elements| ... }` | Returns all permutations of the array and passes each permutation to a block. |
| `pop` | Removes and returns the last element. |
| `pop(n)` | Removes and returns the last n elements. |
| `prepend` | Prepends elements to the beginning of the array. |
| `prepend(*objects)` | Prepends elements to the beginning of the array. |
| `product` | Returns the Cartesian product of the array with the specified arrays. |
| `product(other_arrays...)` | Returns the Cartesian product of the array with the specified arrays. |
| `product(other_arrays...) { |element| ... }` | Returns the Cartesian product of the array with the specified arrays and passes each element to a block. |
| `push` | Appends elements to the end of the array. |
| `push(*objects)` | Appends elements to the end of the array. |
| `rassoc` | Searches for an element that is an array whose last element matches the specified object. |
| `rassoc(obj)` | Searches for an element that is an array whose last element matches the specified object. |
| `reject` | Returns a new array containing all elements that do not satisfy the condition. |
| `reject { |element| ... }` | Returns a new array containing all elements that do not satisfy the condition specified by the block. |
| `reject!` | Replaces the array with all elements that do not satisfy the condition. Returns nil if no changes are made. |
| `reject! { |element| ... }` | Replaces the array with all elements that do not satisfy the condition specified by the block. |
| `repeated_combination` | Returns all combinations of the specified size with repetition. |
| `repeated_combination(n)` | Returns all combinations of the specified size with repetition. |
| `repeated_combination(n) { |elements| ... }` | Returns all combinations of the specified size with repetition and passes each combination to a block. |
| `repeated_permutation` | Returns all permutations of the specified size with repetition. |
| `repeated_permutation(n)` | Returns all permutations of the specified size with repetition. |
| `repeated_permutation(n) { |elements| ... }` | Returns all permutations of the specified size with repetition and passes each permutation to a block. |
| `replace` | Replaces the contents of the array with the specified array. |
| `replace(other_array)` | Replaces the contents of the array with the specified array. |
| `reverse` | Returns a new array with the elements in reverse order. |
| `reverse!` | Reverses the array in place. Returns the array. |
| `reverse_each` | Iterates over the array in reverse order. |
| `reverse_each { |element| ... }` | Iterates over the array in reverse order and passes each element to a block. |
| `rindex` | Searches backward for an element equal to the specified object. |
| `rindex(obj)` | Searches backward for an element equal to the specified object. |
| `rotate` | Rotates the array. |
| `rotate(n)` | Rotates the array by n positions. |
| `rotate!` | Rotates the array in place. Returns the array. |
| `rotate!(n)` | Rotates the array in place by n positions. Returns the array. |
| `sample` | Returns a random element. |
| `sample(n)` | Returns n random elements. |
| `sample(random: rng)` | Returns a random element using the specified random number generator. |
| `select` | Returns a new array containing all elements that satisfy the condition. |
| `select { |element| ... }` | Returns a new array containing all elements that satisfy the condition specified by the block. |
| `select!` | Replaces the array with all elements that satisfy the condition. Returns nil if no changes are made. |
| `select! { |element| ... }` | Replaces the array with all elements that satisfy the condition specified by the block. |
| `shift` | Removes and returns the first element. |
| `shift(n)` | Removes and returns the first n elements. |
| `shuffle` | Returns a new array with the elements in random order. |
| `shuffle(random: rng)` | Returns a new array with the elements in random order using the specified random number generator. |
| `shuffle!` | Shuffles the array in place. Returns the array. |
| `shuffle!(random: rng)` | Shuffles the array in place using the specified random number generator. Returns the array. |
| `size` | Returns the number of elements in the array. |
| `slice` | Returns a subarray. |
| `slice(index)` | Returns the element at the specified index. |
| `slice(start, length)` | Returns a subarray starting at the specified index with the specified length. |
| `slice(range)` | Returns a subarray for the specified range. |
| `slice!` | Removes and returns a subarray. |
| `slice!(index)` | Removes and returns the element at the specified index. |
| `slice!(start, length)` | Removes and returns a subarray starting at the specified index with the specified length. |
| `slice!(range)` | Removes and returns a subarray for the specified range. |
| `slice_after` | Returns subarrays after the specified pattern. |
| `slice_after(pattern)` | Returns subarrays after the specified pattern. |
| `slice_after { |element| ... }` | Returns subarrays after the pattern specified by the block. |
| `slice_before` | Returns subarrays before the specified pattern. |
| `slice_before(pattern)` | Returns subarrays before the specified pattern. |
| `slice_before { |element| ... }` | Returns subarrays before the pattern specified by the block. |
| `slice_when` | Returns subarrays between elements that satisfy the condition. |
| `slice_when { |before, after| ... }` | Returns subarrays between elements that satisfy the condition specified by the block. |
| `sort` | Returns a new array with the elements sorted. |
| `sort { |a, b| ... }` | Returns a new array with the elements sorted using the block for comparison. |
| `sort!` | Sorts the array in place. Returns the array. |
| `sort! { |a, b| ... }` | Sorts the array in place using the block for comparison. Returns the array. |
| `sort_by` | Sorts the array by the result of the block. |
| `sort_by { |element| ... }` | Sorts the array by the result of the block. |
| `sort_by!` | Sorts the array in place by the result of the block. Returns the array. |
| `sort_by! { |element| ... }` | Sorts the array in place by the result of the block. |
| `sum` | Returns the sum of all elements. |
| `sum { |a, b| ... }` | Returns the sum of all elements using the block for addition. |
| `sum(initial)` | Returns the sum of all elements with the specified initial value. |
| `sum(initial) { |a, b| ... }` | Returns the sum of all elements with the specified initial value using the block for addition. |
| `take` | Returns the first n elements. |
| `take(n)` | Returns the first n elements. |
| `take_while` | Returns elements while the condition is true. |
| `take_while { |element| ... }` | Returns elements while the condition specified by the block is true. |
| `to_a` | Returns the array itself. |
| `to_ary` | Returns the array itself. |
| `to_h` | Converts the array to a hash. |
| `to_s` | Returns a string representation of the array. |
| `transpose` | Transposes the rows and columns of the array. |
| `uniq` | Returns a new array with duplicate elements removed. |
| `uniq { |element| ... }` | Returns a new array with duplicate elements removed using the block for comparison. |
| `uniq!` | Removes duplicate elements in place. Returns nil if no changes are made. |
| `uniq! { |element| ... }` | Removes duplicate elements in place using the block for comparison. Returns nil if no changes are made. |
| `unshift` | Prepends elements to the beginning of the array. |
| `unshift(*objects)` | Prepends elements to the beginning of the array. |
| `values_at` | Returns an array containing the elements at the specified indices. |
| `values_at(index1, index2, ...)` | Returns an array containing the elements at the specified indices. |
| `values_at(range1, range2, ...)` | Returns an array containing the elements at the specified ranges. |
| `zip` | Zips the array with the specified arrays. |
| `zip(*other_arrays)` | Zips the array with the specified arrays. |
| `zip(*other_arrays) { |elements| ... }` | Zips the array with the specified arrays and passes each group of elements to a block. |
| `|` | Array union operator. |
| `&` | Array intersection operator. |

---
## Hash Methods

| Code | Description |
|------|-------------|
| `Hash.new` | Creates a new empty hash. |
| `Hash.new(default)` | Creates a new hash with the specified default value. |
| `Hash.new { |hash, key| ... }` | Creates a new hash with a block to determine the default value. |
| `{}` | Creates a new empty hash. |
| `{ key1 => value1, key2 => value2 }` | Creates a new hash with the specified keys and values. |
| `{ key1: value1, key2: value2 }` | Creates a new hash with the specified keys and values using symbol keys. |
| `[]` | Element access. |
| `[]=` | Element assignment. |
| `any?` | Returns true if any key-value pair satisfies the condition. |
| `any? { |key, value| ... }` | Returns true if any key-value pair satisfies the condition specified by the block. |
| `assoc` | Searches for a key-value pair whose key matches the specified object. |
| `assoc(key)` | Searches for a key-value pair whose key matches the specified object. |
| `clear` | Removes all key-value pairs from the hash. |
| `clone` | Returns a shallow copy of the hash. |
| `compact` | Returns a new hash with all nil values removed. |
| `compact!` | Removes all nil values in place. Returns nil if no changes are made. |
| `compare_by_identity` | Compares hash keys by their identity. |
| `compare_by_identity?` | Returns true if the hash compares keys by their identity. |
| `default` | Returns the default value for the hash. |
| `default(key)` | Returns the default value for the specified key. |
| `default=default` | Sets the default value for the hash. |
| `default_proc` | Returns the default procedure for the hash. |
| `default_proc=` | Sets the default procedure for the hash. |
| `delete` | Deletes a key-value pair and returns the value. |
| `delete(key)` | Deletes the key-value pair with the specified key and returns the value. |
| `delete(key) { |k| ... }` | Deletes the key-value pair with the specified key and returns the result of the block if the key is not found. |
| `delete_if` | Deletes all key-value pairs that satisfy the condition. |
| `delete_if { |key, value| ... }` | Deletes all key-value pairs that satisfy the condition specified by the block. |
| `dig` | Safely navigates nested data structures. |
| `dig(key1, key2, ...)` | Safely navigates nested data structures. |
| `dig(key1, key2, ...) { |value| ... }` | Safely navigates nested data structures and passes the value to a block. |
| `each` | Iterates over each key-value pair. |
| `each { |key, value| ... }` | Iterates over each key-value pair and passes each key and value to a block. |
| `each_key` | Iterates over each key. |
| `each_key { |key| ... }` | Iterates over each key and passes each key to a block. |
| `each_pair` | Iterates over each key-value pair. |
| `each_pair { |key, value| ... }` | Iterates over each key-value pair and passes each key and value to a block. |
| `each_value` | Iterates over each value. |
| `each_value { |value| ... }` | Iterates over each value and passes each value to a block. |
| `empty?` | Returns true if the hash has no key-value pairs. |
| `eql?` | Returns true if the hash is equal to the specified object. |
| `except` | Returns a new hash without the specified keys. |
| `except(*keys)` | Returns a new hash without the specified keys. |
| `fetch` | Returns the value for the specified key. |
| `fetch(key)` | Returns the value for the specified key. |
| `fetch(key, default)` | Returns the value for the specified key or the default value if the key is not found. |
| `fetch(key) { |k| ... }` | Returns the value for the specified key or the result of the block if the key is not found. |
| `fetch_values` | Returns an array of values for the specified keys. |
| `fetch_values(*keys)` | Returns an array of values for the specified keys. |
| `fetch_values(*keys) { |k| ... }` | Returns an array of values for the specified keys or the result of the block if a key is not found. |
| `filter` | Returns a new hash containing all key-value pairs that satisfy the condition. |
| `filter { |key, value| ... }` | Returns a new hash containing all key-value pairs that satisfy the condition specified by the block. |
| `filter!` | Replaces the hash with all key-value pairs that satisfy the condition. Returns nil if no changes are made. |
| `filter! { |key, value| ... }` | Replaces the hash with all key-value pairs that satisfy the condition specified by the block. |
| `flatten` | Returns a new array that is a one-dimensional flattening of the hash. |
| `flatten(level)` | Returns a new array that is a one-dimensional flattening of the hash up to the specified level. |
| `has_key?` | Returns true if the hash contains the specified key. |
| `has_value?` | Returns true if the hash contains the specified value. |
| `hash` | Returns a hash value for the hash. |
| `include?` | Returns true if the hash contains the specified key. |
| `index` | Returns the key for the specified value. |
| `index(value)` | Returns the key for the specified value. |
| `inspect` | Returns a string representation of the hash. |
| `invert` | Returns a new hash with the keys and values swapped. |
| `key` | Returns the key for the specified value. |
| `key(value)` | Returns the key for the specified value. |
| `key?` | Returns true if the hash contains the specified key. |
| `keys` | Returns an array of the keys in the hash. |
| `length` | Returns the number of key-value pairs in the hash. |
| `map` | Returns a new array with the results of running the block for each key-value pair. |
| `map { |key, value| ... }` | Returns a new array with the results of running the block for each key-value pair. |
| `merge` | Returns a new hash with the contents of the hash and the specified hash. |
| `merge(other_hash)` | Returns a new hash with the contents of the hash and the specified hash. |
| `merge(other_hash) { |key, old_value, new_value| ... }` | Returns a new hash with the contents of the hash and the specified hash using the block to resolve conflicts. |
| `merge!` | Merges the specified hash into the hash. Returns the hash. |
| `merge!(other_hash)` | Merges the specified hash into the hash. |
| `merge!(other_hash) { |key, old_value, new_value| ... }` | Merges the specified hash into the hash using the block to resolve conflicts. |
| `none?` | Returns true if no key-value pair satisfies the condition. |
| `none? { |key, value| ... }` | Returns true if no key-value pair satisfies the condition specified by the block. |
| `one?` | Returns true if exactly one key-value pair satisfies the condition. |
| `one? { |key, value| ... }` | Returns true if exactly one key-value pair satisfies the condition specified by the block. |
| `permute` | Returns all permutations of the keys. |
| `permute(*keys)` | Returns all permutations of the specified keys. |
| `permute(*keys) { |perm| ... }` | Returns all permutations of the specified keys and passes each permutation to a block. |
| `rassoc` | Searches for a key-value pair whose value matches the specified object. |
| `rassoc(value)` | Searches for a key-value pair whose value matches the specified object. |
| `reject` | Returns a new hash containing all key-value pairs that do not satisfy the condition. |
| `reject { |key, value| ... }` | Returns a new hash containing all key-value pairs that do not satisfy the condition specified by the block. |
| `reject!` | Replaces the hash with all key-value pairs that do not satisfy the condition. Returns nil if no changes are made. |
| `reject! { |key, value| ... }` | Replaces the hash with all key-value pairs that do not satisfy the condition specified by the block. |
| `replace` | Replaces the contents of the hash with the specified hash. |
| `replace(other_hash)` | Replaces the contents of the hash with the specified hash. |
| `select` | Returns a new hash containing all key-value pairs that satisfy the condition. |
| `select { |key, value| ... }` | Returns a new hash containing all key-value pairs that satisfy the condition specified by the block. |
| `select!` | Replaces the hash with all key-value pairs that satisfy the condition. Returns nil if no changes are made. |
| `select! { |key, value| ... }` | Replaces the hash with all key-value pairs that satisfy the condition specified by the block. |
| `shift` | Removes and returns the first key-value pair. |
| `size` | Returns the number of key-value pairs in the hash. |
| `slice` | Returns a new hash with the specified keys. |
| `slice(*keys)` | Returns a new hash with the specified keys. |
| `store` | Sets the value for the specified key. |
| `store(key, value)` | Sets the value for the specified key. |
| `to_a` | Returns an array of the key-value pairs in the hash. |
| `to_h` | Returns the hash itself. |
| `to_hash` | Returns the hash itself. |
| `to_proc` | Returns a Proc that calls the method represented by the hash. |
| `to_s` | Returns a string representation of the hash. |
| `transform_keys` | Returns a new hash with the keys transformed. |
| `transform_keys { |key| ... }` | Returns a new hash with the keys transformed using the block. |
| `transform_keys!` | Transforms the keys in place. Returns the hash. |
| `transform_keys! { |key| ... }` | Transforms the keys in place using the block. |
| `transform_values` | Returns a new hash with the values transformed. |
| `transform_values { |value| ... }` | Returns a new hash with the values transformed using the block. |
| `transform_values!` | Transforms the values in place. Returns the hash. |
| `transform_values! { |value| ... }` | Transforms the values in place using the block. |
| `update` | Updates the hash with the contents of the specified hash. |
| `update(other_hash)` | Updates the hash with the contents of the specified hash. |
| `update(other_hash) { |key, old_value, new_value| ... }` | Updates the hash with the contents of the specified hash using the block to resolve conflicts. |
| `value?` | Returns true if the hash contains the specified value. |
| `values` | Returns an array of the values in the hash. |
| `values_at` | Returns an array of values for the specified keys. |
| `values_at(*keys)` | Returns an array of values for the specified keys. |

---
## Numeric Methods

| Code | Description |
|------|-------------|
| `Numeric` | Abstract base class for numbers. |
| `Integer` | Represents integer numbers. |
| `Fixnum` | Legacy class for small integers. In Ruby 2.4+, all integers are of class Integer. |
| `Bignum` | Legacy class for large integers. In Ruby 2.4+, all integers are of class Integer. |
| `Float` | Represents floating-point numbers. |
| `Rational` | Represents rational numbers as a fraction. |
| `Complex` | Represents complex numbers. |
| `BigDecimal` | Represents arbitrary-precision decimal numbers. |
| `abs` | Returns the absolute value of the number. |
| `abs2` | Returns the square of the absolute value of the number. |
| `angle` | Returns the angle (in radians) of the number. |
| `arg` | Returns the angle (in radians) of the number. |
| `ceil` | Returns the smallest integer greater than or equal to the number. |
| `chr` | Returns the character corresponding to the integer. |
| `clamp` | Returns the number clamped to the specified range. |
| `clamp(min, max)` | Returns the number clamped to the range [min, max]. |
| `coerce` | Returns an array with the number and the specified object converted to the same type. |
| `coerce(other)` | Returns an array with the number and the specified object converted to the same type. |
| `conj` | Returns the complex conjugate of the number. |
| `conjugate` | Returns the complex conjugate of the number. |
| `denominator` | Returns the denominator of the rational number. |
| `div` | Returns the integer division of the number by the specified object. |
| `div(other)` | Returns the integer division of the number by the specified object. |
| `divmod` | Returns an array containing the quotient and modulus of the division. |
| `divmod(other)` | Returns an array containing the quotient and modulus of the division by the specified object. |
| `downto` | Iterates from the number down to the specified limit. |
| `downto(limit) { |n| ... }` | Iterates from the number down to the specified limit and passes each value to a block. |
| `even?` | Returns true if the number is even. |
| `fdiv` | Returns the floating-point division of the number by the specified object. |
| `fdiv(other)` | Returns the floating-point division of the number by the specified object. |
| `finite?` | Returns true if the number is finite. |
| `floor` | Returns the largest integer less than or equal to the number. |
| `gcd` | Returns the greatest common divisor of the number and the specified object. |
| `gcd(other)` | Returns the greatest common divisor of the number and the specified object. |
| `imag` | Returns the imaginary part of the number. |
| `imaginary` | Returns the imaginary part of the number. |
| `infinite?` | Returns true if the number is infinite. |
| `lcm` | Returns the least common multiple of the number and the specified object. |
| `lcm(other)` | Returns the least common multiple of the number and the specified object. |
| `magnitude` | Returns the magnitude of the number. |
| `modulo` | Returns the modulus of the division. |
| `modulo(other)` | Returns the modulus of the division by the specified object. |
| `nan?` | Returns true if the number is not a number (NaN). |
| `negative?` | Returns true if the number is negative. |
| `next` | Returns the next integer. |
| `next_float` | Returns the next floating-point number. |
| `numerator` | Returns the numerator of the rational number. |
| `odd?` | Returns true if the number is odd. |
| `phase` | Returns the phase (in radians) of the number. |
| `polar` | Returns the polar coordinates of the number. |
| `positive?` | Returns true if the number is positive. |
| `pred` | Returns the previous integer. |
| `prev` | Returns the previous integer. |
| `prev_float` | Returns the previous floating-point number. |
| `quoto` | Returns the quotient of the division. |
| `rationalize` | Returns the rational number closest to the number. |
| `rationalize(eps)` | Returns the rational number closest to the number within the specified epsilon. |
| `real` | Returns the real part of the number. |
| `real?` | Returns true if the number is real. |
| `rect` | Returns the rectangular coordinates of the number. |
| `rectangular` | Returns the rectangular coordinates of the number. |
| `remainder` | Returns the remainder of the division. |
| `remainder(other)` | Returns the remainder of the division by the specified object. |
| `round` | Returns the nearest integer to the number. |
| `round(n)` | Returns the nearest integer to the number with n digits of precision. |
| `step` | Iterates from the number to the specified limit by the specified step. |
| `step(limit, step) { |n| ... }` | Iterates from the number to the specified limit by the specified step and passes each value to a block. |
| `to_c` | Converts the number to a complex number. |
| `to_f` | Converts the number to a float. |
| `to_i` | Converts the number to an integer. |
| `to_int` | Converts the number to an integer. |
| `to_r` | Converts the number to a rational number. |
| `to_s` | Converts the number to a string. |
| `truncate` | Returns the nearest integer not larger in magnitude than the number. |
| `upto` | Iterates from the number up to the specified limit. |
| `upto(limit) { |n| ... }` | Iterates from the number up to the specified limit and passes each value to a block. |
| `zero?` | Returns true if the number is zero. |
| `nonzero?` | Returns true if the number is not zero. |
| `abs` | Returns the absolute value of the number. |
| `**(other)` | Exponentiation operator. |
| `%` | Modulo operator. |
| `+` | Addition operator. |
| `-` | Subtraction operator. |
| `*` | Multiplication operator. |
| `/` | Division operator. |
| `==` | Equality operator. |
| `===` | Case equality operator. |
| `<=>` | Comparison operator. Returns -1, 0, or 1. |
| `=` | Assignment operator. |
| `+=` | Addition assignment operator. |
| `-=` | Subtraction assignment operator. |
| `*=` | Multiplication assignment operator. |
| `/=` | Division assignment operator. |
| `%=` | Modulo assignment operator. |
| `**=` | Exponentiation assignment operator. |

---
## Enumerable Methods

| Code | Description |
|------|-------------|
| `all?` | Returns true if all elements satisfy the condition. |
| `all? { |element| ... }` | Returns true if all elements satisfy the condition specified by the block. |
| `all?(pattern)` | Returns true if all elements match the specified pattern. |
| `any?` | Returns true if any element satisfies the condition. |
| `any? { |element| ... }` | Returns true if any element satisfies the condition specified by the block. |
| `any?(pattern)` | Returns true if any element matches the specified pattern. |
| `ascii_only?` | Returns true if all elements are ASCII-only strings. |
| `chain` | Returns a new Enumerator that iterates over the elements and then over the specified enumerables. |
| `chain(*enums)` | Returns a new Enumerator that iterates over the elements and then over the specified enumerables. |
| `chunk` | Groups consecutive elements that satisfy the condition. |
| `chunk { |element| ... }` | Groups consecutive elements that satisfy the condition specified by the block. |
| `chunk_while` | Groups consecutive elements while the condition is true. |
| `chunk_while { |before, after| ... }` | Groups consecutive elements while the condition specified by the block is true. |
| `collect` | Returns a new array with the results of running the block for each element. |
| `collect { |element| ... }` | Returns a new array with the results of running the block for each element. |
| `collect_concat` | Returns a new array with the results of running the block for each element and concatenates the results. |
| `collect_concat { |element| ... }` | Returns a new array with the results of running the block for each element and concatenates the results. |
| `count` | Returns the number of elements. |
| `count(item)` | Counts the number of elements equal to the specified item. |
| `count { |element| ... }` | Counts the number of elements that satisfy the condition specified by the block. |
| `cycle` | Cycles through the elements indefinitely. |
| `cycle { |element| ... }` | Cycles through the elements indefinitely and passes each element to a block. |
| `cycle(n)` | Cycles through the elements n times. |
| `cycle(n) { |element| ... }` | Cycles through the elements n times and passes each element to a block. |
| `detect` | Returns the first element that satisfies the condition. |
| `detect { |element| ... }` | Returns the first element that satisfies the condition specified by the block. |
| `detect(ifnone = nil) { |element| ... }` | Returns the first element that satisfies the condition specified by the block or the ifnone value if no element satisfies the condition. |
| `drop` | Drops the first n elements. |
| `drop(n)` | Drops the first n elements. |
| `drop_while` | Drops elements while the condition is true. |
| `drop_while { |element| ... }` | Drops elements while the condition specified by the block is true. |
| `each` | Iterates over each element. |
| `each { |element| ... }` | Iterates over each element and passes each element to a block. |
| `each_cons` | Iterates over each consecutive subarray. |
| `each_cons(n) { |elements| ... }` | Iterates over each consecutive subarray of size n and passes each subarray to a block. |
| `each_entry` | Iterates over each element. |
| `each_entry { |element| ... }` | Iterates over each element and passes each element to a block. |
| `each_slice` | Iterates over each slice. |
| `each_slice(n) { |elements| ... }` | Iterates over each slice of size n and passes each slice to a block. |
| `each_with_index` | Iterates over each element with its index. |
| `each_with_index { |element, index| ... }` | Iterates over each element with its index and passes each element and index to a block. |
| `each_with_object` | Iterates over each element and accumulates a result. |
| `each_with_object(obj) { |element| ... }` | Iterates over each element and accumulates a result in the specified object. |
| `entries` | Returns an array of the elements. |
| `enum_cons` | Returns an enumerator for each consecutive subarray. |
| `enum_cons(n)` | Returns an enumerator for each consecutive subarray of size n. |
| `enum_slice` | Returns an enumerator for each slice. |
| `enum_slice(n)` | Returns an enumerator for each slice of size n. |
| `enum_with_index` | Returns an enumerator for each element with its index. |
| `enum_with_index { |element, index| ... }` | Returns an enumerator for each element with its index. |
| `filter` | Returns a new array containing all elements that satisfy the condition. |
| `filter { |element| ... }` | Returns a new array containing all elements that satisfy the condition specified by the block. |
| `filter_map` | Returns a new array with the results of running the block for each element that satisfies the condition. |
| `filter_map { |element| ... }` | Returns a new array with the results of running the block for each element that satisfies the condition specified by the block. |
| `find` | Returns the first element that satisfies the condition. |
| `find { |element| ... }` | Returns the first element that satisfies the condition specified by the block. |
| `find(ifnone = nil) { |element| ... }` | Returns the first element that satisfies the condition specified by the block or the ifnone value if no element satisfies the condition. |
| `find_all` | Returns all elements that satisfy the condition. |
| `find_all { |element| ... }` | Returns all elements that satisfy the condition specified by the block. |
| `find_index` | Returns the index of the first element that satisfies the condition. |
| `find_index { |element| ... }` | Returns the index of the first element that satisfies the condition specified by the block. |
| `find_index(item)` | Returns the index of the first element equal to the specified item. |
| `first` | Returns the first element. |
| `first(n)` | Returns the first n elements. |
| `flat_map` | Returns a new array with the concatenated results of running the block for each element. |
| `flat_map { |element| ... }` | Returns a new array with the concatenated results of running the block for each element. |
| `grep` | Returns all elements that match the specified pattern. |
| `grep(pattern)` | Returns all elements that match the specified pattern. |
| `grep(pattern) { |element| ... }` | Returns all elements that match the specified pattern and passes each element to a block. |
| `grep_v` | Returns all elements that do not match the specified pattern. |
| `grep_v(pattern)` | Returns all elements that do not match the specified pattern. |
| `grep_v(pattern) { |element| ... }` | Returns all elements that do not match the specified pattern and passes each element to a block. |
| `group_by` | Groups the elements by the result of the block. |
| `group_by { |element| ... }` | Groups the elements by the result of the block. |
| `include?` | Returns true if any element is equal to the specified object. |
| `inject` | Combines all elements using the block. |
| `inject(initial) { |result, element| ... }` | Combines all elements using the block with the specified initial value. |
| `inject(initial, sym)` | Combines all elements using the specified method. |
| `lazy` | Returns a lazy enumerator for the elements. |
| `map` | Returns a new array with the results of running the block for each element. |
| `map { |element| ... }` | Returns a new array with the results of running the block for each element. |
| `max` | Returns the maximum element. |
| `max { |a, b| ... }` | Returns the maximum element using the block for comparison. |
| `max(n)` | Returns the first n maximum elements. |
| `max(n) { |a, b| ... }` | Returns the first n maximum elements using the block for comparison. |
| `max_by` | Returns the element with the maximum value. |
| `max_by { |element| ... }` | Returns the element with the maximum value specified by the block. |
| `member?` | Returns true if any element is equal to the specified object. |
| `min` | Returns the minimum element. |
| `min { |a, b| ... }` | Returns the minimum element using the block for comparison. |
| `min(n)` | Returns the first n minimum elements. |
| `min(n) { |a, b| ... }` | Returns the first n minimum elements using the block for comparison. |
| `min_by` | Returns the element with the minimum value. |
| `min_by { |element| ... }` | Returns the element with the minimum value specified by the block. |
| `minmax` | Returns a two-element array containing the minimum and maximum elements. |
| `minmax { |a, b| ... }` | Returns a two-element array containing the minimum and maximum elements using the block for comparison. |
| `minmax_by` | Returns a two-element array containing the elements with the minimum and maximum values. |
| `minmax_by { |element| ... }` | Returns a two-element array containing the elements with the minimum and maximum values specified by the block. |
| `none?` | Returns true if no elements satisfy the condition. |
| `none? { |element| ... }` | Returns true if no elements satisfy the condition specified by the block. |
| `one?` | Returns true if exactly one element satisfies the condition. |
| `one? { |element| ... }` | Returns true if exactly one element satisfies the condition specified by the block. |
| `partition` | Partitions the elements into two arrays based on the condition. |
| `partition { |element| ... }` | Partitions the elements into two arrays based on the condition specified by the block. |
| `reduce` | Combines all elements using the block. |
| `reduce(initial) { |result, element| ... }` | Combines all elements using the block with the specified initial value. |
| `reduce(initial, sym)` | Combines all elements using the specified method. |
| `reject` | Returns a new array containing all elements that do not satisfy the condition. |
| `reject { |element| ... }` | Returns a new array containing all elements that do not satisfy the condition specified by the block. |
| `reverse_each` | Iterates over the elements in reverse order. |
| `reverse_each { |element| ... }` | Iterates over the elements in reverse order and passes each element to a block. |
| `select` | Returns a new array containing all elements that satisfy the condition. |
| `select { |element| ... }` | Returns a new array containing all elements that satisfy the condition specified by the block. |
| `slice_after` | Returns subarrays after the specified pattern. |
| `slice_after(pattern)` | Returns subarrays after the specified pattern. |
| `slice_after { |element| ... }` | Returns subarrays after the pattern specified by the block. |
| `slice_before` | Returns subarrays before the specified pattern. |
| `slice_before(pattern)` | Returns subarrays before the specified pattern. |
| `slice_before { |element| ... }` | Returns subarrays before the pattern specified by the block. |
| `slice_when` | Returns subarrays between elements that satisfy the condition. |
| `slice_when { |before, after| ... }` | Returns subarrays between elements that satisfy the condition specified by the block. |
| `sort` | Returns a new array with the elements sorted. |
| `sort { |a, b| ... }` | Returns a new array with the elements sorted using the block for comparison. |
| `sort_by` | Sorts the elements by the result of the block. |
| `sort_by { |element| ... }` | Sorts the elements by the result of the block. |
| `sum` | Returns the sum of all elements. |
| `sum { |a, b| ... }` | Returns the sum of all elements using the block for addition. |
| `sum(initial)` | Returns the sum of all elements with the specified initial value. |
| `sum(initial) { |a, b| ... }` | Returns the sum of all elements with the specified initial value using the block for addition. |
| `take` | Returns the first n elements. |
| `take(n)` | Returns the first n elements. |
| `take_while` | Returns elements while the condition is true. |
| `take_while { |element| ... }` | Returns elements while the condition specified by the block is true. |
| `to_a` | Returns an array of the elements. |
| `to_set` | Returns a Set containing the elements. |
| `uniq` | Returns a new array with duplicate elements removed. |
| `uniq { |element| ... }` | Returns a new array with duplicate elements removed using the block for comparison. |
| `with_index` | Returns an enumerator for each element with its index. |
| `with_index { |element, index| ... }` | Returns an enumerator for each element with its index. |
| `with_object` | Returns an enumerator for each element with the specified object. |
| `with_object(obj) { |element| ... }` | Returns an enumerator for each element with the specified object. |
| `zip` | Zips the elements with the specified enumerables. |
| `zip(*enums)` | Zips the elements with the specified enumerables. |
| `zip(*enums) { |elements| ... }` | Zips the elements with the specified enumerables and passes each group of elements to a block. |

---
## Comparable Methods

| Code | Description |
|------|-------------|
| `<=>` | Comparison operator. Returns -1, 0, or 1. |
| `==` | Equality operator. |
| `===` | Case equality operator. |
| `<` | Less than operator. |
| `<=` | Less than or equal to operator. |
| `>` | Greater than operator. |
| `>=` | Greater than or equal to operator. |
| `between?` | Returns true if the number is between the specified minimum and maximum. |
| `between?(min, max)` | Returns true if the number is between the specified minimum and maximum. |
| `clamp` | Returns the number clamped to the specified range. |
| `clamp(min, max)` | Returns the number clamped to the range [min, max]. |

---
## File and Directory Operations

| Code | Description |
|------|-------------|
| `File` | Represents a file. Provides methods for file operations. |
| `File.new(path, mode)` | Creates a new File object. |
| `File.open(path, mode) { |file| ... }` | Opens a file and passes it to a block. |
| `File.open(path, mode)` | Opens a file and returns the File object. |
| `File.read(path)` | Reads the contents of a file. |
| `File.read(path, length)` | Reads the specified number of bytes from a file. |
| `File.read(path, length, offset)` | Reads the specified number of bytes from a file starting at the specified offset. |
| `File.readlines(path)` | Reads the lines of a file into an array. |
| `File.readlines(path, limit)` | Reads the specified number of lines from a file into an array. |
| `File.foreach(path) { |line| ... }` | Iterates over each line of a file. |
| `File.write(path, content)` | Writes the specified content to a file. |
| `File.binread(path)` | Reads the contents of a file in binary mode. |
| `File.binwrite(path, content)` | Writes the specified content to a file in binary mode. |
| `File.size(path)` | Returns the size of a file. |
| `File.exist?(path)` | Returns true if the file exists. |
| `File.exists?(path)` | Returns true if the file exists. |
| `File.file?(path)` | Returns true if the path is a file. |
| `File.directory?(path)` | Returns true if the path is a directory. |
| `File.symlink?(path)` | Returns true if the path is a symbolic link. |
| `File.readable?(path)` | Returns true if the file is readable. |
| `File.writable?(path)` | Returns true if the file is writable. |
| `File.executable?(path)` | Returns true if the file is executable. |
| `File.zero?(path)` | Returns true if the file is empty. |
| `File.empty?(path)` | Returns true if the file is empty. |
| `File.mtime(path)` | Returns the modification time of a file. |
| `File.atime(path)` | Returns the access time of a file. |
| `File.ctime(path)` | Returns the creation time of a file. |
| `File.utime(atime, mtime, path)` | Sets the access and modification times of a file. |
| `File.chmod(mode, path)` | Changes the permissions of a file. |
| `File.chown(owner, group, path)` | Changes the owner and group of a file. |
| `File.link(old_path, new_path)` | Creates a hard link to a file. |
| `File.symlink(old_path, new_path)` | Creates a symbolic link to a file. |
| `File.unlink(path)` | Removes a file. |
| `File.delete(path)` | Removes a file. |
| `File.rename(old_path, new_path)` | Renames a file. |
| `File.truncate(path, length)` | Truncates a file to the specified length. |
| `File.expand_path(path)` | Expands the path to an absolute path. |
| `File.expand_path(path, dir)` | Expands the path to an absolute path relative to the specified directory. |
| `File.basename(path)` | Returns the basename of a path. |
| `File.basename(path, suffix)` | Returns the basename of a path without the specified suffix. |
| `File.dirname(path)` | Returns the directory name of a path. |
| `File.extname(path)` | Returns the extension of a path. |
| `File.split(path)` | Splits a path into a directory and a basename. |
| `File.join(path1, path2, ...)` | Joins path components. |
| `File.path(path)` | Returns the path as a string. |
| `File.absolute_path(path)` | Returns the absolute path of a file. |
| `File.absolute_path(path, dir)` | Returns the absolute path of a file relative to the specified directory. |
| `File.realpath(path)` | Returns the real path of a file. |
| `File.realpath(path, dir)` | Returns the real path of a file relative to the specified directory. |
| `File.identical?(path1, path2)` | Returns true if the files are identical. |
| `File.fnmatch?(pattern, path)` | Returns true if the path matches the specified pattern. |
| `File.fnmatch(pattern, path)` | Returns true if the path matches the specified pattern. |
| `File.fnmatch?(pattern, path, flags)` | Returns true if the path matches the specified pattern with the specified flags. |
| `File.fnmatch(pattern, path, flags)` | Returns true if the path matches the specified pattern with the specified flags. |
| `File.stat(path)` | Returns a File::Stat object for the specified path. |
| `File.lchmod(mode, path)` | Changes the permissions of a symbolic link. |
| `File.lchown(owner, group, path)` | Changes the owner and group of a symbolic link. |
| `File.lstat(path)` | Returns a File::Stat object for the specified path without following symbolic links. |
| `File.readlink(path)` | Returns the target of a symbolic link. |
| `File.popen(command, mode)` | Opens a pipe to a subprocess. |
| `File.popen(command, mode) { |pipe| ... }` | Opens a pipe to a subprocess and passes it to a block. |
| `Dir` | Represents a directory. Provides methods for directory operations. |
| `Dir.new(path)` | Creates a new Dir object. |
| `Dir.open(path) { |dir| ... }` | Opens a directory and passes it to a block. |
| `Dir.open(path)` | Opens a directory and returns the Dir object. |
| `Dir.foreach(path) { |entry| ... }` | Iterates over each entry in a directory. |
| `Dir.entries(path)` | Returns an array of the entries in a directory. |
| `Dir.chdir(path)` | Changes the current directory. |
| `Dir.chdir(path) { |dir| ... }` | Changes the current directory and passes it to a block. |
| `Dir.getwd` | Returns the current directory. |
| `Dir.pwd` | Returns the current directory. |
| `Dir.mkdir(path)` | Creates a new directory. |
| `Dir.mkdir(path, mode)` | Creates a new directory with the specified permissions. |
| `Dir.rmdir(path)` | Removes a directory. |
| `Dir.delete(path)` | Removes a directory. |
| `Dir.exist?(path)` | Returns true if the directory exists. |
| `Dir.exists?(path)` | Returns true if the directory exists. |
| `Dir.empty?(path)` | Returns true if the directory is empty. |
| `Dir.glob(pattern)` | Returns an array of the files matching the specified pattern. |
| `Dir.glob(pattern) { |file| ... }` | Iterates over the files matching the specified pattern. |
| `Dir.glob(pattern, flags)` | Returns an array of the files matching the specified pattern with the specified flags. |
| `Dir.glob(pattern, flags) { |file| ... }` | Iterates over the files matching the specified pattern with the specified flags. |
| `Dir[]` | Returns an array of the files matching the specified pattern. |
| `FileUtils` | Provides utility methods for file and directory operations. |
| `FileUtils.cd(path)` | Changes the current directory. |
| `FileUtils.cd(path) { |dir| ... }` | Changes the current directory and passes it to a block. |
| `FileUtils.pwd` | Returns the current directory. |
| `FileUtils.mkdir(path)` | Creates a new directory. |
| `FileUtils.mkdir_p(path)` | Creates a new directory and its parent directories. |
| `FileUtils.rmdir(path)` | Removes a directory. |
| `FileUtils.rm_r(path)` | Removes a directory and its contents recursively. |
| `FileUtils.rm_rf(path)` | Removes a directory and its contents recursively and forcefully. |
| `FileUtils.rm(path)` | Removes a file. |
| `FileUtils.rm_f(path)` | Removes a file forcefully. |
| `FileUtils.mv(src, dest)` | Moves a file or directory. |
| `FileUtils.mv(src, dest, options)` | Moves a file or directory with the specified options. |
| `FileUtils.cp(src, dest)` | Copies a file. |
| `FileUtils.cp_r(src, dest)` | Copies a file or directory recursively. |
| `FileUtils.copy(src, dest)` | Copies a file. |
| `FileUtils.copy_file(src, dest)` | Copies a file. |
| `FileUtils.copy_stream(src, dest)` | Copies a stream. |
| `FileUtils.ln(src, dest)` | Creates a hard link. |
| `FileUtils.ln_s(src, dest)` | Creates a symbolic link. |
| `FileUtils.ln_sf(src, dest)` | Creates a symbolic link forcefully. |
| `FileUtils.symlink(src, dest)` | Creates a symbolic link. |
| `FileUtils.readlink_list(path)` | Returns an array of the targets of the symbolic links in a path. |
| `FileUtils.uptodate?(file, comparison_files)` | Returns true if the file is up to date relative to the specified comparison files. |
| `FileUtils.uptodate?(file, comparison_files, options)` | Returns true if the file is up to date relative to the specified comparison files with the specified options. |
| `FileUtils.touch(path)` | Updates the modification time of a file. |
| `FileUtils.touch(path, mtime)` | Updates the modification time of a file to the specified time. |
| `FileUtils.chmod(mode, path)` | Changes the permissions of a file. |
| `FileUtils.chmod_R(mode, path)` | Changes the permissions of a file or directory recursively. |
| `FileUtils.chown(owner, group, path)` | Changes the owner and group of a file. |
| `FileUtils.chown_R(owner, group, path)` | Changes the owner and group of a file or directory recursively. |
| `Find` | Provides methods for finding files. |
| `Find.find(path) { |file| ... }` | Recursively finds files in the specified path and passes each file to a block. |
| `Find.find(path, options) { |file| ... }` | Recursively finds files in the specified path with the specified options and passes each file to a block. |
| `Find.prune` | Prunes the current directory from the search. |
| `Pathname` | Represents a pathname. Provides methods for pathname operations. |
| `Pathname.new(path)` | Creates a new Pathname object. |
| `Pathname.getwd` | Returns the current directory as a Pathname. |
| `Pathname.pwd` | Returns the current directory as a Pathname. |
| `Pathname.glob(pattern)` | Returns an array of the Pathname objects matching the specified pattern. |
| `Pathname.glob(pattern) { |path| ... }` | Iterates over the Pathname objects matching the specified pattern. |
| `Pathname#cleanpath` | Returns a cleaned version of the pathname. |
| `Pathname#cleanpath(consider_symlink: false)` | Returns a cleaned version of the pathname. |
| `Pathname#each_filename` | Iterates over each filename in the pathname. |
| `Pathname#each_filename { |name| ... }` | Iterates over each filename in the pathname. |
| `Pathname#each_line` | Iterates over each line of the file. |
| `Pathname#each_line { |line| ... }` | Iterates over each line of the file. |
| `Pathname#read` | Reads the contents of the file. |
| `Pathname#read(length)` | Reads the specified number of bytes from the file. |
| `Pathname#read(length, offset)` | Reads the specified number of bytes from the file starting at the specified offset. |
| `Pathname#readlines` | Reads the lines of the file into an array. |
| `Pathname#readlines(limit)` | Reads the specified number of lines from the file into an array. |
| `Pathname#foreach` | Iterates over each line of the file. |
| `Pathname#foreach { |line| ... }` | Iterates over each line of the file. |
| `Pathname#open` | Opens the file. |
| `Pathname#open { |file| ... }` | Opens the file and passes it to a block. |
| `Pathname#open(mode)` | Opens the file with the specified mode. |
| `Pathname#open(mode) { |file| ... }` | Opens the file with the specified mode and passes it to a block. |
| `Pathname#write` | Writes the specified content to the file. |
| `Pathname#binread` | Reads the contents of the file in binary mode. |
| `Pathname#binwrite` | Writes the specified content to the file in binary mode. |
| `Pathname#size` | Returns the size of the file. |
| `Pathname#exist?` | Returns true if the file exists. |
| `Pathname#file?` | Returns true if the pathname is a file. |
| `Pathname#directory?` | Returns true if the pathname is a directory. |
| `Pathname#symlink?` | Returns true if the pathname is a symbolic link. |
| `Pathname#readable?` | Returns true if the file is readable. |
| `Pathname#writable?` | Returns true if the file is writable. |
| `Pathname#executable?` | Returns true if the file is executable. |
| `Pathname#zero?` | Returns true if the file is empty. |
| `Pathname#empty?` | Returns true if the file is empty. |
| `Pathname#mtime` | Returns the modification time of the file. |
| `Pathname#atime` | Returns the access time of the file. |
| `Pathname#ctime` | Returns the creation time of the file. |
| `Pathname#utime(atime, mtime)` | Sets the access and modification times of the file. |
| `Pathname#chmod(mode)` | Changes the permissions of the file. |
| `Pathname#chown(owner, group)` | Changes the owner and group of the file. |
| `Pathname#link(old_path)` | Creates a hard link to the file. |
| `Pathname#symlink(old_path)` | Creates a symbolic link to the file. |
| `Pathname#unlink` | Removes the file. |
| `Pathname#rename(new_path)` | Renames the file. |
| `Pathname#truncate(length)` | Truncates the file to the specified length. |
| `Pathname#expand_path` | Expands the pathname to an absolute path. |
| `Pathname#expand_path(dir)` | Expands the pathname to an absolute path relative to the specified directory. |
| `Pathname#realpath` | Returns the real path of the file. |
| `Pathname#realpath(dir)` | Returns the real path of the file relative to the specified directory. |
| `Pathname#relative_path_from(base)` | Returns the relative path from the specified base directory. |
| `Pathname#basename` | Returns the basename of the pathname. |
| `Pathname#basename(suffix)` | Returns the basename of the pathname without the specified suffix. |
| `Pathname#dirname` | Returns the directory name of the pathname. |
| `Pathname#extname` | Returns the extension of the pathname. |
| `Pathname#split` | Splits the pathname into a directory and a basename. |
| `Pathname#join(*paths)` | Joins path components. |
| `Pathname#+` | Joins path components. |
| `Pathname#==` | Equality operator. |
| `Pathname#===` | Case equality operator. |
| `Pathname#<=>` | Comparison operator. |
| `Pathname#eql?` | Equality operator. |
| `Pathname#hash` | Returns a hash value for the pathname. |

---
## IO Operations

| Code | Description |
|------|-------------|
| `IO` | Represents an I/O stream. Provides methods for I/O operations. |
| `IO.new(fd)` | Creates a new IO object from a file descriptor. |
| `IO.new(fd, mode)` | Creates a new IO object from a file descriptor with the specified mode. |
| `IO.new(fd, mode, opt)` | Creates a new IO object from a file descriptor with the specified mode and options. |
| `IO.open(fd)` | Opens an IO object from a file descriptor. |
| `IO.open(fd) { |io| ... }` | Opens an IO object from a file descriptor and passes it to a block. |
| `IO.open(fd, mode)` | Opens an IO object from a file descriptor with the specified mode. |
| `IO.open(fd, mode) { |io| ... }` | Opens an IO object from a file descriptor with the specified mode and passes it to a block. |
| `IO.open(fd, mode, opt)` | Opens an IO object from a file descriptor with the specified mode and options. |
| `IO.open(fd, mode, opt) { |io| ... }` | Opens an IO object from a file descriptor with the specified mode and options and passes it to a block. |
| `IO.popen(command, mode)` | Opens a pipe to a subprocess. |
| `IO.popen(command, mode) { |io| ... }` | Opens a pipe to a subprocess and passes it to a block. |
| `IO.select(reads, writes=nil, errors=nil, timeout=nil)` | Performs a select on the specified I/O objects. |
| `IO.wait(reads, writes=nil, timeout=nil)` | Waits for I/O on the specified objects. |
| `IO.copy_stream(src, dst)` | Copies data from the source to the destination. |
| `IO.copy_stream(src, dst, copy_length)` | Copies data from the source to the destination with the specified copy length. |
| `IO.copy_stream(src, dst, copy_length) { |bytes_copied| ... }` | Copies data from the source to the destination with the specified copy length and passes the number of bytes copied to a block. |
| `IO.read(name)` | Reads the contents of a file. |
| `IO.read(name, length)` | Reads the specified number of bytes from a file. |
| `IO.read(name, length, offset)` | Reads the specified number of bytes from a file starting at the specified offset. |
| `IO.binread(name)` | Reads the contents of a file in binary mode. |
| `IO.binread(name, length)` | Reads the specified number of bytes from a file in binary mode. |
| `IO.binread(name, length, offset)` | Reads the specified number of bytes from a file in binary mode starting at the specified offset. |
| `IO.write(name, string)` | Writes the specified string to a file. |
| `IO.binwrite(name, string)` | Writes the specified string to a file in binary mode. |
| `IO.foreach(name) { |line| ... }` | Iterates over each line of a file. |
| `IO.foreach(name, separator) { |line| ... }` | Iterates over each line of a file using the specified separator. |
| `IO.readlines(name)` | Reads the lines of a file into an array. |
| `IO.readlines(name, limit)` | Reads the specified number of lines from a file into an array. |
| `IO.readlines(name, limit, separator)` | Reads the specified number of lines from a file into an array using the specified separator. |
| `IO#read` | Reads data from the I/O stream. |
| `IO#read(length)` | Reads the specified number of bytes from the I/O stream. |
| `IO#read(length, buffer)` | Reads the specified number of bytes from the I/O stream into the specified buffer. |
| `IO#readpartial` | Reads partial data from the I/O stream. |
| `IO#readpartial(length)` | Reads the specified number of bytes from the I/O stream. |
| `IO#readpartial(length, buffer)` | Reads the specified number of bytes from the I/O stream into the specified buffer. |
| `IO#read_nonblock` | Reads data from the I/O stream in non-blocking mode. |
| `IO#read_nonblock(length)` | Reads the specified number of bytes from the I/O stream in non-blocking mode. |
| `IO#read_nonblock(length, buffer)` | Reads the specified number of bytes from the I/O stream in non-blocking mode into the specified buffer. |
| `IO#write` | Writes data to the I/O stream. |
| `IO#write(string)` | Writes the specified string to the I/O stream. |
| `IO#write_nonblock` | Writes data to the I/O stream in non-blocking mode. |
| `IO#write_nonblock(string)` | Writes the specified string to the I/O stream in non-blocking mode. |
| `IO#puts` | Writes the specified objects to the I/O stream followed by a newline. |
| `IO#puts(obj1, obj2, ...)` | Writes the specified objects to the I/O stream followed by a newline. |
| `IO#putc` | Writes a character to the I/O stream. |
| `IO#putc(char)` | Writes a character to the I/O stream. |
| `IO#print` | Writes the specified objects to the I/O stream. |
| `IO#print(obj1, obj2, ...)` | Writes the specified objects to the I/O stream. |
| `IO#printf` | Writes formatted data to the I/O stream. |
| `IO#printf(format, *args)` | Writes formatted data to the I/O stream. |
| `IO#p` | Writes the specified objects to the I/O stream in inspect format followed by a newline. |
| `IO#p(obj1, obj2, ...)` | Writes the specified objects to the I/O stream in inspect format followed by a newline. |
| `IO#flush` | Flushes the I/O stream. |
| `IO#sync` | Sets the sync mode of the I/O stream. |
| `IO#sync=` | Sets the sync mode of the I/O stream. |
| `IO#close` | Closes the I/O stream. |
| `IO#closed?` | Returns true if the I/O stream is closed. |
| `IO#close_on_exec?` | Returns true if the I/O stream is closed on exec. |
| `IO#close_on_exec=` | Sets whether the I/O stream is closed on exec. |
| `IO#eof?` | Returns true if the I/O stream is at end of file. |
| `IO#eof` | Returns true if the I/O stream is at end of file. |
| `IO#pos` | Returns the current position in the I/O stream. |
| `IO#pos=` | Sets the current position in the I/O stream. |
| `IO#tell` | Returns the current position in the I/O stream. |
| `IO#seek` | Seeks to a position in the I/O stream. |
| `IO#seek(amount, whence)` | Seeks to a position in the I/O stream relative to the specified whence. |
| `IO#rewind` | Rewinds the I/O stream to the beginning. |
| `IO#truncate` | Truncates the I/O stream to the specified length. |
| `IO#truncate(length)` | Truncates the I/O stream to the specified length. |
| `IO#advise` | Provides advice to the kernel about I/O behavior. |
| `IO#advise(advice, offset, len)` | Provides advice to the kernel about I/O behavior. |
| `IO#fcntl` | Performs a fcntl operation on the I/O stream. |
| `IO#fcntl(cmd, arg)` | Performs a fcntl operation on the I/O stream. |
| `IO#ioctl` | Performs an ioctl operation on the I/O stream. |
| `IO#ioctl(cmd, arg)` | Performs an ioctl operation on the I/O stream. |
| `IO#stat` | Returns a File::Stat object for the I/O stream. |
| `IO#each` | Iterates over each line of the I/O stream. |
| `IO#each { |line| ... }` | Iterates over each line of the I/O stream. |
| `IO#each_line` | Iterates over each line of the I/O stream. |
| `IO#each_line(separator) { |line| ... }` | Iterates over each line of the I/O stream using the specified separator. |
| `IO#each_byte` | Iterates over each byte of the I/O stream. |
| `IO#each_byte { |byte| ... }` | Iterates over each byte of the I/O stream. |
| `IO#each_char` | Iterates over each character of the I/O stream. |
| `IO#each_char { |char| ... }` | Iterates over each character of the I/O stream. |
| `IO#each_codepoint` | Iterates over each codepoint of the I/O stream. |
| `IO#each_codepoint { |codepoint| ... }` | Iterates over each codepoint of the I/O stream. |
| `IO#lines` | Returns an enumerator for each line of the I/O stream. |
| `IO#lines(separator)` | Returns an enumerator for each line of the I/O stream using the specified separator. |
| `IO#bytes` | Returns an enumerator for each byte of the I/O stream. |
| `IO#chars` | Returns an enumerator for each character of the I/O stream. |
| `IO#codepoints` | Returns an enumerator for each codepoint of the I/O stream. |
| `IO#readchar` | Reads a character from the I/O stream. |
| `IO#readbyte` | Reads a byte from the I/O stream. |
| `IO#getbyte` | Reads a byte from the I/O stream. |
| `IO#getc` | Reads a character from the I/O stream. |
| `IO#ungetbyte` | Pushes a byte back onto the I/O stream. |
| `IO#ungetc` | Pushes a character back onto the I/O stream. |
| `IO#<<` | Writes the specified object to the I/O stream. |
| `IO#<<(obj)` | Writes the specified object to the I/O stream. |
| `IO#inspect` | Returns a string representation of the I/O stream. |
| `IO#to_io` | Returns the I/O stream itself. |
| `IO#to_i` | Returns the file descriptor of the I/O stream. |
| `IO#fileno` | Returns the file descriptor of the I/O stream. |
| `IO#pid` | Returns the process ID of the subprocess for a pipe. |
| `IO#wait` | Waits for the subprocess to exit for a pipe. |
| `IO#wait2` | Waits for the subprocess to exit for a pipe and returns the process status. |
| `IO#waitpid` | Waits for a specific subprocess to exit. |
| `IO#waitpid(pid, flags)` | Waits for a specific subprocess to exit with the specified flags. |
| `STDIN` | Standard input. |
| `STDOUT` | Standard output. |
| `STDERR` | Standard error. |
| `ARGF` | Represents the current input file from the command line arguments. |

---
## Regexp Methods

| Code | Description |
|------|-------------|
| `Regexp.new(pattern)` | Creates a new regular expression. |
| `Regexp.new(pattern, options)` | Creates a new regular expression with the specified options. |
| `Regexp.compile(pattern)` | Creates a new regular expression. |
| `Regexp.compile(pattern, options)` | Creates a new regular expression with the specified options. |
| `/pattern/` | Regular expression literal. |
| `/pattern/options` | Regular expression literal with options. |
| `%r{pattern}` | Regular expression literal. |
| `%r{pattern}options` | Regular expression literal with options. |
| `Regexp.escape(string)` | Escapes special characters in a string for use in a regular expression. |
| `Regexp.quote(string)` | Escapes special characters in a string for use in a regular expression. |
| `Regexp.last_match` | Returns the last MatchData object. |
| `Regexp.last_match(n)` | Returns the nth capture group from the last match. |
| `Regexp.union` | Returns a new regular expression that matches any of the specified patterns. |
| `Regexp.union(*patterns)` | Returns a new regular expression that matches any of the specified patterns. |
| `~` | Match operator. |
| `=~` | Match operator. Returns the index of the first match or nil. |
| `match` | Match operator. Returns a MatchData object or nil. |
| `match(pattern)` | Match operator with the specified pattern. |
| `match?(pattern)` | Returns true if the string matches the specified pattern. |
| `casefold?` | Returns true if the regular expression is case-insensitive. |
| `encoding` | Returns the encoding of the regular expression. |
| `eql?` | Returns true if the regular expression is equal to the specified object. |
| `fixed_encoding?` | Returns true if the regular expression has a fixed encoding. |
| `hash` | Returns a hash value for the regular expression. |
| `inspect` | Returns a string representation of the regular expression. |
| `named_captures` | Returns a hash of the named captures in the regular expression. |
| `names` | Returns an array of the named captures in the regular expression. |
| `options` | Returns the options of the regular expression. |
| `source` | Returns the source pattern of the regular expression. |
| `to_s` | Returns the source pattern of the regular expression. |
| `to_regexp` | Returns the regular expression itself. |
| `MatchData` | Represents the result of a regular expression match. |
| `MatchData#[]` | Returns the nth capture group. |
| `MatchData#[](n)` | Returns the nth capture group. |
| `MatchData#[](start, length)` | Returns a substring based on the start and length. |
| `MatchData#[](range)` | Returns a substring based on the range. |
| `MatchData#begin` | Returns the offset of the beginning of the nth capture group. |
| `MatchData#begin(n)` | Returns the offset of the beginning of the nth capture group. |
| `MatchData#captures` | Returns an array of the capture groups. |
| `MatchData#end` | Returns the offset of the end of the nth capture group. |
| `MatchData#end(n)` | Returns the offset of the end of the nth capture group. |
| `MatchData#eql?` | Returns true if the MatchData is equal to the specified object. |
| `MatchData#full_match` | Returns the entire matched string. |
| `MatchData#hash` | Returns a hash value for the MatchData. |
| `MatchData#inspect` | Returns a string representation of the MatchData. |
| `MatchData#length` | Returns the number of capture groups. |
| `MatchData#named_captures` | Returns a hash of the named captures. |
| `MatchData#offset` | Returns the offset of the nth capture group. |
| `MatchData#offset(n)` | Returns the offset of the nth capture group. |
| `MatchData#post_match` | Returns the string after the match. |
| `MatchData#pre_match` | Returns the string before the match. |
| `MatchData#regexp` | Returns the regular expression used in the match. |
| `MatchData#size` | Returns the number of capture groups. |
| `MatchData#string` | Returns the string used in the match. |
| `MatchData#to_a` | Returns an array of the capture groups. |
| `MatchData#to_s` | Returns the entire matched string. |
| `MatchData#values_at` | Returns an array of the capture groups at the specified indices. |
| `MatchData#values_at(*indices)` | Returns an array of the capture groups at the specified indices. |

---
## Time and Date Methods

| Code | Description |
|------|-------------|
| `Time` | Represents a date and time. |
| `Time.now` | Returns the current time. |
| `Time.new` | Creates a new Time object. |
| `Time.new(year, month, day, hour, min, sec, zone)` | Creates a new Time object with the specified components. |
| `Time.at(time)` | Creates a new Time object from a Unix timestamp. |
| `Time.at(time, in: zone)` | Creates a new Time object from a Unix timestamp in the specified timezone. |
| `Time.gm(year, month, day, hour, min, sec)` | Creates a new Time object in UTC. |
| `Time.gm(year, month, day, hour, min, sec, usec)` | Creates a new Time object in UTC with microseconds. |
| `Time.local(year, month, day, hour, min, sec)` | Creates a new Time object in the local timezone. |
| `Time.local(year, month, day, hour, min, sec, usec)` | Creates a new Time object in the local timezone with microseconds. |
| `Time.utc(year, month, day, hour, min, sec)` | Creates a new Time object in UTC. |
| `Time.utc(year, month, day, hour, min, sec, usec)` | Creates a new Time object in UTC with microseconds. |
| `Time.mktime(year, month, day, hour, min, sec)` | Creates a new Time object in the local timezone. |
| `Time.mktime(year, month, day, hour, min, sec, usec)` | Creates a new Time object in the local timezone with microseconds. |
| `Time.strptime(string, format)` | Parses a string into a Time object using the specified format. |
| `Time#+` | Addition operator. |
| `Time#+ (other)` | Adds the specified number of seconds to the time. |
| `Time#-` | Subtraction operator. |
| `Time#- (other)` | Subtracts the specified number of seconds from the time or returns the difference between two times. |
| `Time#<=>` | Comparison operator. |
| `Time#==` | Equality operator. |
| `Time#===` | Case equality operator. |
| `Time#eql?` | Equality operator. |
| `Time#hash` | Returns a hash value for the time. |
| `Time#to_i` | Returns the Unix timestamp for the time. |
| `Time#to_f` | Returns the Unix timestamp for the time as a float. |
| `Time#to_s` | Returns a string representation of the time. |
| `Time#inspect` | Returns a string representation of the time. |
| `Time#asctime` | Returns the time as a string in the format "Weekday Month Date HH:MM:SS Year". |
| `Time#ctime` | Returns the time as a string in the format "Weekday Month Date HH:MM:SS Year". |
| `Time#localtime` | Returns the time in the local timezone. |
| `Time#gmtime` | Returns the time in UTC. |
| `Time#utc` | Returns the time in UTC. |
| `Time#getlocal` | Returns the time in the local timezone. |
| `Time#getgm` | Returns the time in UTC. |
| `Time#getutc` | Returns the time in UTC. |
| `Time#year` | Returns the year of the time. |
| `Time#month` | Returns the month of the time. |
| `Time#day` | Returns the day of the time. |
| `Time#yday` | Returns the day of the year of the time. |
| `Time#wday` | Returns the day of the week of the time. |
| `Time#hour` | Returns the hour of the time. |
| `Time#min` | Returns the minute of the time. |
| `Time#sec` | Returns the second of the time. |
| `Time#usec` | Returns the microsecond of the time. |
| `Time#nsec` | Returns the nanosecond of the time. |
| `Time#subsec` | Returns the fractional second of the time. |
| `Time#zone` | Returns the timezone of the time. |
| `Time#utc_offset` | Returns the UTC offset of the time in seconds. |
| `Time#isdst` | Returns true if the time is in daylight saving time. |
| `Time#dst?` | Returns true if the time is in daylight saving time. |
| `Time#sunday?` | Returns true if the time is on a Sunday. |
| `Time#monday?` | Returns true if the time is on a Monday. |
| `Time#tuesday?` | Returns true if the time is on a Tuesday. |
| `Time#wednesday?` | Returns true if the time is on a Wednesday. |
| `Time#thursday?` | Returns true if the time is on a Thursday. |
| `Time#friday?` | Returns true if the time is on a Friday. |
| `Time#saturday?` | Returns true if the time is on a Saturday. |
| `Time#strftime` | Returns the time as a string using the specified format. |
| `Time#strftime(format)` | Returns the time as a string using the specified format. |
| `Time#to_a` | Returns an array of the time components. |
| `Time#to_date` | Returns a Date object for the time. |
| `Time#to_datetime` | Returns a DateTime object for the time. |
| `Time#to_time` | Returns the time itself. |
| `Date` | Represents a calendar date. |
| `Date.today` | Returns the current date. |
| `Date.new(year, month, day)` | Creates a new Date object. |
| `Date.civil(year, month, day)` | Creates a new Date object using the civil calendar. |
| `Date.commercial(year, week, day)` | Creates a new Date object using the commercial calendar. |
| `Date.julian(year, day)` | Creates a new Date object using the Julian calendar. |
| `Date.ordinal(year, day)` | Creates a new Date object using the ordinal calendar. |
| `Date.parse(string)` | Parses a string into a Date object. |
| `Date.strptime(string, format)` | Parses a string into a Date object using the specified format. |
| `Date#+` | Addition operator. |
| `Date#+ (n)` | Adds the specified number of days to the date. |
| `Date#-` | Subtraction operator. |
| `Date#- (other)` | Subtracts the specified number of days from the date or returns the difference between two dates. |
| `Date#<=>` | Comparison operator. |
| `Date#==` | Equality operator. |
| `Date#===` | Case equality operator. |
| `Date#eql?` | Equality operator. |
| `Date#hash` | Returns a hash value for the date. |
| `Date#to_s` | Returns a string representation of the date. |
| `Date#inspect` | Returns a string representation of the date. |
| `Date#year` | Returns the year of the date. |
| `Date#month` | Returns the month of the date. |
| `Date#day` | Returns the day of the date. |
| `Date#yday` | Returns the day of the year of the date. |
| `Date#wday` | Returns the day of the week of the date. |
| `Date#mday` | Returns the day of the month of the date. |
| `Date#leap?` | Returns true if the date is in a leap year. |
| `Date#sunday?` | Returns true if the date is on a Sunday. |
| `Date#monday?` | Returns true if the date is on a Monday. |
| `Date#tuesday?` | Returns true if the date is on a Tuesday. |
| `Date#wednesday?` | Returns true if the date is on a Wednesday. |
| `Date#thursday?` | Returns true if the date is on a Thursday. |
| `Date#friday?` | Returns true if the date is on a Friday. |
| `Date#saturday?` | Returns true if the date is on a Saturday. |
| `Date#strftime` | Returns the date as a string using the specified format. |
| `Date#strftime(format)` | Returns the date as a string using the specified format. |
| `Date#to_date` | Returns the date itself. |
| `Date#to_datetime` | Returns a DateTime object for the date. |
| `Date#to_time` | Returns a Time object for the date. |
| `Date#to_s` | Returns a string representation of the date. |
| `Date#<<` | Returns the previous day. |
| `Date#>>` | Returns the next day. |
| `Date#next_day` | Returns the next day. |
| `Date#prev_day` | Returns the previous day. |
| `Date#next_month` | Returns the next month. |
| `Date#prev_month` | Returns the previous month. |
| `Date#next_year` | Returns the next year. |
| `Date#prev_year` | Returns the previous year. |
| `DateTime` | Represents a date and time with timezone support. |
| `DateTime.new(year, month, day, hour, min, sec, offset)` | Creates a new DateTime object. |
| `DateTime.civil(year, month, day, hour, min, sec, offset)` | Creates a new DateTime object using the civil calendar. |
| `DateTime.commercial(year, week, day, hour, min, sec, offset)` | Creates a new DateTime object using the commercial calendar. |
| `DateTime.julian(year, day, hour, min, sec, offset)` | Creates a new DateTime object using the Julian calendar. |
| `DateTime.ordinal(year, day, hour, min, sec, offset)` | Creates a new DateTime object using the ordinal calendar. |
| `DateTime.parse(string)` | Parses a string into a DateTime object. |
| `DateTime.strptime(string, format)` | Parses a string into a DateTime object using the specified format. |

---
## Error Handling

| Code | Description |
|------|-------------|
| `Exception` | Base class for all exceptions. |
| `StandardError` | Base class for standard errors. |
| `RuntimeError` | Default exception class for `raise`. |
| `NameError` | Raised when a local variable or method name is not found. |
| `NoMethodError` | Raised when a method is called on an object that does not support it. |
| `TypeError` | Raised when an operation is performed on an object of the wrong type. |
| `ArgumentError` | Raised when the number or arguments are wrong. |
| `IndexError` | Raised when an index is out of range. |
| `KeyError` | Raised when a key is not found in a hash. |
| `RangeError` | Raised when a value is out of range. |
| `ZeroDivisionError` | Raised when division by zero is attempted. |
| `NilError` | Raised when a nil value is encountered where it is not allowed (Ruby 2.3+). |
| `FrozenError` | Raised when attempting to modify a frozen object (Ruby 2.4+). |
| `LoadError` | Raised when a file cannot be loaded. |
| `SyntaxError` | Raised when a syntax error is encountered. |
| `SecurityError` | Raised when a security violation occurs. |
| `SignalException` | Base class for signal exceptions. |
| `Interrupt` | Raised when the user interrupts the program (e.g., Ctrl-C). |
| `SystemExit` | Raised when the program exits. |
| `SystemCallError` | Base class for system call errors. |
| `Errno` | Module containing system error constants. |
| `IOError` | Raised when an I/O operation fails. |
| `EOFError` | Raised when end of file is reached. |
| `ThreadError` | Raised when a thread operation fails. |
| `EncodingError` | Raised when an encoding error occurs. |
| `FiberError` | Raised when a fiber operation fails. |
| `RegexpError` | Raised when a regular expression error occurs. |
| `ScriptError` | Base class for script errors. |
| `NotImplementedError` | Raised when a method is not implemented. |
| `NoMemoryError` | Raised when memory allocation fails. |
| `raise` | Raises an exception. |
| `raise ExceptionClass` | Raises an exception of a specific class. |
| `raise ExceptionClass, message` | Raises an exception with a message. |
| `raise ExceptionClass, message, backtrace` | Raises an exception with a message and backtrace. |
| `raise message` | Raises a RuntimeError with a message. |
| `fail` | Alias for raise. |
| `rescue` | Catches exceptions. |
| `rescue ExceptionClass` | Catches exceptions of a specific class. |
| `rescue ExceptionClass => variable` | Catches exceptions of a specific class and assigns the exception to a variable. |
| `begin; ...; rescue; ...; end` | Begins a rescue block for exception handling. |
| `begin; ...; rescue ExceptionClass; ...; end` | Rescues specific exception classes. |
| `begin; ...; rescue ExceptionClass => variable; ...; end` | Rescues specific exception classes and assigns the exception to a variable. |
| `begin; ...; rescue; ...; else; ...; end` | Executes the else clause if no exceptions are raised. |
| `begin; ...; rescue; ...; ensure; ...; end` | Executes the ensure clause regardless of whether an exception is raised. |
| `retry` | Retries the begin block if an exception is rescued. |
| `else` | Executes code if no exceptions are raised. |
| `ensure` | Executes code regardless of whether an exception is raised. |
| `throw` | Throws a symbol. |
| `throw :symbol` | Throws a symbol. |
| `throw :symbol, value` | Throws a symbol with a value. |
| `catch` | Catches a thrown symbol. |
| `catch(:symbol) { ... }` | Catches a thrown symbol. |
| `catch(:symbol, &block)` | Catches a thrown symbol and executes the block. |

---
## Reflection and Introspection

| Code | Description |
|------|-------------|
| `ObjectSpace` | Provides access to all living objects. |
| `ObjectSpace.each_object` | Iterates over each living object. |
| `ObjectSpace.each_object { |obj| ... }` | Iterates over each living object and passes each object to a block. |
| `ObjectSpace.each_object(Class)` | Iterates over each living object of the specified class. |
| `ObjectSpace.each_object(Class) { |obj| ... }` | Iterates over each living object of the specified class and passes each object to a block. |
| `ObjectSpace.define_finalizer` | Defines a finalizer for an object. |
| `ObjectSpace.define_finalizer(obj, &block)` | Defines a finalizer for an object. |
| `ObjectSpace.garbage_collect` | Performs garbage collection. |
| `ObjectSpace.dump` | Dumps all objects to a file. |
| `ObjectSpace.dump(filename)` | Dumps all objects to the specified file. |
| `ObjectSpace.dump_all` | Dumps all objects to a file. |
| `ObjectSpace.dump_all(filename)` | Dumps all objects to the specified file. |
| `ObjectSpace.undump` | Loads objects from a file. |
| `ObjectSpace.undump(filename)` | Loads objects from the specified file. |
| `Object#class` | Returns the class of the object. |
| `Object#is_a?` | Returns true if the object is an instance of the specified class or module. |
| `Object#kind_of?` | Alias for is_a?. |
| `Object#instance_of?` | Returns true if the object is an instance of the specified class. |
| `Object#respond_to?` | Returns true if the object responds to the specified method. |
| `Object#respond_to?(method, include_private=false)` | Returns true if the object responds to the specified method. |
| `Object#public_send` | Calls a public method on the object. |
| `Object#public_send(method, *args)` | Calls a public method on the object with the specified arguments. |
| `Object#send` | Calls a method on the object. |
| `Object#send(method, *args)` | Calls a method on the object with the specified arguments. |
| `Object#method` | Returns a Method object for the specified method. |
| `Object#method(method)` | Returns a Method object for the specified method. |
| `Object#public_method` | Returns a Method object for the specified public method. |
| `Object#public_method(method)` | Returns a Method object for the specified public method. |
| `Object#singleton_method` | Returns a Method object for the specified singleton method. |
| `Object#singleton_method(method)` | Returns a Method object for the specified singleton method. |
| `Object#methods` | Returns an array of the method names available for the object. |
| `Object#public_methods` | Returns an array of the public method names available for the object. |
| `Object#private_methods` | Returns an array of the private method names available for the object. |
| `Object#protected_methods` | Returns an array of the protected method names available for the object. |
| `Object#singleton_methods` | Returns an array of the singleton method names available for the object. |
| `Object#instance_variables` | Returns an array of the instance variable names for the object. |
| `Object#instance_variable_get` | Returns the value of the specified instance variable. |
| `Object#instance_variable_get(variable)` | Returns the value of the specified instance variable. |
| `Object#instance_variable_set` | Sets the value of the specified instance variable. |
| `Object#instance_variable_set(variable, value)` | Sets the value of the specified instance variable. |
| `Object#instance_variable_defined?` | Returns true if the specified instance variable is defined. |
| `Object#instance_variable_defined?(variable)` | Returns true if the specified instance variable is defined. |
| `Object#remove_instance_variable` | Removes the specified instance variable. |
| `Object#remove_instance_variable(variable)` | Removes the specified instance variable. |
| `Object#frozen?` | Returns true if the object is frozen. |
| `Object#freeze` | Freezes the object. |
| `Object#dup` | Returns a shallow copy of the object. |
| `Object#clone` | Returns a shallow copy of the object. |
| `Object#initialize_copy` | Called when copying an object. |
| `Object#taint` | Taints the object. |
| `Object#tainted?` | Returns true if the object is tainted. |
| `Object#untaint` | Untaints the object. |
| `Object#trust` | Trusts the object. |
| `Object#untrust` | Untrusts the object. |
| `Object#untrusted?` | Returns true if the object is untrusted. |
| `Module#name` | Returns the name of the module. |
| `Module#ancestors` | Returns an array of the ancestors of the module. |
| `Module#included_modules` | Returns an array of the modules included in the module. |
| `Module#constants` | Returns an array of the constants defined in the module. |
| `Module#const_get` | Returns the value of the specified constant. |
| `Module#const_get(name)` | Returns the value of the specified constant. |
| `Module#const_set` | Sets the value of the specified constant. |
| `Module#const_set(name, value)` | Sets the value of the specified constant. |
| `Module#const_defined?` | Returns true if the specified constant is defined. |
| `Module#const_defined?(name)` | Returns true if the specified constant is defined. |
| `Module#remove_const` | Removes the specified constant. |
| `Module#remove_const(name)` | Removes the specified constant. |
| `Module#autoload` | Registers a module to be loaded automatically. |
| `Module#autoload(name, path)` | Registers a module to be loaded automatically from the specified path. |
| `Module#autoload?` | Returns true if the specified module is registered for autoloading. |
| `Module#autoload?(name)` | Returns true if the specified module is registered for autoloading. |
| `Module#define_method` | Defines a method in the module. |
| `Module#define_method(name, &block)` | Defines a method in the module. |
| `Module#define_singleton_method` | Defines a singleton method in the module. |
| `Module#define_singleton_method(name, &block)` | Defines a singleton method in the module. |
| `Module#alias_method` | Creates an alias for a method in the module. |
| `Module#alias_method(new_name, old_name)` | Creates an alias for a method in the module. |
| `Module#undef_method` | Removes a method from the module. |
| `Module#undef_method(name)` | Removes a method from the module. |
| `Module#method_defined?` | Returns true if the specified method is defined in the module. |
| `Module#method_defined?(name)` | Returns true if the specified method is defined in the module. |
| `Module#private_method_defined?` | Returns true if the specified private method is defined in the module. |
| `Module#private_method_defined?(name)` | Returns true if the specified private method is defined in the module. |
| `Module#protected_method_defined?` | Returns true if the specified protected method is defined in the module. |
| `Module#protected_method_defined?(name)` | Returns true if the specified protected method is defined in the module. |
| `Module#public_method_defined?` | Returns true if the specified public method is defined in the module. |
| `Module#public_method_defined?(name)` | Returns true if the specified public method is defined in the module. |
| `Module#instance_methods` | Returns an array of the instance method names defined in the module. |
| `Module#public_instance_methods` | Returns an array of the public instance method names defined in the module. |
| `Module#private_instance_methods` | Returns an array of the private instance method names defined in the module. |
| `Module#protected_instance_methods` | Returns an array of the protected instance method names defined in the module. |
| `Module#included` | Called when the module is included in another module or class. |
| `Module#extended` | Called when the module is extended by another module or class. |
| `Module#prepended` | Called when the module is prepended to another module or class. |
| `Module#method_added` | Called when a method is added to the module. |
| `Module#method_removed` | Called when a method is removed from the module. |
| `Module#method_undefined` | Called when a method is undefined in the module. |
| `Class#new` | Creates a new instance of the class. |
| `Class#allocate` | Allocates memory for a new instance of the class. |
| `Class#superclass` | Returns the superclass of the class. |
| `Class#inherited` | Called when the class is inherited. |
| `Class#method_added` | Called when a method is added to the class. |
| `Class#method_removed` | Called when a method is removed from the class. |
| `Class#method_undefined` | Called when a method is undefined in the class. |
| `Class#singleton_method_added` | Called when a singleton method is added to the class. |
| `Class#singleton_method_removed` | Called when a singleton method is removed from the class. |
| `Class#singleton_method_undefined` | Called when a singleton method is undefined in the class. |
| `Binding` | Represents a binding of variables and methods. |
| `Kernel#binding` | Returns a Binding object for the current context. |
| `Proc#binding` | Returns the binding associated with the proc. |
| `Method#owner` | Returns the owner of the method. |
| `Method#name` | Returns the name of the method. |
| `Method#arity` | Returns the arity of the method. |
| `Method#parameters` | Returns an array of the parameters of the method. |
| `Method#source_location` | Returns the source location of the method. |
| `Method#super_method` | Returns the super method of the method. |
| `UnboundMethod#bind` | Binds the unbound method to an object. |
| `UnboundMethod#bind(obj)` | Binds the unbound method to an object. |
| `UnboundMethod#owner` | Returns the owner of the unbound method. |
| `UnboundMethod#name` | Returns the name of the unbound method. |
| `UnboundMethod#arity` | Returns the arity of the unbound method. |
| `UnboundMethod#parameters` | Returns an array of the parameters of the unbound method. |
| `UnboundMethod#source_location` | Returns the source location of the unbound method. |

---
## Concurrency

| Code | Description |
|------|-------------|
| `Thread` | Represents a thread of execution. |
| `Thread.new` | Creates a new thread. |
| `Thread.new { ... }` | Creates a new thread and passes it to a block. |
| `Thread.start` | Creates and starts a new thread. |
| `Thread.start(args) { |args| ... }` | Creates and starts a new thread with the specified arguments. |
| `Thread.fork` | Creates and starts a new thread. |
| `Thread.fork { ... }` | Creates and starts a new thread and passes it to a block. |
| `Thread.current` | Returns the current thread. |
| `Thread.main` | Returns the main thread. |
| `Thread.list` | Returns an array of all threads. |
| `Thread.pass` | Passes execution to another thread. |
| `Thread.stop` | Stops the current thread. |
| `Thread.exit` | Exits the current thread. |
| `Thread.kill` | Kills the specified thread. |
| `Thread.kill(thread)` | Kills the specified thread. |
| `Thread.terminate` | Terminates the specified thread. |
| `Thread.terminate(thread)` | Terminates the specified thread. |
| `Thread.join` | Waits for the specified thread to finish. |
| `Thread.join(thread)` | Waits for the specified thread to finish. |
| `Thread.join(thread, timeout)` | Waits for the specified thread to finish with a timeout. |
| `Thread.value` | Returns the value of the specified thread. |
| `Thread.value(thread)` | Returns the value of the specified thread. |
| `Thread.status` | Returns the status of the specified thread. |
| `Thread.status(thread)` | Returns the status of the specified thread. |
| `Thread.alive?` | Returns true if the specified thread is alive. |
| `Thread.alive?(thread)` | Returns true if the specified thread is alive. |
| `Thread.stop?` | Returns true if the specified thread is stopped. |
| `Thread.stop?(thread)` | Returns true if the specified thread is stopped. |
| `Thread.abort_on_exception` | Returns true if the specified thread aborts on exception. |
| `Thread.abort_on_exception=` | Sets whether the specified thread aborts on exception. |
| `Thread.abort_on_exception=(bool)` | Sets whether the specified thread aborts on exception. |
| `Thread.report_on_exception` | Returns true if the specified thread reports on exception. |
| `Thread.report_on_exception=` | Sets whether the specified thread reports on exception. |
| `Thread.report_on_exception=(bool)` | Sets whether the specified thread reports on exception. |
| `Thread.priority` | Returns the priority of the specified thread. |
| `Thread.priority=` | Sets the priority of the specified thread. |
| `Thread.priority=(priority)` | Sets the priority of the specified thread. |
| `Thread.name` | Returns the name of the specified thread. |
| `Thread.name=` | Sets the name of the specified thread. |
| `Thread.name=(name)` | Sets the name of the specified thread. |
| `Thread.safe_level` | Returns the safe level of the specified thread. |
| `Thread.group` | Returns the thread group of the specified thread. |
| `Thread.backtrace` | Returns the backtrace of the specified thread. |
| `Thread.backtrace_locations` | Returns the backtrace locations of the specified thread. |
| `Thread.thread_id` | Returns the thread ID of the specified thread. |
| `Thread.object_id` | Returns the object ID of the specified thread. |
| `Thread#run` | Starts the thread. |
| `Thread#wakeup` | Wakes up the thread. |
| `Thread#raise` | Raises an exception in the thread. |
| `Thread#raise(exception)` | Raises an exception in the thread. |
| `Thread#raise(exception, message)` | Raises an exception in the thread with a message. |
| `Thread#kill` | Kills the thread. |
| `Thread#terminate` | Terminates the thread. |
| `Thread#join` | Waits for the thread to finish. |
| `Thread#join(timeout)` | Waits for the thread to finish with a timeout. |
| `Thread#value` | Returns the value of the thread. |
| `Thread#status` | Returns the status of the thread. |
| `Thread#alive?` | Returns true if the thread is alive. |
| `Thread#stop?` | Returns true if the thread is stopped. |
| `Thread#abort_on_exception` | Returns true if the thread aborts on exception. |
| `Thread#abort_on_exception=` | Sets whether the thread aborts on exception. |
| `Thread#abort_on_exception=(bool)` | Sets whether the thread aborts on exception. |
| `Thread#report_on_exception` | Returns true if the thread reports on exception. |
| `Thread#report_on_exception=` | Sets whether the thread reports on exception. |
| `Thread#report_on_exception=(bool)` | Sets whether the thread reports on exception. |
| `Thread#priority` | Returns the priority of the thread. |
| `Thread#priority=` | Sets the priority of the thread. |
| `Thread#priority=(priority)` | Sets the priority of the thread. |
| `Thread#name` | Returns the name of the thread. |
| `Thread#name=` | Sets the name of the thread. |
| `Thread#name=(name)` | Sets the name of the thread. |
| `Thread#safe_level` | Returns the safe level of the thread. |
| `Thread#backtrace` | Returns the backtrace of the thread. |
| `Thread#backtrace_locations` | Returns the backtrace locations of the thread. |
| `Thread#thread_id` | Returns the thread ID of the thread. |
| `Thread#object_id` | Returns the object ID of the thread. |
| `Mutex` | Represents a mutex for thread synchronization. |
| `Mutex.new` | Creates a new mutex. |
| `Mutex#lock` | Locks the mutex. |
| `Mutex#try_lock` | Tries to lock the mutex. Returns true if the lock was acquired. |
| `Mutex#unlock` | Unlocks the mutex. |
| `Mutex#locked?` | Returns true if the mutex is locked. |
| `Mutex#owned?` | Returns true if the mutex is owned by the current thread. |
| `Mutex#sleep` | Sleeps while holding the mutex. |
| `Mutex#sleep(timeout)` | Sleeps while holding the mutex with a timeout. |
| `Mutex#condition_variable` | Returns a ConditionVariable associated with the mutex. |
| `ConditionVariable` | Represents a condition variable for thread synchronization. |
| `ConditionVariable.new` | Creates a new condition variable. |
| `ConditionVariable#wait` | Waits for the condition variable. |
| `ConditionVariable#wait(mutex)` | Waits for the condition variable with the specified mutex. |
| `ConditionVariable#wait(mutex, timeout)` | Waits for the condition variable with the specified mutex and timeout. |
| `ConditionVariable#signal` | Signals the condition variable. |
| `ConditionVariable#broadcast` | Broadcasts the condition variable. |
| `Queue` | Represents a thread-safe queue. |
| `Queue.new` | Creates a new queue. |
| `Queue#enq` | Enqueues an object. |
| `Queue#enq(obj)` | Enqueues an object. |
| `Queue#<<` | Enqueues an object. |
| `Queue#<<(obj)` | Enqueues an object. |
| `Queue#push` | Enqueues an object. |
| `Queue#push(obj)` | Enqueues an object. |
| `Queue#deq` | Dequeues an object. |
| `Queue#deq(non_block=false)` | Dequeues an object. |
| `Queue#pop` | Dequeues an object. |
| `Queue#pop(non_block=false)` | Dequeues an object. |
| `Queue#shift` | Dequeues an object. |
| `Queue#shift(non_block=false)` | Dequeues an object. |
| `Queue#empty?` | Returns true if the queue is empty. |
| `Queue#size` | Returns the size of the queue. |
| `Queue#length` | Returns the size of the queue. |
| `Queue#num_waiting` | Returns the number of threads waiting on the queue. |
| `SizedQueue` | Represents a thread-safe queue with a maximum size. |
| `SizedQueue.new(max)` | Creates a new sized queue with the specified maximum size. |
| `SizedQueue#max` | Returns the maximum size of the queue. |
| `SizedQueue#max=` | Sets the maximum size of the queue. |
| `SizedQueue#max=(max)` | Sets the maximum size of the queue. |
| `Fiber` | Represents a fiber for cooperative concurrency. |
| `Fiber.new` | Creates a new fiber. |
| `Fiber.new { ... }` | Creates a new fiber and passes it to a block. |
| `Fiber.current` | Returns the current fiber. |
| `Fiber.yield` | Yields control from the fiber. |
| `Fiber.yield(args)` | Yields control from the fiber with the specified arguments. |
| `Fiber#resume` | Resumes the fiber. |
| `Fiber#resume(args)` | Resumes the fiber with the specified arguments. |
| `Fiber#transfer` | Transfers control to another fiber. |
| `Fiber#transfer(fiber, args)` | Transfers control to another fiber with the specified arguments. |
| `Fiber#alive?` | Returns true if the fiber is alive. |
| `Fiber#terminated?` | Returns true if the fiber is terminated. |

---
## Networking

| Code | Description |
|------|-------------|
| `require 'net/http'` | Loads the Net::HTTP library. |
| `Net::HTTP` | Provides methods for HTTP client functionality. |
| `Net::HTTP.get(uri)` | Performs an HTTP GET request. |
| `Net::HTTP.get(uri, headers)` | Performs an HTTP GET request with the specified headers. |
| `Net::HTTP.get(uri) { |response| ... }` | Performs an HTTP GET request and passes the response to a block. |
| `Net::HTTP.get_response(uri)` | Performs an HTTP request and returns the response. |
| `Net::HTTP.get_print(uri)` | Performs an HTTP GET request and prints the response. |
| `Net::HTTP.get_print(uri, output)` | Performs an HTTP GET request and prints the response to the specified output. |
| `Net::HTTP.post(uri, body)` | Performs an HTTP POST request. |
| `Net::HTTP.post(uri, body, headers)` | Performs an HTTP POST request with the specified headers. |
| `Net::HTTP.post_form(uri, params)` | Performs an HTTP POST request with form data. |
| `Net::HTTP.start(uri.host, uri.port)` | Starts an HTTP session. |
| `Net::HTTP.start(uri.host, uri.port) { |http| ... }` | Starts an HTTP session and passes the HTTP object to a block. |
| `Net::HTTP.start(uri.host, uri.port, options)` | Starts an HTTP session with the specified options. |
| `Net::HTTP.start(uri.host, uri.port, options) { |http| ... }` | Starts an HTTP session with the specified options and passes the HTTP object to a block. |
| `Net::HTTP.new(uri.host, uri.port)` | Creates a new HTTP object. |
| `Net::HTTP.new(uri.host, uri.port, options)` | Creates a new HTTP object with the specified options. |
| `Net::HTTP#request(request)` | Performs an HTTP request. |
| `Net::HTTP#request(request) { |response| ... }` | Performs an HTTP request and passes the response to a block. |
| `Net::HTTP#get(path)` | Performs an HTTP GET request. |
| `Net::HTTP#get(path, headers)` | Performs an HTTP GET request with the specified headers. |
| `Net::HTTP#post(path, body)` | Performs an HTTP POST request. |
| `Net::HTTP#post(path, body, headers)` | Performs an HTTP POST request with the specified headers. |
| `Net::HTTP#head(path)` | Performs an HTTP HEAD request. |
| `Net::HTTP#head(path, headers)` | Performs an HTTP HEAD request with the specified headers. |
| `Net::HTTP#put(path, body)` | Performs an HTTP PUT request. |
| `Net::HTTP#put(path, body, headers)` | Performs an HTTP PUT request with the specified headers. |
| `Net::HTTP#delete(path)` | Performs an HTTP DELETE request. |
| `Net::HTTP#delete(path, headers)` | Performs an HTTP DELETE request with the specified headers. |
| `Net::HTTP#patch(path, body)` | Performs an HTTP PATCH request. |
| `Net::HTTP#patch(path, body, headers)` | Performs an HTTP PATCH request with the specified headers. |
| `Net::HTTP#options(path)` | Performs an HTTP OPTIONS request. |
| `Net::HTTP#options(path, headers)` | Performs an HTTP OPTIONS request with the specified headers. |
| `Net::HTTP#propfind(path)` | Performs an HTTP PROPFIND request. |
| `Net::HTTP#propfind(path, body)` | Performs an HTTP PROPFIND request with the specified body. |
| `Net::HTTP#propfind(path, body, headers)` | Performs an HTTP PROPFIND request with the specified body and headers. |
| `Net::HTTPResponse` | Represents an HTTP response. |
| `Net::HTTPResponse#code` | Returns the HTTP status code. |
| `Net::HTTPResponse#message` | Returns the HTTP status message. |
| `Net::HTTPResponse#body` | Returns the response body. |
| `Net::HTTPResponse#body_permitted?` | Returns true if the response body is permitted. |
| `Net::HTTPResponse#content_type` | Returns the Content-Type header. |
| `Net::HTTPResponse#content_length` | Returns the Content-Length header. |
| `Net::HTTPResponse#chunked?` | Returns true if the response is chunked. |
| `Net::HTTPResponse#read_body` | Reads the response body. |
| `Net::HTTPResponse#read_body { |chunk| ... }` | Reads the response body and passes each chunk to a block. |
| `Net::HTTPRequest` | Represents an HTTP request. |
| `Net::HTTPRequest#body` | Returns the request body. |
| `Net::HTTPRequest#body=` | Sets the request body. |
| `Net::HTTPRequest#body=(body)` | Sets the request body. |
| `Net::HTTPRequest#content_type` | Returns the Content-Type header. |
| `Net::HTTPRequest#content_type=` | Sets the Content-Type header. |
| `Net::HTTPRequest#content_type=(content_type)` | Sets the Content-Type header. |
| `Net::HTTPRequest#content_length` | Returns the Content-Length header. |
| `Net::HTTPRequest#content_length=` | Sets the Content-Length header. |
| `Net::HTTPRequest#content_length=(content_length)` | Sets the Content-Length header. |
| `Net::HTTPRequest#range` | Returns the Range header. |
| `Net::HTTPRequest#range=` | Sets the Range header. |
| `Net::HTTPRequest#range=(range)` | Sets the Range header. |
| `Net::HTTPRequest#if_modified_since` | Returns the If-Modified-Since header. |
| `Net::HTTPRequest#if_modified_since=` | Sets the If-Modified-Since header. |
| `Net::HTTPRequest#if_modified_since=(if_modified_since)` | Sets the If-Modified-Since header. |
| `Net::HTTPRequest#if_unmodified_since` | Returns the If-Unmodified-Since header. |
| `Net::HTTPRequest#if_unmodified_since=` | Sets the If-Unmodified-Since header. |
| `Net::HTTPRequest#if_unmodified_since=(if_unmodified_since)` | Sets the If-Unmodified-Since header. |
| `Net::HTTPRequest#if_match` | Returns the If-Match header. |
| `Net::HTTPRequest#if_match=` | Sets the If-Match header. |
| `Net::HTTPRequest#if_match=(if_match)` | Sets the If-Match header. |
| `Net::HTTPRequest#if_none_match` | Returns the If-None-Match header. |
| `Net::HTTPRequest#if_none_match=` | Sets the If-None-Match header. |
| `Net::HTTPRequest#if_none_match=(if_none_match)` | Sets the If-None-Match header. |
| `Net::HTTPRequest#if_range` | Returns the If-Range header. |
| `Net::HTTPRequest#if_range=` | Sets the If-Range header. |
| `Net::HTTPRequest#if_range=(if_range)` | Sets the If-Range header. |
| `Net::HTTPRequest#basic_auth` | Returns the basic authentication credentials. |
| `Net::HTTPRequest#basic_auth=` | Sets the basic authentication credentials. |
| `Net::HTTPRequest#basic_auth=(user, pass)` | Sets the basic authentication credentials. |
| `URI` | Represents a Uniform Resource Identifier. |
| `URI.parse(string)` | Parses a string into a URI object. |
| `URI.extract(string)` | Extracts URIs from a string. |
| `URI.extract(string, schemes)` | Extracts URIs from a string with the specified schemes. |
| `URI.extract(string, schemes) { |uri| ... }` | Extracts URIs from a string with the specified schemes and passes each URI to a block. |
| `URI.encode(string)` | Encodes a string for use in a URI. |
| `URI.encode(string, unsafe)` | Encodes a string for use in a URI with the specified unsafe characters. |
| `URI.decode(string)` | Decodes a URI-encoded string. |
| `URI.decode(string, encoding)` | Decodes a URI-encoded string with the specified encoding. |
| `URI.escape(string)` | Escapes a string for use in a URI. |
| `URI.escape(string, unsafe)` | Escapes a string for use in a URI with the specified unsafe characters. |
| `URI.unescape(string)` | Unescapes a URI-escaped string. |
| `URI.unescape(string, encoding)` | Unescapes a URI-escaped string with the specified encoding. |
| `URI::Generic` | Base class for URI objects. |
| `URI::HTTP` | Represents an HTTP URI. |
| `URI::HTTPS` | Represents an HTTPS URI. |
| `URI::FTP` | Represents an FTP URI. |
| `URI::MailTo` | Represents a mailto URI. |
| `URI::LDAP` | Represents an LDAP URI. |
| `URI::LDAPS` | Represents an LDAPS URI. |
| `URI#scheme` | Returns the scheme of the URI. |
| `URI#user` | Returns the user of the URI. |
| `URI#password` | Returns the password of the URI. |
| `URI#host` | Returns the host of the URI. |
| `URI#port` | Returns the port of the URI. |
| `URI#path` | Returns the path of the URI. |
| `URI#query` | Returns the query of the URI. |
| `URI#fragment` | Returns the fragment of the URI. |
| `URI#opaque` | Returns the opaque part of the URI. |
| `URI#registry` | Returns the registry part of the URI. |
| `URI#authority` | Returns the authority of the URI. |
| `URI#to_s` | Returns a string representation of the URI. |
| `URI#==` | Equality operator. |
| `URI#eql?` | Equality operator. |
| `URI#hash` | Returns a hash value for the URI. |
| `URI#merge` | Merges the URI with another URI. |
| `URI#merge(other)` | Merges the URI with another URI. |
| `URI#relative?` | Returns true if the URI is relative. |
| `URI#absolute?` | Returns true if the URI is absolute. |
| `URI#normalize` | Normalizes the URI. |
| `URI#normalize!` | Normalizes the URI in place. Returns the URI. |
| `Net::FTP` | Provides methods for FTP client functionality. |
| `Net::FTP.open(host)` | Opens an FTP connection. |
| `Net::FTP.open(host) { |ftp| ... }` | Opens an FTP connection and passes the FTP object to a block. |
| `Net::FTP.open(host, user, pass)` | Opens an FTP connection with the specified username and password. |
| `Net::FTP.open(host, user, pass) { |ftp| ... }` | Opens an FTP connection with the specified username and password and passes the FTP object to a block. |
| `Net::FTP.new` | Creates a new FTP object. |
| `Net::FTP.new(host)` | Creates a new FTP object with the specified host. |
| `Net::FTP.new(host, user, pass)` | Creates a new FTP object with the specified host, username, and password. |
| `Net::FTP#connect` | Connects to the FTP server. |
| `Net::FTP#login` | Logs in to the FTP server. |
| `Net::FTP#login(user, pass)` | Logs in to the FTP server with the specified username and password. |
| `Net::FTP#close` | Closes the FTP connection. |
| `Net::FTP#closed?` | Returns true if the FTP connection is closed. |
| `Net::FTP#get` | Downloads a file from the FTP server. |
| `Net::FTP#get(remote_file, local_file)` | Downloads a file from the FTP server. |
| `Net::FTP#get(remote_file, local_file) { |data| ... }` | Downloads a file from the FTP server and passes the data to a block. |
| `Net::FTP#put` | Uploads a file to the FTP server. |
| `Net::FTP#put(local_file, remote_file)` | Uploads a file to the FTP server. |
| `Net::FTP#put(local_file, remote_file) { |data| ... }` | Uploads a file to the FTP server and passes the data to a block. |
| `Net::FTP#delete` | Deletes a file from the FTP server. |
| `Net::FTP#delete(remote_file)` | Deletes a file from the FTP server. |
| `Net::FTP#rename` | Renames a file on the FTP server. |
| `Net::FTP#rename(from, to)` | Renames a file on the FTP server. |
| `Net::FTP#chdir` | Changes the current directory on the FTP server. |
| `Net::FTP#chdir(dir)` | Changes the current directory on the FTP server. |
| `Net::FTP#pwd` | Returns the current directory on the FTP server. |
| `Net::FTP#mkdir` | Creates a new directory on the FTP server. |
| `Net::FTP#mkdir(dir)` | Creates a new directory on the FTP server. |
| `Net::FTP#rmdir` | Removes a directory from the FTP server. |
| `Net::FTP#rmdir(dir)` | Removes a directory from the FTP server. |
| `Net::FTP#list` | Lists the files in the current directory on the FTP server. |
| `Net::FTP#list(dir)` | Lists the files in the specified directory on the FTP server. |
| `Net::FTP#list(dir) { |file| ... }` | Lists the files in the specified directory on the FTP server and passes each file to a block. |
| `Net::FTP#nlst` | Lists the file names in the current directory on the FTP server. |
| `Net::FTP#nlst(dir)` | Lists the file names in the specified directory on the FTP server. |
| `Net::FTP#stat` | Returns the status of a file on the FTP server. |
| `Net::FTP#stat(file)` | Returns the status of a file on the FTP server. |
| `Net::FTP#raw` | Sends a raw command to the FTP server. |
| `Net::FTP#raw(command)` | Sends a raw command to the FTP server. |
| `Net::FTP#raw(command) { |response| ... }` | Sends a raw command to the FTP server and passes the response to a block. |
| `Net::FTP#voidcmd` | Sends a command to the FTP server and expects no response. |
| `Net::FTP#voidcmd(command)` | Sends a command to the FTP server and expects no response. |
| `Net::FTP#sendcmd` | Sends a command to the FTP server and expects a response. |
| `Net::FTP#sendcmd(command)` | Sends a command to the FTP server and expects a response. |
| `Net::FTP#getbinaryfile` | Downloads a binary file from the FTP server. |
| `Net::FTP#getbinaryfile(remote_file, local_file)` | Downloads a binary file from the FTP server. |
| `Net::FTP#getbinaryfile(remote_file, local_file) { |data| ... }` | Downloads a binary file from the FTP server and passes the data to a block. |
| `Net::FTP#putbinaryfile` | Uploads a binary file to the FTP server. |
| `Net::FTP#putbinaryfile(local_file, remote_file)` | Uploads a binary file to the FTP server. |
| `Net::FTP#putbinaryfile(local_file, remote_file) { |data| ... }` | Uploads a binary file to the FTP server and passes the data to a block. |
| `Net::SMTP` | Provides methods for SMTP client functionality. |
| `Net::SMTP.start(host, port)` | Starts an SMTP session. |
| `Net::SMTP.start(host, port) { |smtp| ... }` | Starts an SMTP session and passes the SMTP object to a block. |
| `Net::SMTP.start(host, port, user, pass)` | Starts an SMTP session with the specified username and password. |
| `Net::SMTP.start(host, port, user, pass) { |smtp| ... }` | Starts an SMTP session with the specified username and password and passes the SMTP object to a block. |
| `Net::SMTP.new` | Creates a new SMTP object. |
| `Net::SMTP.new(host, port)` | Creates a new SMTP object with the specified host and port. |
| `Net::SMTP#sendmail` | Sends an email. |
| `Net::SMTP#sendmail(from, to, msg)` | Sends an email with the specified from, to, and message. |
| `Net::SMTP#send_message` | Sends an email message. |
| `Net::SMTP#send_message(from, to, msg)` | Sends an email message with the specified from, to, and message. |
| `Net::SMTP#auth` | Authenticates with the SMTP server. |
| `Net::SMTP#auth(user, pass)` | Authenticates with the SMTP server with the specified username and password. |
| `Net::SMTP#starttls` | Starts TLS. |
| `Net::SMTP#starttls &block` | Starts TLS and executes the block. |
| `Net::SMTP#finish` | Finishes the SMTP session. |
| `Net::IMAP` | Provides methods for IMAP client functionality. |
| `Net::POP3` | Provides methods for POP3 client functionality. |

---
## JSON

| Code | Description |
|------|-------------|
| `require 'json'` | Loads the JSON library. |
| `JSON` | Provides methods for JSON parsing and generation. |
| `JSON.parse(string)` | Parses a JSON string into a Ruby object. |
| `JSON.parse(string, options)` | Parses a JSON string into a Ruby object with the specified options. |
| `JSON.parse!(string)` | Parses a JSON string into a Ruby object and raises an exception on error. |
| `JSON.parse!(string, options)` | Parses a JSON string into a Ruby object with the specified options and raises an exception on error. |
| `JSON.generate(obj)` | Generates a JSON string from a Ruby object. |
| `JSON.generate(obj, options)` | Generates a JSON string from a Ruby object with the specified options. |
| `JSON.dump(obj)` | Generates a JSON string from a Ruby object. |
| `JSON.dump(obj, options)` | Generates a JSON string from a Ruby object with the specified options. |
| `JSON.pretty_generate(obj)` | Generates a pretty-printed JSON string from a Ruby object. |
| `JSON.pretty_generate(obj, options)` | Generates a pretty-printed JSON string from a Ruby object with the specified options. |
| `JSON.fast_generate(obj)` | Generates a JSON string from a Ruby object using the fast generator. |
| `JSON.fast_generate(obj, options)` | Generates a JSON string from a Ruby object with the specified options using the fast generator. |
| `JSON.load(file)` | Loads a JSON object from a file. |
| `JSON.load(file, options)` | Loads a JSON object from a file with the specified options. |
| `JSON.load!(file)` | Loads a JSON object from a file and raises an exception on error. |
| `JSON.load!(file, options)` | Loads a JSON object from a file with the specified options and raises an exception on error. |
| `JSON.dump(obj, file)` | Dumps a Ruby object to a file as JSON. |
| `JSON.dump(obj, file, options)` | Dumps a Ruby object to a file as JSON with the specified options. |
| `JSON.pretty_dump(obj, file)` | Dumps a Ruby object to a file as pretty-printed JSON. |
| `JSON.pretty_dump(obj, file, options)` | Dumps a Ruby object to a file as pretty-printed JSON with the specified options. |
| `JSON.create_id` | Creates a JSON ID for a class. |
| `JSON.create_id(class, &block)` | Creates a JSON ID for a class. |
| `JSON.add_ruby_class` | Adds a Ruby class for JSON serialization. |
| `JSON.add_ruby_class(class)` | Adds a Ruby class for JSON serialization. |
| `JSON.add_ruby_class(class, &block)` | Adds a Ruby class for JSON serialization with a custom block. |
| `JSON::Ext` | Provides extensions for JSON. |
| `JSON::Ext.parse(string)` | Parses a JSON string into a Ruby object using the extension parser. |
| `JSON::Ext.parse(string, options)` | Parses a JSON string into a Ruby object with the specified options using the extension parser. |
| `JSON::Ext.generate(obj)` | Generates a JSON string from a Ruby object using the extension generator. |
| `JSON::Ext.generate(obj, options)` | Generates a JSON string from a Ruby object with the specified options using the extension generator. |

---
## YAML

| Code | Description |
|------|-------------|
| `require 'yaml'` | Loads the YAML library. |
| `YAML` | Provides methods for YAML parsing and generation. |
| `YAML.load(string)` | Parses a YAML string into a Ruby object. |
| `YAML.load(string, options)` | Parses a YAML string into a Ruby object with the specified options. |
| `YAML.load!(string)` | Parses a YAML string into a Ruby object and raises an exception on error. |
| `YAML.load!(string, options)` | Parses a YAML string into a Ruby object with the specified options and raises an exception on error. |
| `YAML.dump(obj)` | Generates a YAML string from a Ruby object. |
| `YAML.dump(obj, options)` | Generates a YAML string from a Ruby object with the specified options. |
| `YAML.load_file(file)` | Loads a YAML object from a file. |
| `YAML.load_file(file, options)` | Loads a YAML object from a file with the specified options. |
| `YAML.load_file!(file)` | Loads a YAML object from a file and raises an exception on error. |
| `YAML.load_file!(file, options)` | Loads a YAML object from a file with the specified options and raises an exception on error. |
| `YAML.dump_file(file, obj)` | Dumps a Ruby object to a file as YAML. |
| `YAML.dump_file(file, obj, options)` | Dumps a Ruby object to a file as YAML with the specified options. |
| `YAML.add_domain_type` | Adds a domain type for YAML. |
| `YAML.add_domain_type(domain, type_id) { |val| ... }` | Adds a domain type for YAML. |
| `YAML.add_private_type` | Adds a private type for YAML. |
| `YAML.add_private_type(type_id) { |val| ... }` | Adds a private type for YAML. |
| `YAML.add_ruby_type` | Adds a Ruby type for YAML. |
| `YAML.add_ruby_type(type_id) { |val| ... }` | Adds a Ruby type for YAML. |
| `YAML.tag_class` | Tags a class for YAML. |
| `YAML.tag_class(class, tag)` | Tags a class for YAML with the specified tag. |
| `YAML::Store` | Provides methods for YAML document storage. |
| `YAML::Store.new` | Creates a new YAML store. |
| `YAML::Store.new(file)` | Creates a new YAML store with the specified file. |
| `YAML::Store#load` | Loads a YAML document from the store. |
| `YAML::Store#load(key)` | Loads a YAML document from the store with the specified key. |
| `YAML::Store#[]` | Loads a YAML document from the store. |
| `YAML::Store#[](key)` | Loads a YAML document from the store with the specified key. |
| `YAML::Store#save` | Saves a YAML document to the store. |
| `YAML::Store#save(key, obj)` | Saves a YAML document to the store with the specified key and object. |
| `YAML::Store#[]=` | Saves a YAML document to the store. |
| `YAML::Store#[](key)=obj` | Saves a YAML document to the store with the specified key and object. |
| `YAML::Store#transaction` | Begins a transaction. |
| `YAML::Store#transaction { ... }` | Begins a transaction and executes the block. |
| `YAML::Store#commit` | Commits the transaction. |
| `YAML::Store#abort` | Aborts the transaction. |
| `YAML::Store#loaded?` | Returns true if the store is loaded. |
| `YAML::Store#roots` | Returns an array of the root keys in the store. |

---
## CSV

| Code | Description |
|------|-------------|
| `require 'csv'` | Loads the CSV library. |
| `CSV` | Provides methods for CSV parsing and generation. |
| `CSV.parse(string)` | Parses a CSV string into an array of arrays. |
| `CSV.parse(string, options)` | Parses a CSV string into an array of arrays with the specified options. |
| `CSV.parse!(string)` | Parses a CSV string into an array of arrays and raises an exception on error. |
| `CSV.parse!(string, options)` | Parses a CSV string into an array of arrays with the specified options and raises an exception on error. |
| `CSV.generate(arr)` | Generates a CSV string from an array of arrays. |
| `CSV.generate(arr, options)` | Generates a CSV string from an array of arrays with the specified options. |
| `CSV.generate_line(arr)` | Generates a CSV line from an array. |
| `CSV.generate_line(arr, options)` | Generates a CSV line from an array with the specified options. |
| `CSV.parse_line(string)` | Parses a CSV line into an array. |
| `CSV.parse_line(string, options)` | Parses a CSV line into an array with the specified options. |
| `CSV.foreach(file)` | Iterates over each row in a CSV file. |
| `CSV.foreach(file) { |row| ... }` | Iterates over each row in a CSV file and passes each row to a block. |
| `CSV.foreach(file, options)` | Iterates over each row in a CSV file with the specified options. |
| `CSV.foreach(file, options) { |row| ... }` | Iterates over each row in a CSV file with the specified options and passes each row to a block. |
| `CSV.read(file)` | Reads a CSV file into an array of arrays. |
| `CSV.read(file, options)` | Reads a CSV file into an array of arrays with the specified options. |
| `CSV.open(file, mode)` | Opens a CSV file. |
| `CSV.open(file, mode) { |csv| ... }` | Opens a CSV file and passes the CSV object to a block. |
| `CSV.open(file, mode, options)` | Opens a CSV file with the specified options. |
| `CSV.open(file, mode, options) { |csv| ... }` | Opens a CSV file with the specified options and passes the CSV object to a block. |
| `CSV::Row` | Represents a row in a CSV file. |
| `CSV::Row.new(headers, fields)` | Creates a new CSV row. |
| `CSV::Row#[]` | Returns the field at the specified index. |
| `CSV::Row#[](index)` | Returns the field at the specified index. |
| `CSV::Row#[](header)` | Returns the field with the specified header. |
| `CSV::Row#[]=` | Sets the field at the specified index. |
| `CSV::Row#[](index)=value` | Sets the field at the specified index. |
| `CSV::Row#[](header)=value` | Sets the field with the specified header. |
| `CSV::Row#headers` | Returns the headers of the row. |
| `CSV::Row#fields` | Returns the fields of the row. |
| `CSV::Row#header?` | Returns true if the row has headers. |
| `CSV::Table` | Represents a table in a CSV file. |
| `CSV::Table.new(arr)` | Creates a new CSV table from an array of arrays. |
| `CSV::Table.new(arr, headers)` | Creates a new CSV table from an array of arrays with the specified headers. |
| `CSV::Table#[]` | Returns the row at the specified index. |
| `CSV::Table#[](index)` | Returns the row at the specified index. |
| `CSV::Table#headers` | Returns the headers of the table. |
| `CSV::Table#by_col` | Returns the column with the specified header. |
| `CSV::Table#by_col(header)` | Returns the column with the specified header. |
| `CSV::Table#by_col_or_row` | Returns the column or row with the specified header or index. |
| `CSV::Table#by_col_or_row(header_or_index)` | Returns the column or row with the specified header or index. |
| `CSV::Table#delete` | Deletes the column with the specified header. |
| `CSV::Table#delete(header)` | Deletes the column with the specified header. |
| `CSV::Table#each` | Iterates over each row in the table. |
| `CSV::Table#each { |row| ... }` | Iterates over each row in the table and passes each row to a block. |
| `CSV::Table#insert_column` | Inserts a column into the table. |
| `CSV::Table#insert_column(index, header, values)` | Inserts a column into the table at the specified index with the specified header and values. |
| `CSV::Table#delete_if` | Deletes rows that satisfy the condition. |
| `CSV::Table#delete_if { |row| ... }` | Deletes rows that satisfy the condition specified by the block. |
| `CSV::Table#keep_if` | Keeps rows that satisfy the condition. |
| `CSV::Table#keep_if { |row| ... }` | Keeps rows that satisfy the condition specified by the block. |
| `CSV::Writer` | Provides methods for writing CSV files. |
| `CSV::Writer.generate(csv)` | Generates a CSV writer. |
| `CSV::Writer.generate(csv, options)` | Generates a CSV writer with the specified options. |
| `CSV::Writer.generate(csv, options) { |writer| ... }` | Generates a CSV writer with the specified options and passes the writer to a block. |