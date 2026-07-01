## **Django Core Framework**

---
### **Settings and Configuration**

| Setting | Description |
|---------|-------------|
| `DEBUG` | Boolean that enables/disables debug mode. Never use in production |
| `SECRET_KEY` | A secret key used for cryptographic signing. Required for security |
| `ALLOWED_HOSTS` | List of strings representing host/domain names the app can serve |
| `INSTALLED_APPS` | List of strings designating all applications that are enabled in this Django installation |
| `MIDDLEWARE` | List of middleware classes to use. Order matters |
| `ROOT_URLCONF` | Python path to a module containing URL patterns for the project |
| `WSGI_APPLICATION` | Full Python path to the WSGI application object |
| `DATABASES` | Dictionary containing the settings for all databases |
| `DEFAULT_AUTO_FIELD` | Default primary key field type for models |
| `TEMPLATES` | List of dictionaries containing the settings for all template engines |
| `STATIC_URL` | URL prefix for static files |
| `STATIC_ROOT` | Absolute filesystem path to the directory where static files are collected |
| `STATICFILES_DIRS` | List of directories where static files are stored |
| `STATICFILES_STORAGE` | Storage backend for static files |
| `MEDIA_URL` | URL prefix for media files |
| `MEDIA_ROOT` | Absolute filesystem path to the directory for user-uploaded files |
| `LANGUAGE_CODE` | Language code for this installation. Default is 'en-us' |
| `TIME_ZONE` | Time zone for this installation. Default is 'UTC' |
| `USE_I18N` | Boolean that specifies if Django's translation should be enabled |
| `USE_L10N` | Boolean that specifies if localized formatting should be enabled |
| `USE_TZ` | Boolean that specifies if datetimes should be timezone-aware |
| `DEFAULT_CHARSET` | Default charset to use for all HttpResponse objects |
| `FILE_CHARSET` | Charset to use for encoding files |
| `DEFAULT_CONTENT_TYPE` | Default content type to use for HttpResponse objects |
| `SESSION_COOKIE_AGE` | Age of session cookies in seconds |
| `SESSION_COOKIE_DOMAIN` | Domain to use for session cookies |
| `SESSION_COOKIE_HTTPONLY` | Boolean that controls whether the session cookie is HTTP-only |
| `SESSION_COOKIE_NAME` | Name to use for the session cookie |
| `SESSION_COOKIE_PATH` | Path to use for the session cookie |
| `SESSION_COOKIE_SAMESITE` | SameSite attribute for the session cookie |
| `SESSION_COOKIE_SECURE` | Boolean that controls whether the session cookie is secure |
| `SESSION_ENGINE` | Dot path to the session engine to use |
| `SESSION_FILE_PATH` | Directory to store session files if using file-based sessions |
| `SESSION_SAVE_EVERY_REQUEST` | Boolean that controls whether to save the session on every request |
| `SESSION_SERIALIZER` | Dot path to the session serializer class to use |
| `CSRF_COOKIE_AGE` | Age of CSRF cookies in seconds |
| `CSRF_COOKIE_DOMAIN` | Domain to use for CSRF cookies |
| `CSRF_COOKIE_HTTPONLY` | Boolean that controls whether the CSRF cookie is HTTP-only |
| `CSRF_COOKIE_NAME` | Name to use for the CSRF cookie |
| `CSRF_COOKIE_PATH` | Path to use for the CSRF cookie |
| `CSRF_COOKIE_SAMESITE` | SameSite attribute for the CSRF cookie |
| `CSRF_COOKIE_SECURE` | Boolean that controls whether the CSRF cookie is secure |
| `CSRF_TRUSTED_ORIGINS` | List of trusted origins for CSRF validation |
| `CSRF_USE_SESSIONS` | Boolean that controls whether to store CSRF token in session |
| `LOGGING` | Dictionary containing logging configuration |
| `LOGGING_CONFIG` | Default logging configuration |
| `PASSWORD_HASHERS` | List of password hasher backends to use |
| `PASSWORD_HASH_ITERATIONS` | Default number of iterations for PBKDF2 password hashing |
| `AUTH_USER_MODEL` | Dot path to the custom user model to use |
| `AUTHENTICATION_BACKENDS` | List of authentication backends to use |
| `LOGIN_URL` | URL to redirect to for login |
| `LOGIN_REDIRECT_URL` | URL to redirect to after login |
| `LOGOUT_URL` | URL to redirect to for logout |
| `LOGOUT_REDIRECT_URL` | URL to redirect to after logout |
| `LOGIN_REDIRECT_URL` | URL to redirect to after login |
| `PASSWORD_RESET_TIMEOUT` | Number of days a password reset link is valid |
| `AUTH_PASSWORD_VALIDATORS` | List of password validators to use |
| `EMAIL_BACKEND` | Dot path to the email backend to use |
| `EMAIL_HOST` | SMTP server host for sending emails |
| `EMAIL_PORT` | SMTP server port for sending emails |
| `EMAIL_USE_TLS` | Boolean that controls whether to use TLS for email connections |
| `EMAIL_USE_SSL` | Boolean that controls whether to use SSL for email connections |
| `EMAIL_HOST_USER` | Username to use for SMTP authentication |
| `EMAIL_HOST_PASSWORD` | Password to use for SMTP authentication |
| `EMAIL_TIMEOUT` | Timeout in seconds for email connections |
| `DEFAULT_FROM_EMAIL` | Default email address to use for various automated emails |
| `SERVER_EMAIL` | Email address to use for error notifications |
| `ADMINS` | List of tuples containing admin names and email addresses |
| `MANAGERS` | List of tuples containing manager names and email addresses |
| `DATA_UPLOAD_MAX_MEMORY_SIZE` | Maximum size in bytes for request body data |
| `DATA_UPLOAD_MAX_NUMBER_FIELDS` | Maximum number of form fields to process |
| `FILE_UPLOAD_MAX_MEMORY_SIZE` | Maximum size in bytes for file uploads to memory |
| `FILE_UPLOAD_TEMP_DIR` | Directory to store temporary files during upload |
| `FILE_UPLOAD_PERMISSIONS` | File permissions for uploaded files |
| `FILE_UPLOAD_DIRECTORY_PERMISSIONS` | Directory permissions for uploaded files |
| `MESSAGE_STORAGE` | Storage backend for messages framework |
| `MESSAGE_TAGS` | Dictionary mapping message levels to tags |
| `INTERNAL_IPS` | List of IP addresses that are allowed to access debug pages |
| `ALLOWED_HOSTS` | List of host/domain names that the app can serve |
| `SECURE_PROXY_SSL_HEADER` | Tuple of HTTP header name and value to check for secure connections |
| `SECURE_SSL_REDIRECT` | Boolean that controls whether to redirect all non-HTTPS requests to HTTPS |
| `SECURE_HSTS_SECONDS` | Number of seconds for HTTP Strict Transport Security |
| `SECURE_HSTS_INCLUDE_SUBDOMAINS` | Boolean that controls whether to include subdomains in HSTS |
| `SECURE_HSTS_PRELOAD` | Boolean that controls whether to preload HSTS |
| `SECURE_CONTENT_TYPE_NOSNIFF` | Boolean that controls whether to send X-Content-Type-Options header |
| `SECURE_BROWSER_XSS_FILTER` | Boolean that controls whether to send X-XSS-Protection header |
| `SECURE_REFERRER_POLICY` | Referrer-Policy header value |
| `SECURE_CROSS_ORIGIN_OPENER_POLICY` | Cross-Origin-Opener-Policy header value |
| `SECURE_CROSS_ORIGIN_EMBEDDER_POLICY` | Cross-Origin-Embedder-Policy header value |
| `X_FRAME_OPTIONS` | X-Frame-Options header value |
| `REFERRER_POLICY` | Referrer-Policy header value |
| `CROSS_ORIGIN_OPENER_POLICY` | Cross-Origin-Opener-Policy header value |
| `CROSS_ORIGIN_EMBEDDER_POLICY` | Cross-Origin-Embedder-Policy header value |
| `PERMALINKS_USES_APP_LANGUAGE` | Boolean that controls whether to use app language for permalinks |
| `SITE_ID` | Default site ID for the sites framework |
| `SITE_NAME` | Human-readable name for the site |
| `APPEND_SLASH` | Boolean that controls whether to append trailing slashes to URLs |
| `PREPEND_WWW` | Boolean that controls whether to prepend 'www.' to URLs |
| `DEFAULT_INDEX_TABLESPACE` | Default tablespace for index creation |
| `DEFAULT_TABLESPACE` | Default tablespace for table creation |
| `DB_BACKENDS` | Dictionary of database backend settings |
| `FIXTURE_DIRS` | List of directories where fixtures are stored |
| `NUMBER_GROUPING` | Number grouping for localized formatting |
| `DECIMAL_SEPARATOR` | Decimal separator for localized formatting |
| `THOUSAND_SEPARATOR` | Thousand separator for localized formatting |
| `DATE_FORMAT` | Default date format |
| `DATE_INPUT_FORMATS` | List of formats to try when parsing date input |
| `DATETIME_FORMAT` | Default datetime format |
| `DATETIME_INPUT_FORMATS` | List of formats to try when parsing datetime input |
| `TIME_FORMAT` | Default time format |
| `TIME_INPUT_FORMATS` | List of formats to try when parsing time input |
| `YEAR_MONTH_FORMAT` | Default year-month format |
| `MONTH_DAY_FORMAT` | Default month-day format |
| `SHORT_DATE_FORMAT` | Default short date format |
| `SHORT_DATETIME_FORMAT` | Default short datetime format |
| `FIRST_DAY_OF_WEEK` | First day of the week (0=Sunday, 1=Monday, etc.) |

---
---
### **Django Management Commands**

| Command | Description |
|---------|-------------|
| `check` | Checks the entire Django project for potential problems |
| `compilemessages` | Compiles .po files created by makemessages to .mo files for use with builtin gettext support |
| `createcachetable` | Creates the cache table for a specified cache backend |
| `dbshell` | Runs the command-line client for the database specified in DATABASES |
| `diffsettings` | Displays the differences between the current settings and Django's default settings |
| `dumpdata` | Outputs the contents of the database as a fixture to standard output |
| `flush` | Removes all data from the database and re-installs initial data |
| `inspectdb` | Introspects the database tables in DATABASES and outputs a Django model module to standard output |
| `loaddata` | Installs the named fixture(s) in the database |
| `makemessages` | Runs over the entire source tree of the current directory and pulls out all strings marked for translation |
| `makemigrations` | Creates new migrations based on changes detected to your models |
| `migrate` | Applies and unapplies database migrations |
| `optimizemigration` | Optimizes a migration |
| `runserver` | Starts a lightweight development Web server on the local machine |
| `shell` | Starts the Python interactive interpreter |
| `showmigrations` | Lists a project's migrations and their status |
| `showurls` | Displays all URL patterns in the project |
| `sqlflush` | Prints the SQL statements that would be executed for the flush command |
| `sqlmigrate` | Prints the SQL statements for the specified migration |
| `squashmigrations` | Squashes migrations for an app |
| `startapp` | Creates a Django app directory structure for the given app name |
| `startproject` | Creates a Django project directory structure for the given project name |
| `test` | Runs the test suite for the specified applications |
| `testserver` | Runs a development server with data from the given fixture(s) |

---
---
---
## **Django URL Routing**

---
### **URL Configuration Functions and Classes**

| Function/Class | Description |
|----------------|-------------|
| `django.urls.path(route, view, kwargs=None, name=None)` | Defines a URL pattern with a route and view |
| `django.urls.re_path(route, view, kwargs=None, name=None)` | Defines a URL pattern with a regex route and view |
| `django.urls.include(module, namespace=None)` | Includes other URL configurations |
| `django.urls.register_converter(Converter, type_name)` | Registers a custom path converter |
| `django.urls.reverse(viewname, urlconf=None, args=None, kwargs=None)` | Returns a URL matching a view and arguments |
| `django.urls.reverse_lazy(viewname, urlconf=None, args=None, kwargs=None)` | Lazy version of reverse() |
| `django.urls.resolve(path, urlconf=None)` | Resolves a URL path to a view, arguments, and other metadata |
| `django.urls.clear_url_caches()` | Clears all URL caches |
| `django.urls.get_urlconf(module_name)` | Returns the URLconf module for the given module name |
| `django.urls.set_urlconf(urlconf)` | Sets the URLconf module for the current thread |
| `django.urls.get_resolver(urlconf_module)` | Returns the resolver for the given URLconf module |
| `django.urls.get_script_prefix()` | Returns the script prefix for the current request |
| `django.urls.set_script_prefix(prefix)` | Sets the script prefix for the current request |

---
### **Path Converters**

| Converter | Description |
|-----------|-------------|
| `str` | Matches any non-empty string (default) |
| `int` | Matches zero or any positive integer |
| `slug` | Matches slug strings (ASCII letters or numbers, plus hyphens and underscores) |
| `uuid` | Matches UUID strings |
| `path` | Matches any string including the path separator '/' |
| `Registering custom converters` | Can register custom converters using `register_converter()` |

---
---
---
## **Django HTTP Handling**

---
### **Request and Response Classes**

| Class | Description |
|-------|-------------|
| `django.http.HttpRequest` | Represents an HTTP request |
| `django.http.HttpResponse` | Represents an HTTP response |
| `django.http.HttpResponseRedirect` | HTTP response with redirect status code |
| `django.http.HttpResponsePermanentRedirect` | HTTP response with permanent redirect status code |
| `django.http.HttpResponseNotModified` | HTTP response with not modified status code |
| `django.http.HttpResponseBadRequest` | HTTP response with bad request status code |
| `django.http.HttpResponseForbidden` | HTTP response with forbidden status code |
| `django.http.HttpResponseNotFound` | HTTP response with not found status code |
| `django.http.HttpResponseServerError` | HTTP response with server error status code |
| `django.http.HttpResponseNotAllowed` | HTTP response with method not allowed status code |
| `django.http.HttpResponseGone` | HTTP response with gone status code |
| `django.http.JsonResponse` | HTTP response with JSON content type |
| `django.http.StreamingHttpResponse` | HTTP response with streaming content |
| `django.http.FileResponse` | HTTP response with file content |
| `django.http.Http404` | Exception for 404 not found errors |
| `django.http.HttpResponseBase` | Base class for HTTP responses |
| `django.http.UnreadablePostError` | Exception raised when POST data cannot be read |

---
### **HttpRequest Attributes**

| Attribute | Description |
|-----------|-------------|
| `request.method` | A string representing the HTTP method (GET, POST, etc.) |
| `request.GET` | A dictionary-like object containing GET parameters |
| `request.POST` | A dictionary-like object containing POST parameters |
| `request.COOKIES` | A dictionary containing all cookies |
| `request.FILES` | A dictionary-like object containing uploaded files |
| `request.META` | A dictionary containing all available HTTP headers |
| `request.body` | The raw HTTP request body as bytes |
| `request.content_type` | The content type of the request |
| `request.content_length` | The content length of the request |
| `request.content_params` | A dictionary of content parameters from the Content-Type header |
| `request.path` | The path portion of the URL |
| `request.path_info` | The path portion of the URL including PATH_INFO |
| `request.full_path` | The full path including query string and fragment |
| `request.full_path_info` | The full path including PATH_INFO, query string, and fragment |
| `request.build_absolute_uri(location=None)` | Builds an absolute URI from the location |
| `request.get_full_path()` | Returns the full path including query string and fragment |
| `request.get_full_path_info()` | Returns the full path including PATH_INFO, query string, and fragment |
| `request.get_host()` | Returns the origin host based on HTTP headers |
| `request.get_port()` | Returns the port number based on HTTP headers |
| `request.get_raw_uri()` | Returns the raw URI (including scheme and domain) |
| `request.is_ajax()` | Returns True if the request was made via an XMLHttpRequest |
| `request.is_secure()` | Returns True if the request was made over HTTPS |
| `request.scheme` | The scheme of the request (http or https) |
| `request.headers` | A case-insensitive dictionary of HTTP headers |
| `request.resolver_match` | The resolver match for the current request |

---
### **HttpRequest Methods**

| Method | Description |
|--------|-------------|
| `request.get(name, default=None)` | Returns the value of the GET parameter with the given name |
| `request.getlist(name)` | Returns a list of all values for the GET parameter with the given name |
| `request.post(name, default=None)` | Returns the value of the POST parameter with the given name |
| `request.postlist(name)` | Returns a list of all values for the POST parameter with the given name |
| `request.cookies.get(name, default=None)` | Returns the value of the cookie with the given name |
| `request.META.get(name, default=None)` | Returns the value of the HTTP header with the given name |
| `request.headers.get(name, default=None)` | Returns the value of the HTTP header with the given name (case-insensitive) |
| `request.has_header(name)` | Returns True if the request has the specified header (case-insensitive) |

---
### **HttpResponse Methods**

| Method | Description |
|--------|-------------|
| `response.write(content)` | Writes content to the response |
| `response.tell()` | Returns the current position in the response content |
| `response.flush()` | Flushes the response content |
| `response.close()` | Closes the response |
| `response.set_cookie(key, value='', max_age=None, expires=None, path='/', domain=None, secure=False, httponly=True, samesite=None)` | Sets a cookie in the response |
| `response.delete_cookie(key, path='/', domain=None)` | Deletes a cookie from the response |
| `response.setdefault(key, value)` | Sets a header if it is not already set |
| `response.delete_header(key)` | Deletes a header from the response |
| `response.has_header(key)` | Returns True if the response has the specified header (case-insensitive) |

---
---
---
## **Django Views**

---
### **View Functions and Decorators**

| Function/Decorator | Description |
|---------------------|-------------|
| `django.views.decorators.http.require_http_methods(request_method_list)` | Decorator to require specific HTTP methods |
| `django.views.decorators.http.require_GET` | Decorator to require GET method |
| `django.views.decorators.http.require_POST` | Decorator to require POST method |
| `django.views.decorators.http.require_safe` | Decorator to require safe methods (GET, HEAD, OPTIONS) |
| `django.views.decorators.csrf.csrf_protect(view_func)` | Decorator to add CSRF protection to a view |
| `django.views.decorators.csrf.csrf_exempt(view_func)` | Decorator to exempt a view from CSRF protection |
| `django.views.decorators.csrf.requires_csrf_token(view_func)` | Decorator to require CSRF token for a view |
| `django.views.decorators.cache.cache_page(timeout, cache=None, key_prefix=None)` | Decorator to cache the entire view response |
| `django.views.decorators.cache.cache_control(**kwargs)` | Decorator to add cache-control headers to the response |
| `django.views.decorators.cache.never_cache(view_func)` | Decorator to add headers to disable caching |
| `django.views.decorators.vary.vary_on_headers(*headers)` | Decorator to add Vary headers to the response |
| `django.views.decorators.vary.vary_on_cookie` | Decorator to add Vary: Cookie header to the response |
| `django.views.decorators.gzip.gzip_page(view_func)` | Decorator to compress the response with gzip |
| `django.views.decorators.clickjacking.xframe_options_deny` | Decorator to set X-Frame-Options: DENY header |
| `django.views.decorators.clickjacking.xframe_options_sameorigin` | Decorator to set X-Frame-Options: SAMEORIGIN header |
| `django.views.decorators.clickjacking.xframe_options_exempt` | Decorator to exempt a view from X-Frame-Options header |
| `django.views.decorators.debug.sensitive_variables(*variables)` | Decorator to mark variables as sensitive for debug pages |
| `django.views.decorators.debug.sensitive_post_parameters(*parameters)` | Decorator to mark POST parameters as sensitive for debug pages |
| `django.views.decorators.http.condition(etag_func=None, last_modified_func=None)` | Decorator to add conditional GET support |
| `django.views.decorators.http.etag(etag_func)` | Decorator to add ETag header to the response |
| `django.views.decorators.http.last_modified(last_modified_func)` | Decorator to add Last-Modified header to the response |

---
---
### **Class-Based Views**

| Class | Description |
|-------|-------------|
| `django.views.generic.View` | Base class for all class-based views |
| `django.views.generic.base.TemplateView` | Renders a template |
| `django.views.generic.base.RedirectView` | Redirects to a URL |
| `django.views.generic.base.ContextMixin` | Mixin for adding context data to views |
| `django.views.generic.base.TemplateResponseMixin` | Mixin for rendering templates |
| `django.views.generic.detail.DetailView` | Displays a single object |
| `django.views.generic.detail.SingleObjectTemplateResponseMixin` | Mixin for single object template responses |
| `django.views.generic.detail.SingleObjectMixin` | Mixin for single object operations |
| `django.views.generic.list.ListView` | Displays a list of objects |
| `django.views.generic.list.MultipleObjectTemplateResponseMixin` | Mixin for multiple object template responses |
| `django.views.generic.list.MultipleObjectMixin` | Mixin for multiple object operations |
| `django.views.generic.edit.FormView` | Displays a form |
| `django.views.generic.edit.CreateView` | Creates a new object |
| `django.views.generic.edit.UpdateView` | Updates an existing object |
| `django.views.generic.edit.DeleteView` | Deletes an existing object |
| `django.views.generic.edit.FormMixin` | Mixin for form handling |
| `django.views.generic.edit.SingleObjectFormMixin` | Mixin for single object form handling |
| `django.views.generic.edit.ModelFormMixin` | Mixin for model form handling |
| `django.views.generic.edit.ProcessFormView` | Mixin for form processing |
| `django.views.generic.edit.BaseCreateView` | Base class for create views |
| `django.views.generic.edit.BaseUpdateView` | Base class for update views |
| `django.views.generic.edit.BaseDeleteView` | Base class for delete views |
| `django.views.generic.edit.BaseFormView` | Base class for form views |
| `django.views.generic.dates.ArchiveIndexView` | Displays a list of dates with object counts |
| `django.views.generic.dates.YearArchiveView` | Displays a list of objects from a specific year |
| `django.views.generic.dates.MonthArchiveView` | Displays a list of objects from a specific month |
| `django.views.generic.dates.WeekArchiveView` | Displays a list of objects from a specific week |
| `django.views.generic.dates.DayArchiveView` | Displays a list of objects from a specific day |
| `django.views.generic.dates.TodayArchiveView` | Displays a list of objects from today |
| `django.views.generic.dates.DateDetailView` | Displays a single object from a specific date |
| `django.views.generic.dates.YearMixin` | Mixin for year-based archive views |
| `django.views.generic.dates.MonthMixin` | Mixin for month-based archive views |
| `django.views.generic.dates.WeekMixin` | Mixin for week-based archive views |
| `django.views.generic.dates.DayMixin` | Mixin for day-based archive views |
| `django.views.generic.dates.BaseDateListView` | Base class for date-based list views |

---
### **Class-Based View Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `view.http_method_names` | List of HTTP methods the view responds to |
| `view.get(request, *args, **kwargs)` | Handles GET requests |
| `view.post(request, *args, **kwargs)` | Handles POST requests |
| `view.put(request, *args, **kwargs)` | Handles PUT requests |
| `view.patch(request, *args, **kwargs)` | Handles PATCH requests |
| `view.delete(request, *args, **kwargs)` | Handles DELETE requests |
| `view.head(request, *args, **kwargs)` | Handles HEAD requests |
| `view.options(request, *args, **kwargs)` | Handles OPTIONS requests |
| `view.trace(request, *args, **kwargs)` | Handles TRACE requests |
| `view.http_method_not_allowed(request, *args, **kwargs)` | Handles requests with unsupported HTTP methods |
| `view.as_view(**initkwargs)` | Returns a function that can be used as a view |
| `view.setup(request, *args, **kwargs)` | Initializes the view before dispatch |
| `view.dispatch(request, *args, **kwargs)` | Dispatches the request to the appropriate handler |
| `view.get_context_data(**kwargs)` | Returns context data for the template |
| `view.get_template_names()` | Returns a list of template names to use |
| `view.render_to_response(context, **response_kwargs)` | Renders the template and returns an HttpResponse |
| `view.get_queryset()` | Returns the queryset to use for the view |
| `view.get_object(queryset=None)` | Returns the object to display |
| `view.get_form_class()` | Returns the form class to use |
| `view.get_form_kwargs()` | Returns the keyword arguments for the form |
| `view.get_form()` | Returns an instance of the form |
| `view.form_valid(form)` | Handles valid form submissions |
| `view.form_invalid(form)` | Handles invalid form submissions |
| `view.get_success_url()` | Returns the URL to redirect to after successful form submission |
| `view.get_context_object_name(obj)` | Returns the context variable name for the object |
| `view.context_object_name` | Name of the context variable for the object |
| `view.template_name` | Name of the template to use |
| `view.template_name_suffix` | Suffix to append to template names |
| `view.content_type` | Content type for the response |
| `view.paginate_by` | Number of items to display per page |
| `view.paginator_class` | Paginator class to use |
| `view.page_kwarg` | Name of the page kwarg in the URLconf |
| `view.context_object_name` | Name of the context variable for the object list |
| `view.allow_empty` | Whether to allow empty lists |
| `view.model` | Model class to use |
| `view.form_class` | Form class to use |
| `view.success_url` | URL to redirect to after successful form submission |
| `view.fields` | Fields to use in the form |
| `view.exclude` | Fields to exclude from the form |
| `view.widgets` | Widgets to use for form fields |
| `view.localized_fields` | Fields to localize in the form |
| `view.prefix` | Prefix to use for form fields |
| `view.initial` | Initial data for the form |
| `view.success_message` | Success message to display after form submission |
| `view.template_name_field` | Name of the field to use for template name |
| `view.template_name_suffix` | Suffix to append to template names |
| `view.date_field` | Name of the date field to use |
| `view.year_field` | Name of the year field to use |
| `view.month_field` | Name of the month field to use |
| `view.day_field` | Name of the day field to use |
| `view.week_field` | Name of the week field to use |
| `view.make_object_list(year, month, day=None)` | Returns a list of objects for the given date |
| `view.get_date_queryset(year, month, day=None)` | Returns the queryset for the given date |
| `view.get_dated_items()` | Returns a list of dated items |
| `view.get_dated_queryset()` | Returns the queryset for dated items |
| `view.get_next_page()` | Returns the next page |
| `view.get_previous_page()` | Returns the previous page |
| `view.paginator` | Paginator instance for the view |

---
---
---
## **Django Models and ORM**

---
### **Model Base Classes and Metaclasses**

| Class | Description |
|-------|-------------|
| `django.db.models.Model` | Base class for all Django models |
| `django.db.models.Manager` | Base class for model managers |
| `django.db.models.QuerySet` | Base class for queryset operations |
| `django.db.models Manager.descriptor` | Descriptor for accessing the manager from model instances |
| `django.db.models.Model._meta` | Options class containing model metadata |
| `django.db.models.options.Options` | Class containing model options |

---
### **Model Field Types**

| Field Type | Description |
|------------|-------------|
| `django.db.models.AutoField` | An integer field that automatically increments |
| `django.db.models.BigAutoField` | A 64-bit integer field that automatically increments |
| `django.db.models.BigIntegerField` | A 64-bit integer field |
| `django.db.models.BinaryField` | A field for storing raw binary data |
| `django.db.models.BooleanField` | A true/false field |
| `django.db.models.CharField` | A string field for small to large strings |
| `django.db.models.CommaSeparatedIntegerField` | A field for storing comma-separated integers (deprecated) |
| `django.db.models.DateField` | A date field |
| `django.db.models.DateTimeField` | A date and time field |
| `django.db.models.DecimalField` | A fixed-precision decimal number field |
| `django.db.models.DurationField` | A field for storing time periods |
| `django.db.models.EmailField` | A string field for email addresses |
| `django.db.models.FileField` | A field for uploading files |
| `django.db.models.FilePathField` | A field for storing filesystem paths |
| `django.db.models.FloatField` | A floating-point number field |
| `django.db.models.GenericIPAddressField` | A field for storing IPv4 or IPv6 addresses |
| `django.db.models.ImageField` | A field for uploading images |
| `django.db.models.IntegerField` | An integer field |
| `django.db.models.IPAddressField` | A field for storing IPv4 addresses (deprecated) |
| `django.db.models.JSONField` | A field for storing JSON data |
| `django.db.models.PositiveBigIntegerField` | A 64-bit positive integer field |
| `django.db.models.PositiveIntegerField` | A positive integer field |
| `django.db.models.PositiveSmallIntegerField` | A positive small integer field |
| `django.db.models.SlugField` | A field for storing slug strings |
| `django.db.models.SmallAutoField` | A small integer field that automatically increments |
| `django.db.models.SmallIntegerField` | A small integer field |
| `django.db.models.TextField` | A large text field |
| `django.db.models.TimeField` | A time field |
| `django.db.models.URLField` | A string field for URLs |
| `django.db.models.UUIDField` | A field for storing UUIDs |
| `django.db.models.ForeignKey` | A many-to-one relationship field |
| `django.db.models.OneToOneField` | A one-to-one relationship field |
| `django.db.models.ManyToManyField` | A many-to-many relationship field |

---
### **Model Field Options**

| Option | Description |
|--------|-------------|
| `null` | If True, the field can be NULL in the database |
| `blank` | If True, the field is allowed to be blank in forms |
| `choices` | A sequence of 2-tuples to use as choices for the field |
| `db_column` | The name of the database column to use for this field |
| `db_index` | If True, a database index will be created for this field |
| `db_tablespace` | The database tablespace to use for this field's index |
| `default` | The default value for the field |
| `editable` | If False, the field will not be displayed in the admin or other ModelForms |
| `error_messages` | A dictionary of error messages for the field |
| `help_text` | Extra help text to display with the form widget |
| `primary_key` | If True, the field is the primary key for the model |
| `unique` | If True, the field must be unique in the database |
| `unique_for_date` | The name of a DateField or DateTimeField to use for unique checks |
| `unique_for_month` | The name of a DateField or DateTimeField to use for unique checks |
| `unique_for_year` | The name of a DateField or DateTimeField to use for unique checks |
| `verbose_name` | A human-readable name for the field |
| `validators` | A list of validators to run on this field |
| `upload_to` | A path to a callable to generate the upload path for FileField and ImageField |
| `max_length` | The maximum length for CharField, EmailField, etc. |
| `max_digits` | The maximum number of digits for DecimalField |
| `decimal_places` | The number of decimal places for DecimalField |
| `auto_now` | If True, the field is automatically set to now on every save |
| `auto_now_add` | If True, the field is automatically set to now when the object is first created |
| `on_delete` | The behavior to use when the referenced object is deleted |
| `related_name` | The name to use for the relation from the related object back to this one |
| `related_query_name` | The name to use for the reverse filter name |
| `limit_choices_to` | A Q object or callable to limit the choices for this field |
| `symmetrical` | If True, ManyToManyField relationships are symmetrical |
| `through` | The intermediate model to use for ManyToManyField relationships |
| `through_fields` | The fields to use for the intermediate model in ManyToManyField relationships |
| `db_constraint` | If True, a database constraint will be created for this field |

---
### **Model Field Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `field.name` | The name of the field |
| `field.model` | The model class this field belongs to |
| `field.related_model` | The related model class for relationship fields |
| `field.null` | Whether the field can be NULL in the database |
| `field.blank` | Whether the field can be blank in forms |
| `field.default` | The default value for the field |
| `field.unique` | Whether the field must be unique in the database |
| `field.primary_key` | Whether the field is the primary key for the model |
| `field.editable` | Whether the field can be edited in forms |
| `field.choices` | The choices for the field |
| `field.max_length` | The maximum length for the field |
| `field.max_digits` | The maximum number of digits for DecimalField |
| `field.decimal_places` | The number of decimal places for DecimalField |
| `field.upload_to` | The upload path for FileField and ImageField |
| `field.verbose_name` | The human-readable name for the field |
| `field.help_text` | The help text for the field |
| `field.validators` | The validators for the field |
| `field.error_messages` | The error messages for the field |
| `field.get_internal_type()` | Returns the internal type of the field |
| `field.db_type(connection)` | Returns the database type for the field |
| `field.get_db_prep_save(value, connection)` | Prepares the value for saving to the database |
| `field.get_db_prep_value(value, connection, prepared=False)` | Prepares the value for use in a database query |
| `field.from_db_value(value, expression, connection)` | Converts a database value to a Python value |
| `field.to_python(value)` | Converts a value to the Python type for this field |
| `field.get_python_value(value)` | Converts a value to the Python type for this field |
| `field.pre_save(model_instance, add)` | Prepares the value for saving to the database |
| `field.post_init(instance, value)` | Prepares the value after model initialization |
| `field.validate(value, model_instance)` | Validates the value for the field |
| `field.run_validators(value)` | Runs all validators for the field |
| `field.clean(value, model_instance)` | Cleans the value for the field |
| `field.get_choices(include_blank=True)` | Returns the choices for the field |
| `field.get_default()` | Returns the default value for the field |
| `field.set_attributes_from_name(name)` | Sets field attributes based on the field name |
| `field.deconstruct()` | Returns a 4-tuple of (name, path, args, kwargs) for the field |
| `field.clone()` | Returns a copy of the field |

---
### **Model Instance Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `model.pk` | The primary key for the model instance |
| `model.id` | The primary key for the model instance (alias for pk) |
| `model._state` | The state of the model instance |
| `model._meta` | The metadata for the model class |
| `model.save(force_insert=False, force_update=False, using=None, update_fields=None)` | Saves the current instance to the database |
| `model.delete(using=None, keep_parents=False)` | Deletes the current instance from the database |
| `model.refresh_from_db(using=None, fields=None)` | Refreshes the instance from the database |
| `model.get_absolute_url()` | Returns the absolute URL for the model instance |
| `model.get_deferred_fields()` | Returns a set of names of deferred fields for the instance |
| `model.prepare_database_save(sender)` | Prepares the instance for saving to the database |
| `model.pre_save(sender, **kwargs)` | Signal handler for pre-save |
| `model.post_save(sender, created, **kwargs)` | Signal handler for post-save |
| `model.pre_delete(sender, **kwargs)` | Signal handler for pre-delete |
| `model.post_delete(sender, **kwargs)` | Signal handler for post-delete |
| `model.__str__()` | Returns a string representation of the model instance |
| `model.__repr__()` | Returns a string representation of the model instance for debugging |
| `model.__eq__(other)` | Tests if this model instance is equal to another |
| `model.__hash__()` | Returns the hash of the model instance |
| `model.get(name, default=None)` | Returns the value of the field with the given name |
| `model.set(**kwargs)` | Sets the values of the fields with the given names |

---
### **Model Class Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `Model.objects` | The default manager for the model |
| `Model._default_manager` | The default manager for the model |
| `Model._base_manager` | The base manager for the model |
| `Model._meta` | The metadata for the model class |
| `Model.get_absolute_url()` | Returns the absolute URL for the model class |
| `Model.get_fields(include_hidden=False)` | Returns a list of all fields in the model |
| `Model.get_all_field_names()` | Returns a list of all field names in the model (deprecated) |
| `Model.get_concrete_fields(include_hidden=False)` | Returns a list of concrete fields in the model |
| `Model.get_ancestors()` | Returns a list of ancestor models |
| `Model.get_subclass_of(cls)` | Returns True if cls is a subclass of this model |
| `Model.get_content_type()` | Returns the content type for the model |
| `Model.get_permissions()` | Returns a list of permissions for the model |
| `Model.check()` | Checks the model for potential problems |
| `Model.clean()` | Validates the model instance |
| `Model.clean_fields(exclude=None)` | Validates the model fields |
| `Model.full_clean(exclude=None, validate_unique=True)` | Validates the model instance and all fields |
| `Model.validate_unique(exclude=None)` | Validates the uniqueness of the model instance |
| `Model.from_db(db, field_names, values)` | Creates a model instance from database data |
| `Model.to_db()` | Prepares the model instance for saving to the database |
| `Model.prepare_database_save(sender)` | Prepares the instance for saving to the database |
| `Model.get_internal_type()` | Returns the internal type of the model |
| `Model.get_absolute_url()` | Returns the absolute URL for the model class |
| `Model.get_object_queryset()` | Returns the queryset for the model |
| `Model.get_queryset()` | Returns the queryset for the model |
| `Model.get_field(field_name)` | Returns the field with the given name |
| `Model.get_fields()` | Returns a list of all fields in the model |
| `Model.get_all_field_names()` | Returns a list of all field names in the model (deprecated) |

---
---
### **QuerySet API**

| Method | Description |
|--------|-------------|
| `queryset.all()` | Returns all objects in the queryset |
| `queryset.filter(*args, **kwargs)` | Returns a new queryset containing objects that match the given lookup parameters |
| `queryset.exclude(*args, **kwargs)` | Returns a new queryset containing objects that do not match the given lookup parameters |
| `queryset.get(*args, **kwargs)` | Returns the single object matching the given lookup parameters |
| `queryset.create(**kwargs)` | Creates and saves a new object with the given keyword arguments |
| `queryset.get_or_create(defaults=None, **kwargs)` | Looks up an object with the given kwargs, creating one if none exists |
| `queryset.update_or_create(defaults=None, **kwargs)` | Looks up an object with the given kwargs, updating it if it exists or creating one if it doesn't |
| `queryset.bulk_create(objs, batch_size=None, ignore_conflicts=False, update_conflicts=False, update_fields=None, unique_fields=None)` | Inserts each of the instances into the database in a single query |
| `queryset.bulk_update(objs, fields, batch_size=None)` | Updates the given fields on each of the instances in the database in a single query |
| `queryset.count()` | Returns the number of objects in the queryset |
| `queryset.exists()` | Returns True if the queryset contains any objects |
| `queryset.in_bulk(id_list, field_name='pk')` | Returns a dictionary mapping each of the given IDs to its corresponding object |
| `queryset.iterator(chunk_size=2000)` | Returns an iterator over the queryset |
| `queryset.latest(field_name=None)` | Returns the latest object in the queryset according to the given field |
| `queryset.earliest(field_name=None)` | Returns the earliest object in the queryset according to the given field |
| `queryset.first()` | Returns the first object in the queryset |
| `queryset.last()` | Returns the last object in the queryset |
| `queryset.aggregate(*args, **kwargs)` | Returns a dictionary of aggregate values |
| `queryset.annotate(*args, **kwargs)` | Returns a queryset with the specified annotations |
| `queryset.distinct(*fields)` | Returns a new queryset with duplicates removed |
| `queryset.order_by(*fields)` | Orders the queryset by the given fields |
| `queryset.reverse()` | Reverses the order of the queryset |
| `queryset.values(*fields, **expressions)` | Returns a ValuesQuerySet containing dictionaries with the specified fields |
| `queryset.values_list(*fields, flat=False, named=False)` | Returns a ValuesListQuerySet containing tuples with the specified fields |
| `queryset.dates(field, kind, order='ASC')` | Returns a list of dates for the specified field |
| `queryset.datetimes(field, kind, order='ASC', tzinfo=None)` | Returns a list of datetimes for the specified field |
| `queryset.none()` | Returns an empty queryset |
| `queryset.union(*other_qs, all=False)` | Returns a queryset containing the union of this queryset and the others |
| `queryset.intersection(*other_qs)` | Returns a queryset containing the intersection of this queryset and the others |
| `queryset.difference(*other_qs)` | Returns a queryset containing the difference between this queryset and the others |
| `queryset.select_related(*fields)` | Returns a queryset that will automatically perform a JOIN for the specified fields |
| `queryset.prefetch_related(*lookups)` | Returns a queryset that will automatically perform a separate query for the specified related objects |
| `queryset.only(*fields)` | Returns a queryset that will only load the specified fields |
| `queryset.defer(*fields)` | Returns a queryset that will not load the specified fields |
| `queryset.using(alias)` | Returns a queryset that will use the specified database connection |
| `queryset.select_for_update(nowait=False, skip_locked=False, of=())` | Returns a queryset that will lock rows until the end of the transaction |
| `queryset.raw(raw_query, params=None, translations=None)` | Returns a RawQuerySet for the given raw SQL query |
| `queryset.extra(select=None, where=None, params=None, tables=None, order_by=None, select_params=None)` | Adds extra SQL clauses to the queryset (deprecated) |
| `queryset.explain(format=None, options=None)` | Returns a string representing the SQL query with EXPLAIN |
| `queryset.query` | The SQL query object for the queryset |

---
### **QuerySet Field Lookups**

| Lookup | Description |
|--------|-------------|
| `exact` | Exact match |
| `iexact` | Case-insensitive exact match |
| `contains` | Case-sensitive containment test |
| `icontains` | Case-insensitive containment test |
| `in` | In a given list |
| `gin` | Case-sensitive containment test (PostgreSQL only) |
| `gt` | Greater than |
| `gte` | Greater than or equal to |
| `lt` | Less than |
| `lte` | Less than or equal to |
| `startswith` | Case-sensitive starts-with |
| `istartswith` | Case-insensitive starts-with |
| `endswith` | Case-sensitive ends-with |
| `iendswith` | Case-insensitive ends-with |
| `range` | Range test (inclusive) |
| `date` | For datetime fields, casts the value to a date |
| `year` | For date/datetime fields, extracts the year |
| `month` | For date/datetime fields, extracts the month |
| `day` | For date/datetime fields, extracts the day |
| `week` | For date/datetime fields, extracts the ISO week number |
| `week_day` | For date/datetime fields, extracts the day of the week (1=Sunday, 7=Saturday) |
| `iso_week_day` | For date/datetime fields, extracts the ISO day of the week (1=Monday, 7=Sunday) |
| `quarter` | For date/datetime fields, extracts the quarter |
| `time` | For datetime fields, casts the value to a time |
| `hour` | For time/datetime fields, extracts the hour |
| `minute` | For time/datetime fields, extracts the minute |
| `second` | For time/datetime fields, extracts the second |
| `isnull` | Tests if the value is NULL |
| `regex` | Case-sensitive regular expression match |
| `iregex` | Case-insensitive regular expression match |
| `search` | Full-text search (PostgreSQL only) |
| `trigram_similar` | Trigram similarity (PostgreSQL only) |
| `contains` | For JSONField, tests if the value contains the given value |
| `contained_by` | For JSONField, tests if the value is contained by the given value |
| `has_key` | For JSONField, tests if the value has the given key |
| `has_keys` | For JSONField, tests if the value has all the given keys |
| `has_any_keys` | For JSONField, tests if the value has any of the given keys |

---
### **QuerySet Aggregation Functions**

| Function | Description |
|----------|-------------|
| `Avg(expression, output_field=None, **extra)` | Returns the average of the given expression |
| `Count(expression, distinct=False, filter=None, **extra)` | Returns the count of the given expression |
| `Max(expression, output_field=None, **extra)` | Returns the maximum of the given expression |
| `Min(expression, output_field=None, **extra)` | Returns the minimum of the given expression |
| `Sum(expression, output_field=None, **extra)` | Returns the sum of the given expression |
| `StdDev(expression, sample=False, output_field=None, **extra)` | Returns the standard deviation of the given expression |
| `Variance(expression, sample=False, output_field=None, **extra)` | Returns the variance of the given expression |
| `ArrayAgg(expression, ordering=None, distinct=False, filter=None, **extra)` | Returns an array of the given expression (PostgreSQL only) |
| `BitAnd(expression, output_field=None, **extra)` | Returns the bitwise AND of the given expression (PostgreSQL only) |
| `BitOr(expression, output_field=None, **extra)` | Returns the bitwise OR of the given expression (PostgreSQL only) |
| `BitXor(expression, output_field=None, **extra)` | Returns the bitwise XOR of the given expression (PostgreSQL only) |
| `BoolAnd(expression, output_field=None, **extra)` | Returns the boolean AND of the given expression (PostgreSQL only) |
| `BoolOr(expression, output_field=None, **extra)` | Returns the boolean OR of the given expression (PostgreSQL only) |
| `StringAgg(expression, delimiter, ordering=None, distinct=False, filter=None, output_field=None, **extra)` | Returns a string aggregation of the given expression (PostgreSQL only) |

---
### **QuerySet Annotation Functions**

| Function | Description |
|----------|-------------|
| `F(expression)` | Creates a reference to a field for use in annotations and updates |
| `Value(value, output_field=None)` | Creates a constant value for use in annotations |
| `Func(expression, *args, output_field=None, **extra)` | Creates a function call for use in annotations |
| `Subquery(queryset, output_field=None)` | Creates a subquery for use in annotations |
| `Exists(queryset)` | Creates an EXISTS subquery for use in annotations |
| `OuterRef(field)` | Creates a reference to an outer query for use in subqueries |
| `Window(expression, partition_by=None, order_by=None, frame=None, output_field=None)` | Creates a window function for use in annotations |
| `WindowFrame(start=None, end=None)` | Creates a window frame for use in window functions |
| `RowNumber()` | Returns a row number for each row in the window |
| `Rank()` | Returns a rank for each row in the window |
| `DenseRank()` | Returns a dense rank for each row in the window |
| `PercentRank()` | Returns a percent rank for each row in the window |
| `CumeDist()` | Returns a cumulative distribution for each row in the window |
| `Ntile(n)` | Returns the n-tile group for each row in the window |
| `FirstValue(expression, output_field=None, filter=None, **extra)` | Returns the first value in the window |
| `LastValue(expression, output_field=None, filter=None, **extra)` | Returns the last value in the window |
| `NthValue(expression, nth, output_field=None, filter=None, **extra)` | Returns the nth value in the window |
| `Lead(expression, offset=1, default=None, output_field=None, filter=None, **extra)` | Returns the value of the expression from the next row in the window |
| `Lag(expression, offset=1, default=None, output_field=None, filter=None, **extra)` | Returns the value of the expression from the previous row in the window |

---
---
---
## **Django Templates**

---
### **Template Tags**

| Tag | Description |
|-----|-------------|
| `{% autoescape %}` | Controls the auto-escaping behavior |
| `{% block %}` | Defines a block that can be overridden by child templates |
| `{% block.super %}` | Outputs the content of the parent block |
| `{% extends %}` | Extends a parent template |
| `{% filter %}` | Filters the contents of the block |
| `{% for %}` | Loop over each item in an iterable |
| `{% empty %}` | Outputs the contents if the loop is empty |
| `{% if %}` | Conditional statement |
| `{% elif %}` | Else if statement |
| `{% else %}` | Else statement |
| `{% include %}` | Includes another template |
| `{% load %}` | Loads a custom template tag set |
| `{% localize %}` | Enables localization of numbers and dates |
| `{% endlocalize %}` | Ends the localization block |
| `{% now %}` | Displays the current date and/or time |
| `{% regroup %}` | Regroups a list of objects by a common attribute |
| `{% spaceless %}` | Removes whitespace between HTML tags |
| `{% static %}` | Outputs the URL for a static file |
| `{% url %}` | Generates a URL for a given view and arguments |
| `{% with %}` | Caches a complex variable under a simpler name |
| `{% csrf_token %}` | Outputs a hidden form field with a CSRF token |
| `{% get_static_prefix %}` | Outputs the static files URL prefix |
| `{% get_current_language %}` | Outputs the current language code |
| `{% get_available_languages %}` | Outputs a list of available language codes |
| `{% get_current_language_bidi %}` | Outputs the current language bidirectional code |
| `{% get_current_language_info %}` | Outputs information about the current language |
| `{% get_current_language_info_list %}` | Outputs a list of information about all languages |
| `{% language %}` | Activates a specified language |
| `{% trans %}` | Translates a string |
| `{% blocktrans %}` | Translates a string with variables |
| `{% plural %}` | Handles pluralization |
| `{% blocktrans %}` | Translates a string with variables and handles pluralization |
| `{% gettext %}` | Alias for trans |
| `{% ngettext %}` | Alias for blocktrans with pluralization |
| `{% l10n %}` | Alias for localize |
| `{% tz %}` | Time zone template tag |
| `{% timezone %}` | Activates a specified time zone |
| `{% static %}` | Outputs the URL for a static file |
| `{% get_static_prefix %}` | Outputs the static files URL prefix |
| `{% get_media_prefix %}` | Outputs the media files URL prefix |
| `{% debug %}` | Outputs debug information about the current context |

---
### **Template Filters**

| Filter | Description |
|--------|-------------|
| `add` | Adds the argument to the value |
| `addslashes` | Adds slashes before quotes |
| `capfirst` | Capitalizes the first character of the string |
| `center` | Centers the string in a field of a given width |
| `cut` | Removes all values of arg from the string |
| `date` | Formats a date according to the given format |
| `default` | If the value is empty or False, uses the given default |
| `default_if_none` | If the value is None, uses the given default |
| `dictsort` | Sorts a dictionary by key |
| `dictsortreversed` | Sorts a dictionary by key in reverse order |
| `divisibleby` | Returns True if the value is divisible by the argument |
| `escape` | Escapes HTML special characters |
| `escapejs` | Escapes JavaScript special characters |
| `filesizeformat` | Formats the value as a human-readable file size |
| `first` | Returns the first item in a list |
| `floatformat` | Formats a floating-point number to a given precision |
| `force_escape` | Escapes HTML special characters (alias for escape) |
| `format` | Formats the value according to the given format string |
| `get_digit` | Returns the nth digit of the number |
| `grouped` | Groups a list into sublists of a given length |
| `indent` | Indents each line of the string with the given number of spaces |
| `iriencode` | Encodes an IRI to ASCII |
| `is_localized` | Returns True if the value is localized |
| `join` | Joins a list with a string separator |
| `json_script` | Outputs the value as a JSON script tag |
| `last` | Returns the last item in a list |
| `length` | Returns the length of the value |
| `length_is` | Returns True if the length of the value equals the argument |
| `linebreaks` | Replaces newlines with appropriate HTML line break tags |
| `linebreaksbr` | Replaces newlines with HTML line break tags |
| `linenumbers` | Displays text with line numbers |
| `ljust` | Left-aligns the string in a field of a given width |
| `localize` | Localizes a number or date |
| `localize_input` | Localizes a number or date for input |
| `lower` | Converts the string to lowercase |
| `make_list` | Converts the value to a list |
| `map` | Applies a filter to each item in a list |
| `multiply` | Multiplies the value by the argument |
| `naturalday` | Formats a date as "today", "tomorrow", "yesterday", or "X days ago" |
| `naturaltime` | Formats a datetime as "now", "an hour ago", "10 minutes ago", etc. |
| `normalizewhitespace` | Normalizes whitespace in a string |
| `number_format` | Formats a number with commas as thousand separators |
| `phone2numeric` | Converts a phone number to its numeric representation |
| `pluralize` | Pluralizes the value if it is not 1 |
| `random` | Returns a random item from a list |
| `removetags` | Removes a space-separated list of HTML tags from the string |
| `rjust` | Right-aligns the string in a field of a given width |
| `safe` | Marks the string as safe for rendering without escaping |
| `safeseq` | Applies the safe filter to each item in a sequence |
| `slice` | Slices the string |
| `slugify` | Converts a string to a slug |
| `sort` | Sorts a list |
| `sort_reverse` | Sorts a list in reverse order |
| `split` | Splits the string into a list |
| `stringformat` | Formats the value according to the given format string |
| `striptags` | Removes all HTML tags from the string |
| `time` | Formats a time according to the given format |
| `timesince` | Formats a datetime as the time since that datetime |
| `timeuntil` | Formats a datetime as the time until that datetime |
| `title` | Converts the string to title case |
| `truncatechars` | Truncates the string if it is longer than the given number of characters |
| `truncatechars_html` | Truncates the string if it is longer than the given number of characters, preserving HTML tags |
| `truncatewords` | Truncates the string if it has more than the given number of words |
| `truncatewords_html` | Truncates the string if it has more than the given number of words, preserving HTML tags |
| `upper` | Converts the string to uppercase |
| `urlencode` | Escapes the string for use in a URL |
| `urlize` | Converts URLs in text to clickable links |
| `urlizetrunc` | Converts URLs to clickable links and truncates long URLs |
| `wordcount` | Returns the number of words in the string |
| `wordwrap` | Wraps lines longer than the given width |
| `yesno` | Maps a boolean to "yes", "no", or a custom mapping |

---
---
---
## **Django Forms**

---
### **Form Classes and Fields**

| Class | Description |
|-------|-------------|
| `django.forms.Form` | Base class for all forms |
| `django.forms.ModelForm` | Base class for forms that create or update model instances |
| `django.forms.fields.Field` | Base class for all form fields |
| `django.forms.fields.CharField` | A string field |
| `django.forms.fields.IntegerField` | An integer field |
| `django.forms.fields.FloatField` | A floating-point number field |
| `django.forms.fields.DecimalField` | A decimal number field |
| `django.forms.fields.DateField` | A date field |
| `django.forms.fields.TimeField` | A time field |
| `django.forms.fields.DateTimeField` | A date and time field |
| `django.forms.fields.DurationField` | A duration field |
| `django.forms.fields.BooleanField` | A boolean field |
| `django.forms.fields.NullBooleanField` | A nullable boolean field |
| `django.forms.fields.ChoiceField` | A field for selecting from a list of choices |
| `django.forms.fields.TypedChoiceField` | A choice field that coerces the input to a specific type |
| `django.forms.fields.MultipleChoiceField` | A field for selecting multiple items from a list of choices |
| `django.forms.fields.TypedMultipleChoiceField` | A multiple choice field that coerces the input to a specific type |
| `django.forms.fields.ComboField` | A field that combines multiple fields |
| `django.forms.fields.MultiValueField` | A field that handles multiple values |
| `django.forms.fields.SplitDateTimeField` | A field that splits a datetime into date and time fields |
| `django.forms.fields.FileField` | A field for file uploads |
| `django.forms.fields.ImageField` | A field for image uploads |
| `django.forms.fields.FilePathField` | A field for selecting from a list of files in a directory |
| `django.forms.fields.EmailField` | A field for email addresses |
| `django.forms.fields.URLField` | A field for URLs |
| `django.forms.fields.RegexField` | A field that validates input against a regular expression |
| `django.forms.fields.SlugField` | A field for slug strings |
| `django.forms.fields.UUIDField` | A field for UUIDs |
| `django.forms.fields.JSONField` | A field for JSON data |
| `django.forms.fields.GenericIPAddressField` | A field for IPv4 or IPv6 addresses |
| `django.forms.widgets.Widget` | Base class for all form widgets |
| `django.forms.widgets.TextInput` | A widget for single-line text input |
| `django.forms.widgets.Textarea` | A widget for multi-line text input |
| `django.forms.widgets.PasswordInput` | A widget for password input |
| `django.forms.widgets.HiddenInput` | A widget for hidden input |
| `django.forms.widgets.NumberInput` | A widget for numeric input |
| `django.forms.widgets.EmailInput` | A widget for email input |
| `django.forms.widgets.URLInput` | A widget for URL input |
| `django.forms.widgets.DateInput` | A widget for date input |
| `django.forms.widgets.TimeInput` | A widget for time input |
| `django.forms.widgets.DateTimeInput` | A widget for datetime input |
| `django.forms.widgets.CheckboxInput` | A widget for checkbox input |
| `django.forms.widgets.Select` | A widget for select input |
| `django.forms.widgets.NullBooleanSelect` | A widget for null boolean select |
| `django.forms.widgets.SelectMultiple` | A widget for multiple select input |
| `django.forms.widgets.RadioSelect` | A widget for radio button select |
| `django.forms.widgets.CheckboxSelectMultiple` | A widget for multiple checkbox select |
| `django.forms.widgets.FileInput` | A widget for file input |
| `django.forms.widgets.ClearableFileInput` | A widget for clearable file input |
| `django.forms.widgets.MultiWidget` | A widget that combines multiple widgets |
| `django.forms.widgets.SplitDateTimeWidget` | A widget that splits a datetime into date and time widgets |
| `django.forms.widgets.SplitHiddenDateTimeWidget` | A widget that splits a datetime into hidden date and time widgets |

---
### **Form Field Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `field.required` | Whether the field is required |
| `field.label` | The human-readable label for the field |
| `field.label_suffix` | The suffix to append to the label |
| `field.initial` | The initial value for the field |
| `field.widget` | The widget for the field |
| `field.help_text` | The help text for the field |
| `field.error_messages` | The error messages for the field |
| `field.validators` | The validators for the field |
| `field.localize` | Whether the field should be localized |
| `field.disabled` | Whether the field is disabled |
| `field.empty_value` | The value to use when the field is empty |
| `field.choices` | The choices for the field |
| `field.max_length` | The maximum length for the field |
| `field.min_length` | The minimum length for the field |
| `field.max_value` | The maximum value for the field |
| `field.min_value` | The minimum value for the field |
| `field.max_digits` | The maximum number of digits for the field |
| `field.decimal_places` | The number of decimal places for the field |
| `field.input_formats` | The input formats for the field |
| `field.strip` | Whether to strip whitespace from the input |
| `field.empty_label` | The label to use for the empty choice |
| `field.to_python(value)` | Converts the input value to the Python type for this field |
| `field.validate(value)` | Validates the input value for this field |
| `field.run_validators(value)` | Runs all validators for the field |
| `field.clean(value)` | Cleans the input value for this field |
| `field.prepare_value(value)` | Prepares the value for display |
| `field.has_changed(initial, data)` | Tests if the field has changed |
| `field.get_bound_field(form, field_name)` | Returns a bound field for the given form and field name |
| `field.get_initial()` | Returns the initial value for the field |
| `field.get_choices()` | Returns the choices for the field |
| `field.get_default()` | Returns the default value for the field |
| `field.decompress(value)` | Decompresses the value for the field |
| `field.compress(data_list)` | Compresses the data list for the field |

---
### **Form Methods and Attributes**

| Method/Attribute | Description |
|------------------|-------------|
| `form.data` | The submitted data for the form |
| `form.files` | The submitted files for the form |
| `form.errors` | A dictionary of error messages for the form |
| `form.non_field_errors()` | Returns a list of non-field error messages |
| `form.error_class` | The CSS class to use for error messages |
| `form.required_css_class` | The CSS class to use for required fields |
| `form.label_suffix` | The suffix to append to field labels |
| `form.auto_id` | The auto ID prefix for form fields |
| `form.prefix` | The prefix for form field names |
| `form.initial` | The initial data for the form |
| `form.fields` | A dictionary of form fields |
| `form.is_bound` | Whether the form is bound to data |
| `form.is_valid()` | Validates the form and returns True if it is valid |
| `form.is_multipart()` | Returns True if the form requires multipart encoding |
| `form.full_clean()` | Validates the form and all fields |
| `form.clean()` | Validates the form |
| `form.cleaned_data` | A dictionary of cleaned data for the form |
| `form.add_error(field, error)` | Adds an error to the form or a field |
| `form.add_error(error)` | Adds a non-field error to the form |
| `form.non_field_errors()` | Returns a list of non-field error messages |
| `form.has_error(field)` | Returns True if the form has an error for the given field |
| `form.changed_data` | Returns a list of changed field names |
| `form.has_changed()` | Returns True if the form has changed |
| `form.save(commit=True)` | Saves the form data to the database |
| `form.save_m2m()` | Saves the many-to-many relationships for the form |
| `form.instance` | The model instance for the form |
| `form.get_initial_for_field(field, field_name)` | Returns the initial value for the given field |
| `form.get_prefix()` | Returns the prefix for the form |
| `form.render(name, value, attrs=None, renderer=None)` | Renders the form field |

---
### **ModelForm Methods and Attributes**

| Method/Attribute | Description |
|------------------|-------------|
| `ModelForm.model` | The model class for the form |
| `ModelForm.fields` | A dictionary of form fields |
| `ModelForm.exclude` | A list of fields to exclude from the form |
| `ModelForm.localized_fields` | A list of fields to localize |
| `ModelForm.widgets` | A dictionary of widgets to use for form fields |
| `ModelForm.labels` | A dictionary of labels to use for form fields |
| `ModelForm.help_texts` | A dictionary of help texts to use for form fields |
| `ModelForm.error_messages` | A dictionary of error messages to use for form fields |
| `ModelForm.field_classes` | A dictionary of field classes to use for form fields |
| `ModelForm.get_form_class()` | Returns the form class to use |
| `ModelForm.get_queryset()` | Returns the queryset to use for the form |
| `ModelForm.get_object(queryset=None)` | Returns the object for the form |
| `ModelForm.get_form_kwargs()` | Returns the keyword arguments for the form |
| `ModelForm.construct_instance(form, instance, fields=None, exclude=None)` | Constructs a model instance from the form data |
| `ModelForm.save(commit=True)` | Saves the form data to the database |
| `ModelForm.save_m2m()` | Saves the many-to-many relationships for the form |
| `ModelForm.get_success_url()` | Returns the URL to redirect to after successful form submission |

---
---
---
## **Django Authentication**

---
### **Authentication Classes and Functions**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.auth.models.User` | The default user model |
| `django.contrib.auth.models.AbstractUser` | Abstract base class for custom user models |
| `django.contrib.auth.models.AbstractBaseUser` | Abstract base class for custom user models with minimal features |
| `django.contrib.auth.models.Permission` | The permission model |
| `django.contrib.auth.models.Group` | The group model |
| `django.contrib.auth.models.AnonymousUser` | The anonymous user class |
| `django.contrib.auth.get_user_model()` | Returns the currently active User model |
| `django.contrib.auth.get_user(request)` | Returns the user associated with the request |
| `django.contrib.auth.get_permission_codename(name, prefix)` | Returns the permission codename for the given name and prefix |
| `django.contrib.auth.get_permissions(user_obj)` | Returns the permissions for the given user |
| `django.contrib.auth.get_group_permissions(user_obj, obj=None)` | Returns the group permissions for the given user |
| `django.contrib.auth.get_all_permissions(user_obj, obj=None)` | Returns all permissions for the given user |
| `django.contrib.auth.has_perm(user_obj, perm, obj=None)` | Returns True if the user has the specified permission |
| `django.contrib.auth.has_module_perms(user_obj, app_label)` | Returns True if the user has any permissions for the given app |
| `django.contrib.auth.decorators.login_required` | Decorator to require login |
| `django.contrib.auth.decorators.permission_required(perm, raise_exception=False)` | Decorator to require specific permissions |
| `django.contrib.auth.decorators.permission_required(perms, raise_exception=False)` | Decorator to require any of the specified permissions |
| `django.contrib.auth.decorators.user_passes_test(test_func, login_url=None, raise_exception=False)` | Decorator to require a user to pass a test |
| `django.contrib.auth.mixins.LoginRequiredMixin` | Mixin to require login for class-based views |
| `django.contrib.auth.mixins.PermissionRequiredMixin` | Mixin to require permissions for class-based views |
| `django.contrib.auth.mixins.UserPassesTestMixin` | Mixin to require a user to pass a test for class-based views |
| `django.contrib.auth.backends.ModelBackend` | Authentication backend that uses the Django user model |
| `django.contrib.auth.backends.RemoteUserBackend` | Authentication backend that uses REMOTE_USER |
| `django.contrib.auth.password_validation.validate_password(password, user=None, password_validators=None)` | Validates a password against the specified validators |
| `django.contrib.auth.password_validation.get_password_validators(configuration)` | Returns a list of password validators |
| `django.contrib.auth.password_validation.get_default_password_validators()` | Returns the default password validators |
| `django.contrib.auth.tokens.default_token_generator` | Default token generator for password reset tokens |
| `django.contrib.auth.tokens.PasswordResetTokenGenerator` | Token generator for password reset tokens |
| `django.contrib.auth.forms.AuthenticationForm` | Form for user authentication |
| `django.contrib.auth.forms.PasswordChangeForm` | Form for changing a user's password |
| `django.contrib.auth.forms.PasswordResetForm` | Form for requesting a password reset |
| `django.contrib.auth.forms.SetPasswordForm` | Form for setting a user's password |
| `django.contrib.auth.forms.UserCreationForm` | Form for creating a new user |
| `django.contrib.auth.forms.UserChangeForm` | Form for changing a user's information |
| `django.contrib.auth.forms.AdminPasswordChangeForm` | Form for changing a user's password in the admin |

---
### **Authentication Methods**

| Method | Description |
|--------|-------------|
| `user.is_authenticated` | Returns True if the user is authenticated |
| `user.is_anonymous` | Returns True if the user is anonymous |
| `user.is_active` | Returns True if the user is active |
| `user.is_staff` | Returns True if the user is a staff member |
| `user.is_superuser` | Returns True if the user is a superuser |
| `user.get_username()` | Returns the username for the user |
| `user.get_full_name()` | Returns the first name plus the last name for the user |
| `user.get_short_name()` | Returns the first name for the user |
| `user.email_user(subject, message, from_email=None, **kwargs)` | Sends an email to the user |
| `user.has_perm(perm, obj=None)` | Returns True if the user has the specified permission |
| `user.has_perms(perm_list, obj=None)` | Returns True if the user has all the specified permissions |
| `user.has_module_perms(app_label)` | Returns True if the user has any permissions for the given app |
| `user.get_all_permissions(obj=None)` | Returns a set of all permissions for the user |
| `user.get_group_permissions(obj=None)` | Returns a set of group permissions for the user |
| `user.get_user_permissions(obj=None)` | Returns a set of user permissions for the user |
| `user.groups` | Returns a manager for the groups the user belongs to |
| `user.user_permissions` | Returns a manager for the permissions the user has directly |
| `user.get_group_names()` | Returns a list of the names of the groups the user belongs to |
| `user.set_password(raw_password)` | Sets the user's password |
| `user.check_password(raw_password)` | Returns True if the given password is correct for the user |
| `user.set_unusable_password()` | Marks the user's password as unusable |
| `user.has_usable_password()` | Returns True if the user has a usable password |
| `user.get_session_auth_hash()` | Returns the session auth hash for the user |
| `user.log_entry_set` | Returns a manager for the log entries for the user |
| `user.date_joined` | Returns the date the user joined |
| `user.last_login` | Returns the date of the user's last login |
| `user.is_fully_authed()` | Returns True if the user has a usable password |

---
---
---
## **Django Admin**

---
### **Admin Classes and Decorators**

| Class/Decorator | Description |
|-----------------|-------------|
| `django.contrib.admin.ModelAdmin` | Base class for model admin options |
| `django.contrib.admin.TabularInline` | Inline admin for editing related objects in a tabular format |
| `django.contrib.admin.StackedInline` | Inline admin for editing related objects in a stacked format |
| `django.contrib.admin.AdminSite` | Class for the admin site |
| `django.contrib.admin.site.register(model_or_iterable, admin_class=None, **options)` | Registers a model with the admin site |
| `django.contrib.admin.site.unregister(model_or_iterable)` | Unregisters a model from the admin site |
| `django.contrib.admin.decorators.display(description=None, boolean=None, short_description=None, empty_value_display=None, ordering=None, admin_order_field=None, header=None)` | Decorator for custom admin list display methods |
| `django.contrib.admin.decorators.action(permissions=None)` | Decorator for custom admin actions |

---
### **ModelAdmin Attributes**

| Attribute | Description |
|-----------|-------------|
| `list_display` | List of fields to display in the list view |
| `list_display_links` | List of fields to link to the change form |
| `list_filter` | List of fields to use for filtering |
| `list_select_related` | List of fields to select related objects for |
| `list_per_page` | Number of items to display per page |
| `list_max_show_all` | Maximum number of items to show in the "show all" view |
| `list_editable` | List of fields to make editable in the list view |
| `search_fields` | List of fields to use for searching |
| `search_help_text` | Help text to display for the search field |
| `date_hierarchy` | Field to use for date hierarchy navigation |
| `ordering` | Default ordering for the list view |
| `visible_fields` | List of fields to display in the change form |
| `exclude` | List of fields to exclude from the change form |
| `readonly_fields` | List of fields to display as read-only in the change form |
| `fields` | List of fields to display in the change form |
| `fieldsets` | List of fieldset tuples for the change form |
| `filter_horizontal` | List of fields to display with a horizontal filter |
| `filter_vertical` | List of fields to display with a vertical filter |
| `radio_fields` | Dictionary of fields to display with radio buttons |
| `prepopulated_fields` | Dictionary of fields to prepopulate based on other fields |
| `raw_id_fields` | List of fields to display with a raw ID widget |
| `form` | Form class to use for the change form |
| `formfield_overrides` | Dictionary of form field overrides |
| `add_form_template` | Template to use for the add form |
| `change_form_template` | Template to use for the change form |
| `change_list_template` | Template to use for the change list |
| `delete_confirmation_template` | Template to use for the delete confirmation |
| `delete_selected_confirmation_template` | Template to use for the delete selected confirmation |
| `object_history_template` | Template to use for the object history |
| `actions` | List of actions to display in the action dropdown |
| `actions_on_top` | Whether to display actions at the top of the list |
| `actions_on_bottom` | Whether to display actions at the bottom of the list |
| `actions_selection_counter` | Whether to display the selection counter for actions |
| `show_all_rel_details` | Whether to show all related object details |
| `inlines` | List of inline admin classes |
| `preserve_filters` | Whether to preserve filters when editing an object |
| `save_as` | Whether to display the "save as new" button |
| `save_on_top` | Whether to display the save buttons at the top of the form |
| `view_on_site` | Whether to display the "view on site" button |
| `change_list_filter` | Whether to display the filter sidebar |
| `show_changelink` | Whether to display the change link for related objects |

---
### **ModelAdmin Methods**

| Method | Description |
|--------|-------------|
| `get_queryset(request)` | Returns the queryset to use for the list view |
| `get_list_display(request)` | Returns the list of fields to display in the list view |
| `get_list_display_links(request, list_display)` | Returns the list of fields to link to the change form |
| `get_list_filter(request)` | Returns the list of fields to use for filtering |
| `get_list_select_related(request)` | Returns the list of fields to select related objects for |
| `get_search_fields(request)` | Returns the list of fields to use for searching |
| `get_search_results(request, queryset, search_term)` | Returns the search results for the given search term |
| `get_date_hierarchy(request)` | Returns the field to use for date hierarchy navigation |
| `get_ordering(request)` | Returns the ordering for the list view |
| `get_paginator(request, queryset, per_page)` | Returns the paginator for the list view |
| `paginate_queryset(request, queryset, per_page)` | Paginates the queryset for the list view |
| `get_actions(request)` | Returns the list of actions to display in the action dropdown |
| `get_action_choices(request)` | Returns the list of action choices for the action dropdown |
| `get_action_form(request, obj=None)` | Returns the form for the action dropdown |
| `response_action(request, queryset, action)` | Returns the response for the given action |
| `get_form(request, obj=None, **kwargs)` | Returns the form for the change form |
| `get_fieldsets(request, obj=None)` | Returns the fieldsets for the change form |
| `get_readonly_fields(request, obj=None)` | Returns the list of fields to display as read-only in the change form |
| `get_prepopulated_fields(request, obj=None)` | Returns the dictionary of fields to prepopulate based on other fields |
| `get_formset(request, obj=None, **kwargs)` | Returns the formset for the change form |
| `save_model(request, obj, form, change)` | Saves the model instance |
| `delete_model(request, obj)` | Deletes the model instance |
| `save_formset(request, form, formset, change)` | Saves the formset |
| `delete_formset(request, formset)` | Deletes the formset |
| `get_inline_instances(request, obj=None)` | Returns the list of inline instances for the change form |
| `get_urls()` | Returns the list of URL patterns for the admin |
| `get_app_list(request)` | Returns the list of apps for the admin index |
| `index(request, extra_context=None)` | Returns the response for the admin index |
| `app_index(request, app_label, extra_context=None)` | Returns the response for the app index |
| `changelist_view(request, extra_context=None)` | Returns the response for the change list |
| `add_view(request, form_url='', extra_context=None)` | Returns the response for the add form |
| `change_view(request, object_id, form_url='', extra_context=None)` | Returns the response for the change form |
| `delete_view(request, object_id, extra_context=None)` | Returns the response for the delete confirmation |
| `history_view(request, object_id, extra_context=None)` | Returns the response for the object history |
| `action_check(request, obj)` | Returns True if the user has permission to perform the action on the object |
| `has_add_permission(request)` | Returns True if the user has permission to add objects |
| `has_change_permission(request, obj=None)` | Returns True if the user has permission to change objects |
| `has_delete_permission(request, obj=None)` | Returns True if the user has permission to delete objects |
| `has_view_permission(request, obj=None)` | Returns True if the user has permission to view objects |
| `has_module_permission(request)` | Returns True if the user has any permission for the model |
| `get_model_perms(request)` | Returns the permissions for the model |
| `message_user(request, message, level=messages.INFO, extra_tags='', fail_silently=False)` | Sends a message to the user |

---
---
---
## **Django Middleware**

---
### **Middleware Classes**

| Class | Description |
|-------|-------------|
| `django.middleware.security.SecurityMiddleware` | Adds security headers and redirects insecure requests |
| `django.middleware.clickjacking.XFrameOptionsMiddleware` | Adds X-Frame-Options header to responses |
| `django.middleware.csrf.CsrfViewMiddleware` | Adds CSRF protection to requests |
| `django.middleware.common.CommonMiddleware` | Handles some common request processing |
| `django.middleware.gzip.GZipMiddleware` | Compresses responses with gzip |
| `django.middleware.http.ConditionalGetMiddleware` | Handles conditional GET requests |
| `django.middleware.http.ConditionalGetMiddleware` | Handles conditional GET requests |
| `django.middleware.locale.LocaleMiddleware` | Handles locale activation based on the request |
| `django.middleware.http.SetRemoteAddrFromForwardedHeader` | Sets REMOTE_ADDR based on X-Forwarded-For header |
| `django.middleware.simplejson.JsonResponseMiddleware` | Handles JSON responses (deprecated) |
| `django.middleware.cache.UpdateCacheMiddleware` | Updates the cache on response |
| `django.middleware.cache.FetchFromCacheMiddleware` | Fetches responses from the cache |
| `django.middleware.cache.CacheMiddleware` | Cache middleware (deprecated) |
| `django.middleware.common.AppVersionMiddleware` | Adds the app version to the response headers |
| `django.middleware.common.BrotliMiddleware` | Compresses responses with Brotli |
| `django.middleware.common.CacheControlMiddleware` | Adds cache-control headers to responses |
| `django.middleware.common.ContentLengthMiddleware` | Adds Content-Length header to responses |
| `django.middleware.common.DisallowUserAgentsMiddleware` | Disallows requests from certain user agents |
| `django.middleware.common.ForwardedHostMiddleware` | Sets the host based on X-Forwarded-Host header |
| `django.middleware.common.HttpStrictTransportSecurityMiddleware` | Adds HSTS header to responses |
| `django.middleware.common.PermissionPolicyMiddleware` | Adds Permissions-Policy header to responses |
| `django.middleware.common.RealIPMiddleware` | Sets REMOTE_ADDR based on X-Real-IP header |
| `django.middleware.common.RedirectFallbackMiddleware` | Redirects to fallback URLs |
| `django.middleware.common.SetRemoteAddrFromForwardedHeader` | Sets REMOTE_ADDR based on X-Forwarded-For header |
| `django.middleware.csrf.CsrfViewMiddleware` | Adds CSRF protection to requests |
| `django.middleware.gzip.GZipMiddleware` | Compresses responses with gzip |
| `django.middleware.http.ConditionalGetMiddleware` | Handles conditional GET requests |
| `django.middleware.locale.LocaleMiddleware` | Handles locale activation based on the request |

---
### **Middleware Methods**

| Method | Description |
|--------|-------------|
| `middleware.__init__(get_response)` | Initializes the middleware with the get_response callable |
| `middleware.__call__(request)` | Processes the request and returns the response |
| `middleware.process_request(request)` | Processes the request before the view is called |
| `middleware.process_view(request, view_func, view_args, view_kwargs)` | Processes the view before it is called |
| `middleware.process_template_response(request, response)` | Processes the template response before it is rendered |
| `middleware.process_response(request, response)` | Processes the response after the view is called |
| `middleware.process_exception(request, exception)` | Processes an exception raised by the view |

---
---
---
## **Django Signals**

---
### **Signal Classes and Functions**

| Signal | Description |
|--------|-------------|
| `django.db.models.signals.pre_init` | Sent before a model instance is initialized |
| `django.db.models.signals.post_init` | Sent after a model instance is initialized |
| `django.db.models.signals.pre_save` | Sent before a model instance is saved |
| `django.db.models.signals.post_save` | Sent after a model instance is saved |
| `django.db.models.signals.pre_delete` | Sent before a model instance is deleted |
| `django.db.models.signals.post_delete` | Sent after a model instance is deleted |
| `django.db.models.signals.m2m_changed` | Sent when a ManyToManyField is changed |
| `django.db.models.signals.class_prepared` | Sent when a model class is prepared |
| `django.db.models.signals.request_started` | Sent when Django starts processing a request |
| `django.db.models.signals.request_finished` | Sent when Django finishes processing a request |
| `django.core.signals.got_request_exception` | Sent when an exception is raised during request processing |
| `django.test.signals.template_rendered` | Sent after a template is rendered |
| `django.test.signals.test_exception` | Sent when an exception is raised during testing |
| `django.contrib.auth.signals.user_logged_in` | Sent when a user logs in |
| `django.contrib.auth.signals.user_logged_out` | Sent when a user logs out |
| `django.contrib.auth.signals.user_login_failed` | Sent when a user login fails |
| `django.contrib.auth.signals.password_changed` | Sent when a user's password is changed |
| `django.contrib.sessions.signals.session_start` | Sent when a session is started |
| `django.contrib.sessions.signals.session_end` | Sent when a session ends |
| `django.contrib.messages.signals.message_sent` | Sent when a message is sent |
| `django.core.signals.pre_request` | Sent before Django starts processing a request (deprecated) |
| `django.core.signals.post_request` | Sent after Django finishes processing a request (deprecated) |
| `django.core.signals.request_started` | Sent when Django starts processing a request |
| `django.core.signals.request_finished` | Sent when Django finishes processing a request |

---
### **Signal Methods**

| Method | Description |
|--------|-------------|
| `Signal.connect(receiver, sender=None, dispatch_uid=None, weak=True)` | Connects a receiver function to a signal |
| `Signal.disconnect(receiver, sender=None, dispatch_uid=None)` | Disconnects a receiver function from a signal |
| `Signal.send(sender, **named)` | Sends the signal to all connected receivers |
| `Signal.send_robust(sender, **named)` | Sends the signal to all connected receivers, catching exceptions |
| `Signal.receivers` | A list of all receiver functions connected to the signal |
| `Signal.has_listeners` | Returns True if the signal has any listeners |

---
---
---
## **Django Testing**

---
### **Test Classes and Functions**

| Class/Function | Description |
|----------------|-------------|
| `django.test.TestCase` | Base class for Django test cases |
| `django.test.SimpleTestCase` | Base class for simple test cases without database access |
| `django.test.TransactionTestCase` | Base class for test cases with transaction support |
| `django.test.LiveServerTestCase` | Base class for test cases with a live server |
| `django.test.StaticLiveServerTestCase` | Base class for test cases with a live server and static files |
| `django.test.Client` | HTTP client for testing views |
| `django.test.ClientHandler` | Handler for the test client |
| `django.test.RequestFactory` | Factory for creating request objects |
| `django.test.AsyncRequestFactory` | Factory for creating async request objects |
| `django.test.AsyncClient` | Async HTTP client for testing async views |
| `django.test.runner.DiscoverRunner` | Test runner that discovers tests in the filesystem |
| `django.test.utils.setup_test_environment()` | Sets up the test environment |
| `django.test.utils.teardown_test_environment()` | Tears down the test environment |
| `django.test.utils.get_unique_databases_and_mirrors()` | Returns a set of unique database aliases and their mirrors |
| `django.test.utils.get_unique_databases()` | Returns a set of unique database aliases |
| `django.test.utils.create_test_db(verbosity=1, autoclobber=True, serialize=False)` | Creates the test database |
| `django.test.utils.destroy_test_db(old_db_names, verbosity=1)` | Destroys the test database |
| `django.test.utils.get_max_diff_size()` | Returns the maximum size for diffs in test failures |
| `django.test.utils.set_max_diff_size(size)` | Sets the maximum size for diffs in test failures |
| `django.test.utils.TestCase` | Base class for Django test cases |
| `django.test.utils.override_settings(**kwargs)` | Decorator to temporarily override Django settings |
| `django.test.utils.tag(verbosity=1, **kwargs)` | Decorator to tag a test method |
| `django.test.utils.skip(condition)` | Decorator to skip a test method |
| `django.test.utils.skipIf(condition)` | Decorator to skip a test method if a condition is true |
| `django.test.utils.skipUnless(condition)` | Decorator to skip a test method unless a condition is true |
| `django.test.utils.expectedFailure` | Decorator to mark a test method as expected to fail |
| `django.test.utils.captureOnCommitCallbacks` | Context manager to capture on_commit callbacks |
| `django.test.utils.CaptureQueriesContext` | Context manager to capture SQL queries |
| `django.test.utils.assertNumQueries(num, func, *args, **kwargs)` | Asserts that a function executes a specific number of SQL queries |
| `django.test.utils.assertQueries(func, *args, **kwargs)` | Asserts that a function executes specific SQL queries |
| `django.test.utils.assertTemplateUsed(response, template_name, count=None, msg_prefix='')` | Asserts that a response uses a specific template |
| `django.test.utils.assertTemplateNotUsed(response, template_name, msg_prefix='')` | Asserts that a response does not use a specific template |
| `django.test.utils.assertContains(response, text, count=None, status_code=None, msg_prefix='', html=False)` | Asserts that a response contains specific text |
| `django.test.utils.assertNotContains(response, text, status_code=None, msg_prefix='', html=False)` | Asserts that a response does not contain specific text |
| `django.test.utils.assertEqual(response, expected, msg=None)` | Asserts that a response equals an expected value |
| `django.test.utils.assertRedirects(response, expected_url, status_code=302, target_status_code=None, msg_prefix='', fetch_redirect_response=True)` | Asserts that a response redirects to an expected URL |
| `django.test.utils.assertJSONEqual(response, expected_data, msg_prefix='')` | Asserts that a response contains expected JSON data |
| `django.test.utils.assertFormError(response, form, field, errors, msg_prefix='')` | Asserts that a response contains form errors |
| `django.test.utils.assertFieldOutput(html, expected, count=None, msg_prefix='')` | Asserts that HTML contains expected field output |

---
### **Test Client Methods**

| Method | Description |
|--------|-------------|
| `client.get(path, data=None, follow=False, secure=False, **extra)` | Performs a GET request |
| `client.post(path, data=None, content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs a POST request |
| `client.put(path, data=None, content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs a PUT request |
| `client.patch(path, data=None, content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs a PATCH request |
| `client.delete(path, data='', content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs a DELETE request |
| `client.head(path, data=None, follow=False, secure=False, **extra)` | Performs a HEAD request |
| `client.options(path, data='', content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs an OPTIONS request |
| `client.trace(path, data='', content_type='application/octet-stream', follow=False, secure=False, **extra)` | Performs a TRACE request |
| `client.request(**kwargs)` | Performs a generic request |
| `client.logout()` | Logs the user out |
| `client.login(**credentials)` | Logs a user in |
| `client.force_login(user)` | Forces a user to be logged in |
| `client.logout()` | Logs the user out |
| `client.get_cookies()` | Returns a dictionary of cookies |
| `client.set_cookie(name, value, max_age=None, expires=None, path='/', domain=None, secure=False, httponly=True, samesite=None)` | Sets a cookie |
| `client.delete_cookie(name, path='/', domain=None)` | Deletes a cookie |
| `client.session` | Returns the session dictionary |
| `client.last_response` | Returns the last response |

---
---
---
## **Django Utilities**

---
### **URL Utilities**

| Function/Class | Description |
|----------------|-------------|
| `django.urls.reverse(viewname, urlconf=None, args=None, kwargs=None)` | Returns a URL matching a view and arguments |
| `django.urls.reverse_lazy(viewname, urlconf=None, args=None, kwargs=None)` | Lazy version of reverse() |
| `django.urls.resolve(path, urlconf=None)` | Resolves a URL path to a view, arguments, and other metadata |
| `django.urls.clear_url_caches()` | Clears all URL caches |
| `django.urls.get_urlconf(module_name)` | Returns the URLconf module for the given module name |
| `django.urls.set_urlconf(urlconf)` | Sets the URLconf module for the current thread |
| `django.urls.get_resolver(urlconf_module)` | Returns the resolver for the given URLconf module |
| `django.urls.get_script_prefix()` | Returns the script prefix for the current request |
| `django.urls.set_script_prefix(prefix)` | Sets the script prefix for the current request |

---
### **HTML Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.html.escape(s)` | Escapes HTML special characters in a string |
| `django.utils.html.mark_safe(s)` | Marks a string as safe for rendering without escaping |
| `django.utils.html.SafeString` | A string subclass that is marked as safe |
| `django.utils.html.SafeBytes` | A bytes subclass that is marked as safe |
| `django.utils.html.SafeText` | A text subclass that is marked as safe |
| `django.utils.html.format_html(format_string, *args, **kwargs)` | Formats a string with HTML escaping |
| `django.utils.html.strip_tags(html)` | Removes all HTML tags from a string |
| `django.utils.html.strip_whitespace(text)` | Strips leading and trailing whitespace from a string |
| `django.utils.html.smart_urlquote(s, safe='/')` | URL-encodes a string using URL quoting |
| `django.utils.html.urlquote(s, safe='/')` | URL-encodes a string using URL quoting (alias for smart_urlquote) |
| `django.utils.html.urlquote_plus(s, safe='')` | URL-encodes a string using URL quoting with spaces encoded as + |
| `django.utils.html.urlunquote(s)` | URL-decodes a string |
| `django.utils.html.urlunquote_plus(s)` | URL-decodes a string with + converted to spaces |
| `django.utils.html.conditional_escape(func)` | Decorator to conditionally escape the result of a function |
| `django.utils.html.html_safe(func)` | Decorator to mark the result of a function as safe |
| `django.utils.html.smart_split(s)` | Splits a string into a list of strings, handling quoted strings |

---
### **Text Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.text.capfirst(s)` | Capitalizes the first character of a string |
| `django.utils.text.get_valid_filename(name)` | Returns a valid filename from a string |
| `django.utils.text.get_text_list(list_, last_word='or')` | Returns a string representation of a list with the last item joined by the specified word |
| `django.utils.text.javaScriptEscape(s)` | Escapes a string for use in JavaScript |
| `django.utils.text.phone2numeric(phone)` | Converts a phone number to its numeric representation |
| `django.utils.text.smart_split(s)` | Splits a string into a list of strings, handling quoted strings |
| `django.utils.text.truncate_chars(s, num)` | Truncates a string to the specified number of characters |
| `django.utils.text.truncate_words(s, num)` | Truncates a string to the specified number of words |
| `django.utils.text.wrap(text, width=78)` | Wraps text to the specified width |
| `django.utils.text.get_text_list(list_, last_word='or')` | Returns a string representation of a list with the last item joined by the specified word |

---
### **Date and Time Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.timezone.now()` | Returns the current datetime with timezone information |
| `django.utils.timezone.localtime(value=None, timezone=None)` | Converts a datetime to the local timezone |
| `django.utils.timezone.utc` | The UTC timezone |
| `django.utils.timezone.get_current_timezone()` | Returns the current timezone |
| `django.utils.timezone.get_current_timezone_name()` | Returns the name of the current timezone |
| `django.utils.timezone.get_default_timezone()` | Returns the default timezone |
| `django.utils.timezone.set_default_timezone(tz)` | Sets the default timezone |
| `django.utils.timezone.activate(timezone)` | Activates the specified timezone for the current thread |
| `django.utils.timezone.deactivate()` | Deactivates the timezone for the current thread |
| `django.utils.timezone.is_aware(value)` | Returns True if the value is timezone-aware |
| `django.utils.timezone.is_naive(value)` | Returns True if the value is timezone-naive |
| `django.utils.timezone.make_aware(value, timezone=None)` | Makes a timezone-naive datetime timezone-aware |
| `django.utils.timezone.make_naive(value, timezone=None)` | Makes a timezone-aware datetime timezone-naive |
| `django.utils.timezone.normalize(value)` | Normalizes a datetime to the current timezone |
| `django.utils.timezone.localtime(value=None, timezone=None)` | Converts a datetime to the local timezone |
| `django.utils.timezone.fix_localtime(value)` | Fixes the localtime for the given value |
| `django.utils.dateformat.format(date, format_str)` | Formats a date according to the given format string |
| `django.utils.dateformat.DateFormat(date)` | Formats a date according to the given format string |
| `django.utils.dateformat.TimeFormat(time)` | Formats a time according to the given format string |
| `django.utils.dateformat.DateTimeFormat(datetime)` | Formats a datetime according to the given format string |
| `django.utils.dateformat.get_format(format_type)` | Returns the format string for the given format type |
| `django.utils.dateformat.get_formats()` | Returns a dictionary of format strings for all format types |
| `django.utils.dateformat.time_format` | The default time format |
| `django.utils.dateformat.date_format` | The default date format |
| `django.utils.dateformat.datetime_format` | The default datetime format |
| `django.utils.dateformat.year_month_format` | The default year-month format |
| `django.utils.dateformat.month_day_format` | The default month-day format |
| `django.utils.dateformat.short_date_format` | The default short date format |
| `django.utils.dateformat.short_datetime_format` | The default short datetime format |

---
### **Encoding Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.encoding.force_str(s, encoding='utf-8', strings_only=False, errors='strict')` | Forces a string to a str type |
| `django.utils.encoding.force_bytes(s, encoding='utf-8', strings_only=False, errors='strict')` | Forces a string to a bytes type |
| `django.utils.encoding.smart_str(s, encoding='utf-8', strings_only=False, errors='strict')` | Smartly converts a string to a str type |
| `django.utils.encoding.smart_bytes(s, encoding='utf-8', strings_only=False, errors='strict')` | Smartly converts a string to a bytes type |
| `django.utils.encoding.is_protected_type(obj)` | Returns True if the object is of a protected type |
| `django.utils.encoding.ProtectedTypeError` | Exception raised when a protected type is encountered |
| `django.utils.encoding.default_encoding` | The default encoding to use |
| `django.utils.encoding.file_encoding` | The file encoding to use |

---
### **File Utilities**

| Function | Description |
|----------|-------------|
| `django.utils._os.safe_join(base, *paths)` | Safely joins path components |
| `django.utils._os.abspathu(path)` | Returns the absolute path of a path |
| `django.utils._os.normpathu(path)` | Normalizes a path |
| `django.utils._os.splitu(path)` | Splits a path into a drive, head, and tail |
| `django.utils._os.path_join(*paths)` | Joins path components |
| `django.utils._os.upath(path)` | Converts a path to a Unicode string |

---
### **Cryptographic Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.crypto.get_random_string(length=12, allowed_chars='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789')` | Returns a random string of the specified length |
| `django.utils.crypto.get_random_bytes(length)` | Returns a random byte string of the specified length |
| `django.utils.crypto.get_random_secret_key()` | Returns a random secret key |
| `django.utils.crypto.constant_time_compare(a, b)` | Compares two strings in constant time |
| `django.utils.crypto.salted_hmac(key_salt, value, secret=None)` | Returns a salted HMAC for the given value |
| `django.utils.crypto.signing.dumps(obj, key=None, serializer=serializers.json, compress=True)` | Returns a signed JSON string for the given object |
| `django.utils.crypto.signing.loads(s, key=None, serializer=serializers.json, max_size=2**31-1)` | Returns the object for the given signed JSON string |
| `django.utils.crypto.signing.TimestampSigner(key=None, salt=None, sep='.', digest_method='sha256')` | A signer that includes a timestamp in the signature |
| `django.utils.crypto.signing.Signer(key=None, salt=None, sep='.', digest_method='sha256')` | A signer for creating and verifying signed strings |
| `django.utils.crypto.signing.BadSignature` | Exception raised when a signature is invalid |
| `django.utils.crypto.signing.SignatureExpired` | Exception raised when a signature has expired |
| `django.utils.crypto.signing.BadTimestamp` | Exception raised when a timestamp is invalid |

---
### **HTTP Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.http.is_safe_url(url)` | Returns True if the URL is safe for redirecting |
| `django.utils.http.url_has_allowed_netloc(url)` | Returns True if the URL has an allowed netloc |
| `django.utils.http.urlencode(query, doseq=False, safe='', encoding=None, errors=None)` | URL-encodes a query dictionary |
| `django.utils.http.urlquote(s, safe='')` | URL-encodes a string |
| `django.utils.http.urlquote_plus(s, safe='')` | URL-encodes a string with spaces encoded as + |
| `django.utils.http.urlunquote(s, encoding='utf-8', errors='replace')` | URL-decodes a string |
| `django.utils.http.urlunquote_plus(s, encoding='utf-8', errors='replace')` | URL-decodes a string with + converted to spaces |
| `django.utils.http.quote_etag(etag)` | Quotes an ETag for use in HTTP headers |
| `django.utils.http.parse_http_date(s)` | Parses a date from an HTTP header |
| `django.utils.http.parse_http_list(value)` | Parses a list from an HTTP header |
| `django.utils.http.base32_to_int(s)` | Converts a base32 string to an integer |
| `django.utils.http.int_to_base32(i)` | Converts an integer to a base32 string |
| `django.utils.http.content_disposition_header(filename)` | Returns a Content-Disposition header for the given filename |

---
### **Deprecation Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.deprecation.MiddlewareMixin` | Mixin for middleware classes to handle deprecation |
| `django.utils.deprecation.deprecate_function(func, since, replacement=None, level=PendingDeprecationWarning)` | Decorator to mark a function as deprecated |
| `django.utils.deprecation.deprecate_class(Class, since, replacement=None, level=PendingDeprecationWarning)` | Decorator to mark a class as deprecated |
| `django.utils.deprecation.deprecate_component(func, since, replacement=None, level=PendingDeprecationWarning)` | Decorator to mark a component as deprecated |

---
---
---
## **Django Contrib Modules**

---
### **Sessions Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.sessions.backends.base.SessionBase` | Base class for session backends |
| `django.contrib.sessions.backends.cache.CacheSession` | Cache-based session backend |
| `django.contrib.sessions.backends.cached_db.CachedDBSession` | Cached database session backend |
| `django.contrib.sessions.backends.db.DatabaseSession` | Database session backend |
| `django.contrib.sessions.backends.file.FileSession` | File-based session backend |
| `django.contrib.sessions.backends.memcached.MemcachedSession` | Memcached-based session backend |
| `django.contrib.sessions.backends.redis.RedisSession` | Redis-based session backend |
| `django.contrib.sessions.middleware.SessionMiddleware` | Middleware for session handling |
| `django.contrib.sessions.models.Session` | Model for database-based sessions |
| `django.contrib.sessions.serializers.JSONSerializer` | JSON serializer for session data |
| `django.contrib.sessions.serializers.PickleSerializer` | Pickle serializer for session data |
| `django.contrib.sessions.backends.base.create_model_instance(session_dict)` | Creates a model instance from session data |
| `django.contrib.sessions.backends.base.encode(session_dict)` | Encodes session data |
| `django.contrib.sessions.backends.base.decode(session_data)` | Decodes session data |

---
### **Messages Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.messages.storage.base.BaseStorage` | Base class for message storage |
| `django.contrib.messages.storage.cookie.CookieStorage` | Cookie-based message storage |
| `django.contrib.messages.storage.session.SessionStorage` | Session-based message storage |
| `django.contrib.messages.storage.fallback.FallbackStorage` | Fallback message storage |
| `django.contrib.messages.middleware.MessageMiddleware` | Middleware for message handling |
| `django.contrib.messages.api.add_message(request, level, message, extra_tags='', fail_silently=False)` | Adds a message to the request |
| `django.contrib.messages.api.set_level(request, level)` | Sets the minimum message level for the request |
| `django.contrib.messages.api.get_level(request)` | Returns the minimum message level for the request |
| `django.contrib.messages.api.messages(request)` | Returns the messages for the request |
| `django.contrib.messages.api.get_messages(request)` | Returns the messages for the request |
| `django.contrib.messages.api.used(request)` | Returns True if the messages have been used |
| `django.contrib.messages.api.unuse(request)` | Marks the messages as unused |
| `django.contrib.messages.constants.DEBUG` | Debug message level |
| `django.contrib.messages.constants.INFO` | Info message level |
| `django.contrib.messages.constants.SUCCESS` | Success message level |
| `django.contrib.messages.constants.WARNING` | Warning message level |
| `django.contrib.messages.constants.ERROR` | Error message level |

---
### **Static Files Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.staticfiles.storage.StaticFilesStorage` | Storage backend for static files |
| `django.contrib.staticfiles.storage.ManifestStaticFilesStorage` | Storage backend for static files with manifest support |
| `django.contrib.staticfiles.storage.HashedFilesMixin` | Mixin for hashed file storage |
| `django.contrib.staticfiles.handlers.StaticFilesHandler` | WSGI handler for static files |
| `django.contrib.staticfiles.finders.BaseFinder` | Base class for static file finders |
| `django.contrib.staticfiles.finders.FileSystemFinder` | Finder for static files in the filesystem |
| `django.contrib.staticfiles.finders.AppDirectoriesFinder` | Finder for static files in app directories |
| `django.contrib.staticfiles.finders.DefaultStorageFinder` | Finder for static files in default storage |
| `django.contrib.staticfiles.management.commands.collectstatic` | Command to collect static files |
| `django.contrib.staticfiles.management.commands.runserver` | Command to run the development server |
| `django.contrib.staticfiles.templatetags.static` | Template tag for static files |
| `django.contrib.staticfiles.templatetags.staticfiles` | Template tag for static files (deprecated) |

---
### **Humanize Template Filters**

| Filter | Description |
|--------|-------------|
| `apnumber` | Returns the number as an ordinal (1st, 2nd, 3rd, etc.) |
| `intcomma` | Adds commas as thousand separators |
| `intword` | Converts a large integer to a friendly text representation |
| `naturalday` | Formats a date as "today", "tomorrow", "yesterday", or "X days ago" |
| `naturaltime` | Formats a datetime as "now", "an hour ago", "10 minutes ago", etc. |
| `ordinal` | Converts an integer to its ordinal string (1st, 2nd, 3rd, etc.) |

---
### **Markup Template Filters**

| Filter | Description |
|--------|-------------|
| `markdown` | Renders Markdown as HTML |
| `restructuredtext` | Renders reStructuredText as HTML |
| `textile` | Renders Textile as HTML |

---
### **Sitemaps Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.sitemaps.Sitemap` | Base class for sitemap classes |
| `django.contrib.sitemaps.GenericSitemap` | Generic sitemap class for any model |
| `django.contrib.sitemaps.views.index` | Index sitemap view |
| `django.contrib.sitemaps.views.sitemap` | Sitemap view |
| `django.contrib.sitemaps.ping_google` | Pings Google with the sitemap URL |
| `django.contrib.sitemaps.ping_google_sitemap` | Pings Google with the sitemap URL (alias for ping_google) |

---
### **Sitemap Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `sitemap.changefreq` | Default change frequency for sitemap items |
| `sitemap.priority` | Default priority for sitemap items |
| `sitemap.protocol` | Protocol to use for sitemap URLs |
| `sitemap.items()` | Returns a list of items for the sitemap |
| `sitemap.lastmod(obj)` | Returns the last modification date for the given object |
| `sitemap.changefreq(obj)` | Returns the change frequency for the given object |
| `sitemap.priority(obj)` | Returns the priority for the given object |
| `sitemap.location(obj)` | Returns the URL for the given object |

---
### **Syndication Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.syndication.views.Feed` | Base class for feed views |
| `django.contrib.syndication.views.FeedDoesNotExist` | Exception raised when a feed does not exist |
| `django.contrib.syndication.feeds.Feed` | Base class for feed classes |
| `django.contrib.syndication.feeds.RSSFeed` | RSS feed class |
| `django.contrib.syndication.feeds.Atom1Feed` | Atom 1.0 feed class |
| `django.contrib.syndication.feeds.JSONFeed` | JSON feed class |

---
### **Feed Attributes and Methods**

| Attribute/Method | Description |
|------------------|-------------|
| `feed.title` | Title of the feed |
| `feed.link` | URL of the feed |
| `feed.description` | Description of the feed |
| `feed.language` | Language of the feed |
| `feed.feed_type` | Type of the feed |
| `feed.feed_version` | Version of the feed |
| `feed.subtitle` | Subtitle of the feed |
| `feed.author_name` | Author name of the feed |
| `feed.author_email` | Author email of the feed |
| `feed.author_link` | Author link of the feed |
| `feed.categories` | Categories of the feed |
| `feed.feed_url` | URL of the feed |
| `feed.feed_guid` | GUID of the feed |
| `feed.ttl` | Time to live of the feed |
| `feed.items()` | Returns a list of items for the feed |
| `feed.item_title(item)` | Returns the title for the given item |
| `feed.item_description(item)` | Returns the description for the given item |
| `feed.item_link(item)` | Returns the link for the given item |
| `feed.item_guid(item)` | Returns the GUID for the given item |
| `feed.item_guid_is_permalink(item)` | Returns True if the GUID is a permalink |
| `feed.item_pubdate(item)` | Returns the publication date for the given item |
| `feed.item_updateddate(item)` | Returns the update date for the given item |
| `feed.item_categories(item)` | Returns the categories for the given item |
| `feed.item_author_name(item)` | Returns the author name for the given item |
| `feed.item_author_email(item)` | Returns the author email for the given item |
| `feed.item_author_link(item)` | Returns the author link for the given item |
| `feed.item_enclosure_url(item)` | Returns the enclosure URL for the given item |
| `feed.item_enclosure_length(item)` | Returns the enclosure length for the given item |
| `feed.item_enclosure_mime_type(item)` | Returns the enclosure MIME type for the given item |

---
### **Messages Framework Template Tags**

| Tag | Description |
|-----|-------------|
| `{% if messages %}` | Checks if there are any messages |
| `{% for message in messages %}` | Iterates over the messages |
| `message.tags` | Returns the tags for the message |
| `message.level` | Returns the level for the message |
| `message.level_tag` | Returns the level tag for the message |
| `message.message` | Returns the message text |

---
### **CSRF Template Tags and Context Processors**

| Tag/Processor | Description |
|---------------|-------------|
| `{% csrf_token %}` | Outputs a hidden form field with a CSRF token |
| `django.middleware.csrf.get_token(request)` | Returns the CSRF token for the request |
| `django.middleware.csrf.CsrfViewMiddleware` | Middleware for CSRF protection |
| `django.middleware.csrf.CsrfResponseMiddleware` | Middleware for adding CSRF tokens to responses |
| `django.middleware.csrf.RejectedCsrfRequest` | Exception raised when a CSRF token is rejected |

---
---
---
## **Django Exceptions**

| Exception | Description |
|-----------|-------------|
| `django.core.exceptions.ObjectDoesNotExist` | Exception raised when a requested object does not exist |
| `django.core.exceptions.DoesNotExist` | Exception raised when a requested object does not exist (alias for ObjectDoesNotExist) |
| `django.core.exceptions.MultipleObjectsReturned` | Exception raised when get() returns multiple objects |
| `django.core.exceptions.SuspiciousOperation` | Exception raised for suspicious operations |
| `django.core.exceptions.SuspiciousFileOperation` | Exception raised for suspicious file operations |
| `django.core.exceptions.DisallowedRedirect` | Exception raised for disallowed redirects |
| `django.core.exceptions.ImproperlyConfigured` | Exception raised for improper configuration |
| `django.core.exceptions.FieldError` | Exception raised for field errors |
| `django.core.exceptions.ValidationError` | Exception raised for validation errors |
| `django.core.exceptions.PermissionDenied` | Exception raised when a user does not have permission |
| `django.core.exceptions.FieldDoesNotExist` | Exception raised when a field does not exist |
| `django.core.exceptions.AppRegistryNotReady` | Exception raised when the app registry is not ready |
| `django.core.exceptions.SynchronousOnlyOperation` | Exception raised for synchronous-only operations |
| `django.db.utils.OperationalError` | Exception raised for database operational errors |
| `django.db.utils.ProgrammingError` | Exception raised for database programming errors |
| `django.db.utils.IntegrityError` | Exception raised for database integrity errors |
| `django.db.utils.DataError` | Exception raised for database data errors |
| `django.db.utils.DatabaseError` | Exception raised for database errors |
| `django.db.utils.InternalError` | Exception raised for internal database errors |
| `django.http.Http404` | Exception raised for 404 not found errors |
| `django.http.Http500` | Exception raised for 500 server errors |
| `django.http.Http403` | Exception raised for 403 forbidden errors |
| `django.http.Http400` | Exception raised for 400 bad request errors |
| `django.http.Http405` | Exception raised for 405 method not allowed errors |
| `django.http.UnsupportedMediaType` | Exception raised for unsupported media type errors |
| `django.template.TemplateDoesNotExist` | Exception raised when a template does not exist |
| `django.template.TemplateSyntaxError` | Exception raised for template syntax errors |
| `django.views.ViewDoesNotExist` | Exception raised when a view does not exist |
| `django.contrib.auth.exceptions.PermissionDenied` | Exception raised when a user does not have permission |
| `django.contrib.auth.exceptions.ImproperlyConfigured` | Exception raised for improper authentication configuration |

---
---
---
## **Django Context Processors**

| Context Processor | Description |
|-------------------|-------------|
| `django.template.context_processors.debug` | Adds debug information to the context |
| `django.template.context_processors.request` | Adds the request object to the context |
| `django.template.context_processors.auth` | Adds the user object to the context |
| `django.template.context_processors.messages` | Adds the messages to the context |
| `django.template.context_processors.static` | Adds the static URL to the context |
| `django.template.context_processors.media` | Adds the media URL to the context |
| `django.template.context_processors.csrf` | Adds the CSRF token to the context |
| `django.template.context_processors.tz` | Adds timezone information to the context |
| `django.template.context_processors.i18n` | Adds internationalization information to the context |
| `django.template.context_processors.l10n` | Adds localization information to the context |

---
---
---
## **Django Security Utilities**

| Function/Class | Description |
|----------------|-------------|
| `django.middleware.csrf.CsrfViewMiddleware` | Middleware for CSRF protection |
| `django.middleware.csrf.get_token(request)` | Returns the CSRF token for the request |
| `django.middleware.csrf.csrf_protect(view_func)` | Decorator to add CSRF protection to a view |
| `django.middleware.csrf.csrf_exempt(view_func)` | Decorator to exempt a view from CSRF protection |
| `django.middleware.csrf.requires_csrf_token(view_func)` | Decorator to require CSRF token for a view |
| `django.middleware.clickjacking.XFrameOptionsMiddleware` | Middleware for X-Frame-Options header |
| `django.middleware.security.SecurityMiddleware` | Middleware for various security headers |
| `django.utils.deprecation.MiddlewareMixin` | Mixin for middleware classes to handle deprecation |
| `django.utils.http.is_safe_url(url)` | Returns True if the URL is safe for redirecting |
| `django.utils.http.url_has_allowed_netloc(url)` | Returns True if the URL has an allowed netloc |
| `django.middleware.security.ForceHttpsMiddleware` | Middleware to force HTTPS |
| `django.middleware.security.ContentSecurityPolicyMiddleware` | Middleware for Content-Security-Policy header |
| `django.middleware.security.ReferrerPolicyMiddleware` | Middleware for Referrer-Policy header |
| `django.middleware.security.PermissionsPolicyMiddleware` | Middleware for Permissions-Policy header |
| `django.middleware.security.XssProtectMiddleware` | Middleware for X-XSS-Protection header |

---
---
---
## **Django Cache Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.core.cache.cache` | Default cache instance |
| `django.core.cache.caches` | Dictionary of configured cache instances |
| `django.core.cache.get_cache(backend)` | Returns the cache instance for the given backend |
| `django.core.cache.cache_page(timeout, cache=None, key_prefix=None)` | Decorator to cache the entire view response |
| `django.core.cache.never_cache(view_func)` | Decorator to disable caching for a view |
| `django.core.cache.cache_control(**kwargs)` | Decorator to add cache-control headers to the response |
| `django.core.cache.vary_on_headers(*headers)` | Decorator to add Vary headers to the response |
| `django.core.cache.vary_on_cookie` | Decorator to add Vary: Cookie header to the response |
| `django.core.cache.backends.base.BaseCache` | Base class for cache backends |
| `django.core.cache.backends.locmem.LocMemCache` | Local memory cache backend |
| `django.core.cache.backends.dummy.DummyCache` | Dummy cache backend (no-op) |
| `django.core.cache.backends.filebased.FileBasedCache` | File-based cache backend |
| `django.core.cache.backends.db.DatabaseCache` | Database cache backend |
| `django.core.cache.backends.memcached.MemcachedCache` | Memcached cache backend |
| `django.core.cache.backends.memcached.PyLibMCCache` | PyLibMC cache backend |
| `django.core.cache.backends.redis.RedisCache` | Redis cache backend |
| `django.core.cache.backends.redis.RedisCacheServer` | Redis cache server |

---
### **Cache Backend Methods**

| Method | Description |
|--------|-------------|
| `cache.get(key, default=None, version=None)` | Returns the value for the given key |
| `cache.set(key, value, timeout=None, version=None)` | Sets the value for the given key |
| `cache.add(key, value, timeout=None, version=None)` | Adds the value for the given key if it does not exist |
| `cache.replace(key, value, timeout=None, version=None)` | Replaces the value for the given key if it exists |
| `cache.delete(key, version=None)` | Deletes the value for the given key |
| `cache.delete_many(keys, version=None)` | Deletes multiple values |
| `cache.clear()` | Clears the entire cache |
| `cache.incr(key, delta=1, version=None)` | Increments the value for the given key |
| `cache.decr(key, delta=1, version=None)` | Decrements the value for the given key |
| `cache.get_many(keys, version=None)` | Returns a dictionary of values for the given keys |
| `cache.set_many(dict, timeout=None, version=None)` | Sets multiple values |
| `cache.touch(key, timeout=None, version=None)` | Updates the timeout for the given key |
| `cache.has_key(key, version=None)` | Returns True if the key exists in the cache |
| `cache.get_or_set(key, default, timeout=None, version=None)` | Returns the value for the key or sets it if it does not exist |
| `cache.cull()` | Removes stale cache entries |
| `cache.close()` | Closes the cache connection |

---
---
---
## **Django Logging**

| Function/Class | Description |
|----------------|-------------|
| `django.utils.log.getLogger(name)` | Returns a logger with the given name |
| `django.utils.log.setup_logging()` | Sets up Django's logging configuration |
| `django.utils.log.disable_logging()` | Disables Django's logging configuration |
| `django.utils.log.reset_logging()` | Resets Django's logging configuration |
| `django.utils.log.configure_logging(logging_config, logging_settings)` | Configures Django's logging |
| `django.utils.log.get_logging_config()` | Returns the current logging configuration |
| `django.utils.log.get_level_name(level)` | Returns the name of the logging level |
| `django.utils.log.get_level_num(level)` | Returns the numeric value of the logging level |
| `django.utils.log.make_log_record(logger_name, level, fn, lno, msg, args, exc_info, func=None, extra=None, sinfo=None)` | Creates a log record |
| `django.utils.log.callback_log_record_factory(logger, typ, callback, *args, **kwargs)` | Creates a log record factory for callbacks |
| `django.utils.log.default_exception_logging` | Default exception logging function |
| `django.utils.log.default_logging` | Default logging function |
| `django.utils.log.log_response(message, response, logger, level)` | Logs a response |
| `django.utils.log.log_unhandled_exception(exc_type, exc_value, exc_traceback)` | Logs an unhandled exception |
| `django.utils.log.require_debug_false(func)` | Decorator to require DEBUG=False |
| `django.utils.log.require_debug_true(func)` | Decorator to require DEBUG=True |
| `django.utils.log.simple_logging(log_to, level, bubble_up)` | Simple logging configuration |

---
---
---
## **Django Serializers**

| Class/Function | Description |
|----------------|-------------|
| `django.core.serializers.json.DjangoJSONEncoder` | JSON encoder for Django objects |
| `django.core.serializers.jsonSerializer` | JSON serializer |
| `django.core.serializers.pythonSerializer` | Python serializer |
| `django.core.serializers.xmlSerializer` | XML serializer |
| `django.core.serializers.yamlSerializer` | YAML serializer |
| `django.core.serializers.serialize(format, queryset, **options)` | Serializes a queryset to the given format |
| `django.core.serializers.deserialize(format, data, **options)` | Deserializes data from the given format |
| `django.core.serializers.base.Serializer` | Base class for serializers |
| `django.core.serializers.base.Deserializer` | Base class for deserializers |
| `django.core.serializers.base.SerializerDoesNotExist` | Exception raised when a serializer does not exist |
| `django.core.serializers.base.DeserializationError` | Exception raised for deserialization errors |

---
---
---
## **Django Pagination**

| Class/Function | Description |
|----------------|-------------|
| `django.core.paginator.Paginator` | Class for paginating querysets or lists |
| `django.core.paginator.Page` | Class for a single page of results |
| `django.core.paginator.EmptyPage` | Exception raised when a page is empty |
| `django.core.paginator.PageNotAnInteger` | Exception raised when a page is not an integer |
| `django.core.paginator.InvalidPage` | Exception raised for invalid page numbers |

---
### **Paginator Methods and Attributes**

| Method/Attribute | Description |
|------------------|-------------|
| `Paginator.object_list` | The list or queryset to paginate |
| `Paginator.per_page` | The number of items to display per page |
| `Paginator.orphans` | The number of orphans to allow |
| `Paginator.allow_empty_first_page` | Whether to allow an empty first page |
| `Paginator.num_pages` | The total number of pages |
| `Paginator.page_range` | A range of page numbers |
| `Paginator.page(num)` | Returns a Page object for the given page number |
| `Page.has_next()` | Returns True if there is a next page |
| `Page.has_previous()` | Returns True if there is a previous page |
| `Page.has_other_pages()` | Returns True if there are other pages |
| `Page.next_page_number()` | Returns the next page number |
| `Page.previous_page_number()` | Returns the previous page number |
| `Page.start_index()` | Returns the index of the first item on the page |
| `Page.end_index()` | Returns the index of the last item on the page |
| `Page.object_list` | The list of objects on the page |
| `Page.number` | The page number |
| `Page.paginator` | The Paginator instance for the page |

---
---
---
## **Django Email**

| Class/Function | Description |
|----------------|-------------|
| `django.core.mail.EmailMessage` | Base class for email messages |
| `django.core.mail.EmailMultiAlternatives` | Class for email messages with multiple alternatives |
| `django.core.mail.SMTPConnection` | SMTP connection class |
| `django.core.mail.get_connection(backend=None, fail_silently=False, **kwargs)` | Returns a connection to the email backend |
| `django.core.mail.send_mail(subject, message, from_email, recipient_list, fail_silently=False, auth_user=None, auth_password=None, connection=None)` | Sends an email |
| `django.core.mail.send_mass_mail(datatuple, fail_silently=False, auth_user=None, auth_password=None, connection=None)` | Sends multiple emails |
| `django.core.mail.mail_admins(subject, message, fail_silently=False, connection=None, html_message=None)` | Sends an email to the admins |
| `django.core.mail.mail_managers(subject, message, fail_silently=False, connection=None, html_message=None)` | Sends an email to the managers |
| `django.core.mail.EmailMessage.attach(filename=None, content=None, mimetype=None)` | Attaches a file to the email |
| `django.core.mail.EmailMessage.attach_file(filename, mimetype=None)` | Attaches a file from the filesystem to the email |
| `django.core.mail.EmailMessage.send(fail_silently=False)` | Sends the email |
| `django.core.mail.EmailMessage.message()` | Returns the email message as a string |
| `django.core.mail.EmailMessage.recipients()` | Returns the list of recipients |
| `django.core.mail.EmailMessage.from_email` | The from email address |
| `django.core.mail.EmailMessage.to` | The list of to email addresses |
| `django.core.mail.EmailMessage.bcc` | The list of bcc email addresses |
| `django.core.mail.EmailMessage.cc` | The list of cc email addresses |
| `django.core.mail.EmailMessage.subject` | The email subject |
| `django.core.mail.EmailMessage.body` | The email body |
| `django.core.mail.EmailMessage.alternatives` | The list of alternative email bodies |
| `django.core.mail.EmailMessage.mixed_subtype` | The mixed subtype for the email |
| `django.core.mail.EmailMessage.content_subtype` | The content subtype for the email |
| `django.core.mail.EmailMessage.extra_headers` | The extra headers for the email |
| `django.core.mail.EmailMessage.connection` | The connection to use for sending the email |

---
---
---
## **Django File Uploads**

| Class/Function | Description |
|----------------|-------------|
| `django.core.files.File` | Base class for file objects |
| `django.core.files.base.File` | Base class for file objects |
| `django.core.files.base.ContentFile` | File class for content in memory |
| `django.core.files.base.FileDescriptor` | File descriptor class |
| `django.core.files.uploadhandler.BaseUploadHandler` | Base class for upload handlers |
| `django.core.files.uploadhandler.MemoryFileUploadHandler` | Upload handler for small files in memory |
| `django.core.files.uploadhandler.TemporaryFileUploadHandler` | Upload handler for large files on disk |
| `django.core.files.uploadhandler.FileUploadHandler` | Upload handler for files |
| `django.core.files.uploadhandler.FileUploadParser` | Parser for file uploads |
| `django.core.files.uploadhandler.MultiPartParser` | Parser for multipart file uploads |
| `django.core.files.uploadhandler.RawPostDataException` | Exception raised for raw post data errors |
| `django.core.files.storage.Storage` | Base class for storage backends |
| `django.core.files.storage.FileSystemStorage` | Filesystem storage backend |
| `django.core.files.storage.default_storage` | Default storage backend |
| `django.core.files.storage.storages` | Dictionary of configured storage backends |
| `django.core.files.storage.get_storage_class(import_path)` | Returns the storage class for the given import path |
| `django.core.files.storage.get_storage_instance(import_path)` | Returns a storage instance for the given import path |
| `django.core.files.storage.get_default_storage_class()` | Returns the default storage class |
| `django.core.files.storage.get_default_storage_instance()` | Returns the default storage instance |

---
### **Storage Backend Methods**

| Method | Description |
|--------|-------------|
| `storage.save(name, content, max_length=None)` | Saves the file with the given name and content |
| `storage.open(name, mode='rb')` | Opens the file with the given name and mode |
| `storage.delete(name)` | Deletes the file with the given name |
| `storage.exists(name)` | Returns True if the file with the given name exists |
| `storage.listdir(path)` | Returns a list of files and directories in the given path |
| `storage.size(name)` | Returns the size of the file with the given name |
| `storage.url(name)` | Returns the URL for the file with the given name |
| `storage.get_available_name(name, max_length=None)` | Returns an available name for the given name |
| `storage.get_alternative_name(filename, ext)` | Returns an alternative name for the given filename and extension |
| `storage.generate_signed_url(name, parameters=None, expire=3600)` | Returns a signed URL for the file with the given name |
| `storage.get_default_settings()` | Returns the default settings for the storage backend |

---
---
---
## **Django Validators**

| Validator | Description |
|-----------|-------------|
| `django.core.validators.BaseValidator` | Base class for validators |
| `django.core.validators.ValidationError` | Exception raised for validation errors |
| `django.core.validators.validate_slug` | Validator for slug fields |
| `django.core.validators.validate_unicode_slug` | Validator for Unicode slug fields |
| `django.core.validators.validate_ipv4_address` | Validator for IPv4 addresses |
| `django.core.validators.validate_ipv46_address` | Validator for IPv4 or IPv6 addresses |
| `django.core.validators.validate_comma_separated_integer_list` | Validator for comma-separated integer lists |
| `django.core.validators.validate_integer` | Validator for integer fields |
| `django.core.validators.validate_decimal` | Validator for decimal fields |
| `django.core.validators.validate_email` | Validator for email fields |
| `django.core.validators.validate_url` | Validator for URL fields |
| `django.core.validators.validate_file_extension` | Validator for file extensions |
| `django.core.validators.validate_mime_type` | Validator for MIME types |
| `django.core.validators.validate_image_file_extension` | Validator for image file extensions |
| `django.core.validators.FileExtensionValidator` | Validator for file extensions |
| `django.core.validators.MimeTypeValidator` | Validator for MIME types |
| `django.core.validators.ImageFileExtensionValidator` | Validator for image file extensions |
| `django.core.validators.MinValueValidator` | Validator for minimum values |
| `django.core.validators.MaxValueValidator` | Validator for maximum values |
| `django.core.validators.MinLengthValidator` | Validator for minimum lengths |
| `django.core.validators.MaxLengthValidator` | Validator for maximum lengths |
| `django.core.validators.DecimalValidator` | Validator for decimal values |
| `django.core.validators.EmailValidator` | Validator for email addresses |
| `django.core.validators.URLValidator` | Validator for URLs |
| `django.core.validators.IPv4Validator` | Validator for IPv4 addresses |
| `django.core.validators.IPv6Validator` | Validator for IPv6 addresses |
| `django.core.validators.RegexValidator` | Validator for regular expressions |
| `django.core.validators.ProhibitNullCharactersValidator` | Validator to prohibit null characters |
| `django.core.validators.Validator.compare` | Compares the value with the limit value |

---
---
---
## **Django Internationalization and Localization**

| Class/Function | Description |
|----------------|-------------|
| `django.utils.translation.gettext` | Translates a string |
| `django.utils.translation.ugettext` | Translates a string (alias for gettext) |
| `django.utils.translation.gettext_lazy` | Lazy version of gettext |
| `django.utils.translation.ugettext_lazy` | Lazy version of ugettext (alias for gettext_lazy) |
| `django.utils.translation.ngettext` | Translates a string with pluralization |
| `django.utils.translation.ungettext` | Translates a string with pluralization (alias for ngettext) |
| `django.utils.translation.ngettext_lazy` | Lazy version of ngettext |
| `django.utils.translation.ungettext_lazy` | Lazy version of ungettext (alias for ngettext_lazy) |
| `django.utils.translation.pgettext` | Translates a string with context |
| `django.utils.translation.upgettext` | Translates a string with context (alias for pgettext) |
| `django.utils.translation.pgettext_lazy` | Lazy version of pgettext |
| `django.utils.translation.upgettext_lazy` | Lazy version of upgettext (alias for pgettext_lazy) |
| `django.utils.translation.npgettext` | Translates a string with context and pluralization |
| `django.utils.translation.unpgettext` | Translates a string with context and pluralization (alias for npgettext) |
| `django.utils.translation.npgettext_lazy` | Lazy version of npgettext |
| `django.utils.translation.unpgettext_lazy` | Lazy version of unpgettext (alias for npgettext_lazy) |
| `django.utils.translation.gettext_noop` | Marks a string for translation without translating it |
| `django.utils.translation.gettext_lazy_noop` | Lazy version of gettext_noop |
| `django.utils.translation.string_concat` | Concatenates strings for translation |
| `django.utils.translation.trans_real` | Real translation function |
| `django.utils.translation.trans_null` | Null translation function |
| `django.utils.translation.LANGUAGE_SESSION_KEY` | Session key for language |
| `django.utils.translation.LANGUAGE_COOKIE_NAME` | Cookie name for language |
| `django.utils.translation.LANGUAGE_COOKIE_AGE` | Cookie age for language |
| `django.utils.translation.LANGUAGE_COOKIE_DOMAIN` | Cookie domain for language |
| `django.utils.translation.LANGUAGE_COOKIE_PATH` | Cookie path for language |
| `django.utils.translation.LANGUAGE_COOKIE_SECURE` | Cookie secure flag for language |
| `django.utils.translation.LANGUAGE_COOKIE_HTTPONLY` | Cookie HTTP-only flag for language |
| `django.utils.translation.LANGUAGE_COOKIE_SAMESITE` | Cookie SameSite flag for language |
| `django.utils.translation.activate(language)` | Activates the specified language for the current thread |
| `django.utils.translation.deactivate()` | Deactivates the current language for the current thread |
| `django.utils.translation.deactivate_all()` | Deactivates all languages for the current thread |
| `django.utils.translation.get_language()` | Returns the current language for the current thread |
| `django.utils.translation.get_language_from_request(request)` | Returns the language from the request |
| `django.utils.translation.get_language_from_path(path)` | Returns the language from the path |
| `django.utils.translation.get_supported_language_variant(language_code)` | Returns the supported language variant for the given language code |
| `django.utils.translation.to_locale(language)` | Converts a language code to a locale |
| `django.utils.translation.check_for_language(lang_code)` | Checks if the language is supported |
| `django.utils.translation.get_language_info(language_code)` | Returns information about the given language |
| `django.utils.translation.get_language_list()` | Returns a list of supported languages |
| `django.utils.translation.get_language_bidi(language_code)` | Returns the bidirectional code for the given language |
| `django.utils.translation.language` | Context manager for temporarily activating a language |
| `django.utils.translation.override` | Context manager for temporarily overriding the current language |
| `django.utils.translation.translation` | Class for managing translations |
| `django.utils.translation.Translator` | Class for managing translations |
| `django.utils.translation.NullTranslations` | Null translations class |
| `django.utils.translation.DefaultTranslation` | Default translation class |

---
---
---
## **Django Timezone Utilities**

| Function | Description |
|----------|-------------|
| `django.utils.timezone.now()` | Returns the current datetime with timezone information |
| `django.utils.timezone.localtime(value=None, timezone=None)` | Converts a datetime to the local timezone |
| `django.utils.timezone.utc` | The UTC timezone |
| `django.utils.timezone.get_current_timezone()` | Returns the current timezone |
| `django.utils.timezone.get_current_timezone_name()` | Returns the name of the current timezone |
| `django.utils.timezone.get_default_timezone()` | Returns the default timezone |
| `django.utils.timezone.set_default_timezone(tz)` | Sets the default timezone |
| `django.utils.timezone.activate(timezone)` | Activates the specified timezone for the current thread |
| `django.utils.timezone.deactivate()` | Deactivates the timezone for the current thread |
| `django.utils.timezone.is_aware(value)` | Returns True if the value is timezone-aware |
| `django.utils.timezone.is_naive(value)` | Returns True if the value is timezone-naive |
| `django.utils.timezone.make_aware(value, timezone=None)` | Makes a timezone-naive datetime timezone-aware |
| `django.utils.timezone.make_naive(value, timezone=None)` | Makes a timezone-aware datetime timezone-naive |
| `django.utils.timezone.normalize(value)` | Normalizes a datetime to the current timezone |
| `django.utils.timezone.localtime(value=None, timezone=None)` | Converts a datetime to the local timezone |
| `django.utils.timezone.fix_localtime(value)` | Fixes the localtime for the given value |

---
---
---
## **Django Feed Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.syndication.views.Feed` | Base class for feed views |
| `django.contrib.syndication.feeds.Feed` | Base class for feed classes |
| `django.contrib.syndication.feeds.RSSFeed` | RSS feed class |
| `django.contrib.syndication.feeds.Atom1Feed` | Atom 1.0 feed class |
| `django.contrib.syndication.feeds.JSONFeed` | JSON feed class |
| `django.contrib.syndication.feeds.FeedDoesNotExist` | Exception raised when a feed does not exist |
| `django.contrib.syndication.views.Feed` | Base class for feed views |

---
---
---
## **Django Sitemap Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.sitemaps.Sitemap` | Base class for sitemap classes |
| `django.contrib.sitemaps.GenericSitemap` | Generic sitemap class for any model |
| `django.contrib.sitemaps.views.index` | Index sitemap view |
| `django.contrib.sitemaps.views.sitemap` | Sitemap view |
| `django.contrib.sitemaps.ping_google` | Pings Google with the sitemap URL |
| `django.contrib.sitemaps.ping_google_sitemap` | Pings Google with the sitemap URL (alias for ping_google) |

---
---
---
## **Django Flatpages Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.flatpages.models.FlatPage` | Model for flat pages |
| `django.contrib.flatpages.sitemaps.FlatPageSitemap` | Sitemap for flat pages |
| `django.contrib.flatpages.middleware.FlatpageFallbackMiddleware` | Middleware for flat page fallback |
| `django.contrib.flatpages.views.flatpage` | View for displaying flat pages |

---
---
---
## **Django Redirects Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.redirects.models.Redirect` | Model for redirects |
| `django.contrib.redirects.middleware.RedirectFallbackMiddleware` | Middleware for redirect fallback |
| `django.contrib.redirects.views.redirect_to` | View for handling redirects |

---
---
---
## **Django Sites Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.sites.models.Site` | Model for sites |
| `django.contrib.sites.requests.RequestSite` | Request-based site model |
| `django.contrib.sites.shortcuts.get_current_site(request)` | Returns the current site for the request |
| `django.contrib.sites.shortcuts.get_current_site_name(request)` | Returns the name of the current site for the request |

---
---
---
## **Django Messages Framework**

| Class/Function | Description |
|----------------|-------------|
| `django.contrib.messages.storage.base.BaseStorage` | Base class for message storage |
| `django.contrib.messages.storage.cookie.CookieStorage` | Cookie-based message storage |
| `django.contrib.messages.storage.session.SessionStorage` | Session-based message storage |
| `django.contrib.messages.storage.fallback.FallbackStorage` | Fallback message storage |
| `django.contrib.messages.middleware.MessageMiddleware` | Middleware for message handling |
| `django.contrib.messages.api.add_message(request, level, message, extra_tags='', fail_silently=False)` | Adds a message to the request |
| `django.contrib.messages.api.set_level(request, level)` | Sets the minimum message level for the request |
| `django.contrib.messages.api.get_level(request)` | Returns the minimum message level for the request |
| `django.contrib.messages.api.messages(request)` | Returns the messages for the request |
| `django.contrib.messages.api.get_messages(request)` | Returns the messages for the request |
| `django.contrib.messages.api.used(request)` | Returns True if the messages have been used |
| `django.contrib.messages.api.unuse(request)` | Marks the messages as unused |
| `django.contrib.messages.constants.DEBUG` | Debug message level |
| `django.contrib.messages.constants.INFO` | Info message level |
| `django.contrib.messages.constants.SUCCESS` | Success message level |
| `django.contrib.messages.constants.WARNING` | Warning message level |
| `django.contrib.messages.constants.ERROR` | Error message level |