You can always get a reference to an element in Solid through assignment since JSX is creates DOM elements like this:

```jsx
const myDiv = <div>My Element</div>
```

However, there is benefit to not breaking your elements out and putting them in a single contiguous JSX template as it allows Solid to better optimize their creation.

Instead you can get a reference to an element in Solid using the `ref` attribute. Ref's are basically assignments like the example above that happen at creation time before they are attached to the DOM. Simply declare a variable and it will be assigned to.

```jsx
let myDiv;

<div ref={myDiv}>My Element</div>
```

Often we do want to interact with refs after they have been attached to the DOM.

> Todo Example

Refs can also take the form of a callback function. This can be convenient for encapsulate logic especially when you don't need to wait until the elements are attached.

```js
<div ref={el => /* do something with el... */}>My Element</div>
```