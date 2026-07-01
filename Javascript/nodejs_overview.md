# File System (`node:fs`)

| Function              | Description                     |
| --------------------- | ------------------------------- |
| `readFile()`          | Read entire file asynchronously |
| `readFileSync()`      | Read file synchronously         |
| `writeFile()`         | Create or overwrite file        |
| `writeFileSync()`     | Sync version                    |
| `appendFile()`        | Append to file                  |
| `appendFileSync()`    | Sync append                     |
| `copyFile()`          | Copy file                       |
| `rename()`            | Rename or move file             |
| `unlink()`            | Delete file                     |
| `rm()`                | Remove file or directory        |
| `mkdir()`             | Create directory                |
| `rmdir()`             | Remove directory                |
| `readdir()`           | List directory contents         |
| `stat()`              | File statistics                 |
| `lstat()`             | Symbolic link statistics        |
| `existsSync()`        | Check file exists               |
| `access()`            | Test permissions                |
| `chmod()`             | Change permissions              |
| `chown()`             | Change ownership                |
| `watch()`             | Watch for file changes          |
| `watchFile()`         | Poll file for changes           |
| `createReadStream()`  | Read stream                     |
| `createWriteStream()` | Write stream                    |
| `cp()`                | Copy directories recursively    |

---

# File System Promises (`node:fs/promises`)

| Function       | Description           |
| -------------- | --------------------- |
| `readFile()`   | Promise version       |
| `writeFile()`  | Promise write         |
| `appendFile()` | Promise append        |
| `mkdir()`      | Create directory      |
| `readdir()`    | Read directory        |
| `rm()`         | Remove file/directory |
| `rename()`     | Rename                |
| `copyFile()`   | Copy file             |
| `stat()`       | File information      |
| `access()`     | Permission check      |
| `open()`       | Open file handle      |

---

# Path (`node:path`)

| Function       | Description          |
| -------------- | -------------------- |
| `join()`       | Join path segments   |
| `resolve()`    | Build absolute path  |
| `basename()`   | Filename             |
| `dirname()`    | Directory name       |
| `extname()`    | File extension       |
| `normalize()`  | Normalize separators |
| `relative()`   | Relative path        |
| `parse()`      | Parse path           |
| `format()`     | Build path object    |
| `isAbsolute()` | Absolute path check  |

---

# Operating System (`node:os`)

| Function              | Description       |
| --------------------- | ----------------- |
| `platform()`          | Operating system  |
| `arch()`              | CPU architecture  |
| `cpus()`              | CPU information   |
| `hostname()`          | Hostname          |
| `networkInterfaces()` | Network adapters  |
| `homedir()`           | Home directory    |
| `tmpdir()`            | Temp directory    |
| `uptime()`            | System uptime     |
| `totalmem()`          | Total RAM         |
| `freemem()`           | Free RAM          |
| `loadavg()`           | CPU load          |
| `type()`              | OS type           |
| `release()`           | OS version        |
| `version()`           | OS version string |
| `userInfo()`          | Current user      |

---

# Process (`node:process`)

| Property / Function | Description               |
| ------------------- | ------------------------- |
| `argv`              | Command line arguments    |
| `env`               | Environment variables     |
| `cwd()`             | Current directory         |
| `chdir()`           | Change directory          |
| `exit()`            | Exit process              |
| `pid`               | Process ID                |
| `ppid`              | Parent PID                |
| `stdin`             | Standard input            |
| `stdout`            | Standard output           |
| `stderr`            | Error output              |
| `memoryUsage()`     | Memory statistics         |
| `cpuUsage()`        | CPU usage                 |
| `uptime()`          | Process uptime            |
| `kill()`            | Send signal               |
| `nextTick()`        | Execute before event loop |

---

# Child Process (`node:child_process`)

| Function         | Description           |
| ---------------- | --------------------- |
| `exec()`         | Execute shell command |
| `execSync()`     | Sync shell command    |
| `spawn()`        | Start process         |
| `spawnSync()`    | Sync spawn            |
| `fork()`         | Launch Node child     |
| `execFile()`     | Execute executable    |
| `execFileSync()` | Sync executable       |

---

# Streams (`node:stream`)

| Function      | Description              |
| ------------- | ------------------------ |
| `pipeline()`  | Connect streams          |
| `finished()`  | Detect stream completion |
| `Readable`    | Readable stream          |
| `Writable`    | Writable stream          |
| `Duplex`      | Read/write stream        |
| `Transform`   | Transform stream         |
| `PassThrough` | Pass-through stream      |

---

# HTTP (`node:http`)

| Function         | Description     |
| ---------------- | --------------- |
| `createServer()` | HTTP server     |
| `request()`      | HTTP client     |
| `get()`          | HTTP GET        |
| `Agent`          | Connection pool |

---

# HTTPS (`node:https`)

| Function         | Description           |
| ---------------- | --------------------- |
| `createServer()` | HTTPS server          |
| `request()`      | HTTPS request         |
| `get()`          | HTTPS GET             |
| `Agent`          | HTTPS connection pool |

---

# HTTP2 (`node:http2`)

| Function               | Description       |
| ---------------------- | ----------------- |
| `createServer()`       | HTTP/2 server     |
| `createSecureServer()` | TLS HTTP/2 server |
| `connect()`            | HTTP/2 client     |

---

# URL (`node:url`)

| Function          | Description      |
| ----------------- | ---------------- |
| `URL`             | URL parser       |
| `URLSearchParams` | Query parameters |
| `pathToFileURL()` | File path → URL  |
| `fileURLToPath()` | URL → File path  |

---

# Query String (`node:querystring`)

| Function      | Description        |
| ------------- | ------------------ |
| `parse()`     | Parse query string |
| `stringify()` | Build query string |
| `escape()`    | Escape text        |
| `unescape()`  | Decode text        |

---

# Crypto (`node:crypto`)

| Function             | Description             |
| -------------------- | ----------------------- |
| `createHash()`       | Hash data               |
| `createHmac()`       | HMAC                    |
| `createCipheriv()`   | Encrypt                 |
| `createDecipheriv()` | Decrypt                 |
| `randomBytes()`      | Random bytes            |
| `randomUUID()`       | UUID                    |
| `generateKeyPair()`  | Generate keys           |
| `pbkdf2()`           | Password hashing        |
| `scrypt()`           | Secure password hashing |
| `sign()`             | Digital signature       |
| `verify()`           | Verify signature        |

---

# Buffer (`node:buffer`)

| Function              | Description       |
| --------------------- | ----------------- |
| `Buffer.alloc()`      | Allocate buffer   |
| `Buffer.from()`       | Create buffer     |
| `Buffer.concat()`     | Combine buffers   |
| `Buffer.byteLength()` | Buffer size       |
| `toString()`          | Convert to string |

---

# Timers (`node:timers`)

| Function           | Description      |
| ------------------ | ---------------- |
| `setTimeout()`     | Delay execution  |
| `clearTimeout()`   | Cancel timeout   |
| `setInterval()`    | Repeat execution |
| `clearInterval()`  | Cancel interval  |
| `setImmediate()`   | Run immediately  |
| `clearImmediate()` | Cancel immediate |

---

# Events (`node:events`)

| Function               | Description          |
| ---------------------- | -------------------- |
| `EventEmitter`         | Base event class     |
| `on()`                 | Listen               |
| `once()`               | Listen once          |
| `emit()`               | Fire event           |
| `off()`                | Remove listener      |
| `removeListener()`     | Remove listener      |
| `removeAllListeners()` | Remove all listeners |

---

# DNS (`node:dns`)

| Function     | Description     |
| ------------ | --------------- |
| `lookup()`   | DNS lookup      |
| `resolve()`  | Resolve records |
| `resolve4()` | IPv4            |
| `resolve6()` | IPv6            |
| `reverse()`  | Reverse lookup  |

---

# Net (`node:net`)

| Function             | Description |
| -------------------- | ----------- |
| `createServer()`     | TCP server  |
| `connect()`          | TCP client  |
| `createConnection()` | Open socket |
| `Socket`             | TCP socket  |

---

# TLS (`node:tls`)

| Function         | Description |
| ---------------- | ----------- |
| `createServer()` | TLS server  |
| `connect()`      | TLS client  |
| `TLSSocket`      | TLS socket  |

---

# UDP (`node:dgram`)

| Function         | Description  |
| ---------------- | ------------ |
| `createSocket()` | UDP socket   |
| `bind()`         | Bind port    |
| `send()`         | Send packet  |
| `close()`        | Close socket |

---

# Compression (`node:zlib`)

| Function             | Description          |
| -------------------- | -------------------- |
| `gzip()`             | Compress             |
| `gunzip()`           | Decompress           |
| `deflate()`          | Deflate              |
| `inflate()`          | Inflate              |
| `brotliCompress()`   | Brotli compression   |
| `brotliDecompress()` | Brotli decompression |

---

# Readline (`node:readline`)

| Function            | Description          |
| ------------------- | -------------------- |
| `createInterface()` | Interactive terminal |
| `question()`        | Ask question         |
| `close()`           | Close interface      |
| `clearLine()`       | Clear console line   |
| `cursorTo()`        | Move cursor          |

---

# Console (`node:console`)

| Function    | Description    |
| ----------- | -------------- |
| `log()`     | Print output   |
| `error()`   | Print error    |
| `warn()`    | Print warning  |
| `info()`    | Print info     |
| `table()`   | Display table  |
| `time()`    | Start timer    |
| `timeEnd()` | End timer      |
| `clear()`   | Clear terminal |
| `trace()`   | Stack trace    |

---

# Assert (`node:assert`)

| Function            | Description            |
| ------------------- | ---------------------- |
| `equal()`           | Loose equality         |
| `strictEqual()`     | Strict equality        |
| `deepEqual()`       | Deep comparison        |
| `deepStrictEqual()` | Strict deep comparison |
| `ok()`              | Assert truthy          |
| `throws()`          | Expect exception       |
| `rejects()`         | Promise rejection      |

---

# Util (`node:util`)

| Function        | Description           |
| --------------- | --------------------- |
| `promisify()`   | Callback → Promise    |
| `callbackify()` | Promise → Callback    |
| `inspect()`     | Pretty-print objects  |
| `inherits()`    | Classical inheritance |
| `format()`      | String formatting     |
| `types`         | Type helpers          |

---

# Async Hooks (`node:async_hooks`)

| Function             | Description           |
| -------------------- | --------------------- |
| `createHook()`       | Async lifecycle hooks |
| `AsyncLocalStorage`  | Request-local storage |
| `executionAsyncId()` | Async ID              |
| `triggerAsyncId()`   | Parent async ID       |

---

# Worker Threads (`node:worker_threads`)

| Function         | Description          |
| ---------------- | -------------------- |
| `Worker`         | Background thread    |
| `parentPort`     | Parent communication |
| `workerData`     | Initial data         |
| `MessageChannel` | Thread messaging     |
| `MessagePort`    | Communication port   |

---

# Performance (`node:perf_hooks`)

| Function              | Description             |
| --------------------- | ----------------------- |
| `performance.now()`   | High-resolution timer   |
| `mark()`              | Create performance mark |
| `measure()`           | Measure duration        |
| `PerformanceObserver` | Observe metrics         |

---

# Inspector (`node:inspector`)

| Function  | Description       |
| --------- | ----------------- |
| `open()`  | Enable debugger   |
| `close()` | Disable debugger  |
| `url()`   | Debug URL         |
| `Session` | Inspector session |

---

# Test Runner (`node:test`)

| Function       | Description      |
| -------------- | ---------------- |
| `test()`       | Define test      |
| `describe()`   | Group tests      |
| `it()`         | Alias for test   |
| `before()`     | Before all tests |
| `after()`      | After all tests  |
| `beforeEach()` | Before each test |
| `afterEach()`  | After each test  |
| `mock`         | Mock utilities   |

---

# VM (`node:vm`)

| Function            | Description        |
| ------------------- | ------------------ |
| `Script`            | Compile script     |
| `runInContext()`    | Execute in sandbox |
| `runInNewContext()` | New sandbox        |
| `createContext()`   | Create context     |

---

# Module (`node:module`)

| Function            | Description             |
| ------------------- | ----------------------- |
| `createRequire()`   | Create CommonJS require |
| `register()`        | Register module hooks   |
| `findPackageJSON()` | Locate package.json     |

---

# Diagnostics (`node:diagnostics_channel`)

| Function      | Description                |
| ------------- | -------------------------- |
| `channel()`   | Create diagnostics channel |
| `subscribe()` | Subscribe                  |
| `publish()`   | Publish event              |

---

# Other Core Modules

| Module                | Purpose                       |
| --------------------- | ----------------------------- |
| `node:cluster`        | Multi-process scaling         |
| `node:v8`             | V8 engine APIs                |
| `node:tty`            | Terminal detection            |
| `node:string_decoder` | Character decoding            |
| `node:repl`           | Interactive REPL              |
| `node:punycode`       | Unicode domain names (legacy) |
| `node:constants`      | System constants              |
| `node:domain`         | Legacy error handling         |
| `node:trace_events`   | Performance tracing           |

---

# Common Global Objects

These are available without importing any module.

| Global              | Description             |
| ------------------- | ----------------------- |
| `fetch()`           | HTTP client             |
| `Request`           | HTTP request            |
| `Response`          | HTTP response           |
| `Headers`           | HTTP headers            |
| `AbortController`   | Cancel async operations |
| `AbortSignal`       | Cancellation signal     |
| `Buffer`            | Binary data             |
| `process`           | Current process         |
| `console`           | Logging                 |
| `setTimeout()`      | Delay execution         |
| `setInterval()`     | Repeating timer         |
| `setImmediate()`    | Immediate execution     |
| `clearTimeout()`    | Cancel timeout          |
| `clearInterval()`   | Cancel interval         |
| `clearImmediate()`  | Cancel immediate        |
| `URL`               | URL parser              |
| `URLSearchParams`   | URL query parameters    |
| `TextEncoder`       | UTF-8 encoder           |
| `TextDecoder`       | UTF-8 decoder           |
| `ReadableStream`    | Web streams             |
| `WritableStream`    | Web streams             |
| `TransformStream`   | Web streams             |
| `Blob`              | Binary object           |
| `File`              | File object             |
| `FormData`          | Multipart forms         |
| `structuredClone()` | Deep clone              |
| `queueMicrotask()`  | Schedule microtask      |
| `performance`       | High-resolution timing  |
| `crypto`            | Web Crypto API          |