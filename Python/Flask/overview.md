## Application Setup and Configuration

| Code | Description |
|------|-------------|
| `Flask(__name__)` | Creates a Flask application instance. The `__name__` argument helps Flask locate the application root path and static files. |
| `app.config` | Configuration dictionary for the application. Can be modified directly or via `app.config.from_*()` methods. |
| `app.config.from_object(obj)` | Loads configuration from a Python object (typically a module or class with uppercase attributes). |
| `app.config.from_pyfile(filename)` | Loads configuration from a Python file. The file should contain variable assignments. |
| `app.config.from_json(json_str)` | Loads configuration from a JSON string. |
| `app.config.from_prefixed_env(prefix)` | Loads configuration from environment variables with a given prefix. |
| `app.config.get(key, default=None)` | Retrieves a configuration value, returning the default if the key does not exist. |
| `app.config.setdefault(key, value)` | Sets a configuration key to the given value if it is not already set. |
| `current_app` | Proxy to the current Flask application handling the active request. Use within application context. |
| `g` | A namespace object for storing data during a single request. Cleared after each request. |

---

## Routing and URL Handling

| Code | Description |
|------|-------------|
| `@app.route(rule, methods=None, **options)` | Decorator to bind a URL rule to a view function. `rule` is the URL pattern, `methods` is a list of HTTP methods (e.g., `['GET', 'POST']`). |
| `@app.route('/path/<variable>')` | Route with a variable part. The variable is passed as a keyword argument to the view function. |
| `@app.route('/path/<int:variable>')` | Route with a type converter (`int`, `float`, `path`, `string`, `uuid`). |
| `@app.route('/path/<path:variable>')` | Route with a path converter, which accepts slashes in the variable. |
| `url_for(endpoint, **values)` | Generates a URL for the given endpoint with the specified values for variable parts. |
| `redirect(location, code=302)` | Returns a response object that redirects to the given location with the specified status code. |
| `abort(code, description=None)` | Raises an `HTTPException` for the given status code. Optionally includes a description. |
| `app.add_url_rule(rule, endpoint, view_func, **options)` | Adds a URL rule to the application. `endpoint` is the name for the route, `view_func` is the callable to handle requests. |
| `Rule(rule, endpoint, view_func, **options)` | Class representing a URL rule. Used internally by `add_url_rule` and `@route`. |
| `app.url_map` | The `Map` object containing all URL rules for the application. |
| `app.url_map.bind(host, port=0, url_scheme='http')` | Binds the URL map to a specific host, port, and URL scheme for URL generation. |

---

## Request Handling

| Code | Description |
|------|-------------|
| `request` | Proxy to the current request object. Accessible within request context. |
| `request.method` | The HTTP method of the current request (e.g., `GET`, `POST`, `PUT`, `DELETE`). |
| `request.args` | A `MultiDict` of URL parameters (query string) in the request. Immutable. |
| `request.form` | A `MultiDict` of form data from POST or PUT requests with `application/x-www-form-urlencoded` or `multipart/form-data`. |
| `request.values` | A `CombinedMultiDict` combining `args` and `form` for unified access to both. |
| `request.files` | A `MultiDict` of uploaded files from POST or PUT requests with `multipart/form-data`. |
| `request.json` | Parsed JSON data from the request body if the content type is `application/json`. |
| `request.get_json(silent=False)` | Parses JSON data from the request body. Returns `None` if `silent=True` and parsing fails. |
| `request.data` | Raw request body as bytes. |
| `request.headers` | A `EnvironHeaders` object containing the request headers. Case-insensitive. |
| `request.cookies` | A `RequestCookies` object containing the request cookies. |
| `request.host` | The host (e.g., `example.com:5000`) from the request. |
| `request.host_url` | The host URL (e.g., `http://example.com:5000`) from the request. |
| `request.path` | The path part of the URL (e.g., `/index`). |
| `request.full_path` | The path and query string (e.g., `/index?key=value`). |
| `request.url` | The complete request URL (e.g., `http://example.com/index?key=value`). |
| `request.base_url` | The URL without the query string (e.g., `http://example.com/index`). |
| `request.remote_addr` | The IP address of the client. |
| `request.environ` | The raw WSGI environment dictionary. |
| `request.scheme` | The URL scheme (e.g., `http`, `https`). |
| `request.is_json` | `True` if the request has a JSON content type. |
| `request.is_multiprocess` | `True` if the request is running in a multiprocess environment. |
| `request.is_multithread` | `True` if the request is running in a multithread environment. |
| `request.accept_mimetypes` | A `Accept` object containing the mimetypes the client accepts. |
| `request.accept_charsets` | A `Accept` object containing the charsets the client accepts. |
| `request.accept_encodings` | A `Accept` object containing the encodings the client accepts. |
| `request.accept_languages` | A `Accept` object containing the languages the client accepts. |

---

## Response Handling

| Code | Description |
|------|-------------|
| `Response(response, status, headers)` | Creates a response object. `response` can be a string, bytes, or a generator. |
| `make_response(*args)` | Creates a `Response` object from the return value of a view function. If the view returns a string, it is wrapped in a `Response`. |
| `jsonify(*args, **kwargs)` | Creates a `Response` object with a JSON-encoded body. Useful for returning JSON from view functions. |
| `send_file(path_or_file, mimetype=None, as_attachment=False, download_name=None, **kwargs)` | Sends a file as a response. `path_or_file` can be a filesystem path or a file-like object. |
| `send_from_directory(directory, path, mimetype=None, as_attachment=False, download_name=None, **kwargs)` | Sends a file from a directory as a response. Safer than `send_file` for user-provided paths. |
| `stream_with_context(generator_or_function)` | Wraps a generator or function to ensure it runs within the correct request context. |
| `app.make_default_send_file()` | Creates a default `send_file` function for the application. |
| `response.status_code` | The HTTP status code for the response. |
| `response.status` | The HTTP status code as a string (e.g., `200 OK`). |
| `response.headers` | A `Headers` object for the response headers. Case-insensitive. |
| `response.set_cookie(key, value='', max_age=None, expires=None, path='/', domain=None, secure=False, httponly=False, samesite=None)` | Sets a cookie in the response. |
| `response.delete_cookie(key, path='/', domain=None)` | Deletes a cookie from the response. |
| `response.mimetype` | The mimetype of the response. |
| `response.data` | The response body as bytes. |
| `response.is_streamed` | `True` if the response is streamed. |
| `response.iter_encoded()` | Returns an iterator over the encoded response body. |

---

## Templates

| Code | Description |
|------|-------------|
| `render_template(template_name, **context)` | Renders a template with the given context. `template_name` is the name of the template file in the `templates` folder. |
| `render_template_string(source, **context)` | Renders a template from a string with the given context. |
| `app.jinja_env` | The Jinja2 environment for the application. |
| `app.template_folder` | The folder containing the application templates. |
| `Template` | Jinja2 template class. Used internally by Flask. |
| `Environment` | Jinja2 environment class. Used to configure template loading and rendering. |
| `TemplateNotFound` | Exception raised when a template is not found. |
| `TemplateRenderingError` | Exception raised when template rendering fails. |

---

## Sessions and Cookies

| Code | Description |
|------|-------------|
| `session` | Proxy to the current session object. Acts like a dictionary for storing data across requests. |
| `session.get(key, default=None)` | Retrieves a session value, returning the default if the key does not exist. |
| `session.pop(key, default=None)` | Removes a session key and returns its value, or the default if the key does not exist. |
| `session.clear()` | Clears all session data. |
| `app.session_interface` | The session interface for the application. Defaults to `SecureCookieSessionInterface`. |
| `SecureCookieSessionInterface` | Default session interface that stores session data in signed cookies. |
| `Session` | Base session class. |
| `app.secret_key` | The secret key used for signing session cookies. Must be set for session to work. |
| `app.permanent_session_lifetime` | The lifetime of permanent sessions in seconds. Defaults to 31 days. |
| `app.session_cookie_name` | The name of the session cookie. Defaults to `session`. |
| `app.session_cookie_path` | The path for the session cookie. Defaults to `/`. |
| `app.session_cookie_domain` | The domain for the session cookie. |
| `app.session_cookie_secure` | Whether the session cookie is secure (HTTPS only). Defaults to `False`. |
| `app.session_cookie_httponly` | Whether the session cookie is HTTP-only. Defaults to `True`. |
| `app.session_cookie_samesite` | The SameSite attribute for the session cookie. Defaults to `Lax`. |

---

## Error Handling

| Code | Description |
|------|-------------|
| `abort(code, description=None)` | Raises an `HTTPException` for the given status code. Optionally includes a description. |
| `@app.errorhandler(code_or_exception)` | Decorator to register a function as an error handler for a specific HTTP status code or exception. |
| `app.errorhandler(code_or_exception)(f)` | Registers a function as an error handler for a specific HTTP status code or exception. |
| `HTTPException(code, description=None)` | Base class for HTTP exceptions. Subclasses include `BadRequest`, `Unauthorized`, `Forbidden`, `NotFound`, etc. |
| `BadRequest(description=None)` | 400 Bad Request exception. |
| `Unauthorized(description=None)` | 401 Unauthorized exception. |
| `Forbidden(description=None)` | 403 Forbidden exception. |
| `NotFound(description=None)` | 404 Not Found exception. |
| `MethodNotAllowed(description=None)` | 405 Method Not Allowed exception. |
| `InternalServerError(description=None)` | 500 Internal Server Error exception. |
| `app.register_error_handler(code_or_exception, f)` | Registers a function as an error handler for a specific HTTP status code or exception. |
| `app.handle_exception(e)` | Handles an exception by returning a response. |
| `app.handle_user_exception(e)` | Handles a user exception by returning a response. |

---

## Blueprints

| Code | Description |
|------|-------------|
| `Blueprint(name, import_name, static_folder=None, static_url_path=None, template_folder=None, url_prefix=None, subdomain=None, url_defaults=None, root_path=None, cli_group=None)` | Creates a blueprint for organizing related routes and resources. |
| `blueprint.route(rule, **options)` | Decorator to bind a URL rule to a view function within a blueprint. |
| `blueprint.add_url_rule(rule, endpoint, view_func, **options)` | Adds a URL rule to the blueprint. |
| `blueprint.errorhandler(code_or_exception)(f)` | Decorator to register an error handler for a blueprint. |
| `blueprint.before_request(f)` | Decorator to register a function to run before each request to the blueprint. |
| `blueprint.after_request(f)` | Decorator to register a function to run after each request to the blueprint. |
| `blueprint.teardown_request(f)` | Decorator to register a function to run after each request to the blueprint, even if an exception occurs. |
| `blueprint.before_app_request(f)` | Decorator to register a function to run before each request to the application, but only if the request is dispatched to the blueprint. |
| `blueprint.after_app_request(f)` | Decorator to register a function to run after each request to the application, but only if the request is dispatched to the blueprint. |
| `blueprint.teardown_app_request(f)` | Decorator to register a function to run after each request to the application, even if an exception occurs, but only if the request is dispatched to the blueprint. |
| `blueprint.context_processor(f)` | Decorator to register a template context processor for the blueprint. |
| `blueprint.app_context_processor(f)` | Decorator to register an application context processor for the blueprint. |
| `blueprint.app_template_filter(name)(f)` | Decorator to register a template filter for the application. |
| `blueprint.app_template_global(name)(f)` | Decorator to register a template global for the application. |
| `blueprint.app_template_test(name)(f)` | Decorator to register a template test for the application. |
| `blueprint.register(app, options)` | Registers the blueprint with an application. |
| `app.register_blueprint(blueprint, **options)` | Registers a blueprint with the application. |

---

## CLI Commands

| Code | Description |
|------|-------------|
| `flask run` | Runs the Flask development server. |
| `flask run --host=0.0.0.0` | Runs the Flask development server on all network interfaces. |
| `flask run --port=8080` | Runs the Flask development server on a specific port. |
| `flask run --debug` | Runs the Flask development server with debug mode enabled. |
| `flask run --reload` | Runs the Flask development server with automatic reloader enabled. |
| `flask shell` | Starts an interactive Python shell with the Flask application context loaded. |
| `flask shell --command='command'` | Executes a command in the Flask shell context. |
| `@app.cli.command(name)` | Decorator to register a custom CLI command. |
| `@app.cli.command_context(f)` | Decorator to register a context processor for CLI commands. |
| `click` | The Click library used for Flask CLI commands. |
| `app.cli` | The Click command line interface for the application. |

---
## Context Management

| Code | Description |
|------|-------------|
| `app.app_context()` | Creates an application context for the application. |
| `app.request_context(environ)` | Creates a request context for the application. |
| `app.test_request_context(path='/', method='GET', headers=None, **kwargs)` | Creates a test request context for the application. |
| `app.test_client(use_cookies=True)` | Creates a test client for the application. |
| `current_app` | Proxy to the current Flask application handling the active request. |
| `g` | A namespace object for storing data during a single request. |
| `request` | Proxy to the current request object. |
| `session` | Proxy to the current session object. |
| `has_app_context()` | Returns `True` if an application context is active. |
| `has_request_context()` | Returns `True` if a request context is active. |
| `app_context_popped` | Signal sent when an application context is popped. |
| `request_context_popped` | Signal sent when a request context is popped. |
| `appcontext_pushed` | Signal sent when an application context is pushed. |
| `requestcontext_pushed` | Signal sent when a request context is pushed. |

---
## Signals

| Code | Description |
|------|-------------|
| `before_request` | Signal sent before a request is dispatched to the view function. |
| `after_request` | Signal sent after a request is dispatched to the view function. |
| `teardown_request` | Signal sent after a request is dispatched, even if an exception occurs. |
| `before_first_request` | Signal sent before the first request to the application. |
| `after_this_request` | Signal sent after the current request is dispatched. |
| `got_request_exception` | Signal sent when an exception occurs during request handling. |
| `appcontext_tearing_down` | Signal sent when an application context is about to be torn down. |
| `appcontext_pushed` | Signal sent when an application context is pushed. |
| `appcontext_popped` | Signal sent when an application context is popped. |
| `requestcontext_pushed` | Signal sent when a request context is pushed. |
| `requestcontext_popped` | Signal sent when a request context is popped. |
| `message_flashed` | Signal sent when a message is flashed via the `flash()` function. |
| `template_rendered` | Signal sent after a template is rendered. |
| `request_started` | Signal sent when a request starts being processed. |
| `request_finished` | Signal sent when a request finishes being processed. |
| `signals` | The Flask signal namespace. |

---
## Testing

| Code | Description |
|------|-------------|
| `FlaskTestCase` | Base test case class for Flask applications. |
| `app.test_client()` | Creates a test client for the application. The client simulates HTTP requests. |
| `client.get(path, **kwargs)` | Sends a GET request to the specified path. Returns a `Response` object. |
| `client.post(path, data=None, **kwargs)` | Sends a POST request to the specified path. `data` can be a dictionary or bytes. |
| `client.put(path, data=None, **kwargs)` | Sends a PUT request to the specified path. |
| `client.delete(path, **kwargs)` | Sends a DELETE request to the specified path. |
| `client.patch(path, data=None, **kwargs)` | Sends a PATCH request to the specified path. |
| `client.head(path, **kwargs)` | Sends a HEAD request to the specified path. |
| `client.options(path, **kwargs)` | Sends an OPTIONS request to the specified path. |
| `client.open(path, method='GET', **kwargs)` | Sends a request to the specified path with the given method. |
| `client.session` | The session object for the test client. |
| `client.cookie_jar` | The cookie jar for the test client. |
| `app.test_request_context(path='/', method='GET', headers=None, **kwargs)` | Creates a test request context for the application. |
| `app.test_cli_runner()` | Creates a CLI runner for testing Flask CLI commands. |
| `runner.invoke(args, input=None, catch_exceptions=False)` | Invokes a CLI command with the given arguments. |
| `runner.get_output()` | Returns the output of the last CLI command invocation. |

---
## Utilities and Helpers

| Code | Description |
|------|-------------|
| `escape(s)` | Escapes special characters in a string for HTML. |
| `Markup(s)` | Marks a string as safe for HTML rendering. |
| `safe_join(directory, *paths)` | Safely joins a directory with one or more path components, preventing directory traversal. |
| `url_for(endpoint, **values)` | Generates a URL for the given endpoint with the specified values for variable parts. |
| `get_flashed_messages(with_categories=false, category_filter=[])` | Retrieves flashed messages from the session. |
| `flash(message, category='message')` | Flashes a message to the next request. The message is stored in the session. |
| `make_response(*args)` | Creates a `Response` object from the return value of a view function. |
| `jsonify(*args, **kwargs)` | Creates a `Response` object with a JSON-encoded body. |
| `send_file(path_or_file, **kwargs)` | Sends a file as a response. |
| `send_from_directory(directory, path, **kwargs)` | Sends a file from a directory as a response. |
| `stream_with_context(generator_or_function)` | Wraps a generator or function to ensure it runs within the correct request context. |
| `app.open_resource(resource, mode='rb')` | Opens a resource from the application's static or templates folder. |
| `app.open_instance_resource(resource, mode='rb')` | Opens a resource from the application's instance folder. |
| `app.import_name` | The import name of the application. |
| `app.name` | The name of the application. |
| `app.instance_path` | The path to the application's instance folder. |
| `app.root_path` | The root path for the application. |
| `app.static_folder` | The folder containing the application's static files. |
| `app.static_url_path` | The URL path for the application's static files. |
| `app.template_folder` | The folder containing the application's templates. |

---
## Configuration

| Code | Description |
|------|-------------|
| `Config(root_path=None)` | Creates a configuration object. |
| `config.from_object(obj)` | Loads configuration from a Python object. |
| `config.from_pyfile(filename, silent=False)` | Loads configuration from a Python file. |
| `config.from_json(json_str)` | Loads configuration from a JSON string. |
| `config.from_prefixed_env(prefix)` | Loads configuration from environment variables with a given prefix. |
| `config.from_envvar(key, silent=False)` | Loads configuration from an environment variable. |
| `config.get(key, default=None)` | Retrieves a configuration value. |
| `config.setdefault(key, value)` | Sets a configuration key to the given value if it is not already set. |
| `config.update(dict)` | Updates the configuration with the given dictionary. |
| `config.get_namespace(prefix, lowercase=True, trim_prefix=True)` | Retrieves all configuration keys with the given prefix as a dictionary. |
| `app.config` | The configuration object for the application. |

---
## Extensions

| Code | Description |
|------|-------------|
| `Extension` | Base class for Flask extensions. |
| `app.extensions` | A dictionary for storing extension-specific data. |
| `app.teardown_appcontext(f)` | Registers a function to run when the application context is torn down. |
| `app.before_request(f)` | Registers a function to run before each request. |
| `app.after_request(f)` | Registers a function to run after each request. |
| `app.teardown_request(f)` | Registers a function to run after each request, even if an exception occurs. |
| `app.before_first_request(f)` | Registers a function to run before the first request. |
| `app.after_this_request(f)` | Registers a function to run after the current request. |
| `app.context_processor(f)` | Registers a template context processor. |
| `app.template_filter(name)(f)` | Registers a template filter. |
| `app.template_global(name)(f)` | Registers a template global. |
| `app.template_test(name)(f)` | Registers a template test. |
| `app.add_template_filter(f, name=None)` | Adds a template filter. |
| `app.add_template_global(f, name=None)` | Adds a template global. |
| `app.add_template_test(f, name=None)` | Adds a template test. |

---
## Logging

| Code | Description |
|------|-------------|
| `app.logger` | The logger for the application. |
| `current_app.logger` | The logger for the current application. |
| `app.logger.debug(message)` | Logs a debug message. |
| `app.logger.info(message)` | Logs an info message. |
| `app.logger.warning(message)` | Logs a warning message. |
| `app.logger.error(message)` | Logs an error message. |
| `app.logger.critical(message)` | Logs a critical message. |
| `app.logger.exception(message)` | Logs an exception with traceback. |
| `logging` | The Python logging module used by Flask. |

---
## WSGI Utilities

| Code | Description |
|------|-------------|
| `Flask.__call__(self, environ, start_response)` | WSGI entry point for the Flask application. |
| `app.wsgi_app` | The WSGI application for the Flask app. |
| `app.make_default_options_response()` | Creates a default response for OPTIONS requests. |
| `app.handle_url_build_error(error, endpoint, values)` | Handles URL build errors. |
| `app.dispatch_request()` | Dispatches the request to the appropriate view function. |
| `app.full_dispatch_request()` | Fully dispatches the request, including before/after request hooks. |
| `app.preprocess_request()` | Preprocesses the request before dispatching. |
| `app.process_response(response)` | Processes the response after dispatching. |
| `app.finalize_request(response)` | Finalizes the request after processing. |
| `app.handle_exception(e)` | Handles an exception during request processing. |
| `app.handle_user_exception(e)` | Handles a user exception during request processing. |

---
## JSON and Data Handling

| Code | Description |
|------|-------------|
| `json` | The Python `json` module re-exported by Flask. |
| `jsonify(*args, **kwargs)` | Creates a `Response` object with a JSON-encoded body. |
| `request.get_json(silent=False)` | Parses JSON data from the request body. |
| `request.is_json` | `True` if the request has a JSON content type. |
| `app.json_encoder` | The JSON encoder for the application. Defaults to `JSONEncoder`. |
| `app.json_decoder` | The JSON decoder for the application. Defaults to `JSONDecoder`. |
| `JSONEncoder` | Flask's JSON encoder class. Extends `json.JSONEncoder`. |
| `JSONDecoder` | Flask's JSON decoder class. Extends `json.JSONDecoder`. |
| `app.make_default_json_encoder()` | Creates a default JSON encoder for the application. |
| `app.make_default_json_decoder()` | Creates a default JSON decoder for the application. |

---
## File and Static Handling

| Code | Description |
|------|-------------|
| `send_file(path_or_file, mimetype=None, as_attachment=False, download_name=None, **kwargs)` | Sends a file as a response. |
| `send_from_directory(directory, path, mimetype=None, as_attachment=False, download_name=None, **kwargs)` | Sends a file from a directory as a response. |
| `app.send_static_file(filename)` | Sends a static file from the application's static folder. |
| `app.static_url_path` | The URL path for the application's static files. |
| `app.static_folder` | The folder containing the application's static files. |
| `app.add_static_view(rule, endpoint, view_func)` | Adds a static view for serving static files. |

---
## Caching

| Code | Description |
|------|-------------|
| `app.cache` | The cache object for the application. |
| `app.make_default_cache()` | Creates a default cache for the application. |
| `Cache(app, config=None, **kwargs)` | Creates a cache object for the application. |
| `cache.set(key, value, timeout=None)` | Sets a value in the cache with an optional timeout. |
| `cache.get(key)` | Retrieves a value from the cache. |
| `cache.delete(key)` | Deletes a value from the cache. |
| `cache.clear()` | Clears all values from the cache. |
| `cache.add(key, value, timeout=None)` | Adds a value to the cache if it does not already exist. |
| `cache.replace(key, value, timeout=None)` | Replaces a value in the cache if it already exists. |

---
## Security

| Code | Description |
|------|-------------|
| `app.secret_key` | The secret key used for signing session cookies and other security-related operations. |
| `app.permanent_session_lifetime` | The lifetime of permanent sessions in seconds. |
| `session.permanent` | Whether the session should be permanent. |
| `app.session_cookie_secure` | Whether the session cookie is secure (HTTPS only). |
| `app.session_cookie_httponly` | Whether the session cookie is HTTP-only. |
| `app.session_cookie_samesite` | The SameSite attribute for the session cookie. |
| `SecureCookieSessionInterface` | Default session interface that stores session data in signed cookies. |
| `itsdangerous` | The itsdangerous library used by Flask for signing and unsigning data. |