# Python Logging Library Reference

---

## Logging Levels

| Code | Description |
|------|-------------|
| `logging.DEBUG` | Level for detailed debugging information. Numeric value: 10. |
| `logging.INFO` | Level for informational messages. Numeric value: 20. |
| `logging.WARNING` | Level for warning messages. Numeric value: 30. |
| `logging.ERROR` | Level for error messages. Numeric value: 40. |
| `logging.CRITICAL` | Level for critical error messages. Numeric value: 50. |
| `logging.FATAL` | Alias for `CRITICAL`. Numeric value: 50. |
| `logging.NOTSET` | Level indicating that no level has been set. Numeric value: 0. |

---

## Basic Configuration

| Code | Description |
|------|-------------|
| `logging.basicConfig(**kwargs)` | Configures the logging system for basic usage. Accepts arguments like `level`, `format`, `datefmt`, `filename`, `filemode`, `handlers`, `force`, `encoding`, `errors`. |
| `logging.basicConfig(level=logging.WARNING)` | Sets the default logging level to WARNING. |
| `logging.basicConfig(filename='app.log', level=logging.DEBUG)` | Configures logging to write DEBUG-level messages to a file. |
| `logging.basicConfig(format='%(asctime)s - %(name)s - %(levelname)s - %(message)s')` | Configures a custom log message format. |
| `logging.basicConfig(handlers=[handler1, handler2])` | Configures logging with a list of handlers. |
| `logging.basicConfig(force=True)` | Forces reconfiguration even if the root logger already has handlers. |
| `logging.shutdown()` | Performs a clean shutdown of the logging system, flushing and closing all handlers. |

---

## Logger Creation and Retrieval

| Code | Description |
|------|-------------|
| `logging.getLogger(name=None)` | Returns a logger with the specified name. If no name is provided, returns the root logger. |
| `logging.getLogger('my_module')` | Returns a logger named 'my_module'. |
| `logging.getLogger(__name__)` | Returns a logger with the name of the current module. |
| `logging.Logger(name, level=NOTSET)` | Class for creating logger instances. |
| `logging.LoggerAdapter(logger, extra)` | Class for creating a logger adapter that adds contextual information to log messages. |
| `logging.logThread` | Deprecated. Use `logging.getLoggerThread()` instead. |
| `logging.getLoggerThread(name=None)` | Returns a logger for the current thread. |

---

## Logger Methods

| Code | Description |
|------|-------------|
| `logger.debug(msg, *args, **kwargs)` | Logs a message with level DEBUG. |
| `logger.info(msg, *args, **kwargs)` | Logs a message with level INFO. |
| `logger.warning(msg, *args, **kwargs)` | Logs a message with level WARNING. |
| `logger.error(msg, *args, **kwargs)` | Logs a message with level ERROR. |
| `logger.critical(msg, *args, **kwargs)` | Logs a message with level CRITICAL. |
| `logger.fatal(msg, *args, **kwargs)` | Alias for `critical()`. |
| `logger.log(level, msg, *args, **kwargs)` | Logs a message with the specified level. |
| `logger.exception(msg, *args, **kwargs)` | Logs a message with level ERROR and includes the current exception information. |
| `logger.setLevel(level)` | Sets the logging level for the logger. |
| `logger.getEffectiveLevel()` | Returns the effective logging level for the logger, considering inheritance from parent loggers. |
| `logger.isEnabledFor(level)` | Returns True if the logger is enabled for the specified level. |
| `logger.addHandler(hdlr)` | Adds a handler to the logger. |
| `logger.removeHandler(hdlr)` | Removes a handler from the logger. |
| `logger.addFilter(filter)` | Adds a filter to the logger. |
| `logger.removeFilter(filter)` | Removes a filter from the logger. |
| `logger.handlers` | Property returning a list of handlers for the logger. |
| `logger.filters` | Property returning a list of filters for the logger. |
| `logger.parent` | Property returning the parent logger. |
| `logger.propagate` | Property indicating whether the logger propagates messages to parent loggers. |
| `logger.disabled` | Property indicating whether the logger is disabled. |
| `logger.name` | Property returning the name of the logger. |
| `logger.level` | Property returning the logging level of the logger. |

---

## Logger Attributes

| Code | Description |
|------|-------------|
| `logger.handlers` | List of handlers attached to the logger. |
| `logger.filters` | List of filters attached to the logger. |
| `logger.parent` | Parent logger in the hierarchy. |
| `logger.propagate` | Boolean indicating whether log messages should be propagated to parent loggers. |
| `logger.disabled` | Boolean indicating whether the logger is disabled. |
| `logger.level` | Logging level for the logger. |
| `logger.name` | Name of the logger. |
| `logger.manager` | Reference to the Logger.manager. |

---

## Handler Classes

| Code | Description |
|------|-------------|
| `logging.Handler` | Base class for all logging handlers. |
| `logging.StreamHandler(stream=None)` | Handler that sends log messages to a stream (e.g., sys.stdout, sys.stderr). |
| `logging.FileHandler(filename, mode='a', encoding=None, delay=False, errors=None)` | Handler that sends log messages to a file. |
| `logging.RotatingFileHandler(filename, mode='a', maxBytes=0, backupCount=0, encoding=None, delay=False, errors=None)` | Handler that rotates log files when they reach a specified size. |
| `logging.TimedRotatingFileHandler(filename, when='h', interval=1, backupCount=0, encoding=None, delay=False, utc=False, atTime=None, errors=None)` | Handler that rotates log files at specified time intervals. |
| `logging.NullHandler()` | Handler that does nothing. Useful for avoiding "No handler found" warnings. |
| `logging.SocketHandler(host, port)` | Handler that sends log messages to a TCP socket. |
| `logging.DatagramHandler(host, port)` | Handler that sends log messages to a UDP socket. |
| `logging.SMTPHandler(mailhost, fromaddr, toaddrs, subject, credentials=None, secure=None, timeout=1.0)` | Handler that sends log messages via email. |
| `logging.SysLogHandler(address=('localhost', 514), facility=logging.SysLogHandler.LOG_USER, socktype=socket.SOCK_DGRAM)` | Handler that sends log messages to a Unix syslog daemon. |
| `logging.NTEventLogHandler(app_name, dll_name=None, log_type=win32evtlog.EVENTLOG_ERROR_TYPE)` | Handler that sends log messages to the Windows NT event log. |
| `logging.MemoryHandler(capacity, flushLevel=logging.ERROR, target=None)` | Handler that stores log messages in memory and flushes them to a target handler when a specified condition is met. |
| `logging.QueueHandler(queue)` | Handler that sends log messages to a queue. |
| `logging.QueueListener(queue, *handlers)` | Listener that receives log messages from a queue and processes them using the specified handlers. |
| `logging.BufferingHandler(capacity)` | Base class for handlers that buffer log messages. |

---

## Handler Methods and Attributes

| Code | Description |
|------|-------------|
| `handler.setLevel(level)` | Sets the logging level for the handler. |
| `handler.setFormatter(fmt)` | Sets the formatter for the handler. |
| `handler.addFilter(filter)` | Adds a filter to the handler. |
| `handler.removeFilter(filter)` | Removes a filter from the handler. |
| `handler.handle(record)` | Processes the log record. |
| `handler.emit(record)` | Sends the log record to the appropriate destination. |
| `handler.flush()` | Ensures all log messages are written to the destination. |
| `handler.close()` | Closes the handler and releases any resources. |
| `handler.createLock()` | Creates a lock for the handler. |
| `handler.acquire()` | Acquires the lock for the handler. |
| `handler.release()` | Releases the lock for the handler. |
| `handler.level` | Logging level for the handler. |
| `handler.formatter` | Formatter for the handler. |
| `handler.filters` | List of filters for the handler. |
| `handler.stream` | Stream for StreamHandler. |
| `handler.baseFilename` | Base filename for FileHandler and its subclasses. |
| `handler.mode` | File mode for FileHandler. |
| `handler.encoding` | Encoding for FileHandler and its subclasses. |
| `handler.maxBytes` | Maximum file size for RotatingFileHandler. |
| `handler.backupCount` | Number of backup files for RotatingFileHandler. |
| `handler.when` | Rotation interval for TimedRotatingFileHandler (e.g., 'S', 'M', 'H', 'D', 'midnight', 'W0'-'W6'). |
| `handler.interval` | Rotation interval value for TimedRotatingFileHandler. |
| `handler.suffix` | Suffix for rotated files in TimedRotatingFileHandler. |
| `handler.extMatch` | Pattern for matching rotated files in TimedRotatingFileHandler. |

---
## Formatter Classes and Methods

| Code | Description |
|------|-------------|
| `logging.Formatter(fmt=None, datefmt=None, style='%', validate=True)` | Configures the format of log messages. |
| `logging.BasicFormatter(fmt='%(message)s', datefmt=None, style='%', validate=True)` | Basic formatter for log messages. |
| `formatter.format(record)` | Formats the log record as a string. |
| `formatter.formatTime(record)` | Formats the creation time of the log record. |
| `formatter.formatException(info)` | Formats exception information. |
| `formatter.formatStack(stack_info)` | Formats stack information. |
| `formatter.usesTime()` | Returns True if the formatter uses the creation time. |
| `formatter.default_time_format` | Default time format string. |
| `formatter.default_msec_format` | Default millisecond format string. |
| `logging.PercentStyle(fmt)` | Style class for %-formatting. |
| `logging.StrFormatStyle(fmt)` | Style class for str.format() formatting. |
| `logging.StringTemplateStyle(fmt)` | Style class for string.Template formatting. |
| `logging.StructTimeFormatStyle(fmt)` | Style class for struct_time formatting. |

---
## Formatting Attributes

| Code | Description |
|------|-------------|
| `%(name)s` | Name of the logger. |
| `%(levelno)s` | Numeric logging level. |
| `%(levelname)s` | Text logging level. |
| `%(pathname)s` | Full pathname of the source file where the logging call was made. |
| `%(filename)s` | Filename portion of the pathname. |
| `%(module)s` | Module name portion of the filename. |
| `%(lineno)d` | Source line number where the logging call was made. |
| `%(funcName)s` | Name of the function containing the logging call. |
| `%(created)f` | Time when the LogRecord was created (time.time() return value). |
| `%(relativeCreated)d` | Time in milliseconds since the logging module was loaded. |
| `%(asctime)s` | Human-readable time when the LogRecord was created. |
| `%(msecs)d` | Millisecond portion of the creation time. |
| `%(message)s` | The logged message, computed as str(record.getMessage()). |
| `%(msg)s` | The logged message, including the arguments merged into the message. |
| `%(args)s` | Tuple of arguments merged into the message. |
| `%(created)f` | Time when the LogRecord was created. |
| `%(thread)d` | Thread ID. |
| `%(threadName)s` | Thread name. |
| `%(process)d` | Process ID. |
| `%(processName)s` | Process name. |
| `%(exc_info)s` | Exception tuple or None if no exception. |
| `%(exc_text)s` | Stack trace from exception, if any. |
| `%(stack_info)s` | Stack frame information. |

---
## Filter Classes and Methods

| Code | Description |
|------|-------------|
| `logging.Filter(name='')` | Base class for all logging filters. |
| `logging.Filter.filter(record)` | Determines whether the specified log record should be processed. |
| `filter = logging.Filter('my_module')` | Creates a filter that only allows log records from the specified module. |
| `logger.addFilter(filter)` | Adds a filter to a logger. |
| `handler.addFilter(filter)` | Adds a filter to a handler. |

---
## LogRecord Class and Attributes

| Code | Description |
|------|-------------|
| `logging.LogRecord(name, level, pathname, lineno, msg, args, exc_info, func=None, sinfo=None)` | Represents an event being logged. |
| `record.getMessage()` | Returns the log message, with arguments merged in. |
| `record.name` | Name of the logger. |
| `record.levelno` | Numeric logging level. |
| `record.levelname` | Text logging level. |
| `record.pathname` | Full pathname of the source file. |
| `record.filename` | Filename portion of the pathname. |
| `record.module` | Module name portion of the filename. |
| `record.lineno` | Source line number. |
| `record.funcName` | Name of the function containing the logging call. |
| `record.created` | Time when the LogRecord was created (time.time() return value). |
| `record.msecs` | Millisecond portion of the creation time. |
| `record.relativeCreated` | Time in milliseconds since the logging module was loaded. |
| `record.thread` | Thread ID. |
| `record.threadName` | Thread name. |
| `record.process` | Process ID. |
| `record.processName` | Process name. |
| `record.args` | Tuple of arguments merged into the message. |
| `record.msg` | The logged message before argument substitution. |
| `record.message` | The logged message after argument substitution. |
| `record.asctime` | Human-readable time when the LogRecord was created. |
| `record.exc_info` | Exception tuple or None if no exception. |
| `record.exc_text` | Stack trace from exception, if any. |
| `record.stack_info` | Stack frame information. |

---
## Configuration Functions

| Code | Description |
|------|-------------|
| `logging.basicConfig(**kwargs)` | Configures the logging system for basic usage. |
| `logging.shutdown()` | Performs a clean shutdown of the logging system. |
| `logging.disable(level=CRITICAL)` | Disables all logging calls of severity `level` and below. |
| `logging.getLogger(name=None)` | Returns a logger with the specified name. |
| `logging.getLoggerClass()` | Returns the class used for creating loggers. |
| `logging.setLoggerClass(klass)` | Sets the class to be used for creating loggers. |
| `logging.getLogRecordFactory()` | Returns the factory used for creating LogRecord objects. |
| `logging.setLogRecordFactory(factory)` | Sets the factory to be used for creating LogRecord objects. |

---
## Configuration Dictionary

| Code | Description |
|------|-------------|
| `logging.config.dictConfig(config)` | Configures logging using a dictionary. |
| `version` | Required key. Must be 1. |
| `formatters` | Dictionary mapping formatter names to formatter configurations. |
| `handlers` | Dictionary mapping handler names to handler configurations. |
| `loggers` | Dictionary mapping logger names to logger configurations. |
| `root` | Configuration for the root logger. |
| `incremental` | Boolean indicating whether the configuration should be incremental. |
| `disable_existing_loggers` | Boolean indicating whether existing loggers should be disabled. |

---
## Configuration Dictionary Example

| Code | Description |
|------|-------------|
| `{'version': 1, 'formatters': {'simple': {'format': '%(asctime)s - %(name)s - %(levelname)s - %(message)s'}}, 'handlers': {'console': {'class': 'logging.StreamHandler', 'level': 'DEBUG', 'formatter': 'simple', 'stream': 'ext://sys.stdout'}}, 'root': {'level': 'DEBUG', 'handlers': ['console']}}` | Example dictionary configuration for logging. |

---
## File Configuration

| Code | Description |
|------|-------------|
| `logging.config.fileConfig(fname, defaults=None)` | Configures logging using a configuration file. |
| `[loggers]` | Section for defining loggers. |
| `[handlers]` | Section for defining handlers. |
| `[formatters]` | Section for defining formatters. |
| `[loggers.root]` | Section for configuring the root logger. |

---
## File Configuration Example

| Code | Description |
|------|-------------|
| `[loggers] keys=root,my_module [handlers] keys=consoleHandler [formatters] keys=simpleFormatter [logger_root] level=DEBUG handlers=consoleHandler [logger_my_module] level=DEBUG handlers=consoleHandler qualname=my_module propagate=0 [handler_consoleHandler] class=StreamHandler level=DEBUG formatter=simpleFormatter args=(sys.stdout,) [formatter_simpleFormatter] format=%(asctime)s - %(name)s - %(levelname)s - %(message)s datefmt=` | Example file configuration for logging. |

---
## Logger Manager

| Code | Description |
|------|-------------|
| `logging.Logger.manager` | Reference to the Logger.manager. |
| `logging.Manager(loggerClass=None, loggerDict=None)` | Class for managing loggers. |
| `logging.RootLogger(level=WARNING)` | Class for the root logger. |
| `logging PlaceHolder(logger)` | Placeholder class used internally by the logging module. |

---
## Exceptions

| Code | Description |
|------|-------------|
| `logging.LoggingException` | Base class for logging exceptions. |

---
## Thread and Process Safety

| Code | Description |
|------|-------------|
| `logging.LogRecordFactory` | Factory for creating LogRecord objects. |
| `logging.setLogRecordFactory(factory)` | Sets the factory to be used for creating LogRecord objects. |
| `logging.getLogRecordFactory()` | Returns the factory used for creating LogRecord objects. |
| `threading.setLogRecordFactory(factory)` | Sets the factory for the current thread. |

---
## Socket Receiver

| Code | Description |
|------|-------------|
| `logging.handlers.SocketReceiver(port, handler)` | Creates a socket receiver for receiving log messages. |
| `logging.handlers.makeSocket(host, port)` | Creates a socket for receiving log messages. |
| `logging.handlers.sendto(host, port, data)` | Sends data to a socket. |

---
## Queue Listener

| Code | Description |
|------|-------------|
| `logging.handlers.QueueListener(queue, *handlers)` | Creates a listener for receiving log messages from a queue. |
| `listener.start()` | Starts the listener. |
| `listener.stop()` | Stops the listener. |
| `listener.prepare()` | Prepares the listener. |
| `listener.enqueue(s)` | Enqueues a log record. |
| `logging.handlers.QueueHandler(queue)` | Creates a handler that sends log messages to a queue. |

---
## Memory Handler

| Code | Description |
|------|-------------|
| `logging.handlers.MemoryHandler(capacity, flushLevel=ERROR, target=None, flushOnClose=True)` | Creates a handler that buffers log messages in memory. |
| `handler.setTarget(target)` | Sets the target handler for the MemoryHandler. |
| `handler.flush()` | Flushes the buffer to the target handler. |
| `handler.close()` | Closes the handler and flushes the buffer. |

---
## Rotating File Handler

| Code | Description |
|------|-------------|
| `logging.handlers.RotatingFileHandler(filename, mode='a', maxBytes=0, backupCount=0, encoding=None, delay=False, errors=None)` | Creates a handler that rotates log files when they reach a specified size. |
| `handler.doRollover()` | Performs a rollover of the log file. |
| `handler.rotation_filename(suffix)` | Returns the filename for a rotated log file. |
| `handler.namer` | Function for naming rotated log files. |
| `handler.rotator` | Function for rotating log files. |

---
## Timed Rotating File Handler

| Code | Description |
|------|-------------|
| `logging.handlers.TimedRotatingFileHandler(filename, when='h', interval=1, backupCount=0, encoding=None, delay=False, utc=False, atTime=None, errors=None)` | Creates a handler that rotates log files at specified time intervals. |
| `handler.suffix` | Suffix for rotated files. |
| `handler.extMatch` | Pattern for matching rotated files. |
| `handler.getFilesToDelete()` | Returns a list of files to delete during rollover. |
| `handler.computeRollover(time.time())` | Computes the next rollover time. |

---
## SysLog Handler

| Code | Description |
|------|-------------|
| `logging.handlers.SysLogHandler(address=('localhost', 514), facility=SysLogHandler.LOG_USER, socktype=socket.SOCK_DGRAM)` | Creates a handler that sends log messages to a Unix syslog daemon. |
| `handler.encodePriority(facility, priority)` | Encodes the facility and priority into a single integer. |
| `handler.mapPriority(priority)` | Maps a logging level to a syslog priority. |
| `handler.facility` | Syslog facility to use. |
| `handler.socktype` | Socket type to use. |

---
## SMTP Handler

| Code | Description |
|------|-------------|
| `logging.handlers.SMTPHandler(mailhost, fromaddr, toaddrs, subject, credentials=None, secure=None, timeout=1.0)` | Creates a handler that sends log messages via email. |
| `handler.getSubject(record)` | Returns the subject for the email. |
| `handler.emit(record)` | Sends the log message as an email. |
| `handler.createSocket()` | Creates a socket for sending emails. |
| `handler.send(s)` | Sends the email message. |

---
## NT Event Log Handler

| Code | Description |
|------|-------------|
| `logging.handlers.NTEventLogHandler(app_name, dll_name=None, log_type=win32evtlog.EVENTLOG_ERROR_TYPE)` | Creates a handler that sends log messages to the Windows NT event log. |
| `handler.appName` | Name of the application. |
| `handler.dllName` | Name of the DLL containing event descriptions. |
| `handler.logType` | Type of the event log. |

---
## HTTP Handler

| Code | Description |
|------|-------------|
| `logging.handlers.HTTPHandler(host, url, method='GET', secure=False, credentials=None, context=None)` | Creates a handler that sends log messages to an HTTP server. |
| `handler.emit(record)` | Sends the log message to the HTTP server. |

---
## Datagram Handler

| Code | Description |
|------|-------------|
| `logging.handlers.DatagramHandler(host, port)` | Creates a handler that sends log messages to a UDP socket. |
| `handler.makeSocket()` | Creates a socket for sending datagrams. |
| `handler.send(s)` | Sends a datagram. |

---
## Socket Handler

| Code | Description |
|------|-------------|
| `logging.handlers.SocketHandler(host, port)` | Creates a handler that sends log messages to a TCP socket. |
| `handler.makeSocket()` | Creates a socket for sending log messages. |
| `handler.createSocket()` | Creates a socket for sending log messages. |
| `handler.send(s)` | Sends a log message. |

---
## Null Handler

| Code | Description |
|------|-------------|
| `logging.NullHandler()` | Creates a handler that does nothing. |

---
## Buffering Handler

| Code | Description |
|------|-------------|
| `logging.handlers.BufferingHandler(capacity)` | Base class for handlers that buffer log messages. |
| `handler.buffer` | List of buffered log messages. |
| `handler.capacity` | Maximum number of log messages to buffer. |

---
## Utility Functions

| Code | Description |
|------|-------------|
| `logging.addLevelName(level, levelName)` | Adds a level name for the specified level. |
| `logging.getLevelName(level)` | Returns the level name for the specified level. |
| `logging.getLevelNamesMapping()` | Returns a dictionary mapping level names to level numbers. |
| `logging.getLogRecordFactory()` | Returns the factory used for creating LogRecord objects. |
| `logging.setLogRecordFactory(factory)` | Sets the factory to be used for creating LogRecord objects. |