## Decorators

| Code | Description |
|------|-------------|
| `@Component({selector, templateUrl, template, styleUrls, styles, providers, viewProviders, changeDetection, encapsulation, animations, interpolation})` | Decorator that defines a component's metadata, including its selector, template, and styles. |
| `@Directive({selector, providers, exportAs, host, inputs, outputs, queries, standalone})` | Decorator that defines a directive's metadata. |
| `@Pipe({name, pure, standalone})` | Decorator that defines a pipe's metadata, including its name and whether it is pure. |
| `@Injectable({providedIn})` | Decorator that marks a class as available for dependency injection. `providedIn` specifies where the service is provided. |
| `@NgModule({declarations, imports, exports, providers, bootstrap, entryComponents, schemas, id})` | Decorator that defines a module's metadata, including its declarations, imports, and providers. |
| `@Input([bindingPropertyName])` | Decorator that marks a class field as an input property, allowing data to be passed from a parent component. |
| `@Output([bindingPropertyName])` | Decorator that marks a class field as an output property, allowing events to be emitted to a parent component. |
| `@ViewChild(selector, {static, read})` | Decorator that provides a reference to a child component, directive, or element in the view. |
| `@ViewChildren(selector, {read})` | Decorator that provides a reference to multiple child components, directives, or elements in the view. |
| `@ContentChild(selector, {static, read})` | Decorator that provides a reference to projected content (ng-content) in the view. |
| `@ContentChildren(selector, {read})` | Decorator that provides a reference to multiple projected content elements in the view. |
| `@HostListener(eventName, [args])` | Decorator that listens for events on the host element. |
| `@HostBinding(propertyName)` | Decorator that binds a host element property to a class field. |
| `@Attribute(attributeName)` | Decorator that provides access to an attribute value on the host element. |

---

## Lifecycle Hooks

| Code | Description |
|------|-------------|
| `ngOnChanges(changes: SimpleChanges)` | Called when one or more input-bound properties change. Receives a `SimpleChanges` object containing the changes. |
| `ngOnInit()` | Called once after the first `ngOnChanges`. Used for initialization logic. |
| `ngDoCheck()` | Called during every change detection cycle. Used for custom change detection. |
| `ngAfterViewInit()` | Called once after the component's view is initialized. |
| `ngAfterViewChecked()` | Called after every change detection cycle for the component's view. |
| `ngAfterContentInit()` | Called once after the projected content (ng-content) is initialized. |
| `ngAfterContentChecked()` | Called after every change detection cycle for projected content. |
| `ngOnDestroy()` | Called when the component is destroyed. Used for cleanup logic. |

---

## Core Classes

| Code | Description |
|------|-------------|
| `Component` | Base class for Angular components. |
| `Directive` | Base class for Angular directives. |
| `Pipe` | Base class for Angular pipes. |
| `Injectable` | Base class for injectable services. |
| `NgModule` | Base class for Angular modules. |
| `ApplicationRef` | Reference to the running Angular application. Provides methods to manually trigger change detection. |
| `ChangeDetectorRef` | Reference to the change detector for a component. Provides methods like `detectChanges()`, `markForCheck()`, `detach()`, and `reattach()`. |
| `ElementRef` | Wrapper around a native DOM element. Provides access to the native element via the `nativeElement` property. |
| `TemplateRef` | Reference to a template. Used with `ViewContainerRef` to dynamically create views. |
| `ViewContainerRef` | Container for dynamically created views. Provides methods like `createEmbeddedView()`, `createComponent()`, `clear()`, and `remove()`. |
| `EmbeddedViewRef` | Reference to an embedded view. Provides methods like `destroy()` and `markForCheck()`. |
| `ComponentRef` | Reference to a dynamically created component. Provides access to the component instance, host element, and methods like `destroy()`. |
| `ComponentFactory<T>` | Factory for creating components dynamically. |
| `ComponentFactoryResolver` | Resolver for component factories. Provides methods to resolve component factories. |
| `ViewRef` | Base class for views. Provides methods like `markForCheck()` and `onDestroy()`. |
| `NgZone` | Angular zone service. Provides methods like `run()`, `runOutsideAngular()`, `runTask()`, and `onStable`. |
| `SimpleChanges` | Container for changes to input properties. Contains `currentValue`, `previousValue`, `firstChange`, and `isFirstChange()` for each property. |
| `SimpleChange` | Represents a change to a single input property. |

---

## Dependency Injection

| Code | Description |
|------|-------------|
| `Injector` | Container for dependency injection. Provides methods like `get()`, `createInjector()`, and `resolveAndCreateChild()`. |
| `InjectFlags` | Flags for dependency injection. Includes `Default`, `Host`, `Self`, `SkipSelf`, and `Optional`. |
| `@Inject(token)` | Decorator that specifies the injection token for a parameter. |
| `@Optional()` | Decorator that marks a dependency as optional. If the dependency is not available, `null` is injected. |
| `@Self()` | Decorator that restricts the injector search to the current injector. |
| `@SkipSelf()` | Decorator that excludes the current injector from the search. |
| `@Host()` | Decorator that restricts the injector search to the current host injector. |
| `InjectionToken<T>(desc, options?)` | Creates a unique injection token. Used for non-class dependencies. |
| `OpaqueToken` | Deprecated. Use `InjectionToken` instead. |
| `Injector.create({providers, parent})` | Creates a new injector with the specified providers and optional parent injector. |
| `injector.get(token, notFoundValue?, flags?)` | Retrieves a dependency from the injector. |
| `Provider` | Interface for defining providers. Can be a class, value, factory, or existing provider. |
| `{ provide: token, useClass: class }` | Provider that instantiates a class. |
| `{ provide: token, useValue: value }` | Provider that uses a predefined value. |
| `{ provide: token, useFactory: factory, deps: dependencies }` | Provider that uses a factory function. |
| `{ provide: token, useExisting: existingToken }` | Provider that aliases one token to another. |
| `ClassProvider` | Type for class providers. |
| `ValueProvider` | Type for value providers. |
| `FactoryProvider` | Type for factory providers. |
| `ExistingProvider` | Type for existing providers. |
| `StaticProvider` | Type for static providers. |
| `forwardRef(() => SomeClass)` | Allows referencing a class that is not yet defined. Used for circular dependencies. |

---

## HTTP Client

| Code | Description |
|------|-------------|
| `HttpClient` | Service for making HTTP requests. Provides methods like `get()`, `post()`, `put()`, `delete()`, `head()`, `options()`, `patch()`, and `request()`. |
| `HttpClientModule` | Module that provides the `HttpClient` service and related classes. |
| `HttpClient.get(url, options?)` | Sends a GET request to the specified URL. |
| `HttpClient.post(url, body, options?)` | Sends a POST request to the specified URL with the specified body. |
| `HttpClient.put(url, body, options?)` | Sends a PUT request to the specified URL with the specified body. |
| `HttpClient.delete(url, options?)` | Sends a DELETE request to the specified URL. |
| `HttpClient.head(url, options?)` | Sends a HEAD request to the specified URL. |
| `HttpClient.options(url, options?)` | Sends an OPTIONS request to the specified URL. |
| `HttpClient.patch(url, body, options?)` | Sends a PATCH request to the specified URL with the specified body. |
| `HttpClient.request(method, url, options?)` | Sends a request with the specified HTTP method. |
| `HttpHeaders` | Class for creating HTTP headers. Provides methods like `append()`, `set()`, `has()`, `get()`, `getAll()`, and `delete()`. |
| `HttpParams` | Class for creating HTTP URL query parameters. Provides methods like `append()`, `set()`, `has()`, `get()`, `getAll()`, and `delete()`. |
| `HttpErrorResponse` | Class representing an HTTP error response. Contains properties like `error`, `message`, `name`, `ok`, `status`, `statusText`, `type`, and `url`. |
| `HttpResponse<T>` | Class representing an HTTP response. Contains properties like `body`, `headers`, `status`, `statusText`, `type`, and `url`. |
| `HttpEvent<T>` | Base class for HTTP events, including `HttpSentEvent`, `HttpHeaderResponse`, `HttpResponse`, `HttpProgressEvent`, and `HttpUserEvent`. |
| `HttpInterceptor` | Interface for HTTP interceptors. Requires implementation of the `intercept()` method. |
| `HttpInterceptorHandler` | Handler for HTTP interceptors. Provides methods like `handle()`. |
| `HTTP_INTERCEPTORS` | Injection token for HTTP interceptors. |
| `{ provide: HTTP_INTERCEPTORS, useClass: MyInterceptor, multi: true }` | Provider for adding an HTTP interceptor. |
| `HttpClientJsonpModule` | Module for making JSONP requests. |
| `HttpClientXsrfModule` | Module for XSRF protection. |

---
## Router

| Code | Description |
|------|-------------|
| `Router` | Service for navigating and manipulating the router state. Provides methods like `navigate()`, `navigateByUrl()`, `createUrlTree()`, and `serializeUrl()`. |
| `RouterModule` | Module for configuring the router. |
| `RouterModule.forRoot(routes, config?)` | Configures the router at the application's root level. |
| `RouterModule.forChild(routes)` | Configures the router for a lazy-loaded module. |
| `Routes` | Type for defining router routes. An array of `Route` objects. |
| `Route` | Interface for defining a route. Contains properties like `path`, `pathMatch`, `matcher`, `component`, `redirectTo`, `outlet`, `canActivate`, `canDeactivate`, `canActivateChild`, `canDeactivateChild`, `canLoad`, `data`, `resolve`, `children`, `loadChildren`, `runGuardsAndResolvers`. |
| `path: 'path'` | Defines the path for a route. Supports static paths, parameterized paths (e.g., `':id'`), and wildcards (e.g., `'**'`). |
| `pathMatch: 'full'` | Specifies that the path must match the entire URL. |
| `pathMatch: 'prefix'` | Specifies that the path must match the beginning of the URL. |
| `redirectTo: '/path'` | Redirects to the specified path. |
| `outlet: 'outletName'` | Specifies the named router outlet for the route. |
| `component: MyComponent` | Specifies the component to display for the route. |
| `loadChildren: () => import('./module').then(m => m.Module)` | Specifies a lazy-loaded module for the route. |
| `canActivate: [MyGuard]` | Specifies guards that must pass before the route can be activated. |
| `canDeactivate: [MyGuard]` | Specifies guards that must pass before the route can be deactivated. |
| `canActivateChild: [MyGuard]` | Specifies guards that must pass before child routes can be activated. |
| `canDeactivateChild: [MyGuard]` | Specifies guards that must pass before child routes can be deactivated. |
| `canLoad: [MyGuard]` | Specifies guards that must pass before a lazy-loaded module can be loaded. |
| `resolve: { key: MyResolver }` | Specifies resolvers that fetch data before the route is activated. |
| `data: { key: value }` | Specifies static data for the route. |
| `ActivatedRoute` | Service for accessing information about the current route. Provides properties like `url`, `params`, `queryParams`, `fragment`, `data`, `outlet`, `component`, `snapshot`, `routeConfig`, `root`, `firstChild`, `children`, and `pathFromRoot`. |
| `ActivatedRouteSnapshot` | Snapshot of the current route. Provides properties like `url`, `params`, `queryParams`, `fragment`, `data`, `outlet`, `component`, `routeConfig`, `root`, `firstChild`, `children`, and `pathFromRoot`. |
| `RouterStateSnapshot` | Snapshot of the router state. |
| `ParamMap` | Interface for accessing route parameters. Provides methods like `get()`, `getAll()`, `has()`, and `keys`. |
| `QueryParamMap` | Interface for accessing query parameters. |
| `UrlSegment` | Represents a URL segment. Provides properties like `path`, `parameters`, and `parameterMap`. |
| `UrlSegmentGroup` | Represents a group of URL segments. |
| `UrlTree` | Represents a URL tree. |
| `NavigationExtras` | Interface for extra options when navigating. Contains properties like `skipLocationChange`, `replaceUrl`, `state`, `relativeTo`, `queryParams`, `fragment`, `queryParamsHandling`, and `preserveFragment`. |
| `CanActivate` | Interface for route guards that determine if a route can be activated. Requires implementation of the `canActivate()` method. |
| `CanDeactivate<T>` | Interface for route guards that determine if a route can be deactivated. Requires implementation of the `canDeactivate()` method. |
| `CanActivateChild` | Interface for route guards that determine if child routes can be activated. |
| `CanDeactivateChild` | Interface for route guards that determine if child routes can be deactivated. |
| `CanLoad` | Interface for route guards that determine if a lazy-loaded module can be loaded. |
| `Resolve<T>` | Interface for resolvers that fetch data before a route is activated. Requires implementation of the `resolve()` method. |
| `RouterOutlet` | Directive for marking where the router should display components. |
| `RouterLink` | Directive for creating links to routes. |
| `RouterLinkActive` | Directive for adding CSS classes to active router links. |
| `<router-outlet></router-outlet>` | Template tag for marking where the router should display components. |
| `<a routerLink="/path" routerLinkActive="active">Link</a>` | Template syntax for creating a router link. |
| `routerLink="['/path', param]` | Template syntax for creating a router link with parameters. |
| `routerLinkActive="active"` | Template syntax for adding CSS classes to active router links. |

---
## Forms

| Code | Description |
|------|-------------|
| `FormsModule` | Module for template-driven forms. |
| `ReactiveFormsModule` | Module for reactive forms. |
| `FormControl` | Class for managing the state of a single form control. Provides properties like `value`, `status`, `valid`, `invalid`, `pending`, `disabled`, `enabled`, `errors`, `pristine`, `dirty`, `touched`, `untouched`, and `valueChanges`. |
| `FormGroup` | Class for managing a group of form controls. Provides methods like `addControl()`, `removeControl()`, `setControl()`, `get()`, `getRawValue()`, `patchValue()`, `setValue()`, `reset()`, and `disable()`. |
| `FormArray` | Class for managing an array of form controls. Provides methods like `push()`, `insert()`, `removeAt()`, `setControl()`, and `at()`. |
| `FormBuilder` | Service for creating form controls, form groups, and form arrays. Provides methods like `control()`, `group()`, and `array()`. |
| `AbstractControl` | Base class for form controls. Provides properties and methods common to all form controls. |
| `Validator` | Interface for synchronous validators. Requires implementation of the `validate()` method. |
| `AsyncValidator` | Interface for asynchronous validators. Requires implementation of the `validate()` method. |
| `Validators` | Class containing built-in validators. Provides static methods like `required()`, `requiredTrue()`, `min()`, `max()`, `minLength()`, `maxLength()`, `pattern()`, `nullValidator()`, `compose()`, and `composeAsync()`. |
| `ValidatorFn` | Type for synchronous validator functions. |
| `AsyncValidatorFn` | Type for asynchronous validator functions. |
| `NgForm` | Directive for managing a template-driven form. Provides properties like `form`, `controls`, `value`, `valid`, `invalid`, `pending`, `disabled`, `pristine`, `dirty`, `touched`, `untouched`, and `submitted`. |
| `NgModel` | Directive for managing a template-driven form control. Provides properties like `control`, `name`, `value`, `valid`, `invalid`, `pending`, `disabled`, `errors`, `pristine`, `dirty`, `touched`, and `untouched`. |
| `NgModelGroup` | Directive for managing a group of template-driven form controls. |
| `FormGroupDirective` | Directive for managing a reactive form group. |
| `FormControlDirective` | Directive for managing a reactive form control. |
| `FormArrayDirective` | Directive for managing a reactive form array. |
| `[formGroup]="form"` | Template syntax for binding a form group to a template. |
| `[formControl]="control"` | Template syntax for binding a form control to a template. |
| `[formGroupName]="name"` | Template syntax for binding a nested form group to a template. |
| `[formControlName]="name"` | Template syntax for binding a form control to a template by name. |
| `[formArrayName]="name"` | Template syntax for binding a form array to a template. |
| `[(ngModel)]="property"` | Template syntax for two-way binding with `ngModel`. |
| `#ngForm="ngForm"` | Template reference variable for `NgForm`. |
| `#ngModel="ngModel"` | Template reference variable for `NgModel`. |

---
## Directives

| Code | Description |
|------|-------------|
| `NgIf` | Structural directive that conditionally adds or removes a template based on a boolean expression. |
| `NgForOf` | Structural directive that repeats a template for each item in a collection. |
| `NgSwitch` | Structural directive that conditionally swaps the contents of a template based on a switch expression. |
| `NgSwitchCase` | Directive used within `NgSwitch` to define a case. |
| `NgSwitchDefault` | Directive used within `NgSwitch` to define a default case. |
| `NgClass` | Attribute directive that adds or removes CSS classes based on an expression. |
| `NgStyle` | Attribute directive that sets styles based on an expression. |
| `NgModel` | Directive for managing a template-driven form control. |
| `NgNonBindable` | Attribute directive that prevents Angular from compiling or binding the contents of a template. |
| `NgPlural` | Directive for displaying pluralization rules based on a numeric value. |
| `NgPluralCase` | Directive used within `NgPlural` to define a case. |
| `NgTemplateOutlet` | Directive for embedding a template defined in a `<ng-template>`. |
| `NgComponentOutlet` | Directive for dynamically rendering a component. |
| `NgFor` | Alias for `NgForOf`. |
| `NgIf` | Alias for `NgIf`. |
| `NgSwitch` | Alias for `NgSwitch`. |
| `[ngIf]="condition"` | Template syntax for `NgIf`. |
| `[ngIf]="condition; else elseBlock"` | Template syntax for `NgIf` with an else clause. |
| `<ng-template #elseBlock>...</ng-template>` | Template for the else clause of `NgIf`. |
| `*ngFor="let item of items; index as i; trackBy: trackByFn"` | Template syntax for `NgForOf`. |
| `[ngSwitch]="expression"` | Template syntax for `NgSwitch`. |
| `*ngSwitchCase="value"` | Template syntax for `NgSwitchCase`. |
| `*ngSwitchDefault` | Template syntax for `NgSwitchDefault`. |
| `[ngClass]="{'class1': condition1, 'class2': condition2}"` | Template syntax for `NgClass`. |
| `[ngStyle]="{'property1': value1, 'property2': value2}"` | Template syntax for `NgStyle`. |
| `[ngModel]="property"` | Template syntax for one-way binding with `NgModel`. |
| `[(ngModel)]="property"` | Template syntax for two-way binding with `NgModel`. |
| `[ngNonBindable]` | Template syntax for `NgNonBindable`. |

---
## Pipes

| Code | Description |
|------|-------------|
| `AsyncPipe` | Pipe for automatically subscribing to an Observable or Promise and returning its latest emitted value. |
| `UpperCasePipe` | Transforms text to uppercase. |
| `LowerCasePipe` | Transforms text to lowercase. |
| `TitleCasePipe` | Transforms text to title case. |
| `JsonPipe` | Transforms a value into its JSON string representation. |
| `DatePipe` | Formats a date value according to locale rules. |
| `CurrencyPipe` | Transforms a number into a currency string. |
| `DecimalPipe` | Transforms a number into a decimal string. |
| `PercentPipe` | Transforms a number into a percentage string. |
| `SlicePipe` | Creates a new array or string containing a subset of the elements. |
| `KeyValuePipe` | Transforms an object or map into an array of key-value pairs. |
| `I18nPluralPipe` | Maps a value to a string that pluralizes the value according to locale rules. |
| `I18nSelectPipe` | Maps a value to a string that selects one of the provided strings based on the value. |
| `pipe.transform(value, ...args)` | Method for transforming a value. |
| `{{ value | pipe }}` | Template syntax for using a pipe. |
| `{{ value | pipe1 | pipe2 }}` | Template syntax for chaining pipes. |
| `{{ value | pipe:arg1:arg2 }}` | Template syntax for passing arguments to a pipe. |
| `{{ value | pipe as alias }}` | Template syntax for storing the result of a pipe in a variable. |

---
## Common Built-in Pipes

| Code | Description |
|------|-------------|
| `async` | Automatically subscribes to an Observable or Promise and returns its latest emitted value. |
| `uppercase` | Transforms text to uppercase. |
| `lowercase` | Transforms text to lowercase. |
| `titlecase` | Transforms text to title case. |
| `json` | Transforms a value into its JSON string representation. |
| `date` | Formats a date value according to locale rules. Accepts a format string (e.g., `'short'`, `'fullDate'`, `'longTime'`, `'MM/dd/yyyy'`). |
| `currency` | Transforms a number into a currency string. Accepts a currency code (e.g., `'USD'`, `'EUR'`), a display format (e.g., `'symbol'`, `'code'`, `'symbol-narrow'`), and a digit format (e.g., `'1.2-2'`). |
| `decimal` | Transforms a number into a decimal string. Accepts a digit format (e.g., `'1.2-2'`). |
| `percent` | Transforms a number into a percentage string. Accepts a digit format (e.g., `'1.2-2'`). |
| `slice` | Creates a new array or string containing a subset of the elements. Accepts a start index and an optional end index. |
| `keyvalue` | Transforms an object or map into an array of key-value pairs. |
| `i18nPlural` | Maps a value to a string that pluralizes the value according to locale rules. |
| `i18nSelect` | Maps a value to a string that selects one of the provided strings based on the value. |

---
## Common Modules

| Code | Description |
|------|-------------|
| `BrowserModule` | Module for running Angular applications in a browser. |
| `CommonModule` | Module that provides common directives, pipes, and services (e.g., `NgIf`, `NgForOf`, `AsyncPipe`). |
| `HttpClientModule` | Module that provides the `HttpClient` service and related classes. |
| `RouterModule` | Module for configuring the router. |
| `FormsModule` | Module for template-driven forms. |
| `ReactiveFormsModule` | Module for reactive forms. |
| `PlatformBrowserModule` | Module for running Angular applications in a browser. |
| `PlatformBrowserDynamicModule` | Module for running Angular applications with Just-In-Time (JIT) compilation. |
| `NoopAnimationsModule` | Module for disabling animations. |
| `BrowserAnimationsModule` | Module for enabling animations. |
| `ServiceWorkerModule` | Module for registering a service worker. |
| `AppRoutingModule` | Module for configuring routes in an Angular application. |

---
## Platform and Compiler

| Code | Description |
|------|-------------|
| `platformBrowser()` | Function that returns the browser platform. |
| `platformBrowserDynamic()` | Function that returns the browser platform with Just-In-Time (JIT) compilation. |
| `platformServer()` | Function that returns the server platform. |
| `platformCoreDynamic()` | Function that returns the core platform with JIT compilation. |
| `PLATFORM_ID` | Injection token for the current platform ID. |
| `isPlatformBrowser(platformId)` | Function that checks if the current platform is a browser. |
| `isPlatformServer(platformId)` | Function that checks if the current platform is a server. |
| `Compiler` | Class for compiling Angular components and templates. |
| `CompilerFactory` | Factory for creating compilers. |
| `JitCompiler` | Just-In-Time compiler for Angular applications. |
| `AotCompiler` | Ahead-of-Time compiler for Angular applications. |
| `CompilerOptions` | Options for the Angular compiler. |
| `ComponentFactory` | Factory for creating components. |
| `ComponentRef` | Reference to a dynamically created component. |

---
## Change Detection

| Code | Description |
|------|-------------|
| `ChangeDetectorRef` | Reference to the change detector for a component. |
| `ChangeDetectorRef.detectChanges()` | Triggers change detection for the component and its children. |
| `ChangeDetectorRef.markForCheck()` | Marks the component to be checked in the next change detection cycle. |
| `ChangeDetectorRef.detach()` | Detaches the change detector from the change detection tree. |
| `ChangeDetectorRef.reattach()` | Reattaches the change detector to the change detection tree. |
| `ChangeDetectionStrategy.Default` | Default change detection strategy. Uses the standard Angular change detection mechanism. |
| `ChangeDetectionStrategy.OnPush` | OnPush change detection strategy. Only checks a component when its input properties change or an event originates from the component or one of its children. |
| `DefaultIterableDiffer` | Default iterable differ for tracking changes in iterables. |
| `DefaultKeyValueDiffer` | Default key-value differ for tracking changes in key-value structures. |
| `IterableDiffer` | Interface for tracking changes in iterables. |
| `KeyValueDiffer` | Interface for tracking changes in key-value structures. |
| `Differs` | Service for creating differ objects. |
| `IterableDiffers` | Service for creating iterable differ objects. |
| `KeyValueDiffers` | Service for creating key-value differ objects. |

---
## Zone.js Integration

| Code | Description |
|------|-------------|
| `NgZone` | Angular zone service. |
| `NgZone.isInAngularZone()` | Returns True if the current code is running in the Angular zone. |
| `NgZone.run(fn)` | Runs a function inside the Angular zone. |
| `NgZone.runOutsideAngular(fn)` | Runs a function outside the Angular zone. |
| `NgZone.runTask(fn)` | Runs a task inside the Angular zone. |
| `NgZone.onStable.subscribe(callback)` | Subscribes to notifications when the Angular zone becomes stable. |
| `NgZone.onUnstable.subscribe(callback)` | Subscribes to notifications when the Angular zone becomes unstable. |
| `NgZone.onMicrotaskEmpty.subscribe(callback)` | Subscribes to notifications when the Angular zone has no pending microtasks. |
| `NgZone.onError.subscribe(callback)` | Subscribes to error notifications in the Angular zone. |

---
## RxJS Integration

| Code | Description |
|------|-------------|
| `AsyncPipe` | Pipe for automatically subscribing to an Observable or Promise and returning its latest emitted value. |
| `HttpClient` | Service for making HTTP requests. Returns Observables. |
| `ActivatedRoute.params` | Observable of route parameters. |
| `ActivatedRoute.queryParams` | Observable of query parameters. |
| `FormControl.valueChanges` | Observable of value changes for a form control. |
| `FormGroup.valueChanges` | Observable of value changes for a form group. |
| `Router.events` | Observable of router events. |
| `NavigationStart` | Router event emitted when navigation starts. |
| `NavigationEnd` | Router event emitted when navigation ends successfully. |
| `NavigationCancel` | Router event emitted when navigation is canceled. |
| `NavigationError` | Router event emitted when navigation fails due to an error. |
| `RoutesRecognized` | Router event emitted when routes are recognized. |
| `GuardsCheckStart` | Router event emitted when the guards check starts. |
| `GuardsCheckEnd` | Router event emitted when the guards check ends. |
| `ResolveStart` | Router event emitted when the resolver starts. |
| `ResolveEnd` | Router event emitted when the resolver ends. |
| `ChildActivationStart` | Router event emitted when child activation starts. |
| `ChildActivationEnd` | Router event emitted when child activation ends. |
| `ActivationStart` | Router event emitted when activation starts. |
| `ActivationEnd` | Router event emitted when activation ends. |
| `Scroll` | Router event emitted when the router scrolls. |

---
## Animations

| Code | Description |
|------|-------------|
| `BrowserAnimationsModule` | Module for enabling animations. |
| `NoopAnimationsModule` | Module for disabling animations. |
| `trigger(name, definitions)` | Creates an animation trigger. |
| `state(name, style, options?)` | Defines a state for an animation. |
| `style(style)` | Defines styles for an animation state or transition. |
| `animate(timing, styles?)` | Defines an animation step with timing and optional styles. |
| `transition(stateChangeExpr, steps, options?)` | Defines a transition between states. |
| `keyframes(steps)` | Defines a keyframe animation. |
| `group(steps, options?)` | Groups animation steps to run in parallel. |
| `sequence(steps, options?)` | Sequences animation steps to run one after another. |
| `query(selector, steps, options?)` | Queries elements within the animation. |
| `stagger(timing, steps, options?)` | Staggers animations for multiple elements. |
| `useAnimation(animation, options?)` | Uses a predefined animation. |
| `@angular/animations` | Package containing Angular animations. |
| `AnimationTriggerMetadata` | Metadata for an animation trigger. |
| `AnimationStateMetadata` | Metadata for an animation state. |
| `AnimationStyleMetadata` | Metadata for animation styles. |
| `AnimationAnimateMetadata` | Metadata for an animation step. |
| `AnimationTransitionMetadata` | Metadata for an animation transition. |
| `AnimationKeyframesSequenceMetadata` | Metadata for keyframe animations. |
| `AnimationGroupMetadata` | Metadata for grouped animations. |
| `AnimationSequenceMetadata` | Metadata for sequenced animations. |

---
## Service Worker

| Code | Description |
|------|-------------|
| `ServiceWorkerModule` | Module for registering a service worker. |
| `ServiceWorkerModule.register(script, options?)` | Registers a service worker. |
| `SwRegistration` | Service for interacting with the service worker registration. |
| `SwPush` | Service for managing push notifications. |
| `SwUpdate` | Service for checking for updates to the service worker. |
| `SwUpdate.checkForUpdate()` | Checks for updates to the service worker. |
| `SwUpdate.activateUpdate()` | Activates an update to the service worker. |
| `SwPush.requestSubscription(options)` | Requests a push subscription. |
| `SwPush.unsubscribe()` | Unsubscribes from push notifications. |
| `SwPush.message` | Observable of push messages. |
| `SwPush.subscription` | Observable of the current push subscription. |
| `SwRegistration.update` | Observable of updates to the service worker. |

---
## Internationalization (i18n)

| Code | Description |
|------|-------------|
| `@angular/localize` | Package for localizing Angular applications. |
| `$localize` | Function for localizing strings. |
| `i18n` | Attribute for marking strings for localization. |
| `<span i18n>Hello</span>` | Template syntax for marking a string for localization. |
| `<span i18n="@@uniqueId">Hello</span>` | Template syntax for marking a string with a unique ID for localization. |
| `<span i18n="description">Hello</span>` | Template syntax for marking a string with a description for localization. |
| `<span i18n="meaning|description">Hello</span>` | Template syntax for marking a string with a meaning and description for localization. |
| `ng add @angular/localize` | Angular CLI command for adding localization support. |
| `ng extract-i18n` | Angular CLI command for extracting strings for localization. |
| `ng xi18n` | Angular CLI command for extracting strings for localization (deprecated). |

---
## Testing

| Code | Description |
|------|-------------|
| `TestBed` | Class for configuring and creating an Angular testing module. |
| `TestBed.configureTestingModule(moduleDef)` | Configures a testing module. |
| `TestBed.createComponent(Component)` | Creates a component for testing. |
| `TestBed.inject(token)` | Retrieves a dependency from the testing module. |
| `TestBed.resetTestingModule()` | Resets the testing module. |
| `ComponentFixture<T>` | Wrapper for a component and its environment. Provides methods like `detectChanges()`, `autoDetectChanges()`, `whenStable()`, `destroy()`, and `nativeElement`. |
| `DebugElement` | Wrapper for a DOM element in a testing environment. Provides methods like `query()`, `queryAll()`, `triggerEventHandler()`, and `nativeElement`. |
| `By` | Class for creating predicates to query DOM elements. Provides static methods like `css()`, `directive()`, and `all()`. |
| `By.css(selector)` | Creates a predicate to query DOM elements by CSS selector. |
| `By.directive(Directive)` | Creates a predicate to query DOM elements by directive. |
| `fakeAsync(fn)` | Runs a function in a fake asynchronous zone. |
| `tick(milliseconds?)` | Simulates the passage of time in a fake asynchronous zone. |
| `discardPeriodicTasks()` | Discards all pending periodic tasks (e.g., `setInterval`). |
| `flushMicrotasks()` | Flushes all pending microtasks. |
| `flush()` | Flushes all pending tasks. |
| `HttpClientTestingModule` | Module for testing HTTP requests. |
| `HttpTestingController` | Controller for mocking and flushing HTTP requests. |
| `RouterTestingModule` | Module for testing the router. |
| `RouterTestingHarness` | Harness for testing the router. |
| `LocationTestingHarness` | Harness for testing the location service. |

---
## Angular CLI Commands

| Code | Description |
|------|-------------|
| `ng new name` | Creates a new Angular application. |
| `ng new name --skip-install` | Creates a new Angular application without installing dependencies. |
| `ng new name --style=scss` | Creates a new Angular application with SCSS styles. |
| `ng new name --routing` | Creates a new Angular application with routing enabled. |
| `ng new name --prefix=prefix` | Creates a new Angular application with a custom prefix for component selectors. |
| `ng serve` | Builds and serves the application in development mode. |
| `ng serve --port=4200` | Builds and serves the application on a specific port. |
| `ng serve --host=0.0.0.0` | Builds and serves the application on all network interfaces. |
| `ng serve --open` | Builds and serves the application and opens it in the default browser. |
| `ng build` | Builds the application for production. |
| `ng build --prod` | Builds the application for production with optimizations. |
| `ng build --configuration=production` | Builds the application using the production configuration. |
| `ng build --base-href=/base/` | Builds the application with a custom base href. |
| `ng build --deploy-url=/url/` | Builds the application with a custom deploy URL. |
| `ng test` | Runs unit tests using Karma. |
| `ng test --watch=false` | Runs unit tests without watching for changes. |
| `ng test --code-coverage` | Runs unit tests with code coverage. |
| `ng e2e` | Runs end-to-end tests using Protractor. |
| `ng e2e --protractor-config=file` | Runs end-to-end tests with a custom Protractor configuration file. |
| `ng lint` | Runs linting using TSLint. |
| `ng lint --fix` | Runs linting and fixes linting errors where possible. |
| `ng generate component name` | Generates a new component. |
| `ng generate component name --skip-tests` | Generates a new component without test files. |
| `ng generate component name --inline-template` | Generates a new component with an inline template. |
| `ng generate component name --inline-style` | Generates a new component with inline styles. |
| `ng generate component name --flat` | Generates a new component without its own folder. |
| `ng generate directive name` | Generates a new directive. |
| `ng generate pipe name` | Generates a new pipe. |
| `ng generate service name` | Generates a new service. |
| `ng generate class name` | Generates a new class. |
| `ng generate interface name` | Generates a new interface. |
| `ng generate enum name` | Generates a new enum. |
| `ng generate module name` | Generates a new module. |
| `ng add package` | Adds a package to the project. |
| `ng add @angular/material` | Adds Angular Material to the project. |
| `ng add @angular/pwa` | Adds Progressive Web App (PWA) support to the project. |
| `ng update` | Updates the project dependencies. |
| `ng update --all` | Updates all project dependencies. |
| `ng update @angular/core @angular/cli` | Updates Angular core and CLI. |
| `ng run target` | Runs a custom target defined in the project. |
| `ng run project:target` | Runs a custom target for a specific project. |
| `ng config key value` | Sets a configuration value in `angular.json`. |
| `ng doc keyword` | Opens the official Angular documentation for a keyword. |
| `ng version` | Displays the Angular CLI version. |
| `ng help` | Displays help for Angular CLI commands. |

---
## Angular Compiler Options

| Code | Description |
|------|-------------|
| `angular.json` | Configuration file for Angular CLI. |
| `tsconfig.json` | TypeScript configuration file. |
| `tsconfig.app.json` | TypeScript configuration file for the application. |
| `tsconfig.spec.json` | TypeScript configuration file for tests. |
| `aot` | Enables Ahead-of-Time (AOT) compilation. |
| `buildOptimizer` | Enables build optimizations. |
| `vendorChunk` | Enables vendor chunking. |
| `extractCss` | Extracts CSS from global styles into separate files. |
| `sourceMap` | Enables source map generation. |
| `preserveSymlinks` | Preserves symlinks when resolving modules. |
| `showCircularDependencies` | Shows circular dependency warnings. |
| `subresourceIntegrity` | Enables subresource integrity for scripts and styles. |
| `styles` | Array of global styles files. |
| `scripts` | Array of global script files. |
| `assets` | Array of static assets to include in the build. |

---
## Angular Configuration

| Code | Description |
|------|-------------|
| `angular.json` | Configuration file for Angular CLI. Contains project-specific configurations. |
| `browserslist` | Configuration file for specifying target browsers. |
| `karma.conf.js` | Configuration file for Karma. |
| `protractor.conf.js` | Configuration file for Protractor. |
| `tslint.json` | Configuration file for TSLint. |
| `environment.ts` | Environment-specific configuration file for development. |
| `environment.prod.ts` | Environment-specific configuration file for production. |
| `app.module.ts` | Root module for the Angular application. |
| `main.ts` | Entry point for the Angular application. |
| `polyfills.ts` | File for including polyfills for browser compatibility. |
| `styles.scss` | Global styles file. |
| `index.html` | Main HTML file for the application. |

---
## Angular Utilities

| Code | Description |
|------|-------------|
| `APP_ID` | Injection token for the application ID. |
| `APP_BOOTSTRAP_LISTENER` | Injection token for bootstrap listeners. |
| `APP_INITIALIZER` | Injection token for application initializers. |
| `LOCALE_ID` | Injection token for the locale ID. |
| `DEFAULT_CURRENCY_CODE` | Injection token for the default currency code. |
| `ErrorHandler` | Class for handling errors in Angular applications. |
| `NgProbeToken` | Injection token for Angular debugging tools. |
| `ApplicationInitStatus` | Service for tracking the initialization status of the application. |
| `APP_BASE_HREF` | Injection token for the base href. |
| `DOCUMENT` | Injection token for the document object. |
| `WINDOW` | Injection token for the window object. |
| `HAMMER_GESTURE_CONFIG` | Injection token for HammerJS gesture configuration. |
| `Platform` | Abstract class for platform-specific implementations. |
| `PlatformLocation` | Service for interacting with the browser's URL. |
| `Location` | Service for interacting with the browser's URL. |
| `LocationStrategy` | Abstract class for location strategies. |
| `PathLocationStrategy` | Location strategy that uses the browser's history.pushState. |
| `HashLocationStrategy` | Location strategy that uses the browser's hash fragment. |
| `DomSanitizer` | Service for sanitizing HTML, styles, and URLs. |
| `SafeHtml` | Type for safe HTML. |
| `SafeStyle` | Type for safe styles. |
| `SafeScript` | Type for safe scripts. |
| `SafeUrl` | Type for safe URLs. |
| `SafeResourceUrl` | Type for safe resource URLs. |
| `Meta` | Service for managing meta tags in the document. |
| `Title` | Service for managing the document title. |