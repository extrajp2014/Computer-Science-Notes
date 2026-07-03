## Core React APIs

| Code | Description |
|------|-------------|
| `React` | The entry point to the React library. All React APIs are accessible through this object. |
| `React.version` | String indicating the current React version. |
| `React.createElement(type, [props], [...children])` | Creates and returns a new React element. Used internally by JSX. |
| `React.cloneElement(element, [props], [...children])` | Clones and returns a new React element using the original element as a template. |
| `React.createFactory(type)` | Creates a function that returns a React element of the specified type. |
| `React.isValidElement(object)` | Verifies if the object is a valid React element. |
| `React.createContext(defaultValue)` | Creates a Context object. Used with the Context API for sharing values across component trees. |
| `React.createRef()` | Creates a ref object that can be attached to React elements. |
| `React.forwardRef(renderFunction)` | Creates a React component that forwards the ref attribute to a child component. |
| `React.lazy(importFunction)` | Allows rendering a dynamic import as a regular component. Used for code-splitting. |
| `React.memo(Component, [arePropsEqual])` | Higher-order component that memoizes a functional component to prevent unnecessary re-renders. |
| `React.startTransition(scope)` | Marks state updates inside the provided callback as transitions. |
| `React.useTransition()` | Returns a stateful pair consisting of an isPending flag and a startTransition function. |
| `React.useDeferredValue(value)` | Accepts a value and returns a deferred version of it that may lag behind it. |
| `React.useId()` | Generates unique IDs that are stable across server and client, and consistent between multiple renders of the same component. |
| `React.useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?)` | Subscribes to an external store and returns the current snapshot of the store data. |
| `React.useInsertionEffect(callback, [dependencies])` | Similar to useEffect, but fires before all DOM mutations. Used by CSS-in-JS libraries. |
| `React.Fragment` | Component for grouping a list of children without adding extra nodes to the DOM. |
| `React.Profiler` | Component for measuring rendering performance of a React application. |
| `React.StrictMode` | Component for highlighting potential problems in an application. |
| `React.Suspense` | Component for displaying fallback content while waiting for lazy-loaded components or data to load. |

---

## ReactDOM APIs

| Code | Description |
|------|-------------|
| `ReactDOM` | The entry point to the ReactDOM library. Provides DOM-specific methods. |
| `ReactDOM.createRoot(container, [options])` | Creates a root for a React application to render into the specified DOM container. Returns a root object. |
| `root.render(element)` | Renders a React element into the root. |
| `root.unmount()` | Unmounts a React application from the root. |
| `ReactDOM.hydrateRoot(container, element, [options])` | Hydrates a container whose HTML was rendered by ReactDOMServer.renderToString() or renderToStaticMarkup(). Returns a root object. |
| `ReactDOM.unmountComponentAtNode(container)` | Removes a mounted React component from the DOM and cleans up its event handlers and state. |
| `ReactDOM.findDOMNode(componentOrElement)` | Returns the corresponding DOM node for a React component or element. Deprecated in React 18. |
| `ReactDOM.createPortal(children, domContainer, [key])` | Creates a portal. Portals provide a way to render children into a DOM node that exists outside the DOM hierarchy of the parent component. |

---
## ReactDOMServer APIs

| Code | Description |
|------|-------------|
| `ReactDOMServer` | The entry point to the ReactDOMServer library. Provides server-side rendering methods. |
| `ReactDOMServer.renderToString(element)` | Renders a React element to its initial HTML. Returns a string. |
| `ReactDOMServer.renderToStaticMarkup(element)` | Similar to renderToString, but does not create extra DOM attributes such as data-reactroot. Returns a string. |
| `ReactDOMServer.renderToNodeStream(element)` | Renders a React element to its initial HTML. Returns a Node.js readable stream. |
| `ReactDOMServer.renderToStaticNodeStream(element)` | Similar to renderToNodeStream, but does not create extra DOM attributes. Returns a Node.js readable stream. |
| `ReactDOMServer.renderToWebStream(element)` | Renders a React element to its initial HTML. Returns a Web ReadableStream. |
| `ReactDOMServer.renderToStaticWebStream(element)` | Similar to renderToWebStream, but does not create extra DOM attributes. Returns a Web ReadableStream. |
| `ReactDOMServer.renderToPipeableStream(element, options?)` | Renders a React element to its initial HTML. Returns a PipeableStream that can be piped to a Node.js response. |
| `ReactDOMServer.renderToReadableStream(element, options?)` | Renders a React element to its initial HTML. Returns a ReadableStream. |

---
## Hooks

| Code | Description |
|------|-------------|
| `useState(initialState)` | Returns a stateful value and a function to update it. Used for adding state to functional components. |
| `useEffect(effect, [dependencies])` | Accepts a function that contains imperative code, and runs it after rendering. Used for side effects in functional components. |
| `useLayoutEffect(effect, [dependencies])` | Similar to useEffect, but fires synchronously after all DOM mutations. Use this to read layout from the DOM and synchronously re-render. |
| `useContext(Context)` | Accepts a context object (the value returned from React.createContext) and returns the current context value. |
| `useReducer(reducer, initialArg, init?)` | Alternative to useState. Accepts a reducer function and an initial state, and returns the current state paired with a dispatch method. |
| `useCallback(callback, [dependencies])` | Returns a memoized callback function. Used to prevent unnecessary re-renders. |
| `useMemo(factory, [dependencies])` | Returns a memoized value. Used to optimize expensive calculations. |
| `useRef(initialValue)` | Returns a mutable ref object whose .current property is initialized to the passed argument. |
| `useImperativeHandle(ref, factory, [deps])` | Customizes the instance value that is exposed when using ref with useRef. |
| `useDebugValue(value, formatFn?)` | Displays a label for custom hooks in React DevTools. |
| `useId()` | Generates unique IDs that are stable across server and client, and consistent between multiple renders of the same component. |
| `useTransition()` | Returns a stateful pair consisting of an isPending flag and a startTransition function. Used for marking updates as transitions. |
| `useDeferredValue(value)` | Accepts a value and returns a deferred version of it that may lag behind it. Used for deferring updates. |
| `useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?)` | Subscribes to an external store and returns the current snapshot of the store data. Used for integrating with external stores. |
| `useInsertionEffect(callback, [dependencies])` | Similar to useEffect, but fires before all DOM mutations. Used by CSS-in-JS libraries. |

---
## Component APIs

| Code | Description |
|------|-------------|
| `class Component extends React.Component` | Base class for defining React components using ES6 classes. |
| `class PureComponent extends React.PureComponent` | Similar to Component, but skips re-renders for same props and state. |
| `component.render()` | Required lifecycle method that returns a React element. |
| `component.constructor(props)` | Constructor for a React component. Used for initializing state and binding methods. |
| `component.state` | Object containing the component's state. Should not be modified directly. |
| `component.setState(updater, [callback])` | Enqueues changes to the component state and triggers a re-render. Can accept an object or a function. |
| `component.forceUpdate([callback])` | Forces a re-render of the component. |
| `component.props` | Object containing the component's props. Read-only. |
| `component.context` | The current context. Available only when the component specifies contextTypes. |
| `component.refs` | Object containing refs to child components or DOM elements. Deprecated in favor of createRef and useRef. |
| `component.defaultProps` | Static property for defining default props. |
| `component.displayName` | Static property for defining the display name of the component. |

---
## Lifecycle Methods

| Code | Description |
|------|-------------|
| `static getDerivedStateFromProps(nextProps, prevState)` | Static method called immediately after a component is instantiated or when it receives new props. Must return an object to update state or null to update nothing. |
| `componentDidMount()` | Called immediately after a component is mounted. Used for initialization that requires DOM nodes. |
| `shouldComponentUpdate(nextProps, nextState)` | Called before rendering when new props or state are received. Returns a boolean to determine whether to re-render. |
| `componentDidUpdate(prevProps, prevState, snapshot?)` | Called immediately after updating occurs. Used for performing DOM operations after updates. |
| `getSnapshotBeforeUpdate(prevProps, prevState)` | Called right before the most recently rendered output is committed. Returns a snapshot value or null. |
| `componentWillUnmount()` | Called immediately before a component is unmounted. Used for cleanup. |
| `componentDidCatch(error, info)` | Called when an error is thrown by a child component. Used for error boundaries. |
| `static getDerivedStateFromError(error)` | Static method called when an error is thrown by a child component during rendering. Used for error boundaries. |

---
## Legacy Lifecycle Methods

| Code | Description |
|------|-------------|
| `componentWillMount()` | Called immediately before a component is mounted. Deprecated. Use componentDidMount or constructor instead. |
| `componentWillReceiveProps(nextProps)` | Called when a component is receiving new props. Deprecated. Use static getDerivedStateFromProps or componentDidUpdate instead. |
| `componentWillUpdate(nextProps, nextState)` | Called immediately before rendering when new props or state are received. Deprecated. Use getSnapshotBeforeUpdate or componentDidUpdate instead. |

---
## Context API

| Code | Description |
|------|-------------|
| `React.createContext(defaultValue)` | Creates a Context object. Used for sharing values across component trees without explicitly passing props. |
| `Context.Provider` | Component that provides a context value to its children. Accepts a value prop. |
| `Context.Consumer` | Component that consumes a context value. Accepts a children prop as a function. |
| `useContext(Context)` | Hook that accepts a context object and returns the current context value. |
| `Context.displayName` | String used to display the context in React DevTools. |
| `Context.defaultValue` | Default value for the context. Used when no matching Provider is found. |
| `<Context.Provider value={value}>...</Context.Provider>` | JSX syntax for providing a context value. |
| `<Context.Consumer>{value => ...}</Context.Consumer>` | JSX syntax for consuming a context value. |

---
## Refs

| Code | Description |
|------|-------------|
| `React.createRef()` | Creates a ref object that can be attached to React elements. |
| `useRef(initialValue)` | Hook that returns a mutable ref object whose .current property is initialized to the passed argument. |
| `React.forwardRef(renderFunction)` | Creates a React component that forwards the ref attribute to a child component. |
| `useImperativeHandle(ref, factory, [deps])` | Customizes the instance value that is exposed when using ref with useRef. |
| `ref.current` | Property of a ref object that holds the current ref value. |
| `<div ref={ref} />` | JSX syntax for attaching a ref to a DOM element. |
| `<MyComponent ref={ref} />` | JSX syntax for attaching a ref to a class component. |
| `callbackRef` | Pattern for using a function as a ref. The function receives the DOM element or component instance as an argument. |

---
## Fragments

| Code | Description |
|------|-------------|
| `React.Fragment` | Component for grouping a list of children without adding extra nodes to the DOM. |
| `<React.Fragment>...</React.Fragment>` | JSX syntax for using a Fragment. |
| `<>...</>` | Shorthand JSX syntax for using a Fragment. |
| `<Fragment>...</Fragment>` | Alternative JSX syntax for using a Fragment (requires import). |

---
## Portals

| Code | Description |
|------|-------------|
| `ReactDOM.createPortal(children, domContainer, [key])` | Creates a portal. Portals provide a way to render children into a DOM node that exists outside the DOM hierarchy of the parent component. |
| `<Portal>{children}</Portal>` | JSX syntax for using a portal (requires custom implementation). |

---
## Error Boundaries

| Code | Description |
|------|-------------|
| `componentDidCatch(error, info)` | Lifecycle method called when an error is thrown by a child component. Used for error boundaries. |
| `static getDerivedStateFromError(error)` | Static method called when an error is thrown by a child component during rendering. Used for error boundaries. |
| `class ErrorBoundary extends React.Component` | Base class for defining error boundary components. |
| `<ErrorBoundary>{children}</ErrorBoundary>` | JSX syntax for using an error boundary component. |

---
## Suspense and Lazy Loading

| Code | Description |
|------|-------------|
| `React.Suspense` | Component for displaying fallback content while waiting for lazy-loaded components or data to load. |
| `React.lazy(importFunction)` | Allows rendering a dynamic import as a regular component. Used for code-splitting. |
| `<Suspense fallback={fallback}>...</Suspense>` | JSX syntax for using Suspense. |
| `lazy(() => import('./MyComponent'))` | Syntax for lazy-loading a component. |

---
## Concurrent Features

| Code | Description |
|------|-------------|
| `React.startTransition(scope)` | Marks state updates inside the provided callback as transitions. |
| `useTransition()` | Returns a stateful pair consisting of an isPending flag and a startTransition function. |
| `useDeferredValue(value)` | Accepts a value and returns a deferred version of it that may lag behind it. |
| `useId()` | Generates unique IDs that are stable across server and client, and consistent between multiple renders of the same component. |
| `useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?)` | Subscribes to an external store and returns the current snapshot of the store data. |
| `useInsertionEffect(callback, [dependencies])` | Similar to useEffect, but fires before all DOM mutations. Used by CSS-in-JS libraries. |

---
## Synthetic Events

| Code | Description |
|------|-------------|
| `SyntheticEvent` | Base class for all React synthetic events. Provides methods like `preventDefault()`, `stopPropagation()`, `persist()`, and properties like `target`, `currentTarget`, `eventPhase`, `bubbles`, `cancelable`, `timeStamp`, `defaultPrevented`, `isTrusted`, `nativeEvent`, and `type`. |
| `ClipboardEvent` | Synthetic event for clipboard operations. |
| `CompositionEvent` | Synthetic event for composition events. |
| `KeyboardEvent` | Synthetic event for keyboard events. Provides properties like `key`, `code`, `location`, `ctrlKey`, `shiftKey`, `altKey`, `metaKey`, `repeat`, `charCode`, `keyCode`, `which`, and `getModifierState()`. |
| `FocusEvent` | Synthetic event for focus events. |
| `FormEvent` | Synthetic event for form events. |
| `MouseEvent` | Synthetic event for mouse events. Provides properties like `screenX`, `screenY`, `clientX`, `clientY`, `pageX`, `pageY`, `ctrlKey`, `shiftKey`, `altKey`, `metaKey`, `button`, `buttons`, `relatedTarget`, and `getModifierState()`. |
| `PointerEvent` | Synthetic event for pointer events. |
| `SelectionEvent` | Synthetic event for selection events. |
| `TouchEvent` | Synthetic event for touch events. Provides properties like `touches`, `targetTouches`, `changedTouches`, `altKey`, `metaKey`, `ctrlKey`, `shiftKey`, and `getModifierState()`. |
| `UIEvent` | Synthetic event for UI events. |
| `WheelEvent` | Synthetic event for wheel events. Provides properties like `deltaX`, `deltaY`, `deltaZ`, `deltaMode`. |
| `AnimationEvent` | Synthetic event for animation events. |
| `TransitionEvent` | Synthetic event for transition events. |
| `onClick` | Event handler for click events. |
| `onChange` | Event handler for change events. |
| `onSubmit` | Event handler for form submission events. |
| `onFocus` | Event handler for focus events. |
| `onBlur` | Event handler for blur events. |
| `onKeyDown` | Event handler for keydown events. |
| `onKeyPress` | Event handler for keypress events. |
| `onKeyUp` | Event handler for keyup events. |
| `onMouseDown` | Event handler for mousedown events. |
| `onMouseUp` | Event handler for mouseup events. |
| `onMouseMove` | Event handler for mousemove events. |
| `onMouseEnter` | Event handler for mouseenter events. |
| `onMouseLeave` | Event handler for mouseleave events. |
| `onMouseOver` | Event handler for mouseover events. |
| `onTouchStart` | Event handler for touchstart events. |
| `onTouchMove` | Event handler for touchmove events. |
| `onTouchEnd` | Event handler for touchend events. |
| `onScroll` | Event handler for scroll events. |
| `onCopy` | Event handler for copy events. |
| `onCut` | Event handler for cut events. |
| `onPaste` | Event handler for paste events. |

---
## DOM Events

| Code | Description |
|------|-------------|
| `onCopy` | Event handler for copy events. |
| `onCut` | Event handler for cut events. |
| `onPaste` | Event handler for paste events. |
| `onCompositionEnd` | Event handler for compositionend events. |
| `onCompositionStart` | Event handler for compositionstart events. |
| `onCompositionUpdate` | Event handler for compositionupdate events. |
| `onFocus` | Event handler for focus events. |
| `onBlur` | Event handler for blur events. |
| `onChange` | Event handler for change events. |
| `onInput` | Event handler for input events. |
| `onInvalid` | Event handler for invalid events. |
| `onReset` | Event handler for reset events. |
| `onSubmit` | Event handler for submit events. |
| `onKeyDown` | Event handler for keydown events. |
| `onKeyPress` | Event handler for keypress events. |
| `onKeyUp` | Event handler for keyup events. |
| `onAbort` | Event handler for abort events. |
| `onCanPlay` | Event handler for canplay events. |
| `onCanPlayThrough` | Event handler for canplaythrough events. |
| `onDurationChange` | Event handler for durationchange events. |
| `onEmptied` | Event handler for emptied events. |
| `onEncrypted` | Event handler for encrypted events. |
| `onEnded` | Event handler for ended events. |
| `onError` | Event handler for error events. |
| `onLoadedData` | Event handler for loadeddata events. |
| `onLoadedMetadata` | Event handler for loadedmetadata events. |
| `onLoadStart` | Event handler for loadstart events. |
| `onPause` | Event handler for pause events. |
| `onPlay` | Event handler for play events. |
| `onPlaying` | Event handler for playing events. |
| `onProgress` | Event handler for progress events. |
| `onRateChange` | Event handler for ratechange events. |
| `onSeeked` | Event handler for seeked events. |
| `onSeeking` | Event handler for seeking events. |
| `onStalled` | Event handler for stalled events. |
| `onSuspend` | Event handler for suspend events. |
| `onTimeUpdate` | Event handler for timeupdate events. |
| `onVolumeChange` | Event handler for volumechange events. |
| `onWaiting` | Event handler for waiting events. |
| `onAuxClick` | Event handler for auxclick events. |
| `onClick` | Event handler for click events. |
| `onContextMenu` | Event handler for contextmenu events. |
| `onDoubleClick` | Event handler for double-click events. |
| `onDrag` | Event handler for drag events. |
| `onDragEnd` | Event handler for dragend events. |
| `onDragEnter` | Event handler for dragenter events. |
| `onDragExit` | Event handler for dragexit events. |
| `onDragLeave` | Event handler for dragleave events. |
| `onDragOver` | Event handler for dragover events. |
| `onDragStart` | Event handler for dragstart events. |
| `onDrop` | Event handler for drop events. |
| `onMouseDown` | Event handler for mousedown events. |
| `onMouseEnter` | Event handler for mouseenter events. |
| `onMouseLeave` | Event handler for mouseleave events. |
| `onMouseMove` | Event handler for mousemove events. |
| `onMouseOut` | Event handler for mouseout events. |
| `onMouseOver` | Event handler for mouseover events. |
| `onMouseUp` | Event handler for mouseup events. |
| `onPointerCancel` | Event handler for pointercancel events. |
| `onPointerDown` | Event handler for pointerdown events. |
| `onPointerEnter` | Event handler for pointerenter events. |
| `onPointerLeave` | Event handler for pointerleave events. |
| `onPointerMove` | Event handler for pointermove events. |
| `onPointerOut` | Event handler for pointerout events. |
| `onPointerOver` | Event handler for pointerover events. |
| `onPointerUp` | Event handler for pointerup events. |
| `onScroll` | Event handler for scroll events. |
| `onSelectionChange` | Event handler for selectionchange events. |
| `onTouchCancel` | Event handler for touchcancel events. |
| `onTouchEnd` | Event handler for touchend events. |
| `onTouchMove` | Event handler for touchmove events. |
| `onTouchStart` | Event handler for touchstart events. |
| `onWheel` | Event handler for wheel events. |

---
## React Children APIs

| Code | Description |
|------|-------------|
| `React.Children.map(children, fn, [thisArg])` | Invokes a function on each immediate child in children. |
| `React.Children.forEach(children, fn, [thisArg])` | Invokes a function on each immediate child in children. Similar to map, but does not return an array. |
| `React.Children.count(children)` | Returns the total number of children in children. |
| `React.Children.only(children)` | Returns the only child in children. Throws an error if there is more than one child. |
| `React.Children.toArray(children)` | Returns the children as an array. |

---
## PropTypes

| Code | Description |
|------|-------------|
| `PropTypes` | Object containing validators for React props. |
| `PropTypes.array` | Validator for array props. |
| `PropTypes.bool` | Validator for boolean props. |
| `PropTypes.func` | Validator for function props. |
| `PropTypes.number` | Validator for number props. |
| `PropTypes.object` | Validator for object props. |
| `PropTypes.string` | Validator for string props. |
| `PropTypes.symbol` | Validator for symbol props. |
| `PropTypes.element` | Validator for React element props. |
| `PropTypes.node` | Validator for any renderable props (numbers, strings, elements, or arrays). |
| `PropTypes.elementType` | Validator for React element type props (e.g., a component class). |
| `PropTypes.instanceOf(ExpectedClass)` | Validator for props that are instances of a specific class. |
| `PropTypes.oneOf([...values])` | Validator for props that are one of the specified values. |
| `PropTypes.oneOfType([...types])` | Validator for props that are one of the specified types. |
| `PropTypes.arrayOf(type)` | Validator for props that are arrays of a specific type. |
| `PropTypes.objectOf(type)` | Validator for props that are objects with values of a specific type. |
| `PropTypes.shape({...})` | Validator for props that are objects with a specific shape. |
| `PropTypes.exact({...})` | Validator for props that are objects with an exact shape. |
| `PropTypes.isRequired` | Chains with any validator to require the prop. |
| `MyComponent.propTypes = {...}` | Static property for defining prop types for a component. |
| `MyComponent.defaultProps = {...}` | Static property for defining default props for a component. |

---
## Test Utilities

| Code | Description |
|------|-------------|
| `ReactDOMTestUtils` | Utilities for testing React components. Deprecated in favor of React Testing Library. |
| `act(callback)` | Function from react-dom/test-utils that prepares a component for assertions. Used with React Testing Library. |
| `render(element, [options])` | Renders a React element into the DOM for testing. Provided by React Testing Library. |
| `renderHook(callback, [options])` | Renders a React hook for testing. Provided by React Testing Library. |
| `fireEvent(node, eventName, [eventProperties])` | Fires a DOM event for testing. Provided by React Testing Library. |
| `userEvent` | Simulates user interactions for testing. Provided by React Testing Library. |
| `screen` | Queries for elements in the DOM for testing. Provided by React Testing Library. |
| `waitFor(callback, [options])` | Waits for a callback to resolve for testing asynchronous behavior. Provided by React Testing Library. |
| `within(element)` | Scopes queries to a specific element for testing. Provided by React Testing Library. |
| `Simulate.event(element, [eventData])` | Simulates an event on a DOM node. Provided by ReactDOMTestUtils. Deprecated. |
| `findAllInRenderedTree(tree, test)` | Finds all nodes in a tree that match a test. Provided by ReactDOMTestUtils. Deprecated. |
| `findRenderedDOMComponentWithClass(tree, className)` | Finds a DOM component with a specific class. Provided by ReactDOMTestUtils. Deprecated. |
| `findRenderedDOMComponentWithTag(tree, tagName)` | Finds a DOM component with a specific tag. Provided by ReactDOMTestUtils. Deprecated. |
| `isCompositeComponent(tree)` | Checks if a tree is a composite component. Provided by ReactDOMTestUtils. Deprecated. |
| `isCompositeComponentWithType(tree, type)` | Checks if a tree is a composite component of a specific type. Provided by ReactDOMTestUtils. Deprecated. |
| `isDOMComponent(tree)` | Checks if a tree is a DOM component. Provided by ReactDOMTestUtils. Deprecated. |
| `isElement(element)` | Checks if an object is a React element. Provided by ReactDOMTestUtils. Deprecated. |
| `isElementOfType(element, type)` | Checks if an element is of a specific type. Provided by ReactDOMTestUtils. Deprecated. |
| `scryRenderedComponentsWithType(tree, type)` | Finds all components of a specific type in a tree. Provided by ReactDOMTestUtils. Deprecated. |

---
## JSX Syntax

| Code | Description |
|------|-------------|
| `<div />` | JSX syntax for a self-closing element. |
| `<div></div>` | JSX syntax for an element with children. |
| `<div className="my-class" />` | JSX syntax for an element with a class attribute. |
| `<div style={{ color: 'red' }} />` | JSX syntax for an element with inline styles. |
| `<div onClick={handleClick} />` | JSX syntax for an element with an event handler. |
| `<MyComponent />` | JSX syntax for a custom component. |
| `<MyComponent prop={value} />` | JSX syntax for a custom component with props. |
| `<MyComponent prop="value" />` | JSX syntax for a custom component with a string prop. |
| `<MyComponent {...props} />` | JSX syntax for spreading props onto a component. |
| `{expression}` | JSX syntax for embedding a JavaScript expression. |
| `{condition && <div />}` | JSX syntax for conditional rendering using logical AND. |
| `{condition ? <div /> : <span />}` | JSX syntax for conditional rendering using ternary operator. |
| `{items.map(item => <div key={item.id} />)}` | JSX syntax for rendering a list of items. |
| `<>...</>` | JSX syntax for a Fragment (shorthand). |
| `<React.Fragment>...</React.Fragment>` | JSX syntax for a Fragment (explicit). |

---
## DOM Attributes

| Code | Description |
|------|-------------|
| `className` | JSX attribute for specifying CSS classes. Replaces the HTML `class` attribute. |
| `htmlFor` | JSX attribute for specifying the `for` attribute of a label. Replaces the HTML `for` attribute. |
| `onChange` | JSX attribute for specifying the change event handler. |
| `value` | JSX attribute for specifying the value of an input, select, or textarea. |
| `checked` | JSX attribute for specifying the checked state of a checkbox or radio button. |
| `selected` | JSX attribute for specifying the selected state of an option. |
| `disabled` | JSX attribute for specifying whether an element is disabled. |
| `readOnly` | JSX attribute for specifying whether an element is read-only. |
| `placeholder` | JSX attribute for specifying placeholder text for an input. |
| `autoFocus` | JSX attribute for specifying whether an element should be auto-focused. |
| `tabIndex` | JSX attribute for specifying the tab index of an element. |
| `title` | JSX attribute for specifying the title (tooltip) of an element. |
| `lang` | JSX attribute for specifying the language of an element. |
| `dir` | JSX attribute for specifying the text direction of an element. |
| `hidden` | JSX attribute for specifying whether an element is hidden. |
| `spellCheck` | JSX attribute for specifying whether spell checking is enabled for an element. |
| `autoComplete` | JSX attribute for specifying whether autocomplete is enabled for an input. |
| `autoCapitalize` | JSX attribute for specifying the autocapitalization behavior for an input. |
| `autoCorrect` | JSX attribute for specifying whether autocorrection is enabled for an input. |
| `multiple` | JSX attribute for specifying whether multiple selections are allowed for a select. |
| `size` | JSX attribute for specifying the size of an input or select. |
| `maxLength` | JSX attribute for specifying the maximum length of an input. |
| `minLength` | JSX attribute for specifying the minimum length of an input. |
| `max` | JSX attribute for specifying the maximum value of an input. |
| `min` | JSX attribute for specifying the minimum value of an input. |
| `step` | JSX attribute for specifying the step value of an input. |
| `pattern` | JSX attribute for specifying the pattern of an input. |
| `required` | JSX attribute for specifying whether an input is required. |
| `accept` | JSX attribute for specifying the accepted file types for an input. |
| `capture` | JSX attribute for specifying whether event handlers should capture events. |
| `dangerouslySetInnerHTML` | JSX attribute for setting inner HTML directly. Accepts an object with an `__html` key. |
| `suppressContentEditableWarning` | JSX attribute for suppressing content editable warnings. |
| `suppressHydrationWarning` | JSX attribute for suppressing hydration warnings. |

---
## Style Attributes

| Code | Description |
|------|-------------|
| `style` | JSX attribute for specifying inline styles. Accepts an object with camelCased CSS property names. |
| `style={{ color: 'red' }}` | JSX syntax for specifying a single style property. |
| `style={{ color: 'red', backgroundColor: 'blue' }}` | JSX syntax for specifying multiple style properties. |
| `style={{ marginTop: '10px' }}` | JSX syntax for specifying a style property with a vendor prefix. |
| `style={{ WebkitTransition: 'all 0.3s' }}` | JSX syntax for specifying a style property with a vendor prefix. |

---
## Event Handlers

| Code | Description |
|------|-------------|
| `onCopy` | Event handler for copy events. |
| `onCut` | Event handler for cut events. |
| `onPaste` | Event handler for paste events. |
| `onCompositionEnd` | Event handler for compositionend events. |
| `onCompositionStart` | Event handler for compositionstart events. |
| `onCompositionUpdate` | Event handler for compositionupdate events. |
| `onFocus` | Event handler for focus events. |
| `onBlur` | Event handler for blur events. |
| `onChange` | Event handler for change events. |
| `onInput` | Event handler for input events. |
| `onInvalid` | Event handler for invalid events. |
| `onReset` | Event handler for reset events. |
| `onSubmit` | Event handler for submit events. |
| `onKeyDown` | Event handler for keydown events. |
| `onKeyPress` | Event handler for keypress events. |
| `onKeyUp` | Event handler for keyup events. |
| `onAbort` | Event handler for abort events. |
| `onCanPlay` | Event handler for canplay events. |
| `onCanPlayThrough` | Event handler for canplaythrough events. |
| `onDurationChange` | Event handler for durationchange events. |
| `onEmptied` | Event handler for emptied events. |
| `onEncrypted` | Event handler for encrypted events. |
| `onEnded` | Event handler for ended events. |
| `onError` | Event handler for error events. |
| `onLoadedData` | Event handler for loadeddata events. |
| `onLoadedMetadata` | Event handler for loadedmetadata events. |
| `onLoadStart` | Event handler for loadstart events. |
| `onPause` | Event handler for pause events. |
| `onPlay` | Event handler for play events. |
| `onPlaying` | Event handler for playing events. |
| `onProgress` | Event handler for progress events. |
| `onRateChange` | Event handler for ratechange events. |
| `onSeeked` | Event handler for seeked events. |
| `onSeeking` | Event handler for seeking events. |
| `onStalled` | Event handler for stalled events. |
| `onSuspend` | Event handler for suspend events. |
| `onTimeUpdate` | Event handler for timeupdate events. |
| `onVolumeChange` | Event handler for volumechange events. |
| `onWaiting` | Event handler for waiting events. |

---
## Server-Side Rendering

| Code | Description |
|------|-------------|
| `ReactDOMServer.renderToString(element)` | Renders a React element to its initial HTML. Returns a string. |
| `ReactDOMServer.renderToStaticMarkup(element)` | Similar to renderToString, but does not create extra DOM attributes such as data-reactroot. Returns a string. |
| `ReactDOMServer.renderToNodeStream(element)` | Renders a React element to its initial HTML. Returns a Node.js readable stream. |
| `ReactDOMServer.renderToStaticNodeStream(element)` | Similar to renderToNodeStream, but does not create extra DOM attributes. Returns a Node.js readable stream. |
| `ReactDOMServer.renderToWebStream(element)` | Renders a React element to its initial HTML. Returns a Web ReadableStream. |
| `ReactDOMServer.renderToStaticWebStream(element)` | Similar to renderToWebStream, but does not create extra DOM attributes. Returns a Web ReadableStream. |
| `ReactDOMServer.renderToPipeableStream(element, options?)` | Renders a React element to its initial HTML. Returns a PipeableStream that can be piped to a Node.js response. |
| `ReactDOMServer.renderToReadableStream(element, options?)` | Renders a React element to its initial HTML. Returns a ReadableStream. |

---
## Experimental APIs

| Code | Description |
|------|-------------|
| `React.cache(fn)` | Caches the result of a function. Used for memoizing module-level functions. |
| `React.use` | Allows reading a value from a promise or context during render. |
| `React.useOptimistic` | Allows displaying optimistic updates while an async action is in progress. |
| `React.useFormStatus` | Returns the status of the nearest form ancestor. |
| `React.useFormState(action, initialState)` | Manages a form state and handles form submission. |
| `React.taint` | Marks a value as tainted, preventing it from being used in certain contexts. |
| `React.experimental_taint` | Experimental API for marking values as tainted. |
| `React.unstable_postpone` | Experimental API for postponing a render. |
| `React.unstable_scheduleCallback` | Experimental API for scheduling a callback. |
| `React.unstable_runWithPriority` | Experimental API for running a function with a specific priority. |
| `React.unstable_next` | Experimental API for yielding execution. |
| `React.unstable_flushAll` | Experimental API for flushing all pending work. |
| `React.unstable_flushDiscreteUpdates` | Experimental API for flushing discrete updates. |