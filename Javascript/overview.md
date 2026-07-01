Here is a **comprehensive list of JavaScript Standard Library (ECMAScript) built-in objects, methods, and properties**, organized by category. This covers the **ECMAScript standard** (not browser-specific APIs like DOM, Web APIs, or Node.js modules).

---

---

## **Global Objects and Functions**
*(Available in the global scope)*

### **Value Properties**
| Property | Description |
|----------|-------------|
| `Infinity` | Represents positive/negative infinity |
| `NaN` | Not-a-Number value |
| `undefined` | Primitive value representing undefined |
| `globalThis` | Global `this` value (ES2020) |

### **Function Properties**
| Function | Description |
|----------|-------------|
| `eval(x)` | Evaluates a string as JavaScript code |
| `parseInt(string, radix)` | Parses a string and returns an integer |
| `parseFloat(string)` | Parses a string and returns a floating-point number |
| `isNaN(value)` | Determines if a value is `NaN` |
| `isFinite(value)` | Determines if a value is a finite number |
| `decodeURI(encodedURI)` | Decodes a Uniform Resource Identifier (URI) |
| `decodeURIComponent(encodedURIComponent)` | Decodes a URI component |
| `encodeURI(uri)` | Encodes a URI |
| `encodeURIComponent(uriComponent)` | Encodes a URI component |

---

---
## **Fundamental Objects**

### **Object**
*(Base for all objects)*

| Method/Property | Description |
|-----------------|-------------|
| `Object()` | Constructor for creating objects |
| `Object.assign(target, ...sources)` | Copies properties from source objects to a target |
| `Object.create(proto, properties)` | Creates a new object with the specified prototype |
| `Object.defineProperty(obj, prop, descriptor)` | Defines a new property on an object |
| `Object.defineProperties(obj, props)` | Defines new properties on an object |
| `Object.entries(obj)` | Returns an array of key-value pairs |
| `Object.freeze(obj)` | Freezes an object (prevents modification) |
| `Object.fromEntries(iterable)` | Creates an object from key-value pairs |
| `Object.getOwnPropertyDescriptor(obj, prop)` | Returns a property descriptor |
| `Object.getOwnPropertyDescriptors(obj)` | Returns all property descriptors |
| `Object.getOwnPropertyNames(obj)` | Returns an array of all property names |
| `Object.getOwnPropertySymbols(obj)` | Returns an array of own symbol properties |
| `Object.getPrototypeOf(obj)` | Returns the prototype of an object |
| `Object.hasOwn(obj, prop)` | Returns true if property is an own property |
| `Object.is(value1, value2)` | Compares if two values are the same |
| `Object.isExtensible(obj)` | Determines if an object is extensible |
| `Object.isFrozen(obj)` | Determines if an object is frozen |
| `Object.isSealed(obj)` | Determines if an object is sealed |
| `Object.keys(obj)` | Returns an array of enumerable property names |
| `Object.preventExtensions(obj)` | Prevents new properties from being added |
| `Object.seal(obj)` | Seals an object (prevents new properties) |
| `Object.setPrototypeOf(obj, prototype)` | Sets the prototype of an object |
| `Object.values(obj)` | Returns an array of enumerable property values |
| **Properties** | |
| `Object.prototype` | Prototype for all objects |
| `Object.prototype.__proto__` | Reference to the prototype |
| `Object.prototype.constructor` | Returns the constructor function |
| `Object.prototype.hasOwnProperty(prop)` | Checks if an object has a property |
| `Object.prototype.isPrototypeOf(obj)` | Checks if an object is in the prototype chain |
| `Object.prototype.propertyIsEnumerable(prop)` | Checks if a property is enumerable |
| `Object.prototype.toLocaleString()` | Returns a localized string |
| `Object.prototype.toString()` | Returns a string representation |
| `Object.prototype.valueOf()` | Returns the primitive value of an object |

---

### **Function**
*(Constructor for functions)*

| Method/Property | Description |
|-----------------|-------------|
| `Function()` | Constructor for creating functions |
| **Instance Methods** | |
| `function.apply(thisArg, argsArray)` | Calls a function with a given `this` value and arguments as an array |
| `function.bind(thisArg, ...args)` | Creates a new function with a bound `this` and arguments |
| `function.call(thisArg, ...args)` | Calls a function with a given `this` value and arguments |
| `function.toString()` | Returns the source code of the function |
| **Properties** | |
| `Function.prototype` | Prototype for all functions |
| `Function.prototype.constructor` | Returns the constructor function |
| `Function.length` | Number of arguments expected by the function |
| `Function.name` | Name of the function |

---

### **Boolean**
*(Primitive boolean value wrapper)*

| Method/Property | Description |
|-----------------|-------------|
| `Boolean()` | Constructor for boolean values |
| `Boolean.prototype` | Prototype for boolean objects |
| `Boolean.prototype.constructor` | Returns the constructor function |
| `Boolean.prototype.toString()` | Returns a string representation |
| `Boolean.prototype.valueOf()` | Returns the primitive value |

---

### **Symbol**
*(Primitive symbol value)*

| Method/Property | Description |
|-----------------|-------------|
| `Symbol()` | Constructor for symbols |
| `Symbol.for(key)` | Returns a symbol from the global symbol registry |
| `Symbol.keyFor(sym)` | Returns the key for a symbol from the global registry |
| **Well-Known Symbols** | |
| `Symbol.asyncIterator` | Method to get the async iterator |
| `Symbol.hasInstance` | Method to determine if a constructor recognizes an object |
| `Symbol.isConcatSpreadable` | Boolean indicating if an object should be flattened |
| `Symbol.iterator` | Method to get the iterator |
| `Symbol.match` | Method used for string matching |
| `Symbol.matchAll` | Method to return all matches |
| `Symbol.replace` | Method used for string replacement |
| `Symbol.search` | Method used for string searching |
| `Symbol.species` | Constructor function for creating derived objects |
| `Symbol.split` | Method used for string splitting |
| `Symbol.toPrimitive` | Method to convert an object to a primitive |
| `Symbol.toStringTag` | String tag for an object |
| `Symbol.unscopables` | Object whose properties are excluded from `with` bindings |
| **Instance Methods** | |
| `symbol.description` | Returns the description of the symbol |
| `symbol.toString()` | Returns a string representation |
| `symbol.valueOf()` | Returns the primitive value |

---

### **Error**
*(Base for all error types)*

| Error Type | Description |
|------------|-------------|
| `Error` | Base error type |
| `AggregateError` (ES2021) | Error for multiple errors wrapped in one |
| `EvalError` | Error related to the `eval` function |
| `RangeError` | Error for invalid range |
| `ReferenceError` | Error for invalid reference |
| `SyntaxError` | Error for syntax errors |
| `TypeError` | Error for invalid type |
| `URIError` | Error related to URI handling |

| Method/Property | Description |
|-----------------|-------------|
| `Error.prototype` | Prototype for error objects |
| `Error.prototype.constructor` | Returns the constructor function |
| `Error.prototype.message` | Error message |
| `Error.prototype.name` | Error name |
| `Error.prototype.stack` | Stack trace |
| `Error.prototype.toString()` | Returns a string representation |

---

---
## **Numbers and Dates**

### **Number**
*(Primitive number value wrapper)*

| Method/Property | Description |
|-----------------|-------------|
| `Number()` | Constructor for numbers |
| `Number.EPSILON` | Smallest interval between representable numbers |
| `Number.MAX_SAFE_INTEGER` | Maximum safe integer |
| `Number.MAX_VALUE` | Maximum representable number |
| `Number.MIN_SAFE_INTEGER` | Minimum safe integer |
| `Number.MIN_VALUE` | Smallest positive representable number |
| `Number.NaN` | Not-a-Number |
| `Number.NEGATIVE_INFINITY` | Negative infinity |
| `Number.POSITIVE_INFINITY` | Positive infinity |
| `Number.isFinite(value)` | Checks if a value is a finite number |
| `Number.isInteger(value)` | Checks if a value is an integer |
| `Number.isNaN(value)` | Checks if a value is `NaN` |
| `Number.isSafeInteger(value)` | Checks if a value is a safe integer |
| `Number.parseFloat(string)` | Parses a string into a floating-point number |
| `Number.parseInt(string, radix)` | Parses a string into an integer |
| **Instance Methods** | |
| `number.toExponential(fractionDigits)` | Returns a string in exponential notation |
| `number.toFixed(digits)` | Returns a string in fixed-point notation |
| `number.toLocaleString(locales, options)` | Returns a localized string |
| `number.toPrecision(precision)` | Returns a string with specified precision |
| `number.toString(radix)` | Returns a string representation |
| `number.valueOf()` | Returns the primitive value |

---

### **BigInt**
*(Arbitrary-precision integers, ES2020)*

| Method/Property | Description |
|-----------------|-------------|
| `BigInt()` | Constructor for BigInt values |
| `BigInt.asIntN(bits, bigint)` | Returns a BigInt truncated to `bits` bits |
| `BigInt.asUintN(bits, bigint)` | Returns a BigInt truncated to `bits` unsigned bits |
| **Instance Methods** | |
| `bigint.toLocaleString()` | Returns a localized string |
| `bigint.toString(radix)` | Returns a string representation |
| `bigint.valueOf()` | Returns the primitive value |

---

### **Math**
*(Mathematical functions and constants)*

| Property/Method | Description |
|-----------------|-------------|
| `Math.E` | Euler's constant (~2.718) |
| `Math.LN10` | Natural log of 10 (~2.302) |
| `Math.LN2` | Natural log of 2 (~0.693) |
| `Math.LOG10E` | Base-10 log of E (~0.434) |
| `Math.LOG2E` | Base-2 log of E (~1.442) |
| `Math.PI` | Pi (~3.14159) |
| `Math.SQRT1_2` | Square root of 0.5 (~0.707) |
| `Math.SQRT2` | Square root of 2 (~1.414) |
| `Math.abs(x)` | Absolute value |
| `Math.acos(x)` | Arccosine |
| `Math.acosh(x)` | Hyperbolic arccosine |
| `Math.asin(x)` | Arcsine |
| `Math.asinh(x)` | Hyperbolic arcsine |
| `Math.atan(x)` | Arctangent |
| `Math.atan2(y, x)` | Arctangent of quotient of arguments |
| `Math.atanh(x)` | Hyperbolic arctangent |
| `Math.cbrt(x)` | Cube root |
| `Math.ceil(x)` | Round up to the nearest integer |
| `Math.clz32(x)` | Count leading zeros in 32-bit integer |
| `Math.cos(x)` | Cosine |
| `Math.cosh(x)` | Hyperbolic cosine |
| `Math.exp(x)` | Exponential function |
| `Math.expm1(x)` | Exponential minus 1 |
| `Math.floor(x)` | Round down to the nearest integer |
| `Math.fround(x)` | Round to nearest 32-bit float |
| `Math.hypot(x, ...values)` | Square root of sum of squares |
| `Math.imul(x, y)` | 32-bit integer multiplication |
| `Math.log(x)` | Natural logarithm |
| `Math.log10(x)` | Base-10 logarithm |
| `Math.log1p(x)` | Natural log of 1 + x |
| `Math.log2(x)` | Base-2 logarithm |
| `Math.max(value1, ...values)` | Maximum of values |
| `Math.min(value1, ...values)` | Minimum of values |
| `Math.pow(x, y)` | Power function |
| `Math.random()` | Random number between 0 and 1 |
| `Math.round(x)` | Round to the nearest integer |
| `Math.sign(x)` | Sign of a number |
| `Math.sin(x)` | Sine |
| `Math.sinh(x)` | Hyperbolic sine |
| `Math.sqrt(x)` | Square root |
| `Math.tan(x)` | Tangent |
| `Math.tanh(x)` | Hyperbolic tangent |
| `Math.trunc(x)` | Truncate to integer |

---

### **Date**
*(Date and time handling)*

| Method/Property | Description |
|-----------------|-------------|
| `Date()` | Constructor for date objects |
| `Date.parse(dateString)` | Parses a date string and returns milliseconds since epoch |
| `Date.UTC(year, month, ...)` | Returns milliseconds since epoch for UTC date |
| `Date.now()` | Returns current timestamp in milliseconds |
| **Instance Methods** | |
| `date.getDate()` | Day of the month (1-31) |
| `date.getDay()` | Day of the week (0-6) |
| `date.getFullYear()` | Year (4 digits) |
| `date.getHours()` | Hours (0-23) |
| `date.getMilliseconds()` | Milliseconds (0-999) |
| `date.getMinutes()` | Minutes (0-59) |
| `date.getMonth()` | Month (0-11) |
| `date.getSeconds()` | Seconds (0-59) |
| `date.getTime()` | Milliseconds since epoch |
| `date.getTimezoneOffset()` | Timezone offset in minutes |
| `date.getUTCDate()` | UTC day of the month |
| `date.getUTCDay()` | UTC day of the week |
| `date.getUTCFullYear()` | UTC year |
| `date.getUTCHours()` | UTC hours |
| `date.getUTCMilliseconds()` | UTC milliseconds |
| `date.getUTCMinutes()` | UTC minutes |
| `date.getUTCMonth()` | UTC month |
| `date.getUTCSeconds()` | UTC seconds |
| `date.setDate(day)` | Set day of the month |
| `date.setFullYear(year, month, day)` | Set year, month, and day |
| `date.setHours(hours, min, sec, ms)` | Set hours, minutes, seconds, milliseconds |
| `date.setMilliseconds(ms)` | Set milliseconds |
| `date.setMinutes(min, sec, ms)` | Set minutes, seconds, milliseconds |
| `date.setMonth(month, day)` | Set month and day |
| `date.setSeconds(sec, ms)` | Set seconds and milliseconds |
| `date.setTime(time)` | Set time in milliseconds since epoch |
| `date.setUTCDate(day)` | Set UTC day of the month |
| `date.setUTCFullYear(year, month, day)` | Set UTC year, month, and day |
| `date.setUTCHours(hours, min, sec, ms)` | Set UTC hours, minutes, seconds, milliseconds |
| `date.setUTCMilliseconds(ms)` | Set UTC milliseconds |
| `date.setUTCMinutes(min, sec, ms)` | Set UTC minutes, seconds, milliseconds |
| `date.setUTCMonth(month, day)` | Set UTC month and day |
| `date.setUTCSeconds(sec, ms)` | Set UTC seconds and milliseconds |
| `date.toDateString()` | Human-readable date string |
| `date.toISOString()` | ISO 8601 date string |
| `date.toJSON()` | JSON-formatted date string |
| `date.toLocaleDateString()` | Localized date string |
| `date.toLocaleString()` | Localized date-time string |
| `date.toLocaleTimeString()` | Localized time string |
| `date.toString()` | Human-readable string |
| `date.toTimeString()` | Human-readable time string |
| `date.toUTCString()` | UTC date string |
| `date.valueOf()` | Primitive value (milliseconds since epoch) |

---

---
## **Text Processing**

### **String**
*(Primitive string value wrapper)*

| Method/Property | Description |
|-----------------|-------------|
| `String()` | Constructor for strings |
| `String.fromCharCode(code1, ...)` | Returns a string from character codes |
| `String.fromCodePoint(codePoint1, ...)` | Returns a string from Unicode code points |
| `String.raw(template, ...substitutions)` | Returns the raw string form of template literals |
| **Instance Methods** | |
| `string.at(index)` (ES2022) | Returns the character at the specified index |
| `string.charAt(index)` | Returns the character at the specified index |
| `string.charCodeAt(index)` | Returns the Unicode value at the specified index |
| `string.codePointAt(index)` | Returns the Unicode code point at the specified index |
| `string.concat(str1, ...)` | Concatenates strings |
| `string.endsWith(searchString, length)` | Checks if a string ends with another string |
| `string.includes(searchString, start)` | Checks if a string contains another string |
| `string.indexOf(searchValue, fromIndex)` | Returns the first index of a substring |
| `string.lastIndexOf(searchValue, fromIndex)` | Returns the last index of a substring |
| `string.localeCompare(compareString, locales, options)` | Compares two strings in the current locale |
| `string.match(regexp)` | Matches a string against a regular expression |
| `string.matchAll(regexp)` (ES2020) | Returns all matches of a regular expression |
| `string.normalize(form)` | Returns the Unicode normalization form |
| `string.padEnd(targetLength, padString)` | Pads the end of a string |
| `string.padStart(targetLength, padString)` | Pads the start of a string |
| `string.repeat(count)` | Returns a string repeated `count` times |
| `string.replace(searchValue, replaceValue)` | Replaces occurrences of a substring |
| `string.replaceAll(searchValue, replaceValue)` (ES2021) | Replaces all occurrences of a substring |
| `string.search(regexp)` | Returns the index of the first match |
| `string.slice(start, end)` | Extracts a section of a string |
| `string.split(separator, limit)` | Splits a string into an array of substrings |
| `string.startsWith(searchString, start)` | Checks if a string starts with another string |
| `string.substring(start, end)` | Returns a substring |
| `string.toLocaleLowerCase(locales)` | Returns a string converted to lowercase according to locale |
| `string.toLocaleUpperCase(locales)` | Returns a string converted to uppercase according to locale |
| `string.toLowerCase()` | Returns a string converted to lowercase |
| `string.toString()` | Returns the string itself |
| `string.toUpperCase()` | Returns a string converted to uppercase |
| `string.trim()` | Removes whitespace from both ends |
| `string.trimEnd()` (ES2019) | Removes whitespace from the end |
| `string.trimStart()` (ES2019) | Removes whitespace from the start |
| `string.valueOf()` | Returns the primitive value |
| **Properties** | |
| `string.length` | Length of the string |

---

### **RegExp**
*(Regular expressions)*

| Method/Property | Description |
|-----------------|-------------|
| `RegExp()` | Constructor for regular expressions |
| **Instance Properties** | |
| `regexp.dotAll` | Whether `.` matches newline characters |
| `regexp.flags` | String containing the flags |
| `regexp.global` | Whether to test the regular expression against all possible matches |
| `regexp.ignoreCase` | Whether to ignore case |
| `regexp.multiline` | Whether to match across multiple lines |
| `regexp.source` | Text of the regular expression |
| `regexp.sticky` | Whether matching is sticky |
| `regexp.unicode` | Whether to use Unicode matching |
| **Instance Methods** | |
| `regexp.exec(string)` | Executes a search for a match in a string |
| `regexp.test(string)` | Tests for a match in a string |
| `regexp.toString()` | Returns a string representation |
| **Static Properties** | |
| `RegExp.$1-$9` | Parenthesized substring matches |
| `RegExp.input` | The string against which a regular expression is tested |
| `RegExp.lastMatch` | The last matched characters |
| `RegExp.lastParen` | The last parenthesized substring match |
| `RegExp.leftContext` | The substring preceding the most recent match |
| `RegExp.rightContext` | The substring following the most recent match |

---

---
## **Indexed Collections**

### **Array**
*(Ordered list of values)*

| Method/Property | Description |
|-----------------|-------------|
| `Array()` | Constructor for arrays |
| `Array.from(arrayLike, mapFn, thisArg)` | Creates a new array from an array-like or iterable object |
| `Array.isArray(obj)` | Determines if a value is an array |
| `Array.of(element0, element1, ...)` | Creates a new array with the given elements |
| **Instance Methods** | |
| `array.at(index)` (ES2022) | Returns the element at the specified index |
| `array.concat(value1, ...)` | Merges arrays |
| `array.copyWithin(target, start, end)` | Copies array elements within the array |
| `array.entries()` | Returns an iterator of key-value pairs |
| `array.every(callback, thisArg)` | Tests if all elements pass a test |
| `array.fill(value, start, end)` | Fills all elements with a value |
| `array.filter(callback, thisArg)` | Returns a new array with elements that pass a test |
| `array.find(callback, thisArg)` | Returns the first element that satisfies a condition |
| `array.findIndex(callback, thisArg)` | Returns the first index that satisfies a condition |
| `array.findLast(callback, thisArg)` (ES2023) | Returns the last element that satisfies a condition |
| `array.findLastIndex(callback, thisArg)` (ES2023) | Returns the last index that satisfies a condition |
| `array.flat(depth)` | Flattens nested arrays |
| `array.flatMap(callback, thisArg)` | Maps and flattens the array |
| `array.forEach(callback, thisArg)` | Executes a function for each element |
| `array.includes(searchElement, fromIndex)` | Checks if an array includes a value |
| `array.indexOf(searchElement, fromIndex)` | Returns the first index of an element |
| `array.join(separator)` | Joins all elements into a string |
| `array.keys()` | Returns an iterator of keys |
| `array.lastIndexOf(searchElement, fromIndex)` | Returns the last index of an element |
| `array.map(callback, thisArg)` | Maps each element to a new value |
| `array.pop()` | Removes and returns the last element |
| `array.push(element1, ...)` | Adds elements to the end and returns the new length |
| `array.reduce(callback, initialValue)` | Reduces the array to a single value |
| `array.reduceRight(callback, initialValue)` | Reduces the array from right to left |
| `array.reverse()` | Reverses the array in place |
| `array.shift()` | Removes and returns the first element |
| `array.slice(start, end)` | Returns a shallow copy of a portion |
| `array.some(callback, thisArg)` | Tests if any element passes a test |
| `array.sort(compareFn)` | Sorts the array in place |
| `array.splice(start, deleteCount, ...items)` | Adds/removes elements |
| `array.toLocaleString(locales, options)` | Returns a localized string |
| `array.toString()` | Returns a string representation |
| `array.unshift(element1, ...)` | Adds elements to the beginning and returns the new length |
| `array.values()` | Returns an iterator of values |
| `array.with(index, value)` (ES2023) | Returns a new array with the element at index replaced |
| **Properties** | |
| `array.length` | Number of elements in the array |

---

### **Typed Arrays**
*(Array-like views over binary data)*

| Type | Description |
|------|-------------|
| `Int8Array` | 8-bit signed integer |
| `Uint8Array` | 8-bit unsigned integer |
| `Uint8ClampedArray` | 8-bit unsigned integer (clamped) |
| `Int16Array` | 16-bit signed integer |
| `Uint16Array` | 16-bit unsigned integer |
| `Int32Array` | 32-bit signed integer |
| `Uint32Array` | 32-bit unsigned integer |
| `Float32Array` | 32-bit floating point |
| `Float64Array` | 64-bit floating point |
| `BigInt64Array` | 64-bit signed big integer |
| `BigUint64Array` | 64-bit unsigned big integer |

| Method/Property | Description |
|-----------------|-------------|
| `TypedArray()` | Constructor for typed arrays |
| `TypedArray.from(arrayLike, mapFn, thisArg)` | Creates a new typed array from an array-like or iterable object |
| `TypedArray.of(element0, element1, ...)` | Creates a new typed array with the given elements |
| **Instance Methods** | |
| `typedArray.at(index)` (ES2022) | Returns the element at the specified index |
| `typedArray.buffer` | Returns the `ArrayBuffer` referenced by the typed array |
| `typedArray.byteLength` | Returns the length in bytes of the typed array |
| `typedArray.byteOffset` | Returns the offset in bytes from the start of the `ArrayBuffer` |
| `typedArray.copyWithin(target, start, end)` | Copies elements within the typed array |
| `typedArray.entries()` | Returns an iterator of key-value pairs |
| `typedArray.every(callback, thisArg)` | Tests if all elements pass a test |
| `typedArray.fill(value, start, end)` | Fills all elements with a value |
| `typedArray.filter(callback, thisArg)` | Returns a new typed array with elements that pass a test |
| `typedArray.find(callback, thisArg)` | Returns the first element that satisfies a condition |
| `typedArray.findIndex(callback, thisArg)` | Returns the first index that satisfies a condition |
| `typedArray.forEach(callback, thisArg)` | Executes a function for each element |
| `typedArray.includes(searchElement, fromIndex)` | Checks if a typed array includes a value |
| `typedArray.indexOf(searchElement, fromIndex)` | Returns the first index of an element |
| `typedArray.join(separator)` | Joins all elements into a string |
| `typedArray.keys()` | Returns an iterator of keys |
| `typedArray.lastIndexOf(searchElement, fromIndex)` | Returns the last index of an element |
| `typedArray.length` | Returns the number of elements |
| `typedArray.map(callback, thisArg)` | Maps each element to a new value |
| `typedArray.reduce(callback, initialValue)` | Reduces the typed array to a single value |
| `typedArray.reduceRight(callback, initialValue)` | Reduces the typed array from right to left |
| `typedArray.reverse()` | Reverses the typed array in place |
| `typedArray.set(array, offset)` | Stores multiple values in the typed array |
| `typedArray.slice(start, end)` | Returns a shallow copy of a portion |
| `typedArray.some(callback, thisArg)` | Tests if any element passes a test |
| `typedArray.sort(compareFn)` | Sorts the typed array in place |
| `typedArray.subarray(begin, end)` | Returns a new typed array from a portion |
| `typedArray.values()` | Returns an iterator of values |
| `typedArray.with(index, value)` (ES2023) | Returns a new typed array with the element at index replaced |
| **Static Methods** | |
| `TypedArray.BYTES_PER_ELEMENT` | Returns the number of bytes per element |

---

---
## **Keyed Collections**

### **Map**
*(Key-value pairs with any value as key)*

| Method/Property | Description |
|-----------------|-------------|
| `Map()` | Constructor for maps |
| `Map.groupBy(items, callback)` (ES2024) | Groups items by a callback |
| **Instance Methods** | |
| `map.clear()` | Removes all key-value pairs |
| `map.delete(key)` | Removes a key-value pair |
| `map.entries()` | Returns an iterator of key-value pairs |
| `map.forEach(callback, thisArg)` | Executes a function for each key-value pair |
| `map.get(key)` | Returns the value for a key |
| `map.has(key)` | Checks if a key exists |
| `map.keys()` | Returns an iterator of keys |
| `map.set(key, value)` | Adds or updates a key-value pair |
| `map.values()` | Returns an iterator of values |
| **Properties** | |
| `map.size` | Number of key-value pairs |

---

### **Set**
*(Unique values)*

| Method/Property | Description |
|-----------------|-------------|
| `Set()` | Constructor for sets |
| **Instance Methods** | |
| `set.add(value)` | Adds a value to the set |
| `set.clear()` | Removes all values |
| `set.delete(value)` | Removes a value |
| `set.entries()` | Returns an iterator of key-value pairs |
| `set.forEach(callback, thisArg)` | Executes a function for each value |
| `set.has(value)` | Checks if a value exists |
| `set.keys()` | Returns an iterator of values |
| `set.values()` | Returns an iterator of values |
| **Properties** | |
| `set.size` | Number of values |

---
### **WeakMap**
*(Weak key-value pairs)*

| Method/Property | Description |
|-----------------|-------------|
| `WeakMap()` | Constructor for weak maps |
| **Instance Methods** | |
| `weakMap.delete(key)` | Removes a key-value pair |
| `weakMap.get(key)` | Returns the value for a key |
| `weakMap.has(key)` | Checks if a key exists |
| `weakMap.set(key, value)` | Adds or updates a key-value pair |

---
### **WeakSet**
*(Weak set of objects)*

| Method/Property | Description |
|-----------------|-------------|
| `WeakSet()` | Constructor for weak sets |
| **Instance Methods** | |
| `weakSet.add(value)` | Adds a value to the weak set |
| `weakSet.delete(value)` | Removes a value |
| `weakSet.has(value)` | Checks if a value exists |

---
---
## **Structured Data**

### **ArrayBuffer**
*(Raw binary data buffer)*

| Method/Property | Description |
|-----------------|-------------|
| `ArrayBuffer()` | Constructor for array buffers |
| `ArrayBuffer.isView(obj)` | Checks if an object is a typed array view |
| **Instance Methods** | |
| `arrayBuffer.slice(begin, end)` | Returns a new `ArrayBuffer` from a portion |
| **Properties** | |
| `arrayBuffer.byteLength` | Length in bytes |

---
### **SharedArrayBuffer**
*(Shared memory buffer, ES2017)*

| Method/Property | Description |
|-----------------|-------------|
| `SharedArrayBuffer()` | Constructor for shared array buffers |
| **Instance Properties** | |
| `sharedArrayBuffer.byteLength` | Length in bytes |

---
### **DataView**
*(View over an `ArrayBuffer` with custom byte alignment)*

| Method/Property | Description |
|-----------------|-------------|
| `DataView()` | Constructor for data views |
| **Instance Methods** | |
| `dataView.buffer` | Returns the `ArrayBuffer` referenced by the view |
| `dataView.byteLength` | Returns the length in bytes of the view |
| `dataView.byteOffset` | Returns the offset in bytes from the start of the `ArrayBuffer` |
| `dataView.getInt8(byteOffset)` | Gets an 8-bit signed integer |
| `dataView.getUint8(byteOffset)` | Gets an 8-bit unsigned integer |
| `dataView.getInt16(byteOffset, littleEndian)` | Gets a 16-bit signed integer |
| `dataView.getUint16(byteOffset, littleEndian)` | Gets a 16-bit unsigned integer |
| `dataView.getInt32(byteOffset, littleEndian)` | Gets a 32-bit signed integer |
| `dataView.getUint32(byteOffset, littleEndian)` | Gets a 32-bit unsigned integer |
| `dataView.getFloat32(byteOffset, littleEndian)` | Gets a 32-bit floating point |
| `dataView.getFloat64(byteOffset, littleEndian)` | Gets a 64-bit floating point |
| `dataView.getBigInt64(byteOffset, littleEndian)` | Gets a 64-bit signed big integer |
| `dataView.getBigUint64(byteOffset, littleEndian)` | Gets a 64-bit unsigned big integer |
| `dataView.setInt8(byteOffset, value)` | Sets an 8-bit signed integer |
| `dataView.setUint8(byteOffset, value)` | Sets an 8-bit unsigned integer |
| `dataView.setInt16(byteOffset, value, littleEndian)` | Sets a 16-bit signed integer |
| `dataView.setUint16(byteOffset, value, littleEndian)` | Sets a 16-bit unsigned integer |
| `dataView.setInt32(byteOffset, value, littleEndian)` | Sets a 32-bit signed integer |
| `dataView.setUint32(byteOffset, value, littleEndian)` | Sets a 32-bit unsigned integer |
| `dataView.setFloat32(byteOffset, value, littleEndian)` | Sets a 32-bit floating point |
| `dataView.setFloat64(byteOffset, value, littleEndian)` | Sets a 64-bit floating point |
| `dataView.setBigInt64(byteOffset, value, littleEndian)` | Sets a 64-bit signed big integer |
| `dataView.setBigUint64(byteOffset, value, littleEndian)` | Sets a 64-bit unsigned big integer |

---
### **Atomics**
*(Atomic operations for shared memory, ES2017)*

| Method/Property | Description |
|-----------------|-------------|
| `Atomics.add(typedArray, index, value)` | Atomically adds a value to the element at the specified position |
| `Atomics.and(typedArray, index, value)` | Atomically performs a bitwise AND |
| `Atomics.compareExchange(typedArray, index, expectedValue, replacementValue)` | Atomically compares and exchanges values |
| `Atomics.exchange(typedArray, index, value)` | Atomically exchanges a value |
| `Atomics.isLockFree(size)` | Determines if the specified size is lock-free |
| `Atomics.load(typedArray, index)` | Atomically loads a value |
| `Atomics.notEqual(typedArray, index, expectedValue)` | Atomically checks if the value is not equal |
| `Atomics.notEqual(typedArray, index, expectedValue)` | Atomically checks if the value is not equal |
| `Atomics.or(typedArray, index, value)` | Atomically performs a bitwise OR |
| `Atomics.store(typedArray, index, value)` | Atomically stores a value |
| `Atomics.sub(typedArray, index, value)` | Atomically subtracts a value |
| `Atomics.wait(typedArray, index, value, timeout)` | Waits on a condition |
| `Atomics.wake(typedArray, index, count)` | Wakes up sleeping agents |
| `Atomics.xor(typedArray, index, value)` | Atomically performs a bitwise XOR |

---
### **JSON**
*(JavaScript Object Notation parsing and serialization)*

| Method | Description |
|--------|-------------|
| `JSON.parse(text, reviver)` | Parses a JSON string into a JavaScript value |
| `JSON.stringify(value, replacer, space)` | Converts a JavaScript value to a JSON string |

---
---
## **Control Abstraction Objects**

### **Promise**
*(Asynchronous operations)*

| Method/Property | Description |
|-----------------|-------------|
| `Promise()` | Constructor for promises |
| `Promise.all(iterable)` | Returns a promise that resolves when all promises resolve |
| `Promise.allSettled(iterable)` (ES2020) | Returns a promise that resolves after all promises settle |
| `Promise.any(iterable)` (ES2021) | Returns a promise that resolves when any promise resolves |
| `Promise.race(iterable)` | Returns a promise that resolves or rejects as soon as one promise resolves or rejects |
| `Promise.reject(reason)` | Returns a new rejected promise |
| `Promise.resolve(value)` | Returns a new resolved promise |
| **Instance Methods** | |
| `promise.catch(onRejected)` | Appends a rejection handler |
| `promise.finally(onFinally)` (ES2018) | Appends a handler for when the promise settles |
| `promise.then(onFulfilled, onRejected)` | Appends fulfillment and rejection handlers |

---
### **Generator**
*(Generator functions)*

| Method/Property | Description |
|-----------------|-------------|
| `Generator()` | Constructor for generator objects |
| **Instance Methods** | |
| `generator.next(value)` | Returns the next value from the generator |
| `generator.return(value)` | Returns the given value and finishes the generator |
| `generator.throw(exception)` | Throws an exception into the generator |
| **Properties** | |
| `Generator.prototype` | Prototype for generator objects |
| `Generator.prototype.constructor` | Returns the constructor function |

---
### **GeneratorFunction**
*(Generator function constructor)*

| Method/Property | Description |
|-----------------|-------------|
| `GeneratorFunction()` | Constructor for generator functions |
| **Properties** | |
| `GeneratorFunction.prototype` | Prototype for generator function objects |

---
### **AsyncFunction**
*(Async function constructor, ES2017)*

| Method/Property | Description |
|-----------------|-------------|
| `AsyncFunction()` | Constructor for async functions |

---
### **AsyncGenerator**
*(Async generator objects, ES2018)*

| Method/Property | Description |
|-----------------|-------------|
| `AsyncGenerator()` | Constructor for async generator objects |
| **Instance Methods** | |
| `asyncGenerator.next(value)` | Returns the next value from the async generator |
| `asyncGenerator.return(value)` | Returns the given value and finishes the async generator |
| `asyncGenerator.throw(exception)` | Throws an exception into the async generator |

---
### **AsyncGeneratorFunction**
*(Async generator function constructor, ES2018)*

| Method/Property | Description |
|-----------------|-------------|
| `AsyncGeneratorFunction()` | Constructor for async generator functions |

---
### **Reflect**
*(Reflection API, ES2015)*

| Method | Description |
|--------|-------------|
| `Reflect.apply(target, thisArgument, argumentsList)` | Calls a target function with arguments |
| `Reflect.construct(target, argumentsList, newTarget)` | Equivalent to the `new` operator |
| `Reflect.defineProperty(target, propertyKey, attributes)` | Defines a property on an object |
| `Reflect.deleteProperty(target, propertyKey)` | Deletes a property from an object |
| `Reflect.get(target, propertyKey, receiver)` | Gets a property value |
| `Reflect.getOwnPropertyDescriptor(target, propertyKey)` | Gets a property descriptor |
| `Reflect.getPrototypeOf(target)` | Gets the prototype of an object |
| `Reflect.has(target, propertyKey)` | Checks if an object has a property |
| `Reflect.isExtensible(target)` | Checks if an object is extensible |
| `Reflect.ownKeys(target)` | Returns an array of own property keys |
| `Reflect.preventExtensions(target)` | Prevents new properties from being added |
| `Reflect.set(target, propertyKey, value, receiver)` | Sets a property value |
| `Reflect.setPrototypeOf(target, prototype)` | Sets the prototype of an object |

---
### **Proxy**
*(Proxy objects, ES2015)*

| Method/Property | Description |
|-----------------|-------------|
| `Proxy()` | Constructor for proxy objects |
| **Static Methods** | |
| `Proxy.revocable(target, handler)` | Creates a revocable proxy |
| **Handler Methods** | |
| `handler.apply(target, thisArg, argumentsList)` | Intercepts function calls |
| `handler.construct(target, argumentsList, newTarget)` | Intercepts `new` operator |
| `handler.defineProperty(target, propertyKey, descriptor)` | Intercepts property definition |
| `handler.deleteProperty(target, propertyKey)` | Intercepts property deletion |
| `handler.get(target, propertyKey, receiver)` | Intercepts property reading |
| `handler.getOwnPropertyDescriptor(target, propertyKey)` | Intercepts property descriptor retrieval |
| `handler.getPrototypeOf(target)` | Intercepts prototype retrieval |
| `handler.has(target, propertyKey)` | Intercepts `in` operator |
| `handler.isExtensible(target)` | Intercepts extensibility check |
| `handler.ownKeys(target)` | Intercepts property enumeration |
| `handler.preventExtensions(target)` | Intercepts extensibility prevention |
| `handler.set(target, propertyKey, value, receiver)` | Intercepts property setting |
| `handler.setPrototypeOf(target, prototype)` | Intercepts prototype setting |

---
---
## **Internationalization (Intl)**
*(ECMAScript Internationalization API, ES2015+)*

### **Intl**
*(Namespace for Internationalization constructors)*

| Property | Description |
|----------|-------------|
| `Intl.Collator` | Constructor for collators |
| `Intl.DateTimeFormat` | Constructor for date/time formatters |
| `Intl.DisplayNames` (ES2020) | Constructor for display names |
| `Intl.ListFormat` (ES2020) | Constructor for list formatters |
| `Intl.Locale` (ES2021) | Constructor for locale objects |
| `Intl.NumberFormat` | Constructor for number formatters |
| `Intl.PluralRules` (ES2018) | Constructor for plural rules |
| `Intl.RelativeTimeFormat` (ES2020) | Constructor for relative time formatters |
| `Intl.Segmenter` (ES2022) | Constructor for segmenters |

---
### **Intl.Collator**
*(String comparison)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.Collator()` | Constructor for collators |
| **Instance Methods** | |
| `collator.compare(string1, string2)` | Compares two strings |
| `collator.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.Collator.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.DateTimeFormat**
*(Date and time formatting)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.DateTimeFormat()` | Constructor for date/time formatters |
| **Instance Methods** | |
| `dateTimeFormat.format(date)` | Formats a date |
| `dateTimeFormat.formatRange(date1, date2)` (ES2021) | Formats a date range |
| `dateTimeFormat.formatToParts(date)` (ES2017) | Returns an array of objects representing parts of the formatted date |
| `dateTimeFormat.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.DateTimeFormat.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.DisplayNames** (ES2020)
*(Localized display names)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.DisplayNames()` | Constructor for display names |
| **Instance Methods** | |
| `displayNames.of(code)` | Returns the display name for a code |
| `displayNames.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.DisplayNames.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.ListFormat** (ES2020)
*(List formatting)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.ListFormat()` | Constructor for list formatters |
| **Instance Methods** | |
| `listFormat.format(list)` | Formats a list |
| `listFormat.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.ListFormat.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.Locale** (ES2021)
*(Locale identification and negotiation)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.Locale()` | Constructor for locale objects |
| **Static Methods** | |
| `Intl.Locale.canonicalize(locale)` | Canonicalizes a locale string |
| **Instance Properties** | |
| `locale.baseName` | Base name of the locale |
| `locale.calendar` | Calendar used by the locale |
| `locale.caseFirst` | Case ordering for the locale |
| `locale.collation` | Collation type for the locale |
| `locale.hourCycle` | Hour cycle for the locale |
| `locale.language` | Language code for the locale |
| `locale.numeric` | Numeric system for the locale |
| `locale.region` | Region code for the locale |
| `locale.script` | Script code for the locale |
| `locale.timeZone` | Time zone for the locale |
| **Instance Methods** | |
| `locale.maximize()` | Returns a locale with maximized information |
| `locale.minimize()` | Returns a locale with minimized information |
| `locale.toString()` | Returns a string representation |

---
### **Intl.NumberFormat**
*(Number formatting)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.NumberFormat()` | Constructor for number formatters |
| **Instance Methods** | |
| `numberFormat.format(number)` | Formats a number |
| `numberFormat.formatToParts(number)` (ES2017) | Returns an array of objects representing parts of the formatted number |
| `numberFormat.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.NumberFormat.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.PluralRules** (ES2018)
*(Plural-sensitive formatting)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.PluralRules()` | Constructor for plural rules |
| **Instance Methods** | |
| `pluralRules.select(number)` | Returns the plural category for a number |
| `pluralRules.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.PluralRules.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.RelativeTimeFormat** (ES2020)
*(Relative time formatting)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.RelativeTimeFormat()` | Constructor for relative time formatters |
| **Instance Methods** | |
| `relativeTimeFormat.format(value, unit)` | Formats a relative time |
| `relativeTimeFormat.formatToParts(value, unit)` (ES2021) | Returns an array of objects representing parts of the formatted relative time |
| `relativeTimeFormat.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.RelativeTimeFormat.supportedLocalesOf(locales, options)` | Returns an array of supported locales |

---
### **Intl.Segmenter** (ES2022)
*(Text segmentation)*

| Method/Property | Description |
|-----------------|-------------|
| `Intl.Segmenter()` | Constructor for segmenters |
| **Instance Methods** | |
| `segmenter.segment(string)` | Segments a string into an iterator of segments |
| `segmenter.resolvedOptions()` | Returns a new object with properties reflecting the resolved options |
| **Constructor Properties** | |
| `Intl.Segmenter.supportedLocalesOf(locales, options)` | Returns an array of supported locales |