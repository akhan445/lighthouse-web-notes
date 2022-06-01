# Event Propagation

Since DOM elements are nested, the events that occur on the inner elements, will spread to it's parent and continue on all it's ancestors. This is known as bubbling.

## **Bubbling**

**Bubbling principle**- When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

```javascript
<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

![bubbling](https://javascript.info/article/bubbling-and-capturing/event-order-bubbling.svg)

When you click <p>, first p alert will appear, then div, then form
- p is the **target element** accessible through `event.target`

To stop propagation use `event.stopPropagation()`
- if element has multiple events then use `event.stopImmediatePropagation()`

```javascript
<body onclick="alert(`the bubbling doesn't reach here`)">
  <button onclick="event.stopPropagation()">Click me</button>
</body>
```

## **Capturing**

Though rarely used, it's important to understand the other side of event processing called capturing.

Bubbling is the end phase of event processing. Capturing is how event processing begins.

DOM Events have 3 phases of propagation:
1. ***Capturing phase***  -  event goes down to target
2. ***Target Phase***     -  event reached the target element
3. ***Bubbling Phase***   -  event bubbles up from element

So you can also capture an event on the "way down" in capturing instead of during bubbling on the "way up"

![event-propagation](https://javascript.info/article/bubbling-and-capturing/eventflow.svg)

```javascript
<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

For above:
- Capturing    = `html` --> `body` --> `form` --> `div`
- Event target = `p`
- Bubbling     = `div` --> `form` --> `body` --> `html`