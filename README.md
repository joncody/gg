# gg.js

`gg.js` is a lightweight, chainable, utility-first JavaScript library for DOM manipulation and interaction. It offers a simplified jQuery-like API with modern enhancements, event handling, and useful utilities baked in.

---

## 📦 Summary

`gg.js` aims to streamline common DOM manipulation tasks such as element selection, insertion, event handling, styling, and traversal. Built with modern JavaScript in mind, it supports chainable methods, automatic event listener tracking, and a minimal dependency surface. The library is ideal for small projects or custom frontend frameworks where full jQuery is unnecessary.

---

## ✨ Features

- Lightweight and modular
- jQuery-like chainable API
- DOM selection and traversal
- Attribute and property manipulation
- Event handling with `.on()`, `.off()`, `.once()`
- Class and style manipulation
- HTML and text content utilities
- Custom data attribute helpers
- Keyboard and mouse event abstraction
- Cloning with deep event listener preservation

---

## 📥 Installation

Include directly in HTML:

```html
<script type="module" src="gg.js"></script>
```

---

## 🚀 Quick Start

```js
import gg from 'gg';

// Create and append a div
gg.create('div')
  .addClass('my-box')
  .text('Hello, gg!')
  .appendTo(document.body);

// Handle events
gg('.my-box').on('click', (e, el) => {
  el.toggleClass('active');
});
```

---

## 📘 API Documentation

### Core Function: `gg(selector[, context])`

Selects DOM nodes.

```js
gg('.my-class');
gg(document.querySelectorAll('div'));
```

---

### Element Creation

- `gg.create(tagName)` — Creates a new DOM element.

---

### Class Manipulation

- `.addClass(name)`
- `.hasClass(name)`
- `.togClass(name)`
- `.remClass(name)`
- `.classes([value])`

---

### Attributes

- `.attr(name)`
- `.attr(name, value)`
- `.attr({ name: value })`
- `.remAttr(name)`

---

### Properties & Styles

- `.prop(name)`
- `.prop(name, value)`
- `.prop({ name: value })`
- `.css(...)`, `.style(...)` — Aliases
- `.remProp(name)`
- `.remCss(name)` / `.remStyle(name)` — Aliases

---

### HTML & Text

- `.html()` / `.html(value)`
- `.text()` / `.text(value)`
- `.remHtml()` / `.remText()`

---

### Data Attributes

- `.data(name)` / `.data(name, value)`
- `.data({ name: value })`
- `.remData(name)`

---

### DOM Manipulation

- `.append(element)`
- `.prepend(element)`
- `.after(element)`
- `.before(element)`
- `.appendTo(parent)`
- `.prependTo(parent)`
- `.remove([child])`
- `.clone(deep, deeper)` — Optional deep clone + event listeners
- `.create(tag)` — Create new child

---

### Traversal

- `.children()` — Get children
- `.parents()` — Get parents
- `.select(selector)` — Query within each node
- `.selectAll(selector)` — Query all within each node
- `.get(index)` — Get a single wrapped element
- `.raw([index])` — Get raw DOM node

---

### Events

- `.on(type, handler[, useCapture, arg])`
- `.off(type[, handler, useCapture])`
- `.once(type, handler[, useCapture, arg])`

Handlers receive: `(event, ggElement, arg)`

---

### Iteration

- `.each(fn)` — Wrapped elements
- `.eachRaw(fn)` — Raw DOM elements

---

### Utility Methods

- `.length()` — Number of elements
- `.subtract(index)` — Remove from internal collection

---

### Device Listeners

- `gg.keyboardListener({ key: fn, ... })`
  - Example keys: `"enter"`, `"left"`, `13`
- `gg.mouseListener({ left: fn, right: fn })`

To remove listeners:

```js
gg.removeKeyboardListeners();
gg.removeMouseListeners();
```

---

## 📚 Utilities

Accessed via `gg.utils`:

- `isString`, `isNumber`, `isBoolean`, `isObject`, `isFunction`, `isUndefined`
- `each`, `inArray`, `toArray`, `extend`, `toCamelCase`, `toHyphenated`
- `select`, `selectAll`

---

## 🧱 Modules Included

- `utils.js`: Core helpers
- `ease.js`: Easing functions
- `emitter.js`: Pub/sub event emitter
- `betterview.js`: Viewport management
- `cdb.js`: In-memory component data store

---

## 📄 License

See the [LICENSE](./LICENSE) file for details.
