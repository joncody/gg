# `gg.js` – The "Good Game" Framework

A lightweight, chainable DOM manipulation library and utility suite.

**gg.js** provides a jQuery-like syntax for selecting, traversing, and manipulating DOM elements. It also bundles the entire ecosystem of utilities (`utils`, `emitter`, `betterview`, `cdb`) into a single, cohesive namespace, making it a complete toolkit for modern web applications.

---

## ✅ Features

- 🎯 **DOM Selection:** Robust selection via CSS selectors or raw nodes.
- ⛓️ **Chainable API:** Fluent interface for CSS, attributes, events, and manipulation.
- ⚡ **Event Handling:** Simplified `on`/`off`/`once` with automatic scope binding.
- 🎹 **Device Listeners:** built-in keyboard and mouse input managers.
- 📦 **Ecosystem Bundle:** Includes `utils`, `emitter`, `betterview`, and `cdb` built-in.
- ❄️ **Immutable & Safe:** Returns frozen objects to prevent accidental modification.
- 📦 **Zero dependencies**, modern ES module.

---

## 📦 Installation

Copy `gg.js` (and its dependencies: `utils.js`, `emitter.js`, `betterview.js`, `cdb.js`) into your project.

Import as a module:

```js
import gg from './gg.js';
```

---

## 🧠 Quick Examples

### 1. DOM Manipulation

```js
import gg from "./gg.js";

// Select elements
const box = gg("#box");

// Chain methods
box.addClass("active")
   .css({ color: "red", fontSize: "20px" })
   .text("Hello World!")
   .on("click", () => console.log("Clicked!"));
   
// Create new elements
gg.create("div")
  .addClass("overlay")
  .appendTo(document.body);
```

### 2. Input Handling

```js
// Listen for specific keys
gg.keyboardListener({
    "enter": () => console.log("Form submitted"),
    "esc":   () => console.log("Modal closed"),
    "up":    () => movePlayer("up")
});

// Listen for mouse buttons
gg.mouseListener({
    "left":  (e) => console.log("Primary click at", e.clientX, e.clientY),
    "right": (e) => console.log("Context menu requested")
});
```

---

## 📚 API Reference

### 🟢 Initialization

| Function | Description |
|----------|-------------|
| `gg(selector, [supplanter])` | Selects elements. Accepts CSS string, Node, NodeList, or existing `gg` object. Supports templating via `supplanter`. |
| `gg.create(tagName)` | Creates a new DOM element wrapped in a `gg` object. |

---

### 🎨 CSS & Attributes

| Function | Description |
|----------|-------------|
| `addClass(class)` | Adds one or more classes. |
| `remClass(class)` | Removes one or more classes. |
| `togClass(class)` | Toggles classes. |
| `hasClass(class)` | Returns `true` if element has the class. |
| `css(prop, [val])` | Get or set inline styles. Accepts object for multiple styles. Alias: `style`, `prop`. |
| `attr(name, [val])` | Get or set HTML attributes. |
| `remAttr(name)` | Remove attributes. |
| `data(name, [val])` | Get or set `data-*` attributes (automatically hyphenated). |

---

### 🌲 Manipulation & Traversal

| Function | Description |
|----------|-------------|
| `html([html])` | Get or set inner HTML. |
| `text([text])` | Get or set text content. |
| `append(content)` | Append content to the end of element(s). |
| `prepend(content)` | Prepend content to the start of element(s). |
| `after(content)` | Insert content after the element. |
| `before(content)` | Insert content before the element. |
| `remove()` | Remove element from DOM. |
| `empty()` | Remove all child nodes. Alias: `remHtml`, `remText`. |
| `children()` | Get children as a `gg` object. |
| `parents()` | Get parent nodes as a `gg` object. |
| `select(selector)` | Find descendant elements (querySelector). |
| `selectAll(selector)` | Find descendant elements (querySelectorAll). |

---

### ⚡ Events

| Function | Description |
|----------|-------------|
| `on(type, fn, [capture], [arg])` | Add event listener. |
| `off(type, [fn], [capture])` | Remove event listener. If `fn` omitted, removes all listeners of that type. |
| `once(type, fn, [capture], [arg])` | Add one-time listener. |

---

### 🎹 Global Input Listeners

These are static methods on the `gg` object.

| Function | Description |
|----------|-------------|
| `gg.keyboardListener(map)` | Registers global keydown handlers. Map keys: `"enter"`, `"left"`, `"up"`, `"right"`, `"down"`, or keycodes. |
| `gg.mouseListener(map)` | Registers global mousedown handlers. Map keys: `"left"`, `"middle"`, `"right"`. |
| `gg.removeKeyboardListeners()` | Removes all registered global keyboard listeners. |
| `gg.removeMouseListeners()` | Removes all registered global mouse listeners. |

---

## 🧰 Bundled Ecosystem

`gg.js` exports your entire library suite as static properties:

*   **`gg.utils`**: The utility library (type checking, object copying, etc).
*   **`gg.emitter`**: The event emitter factory.
*   **`gg.betterview`**: The advanced DataView wrapper.
*   **`gg.cdb`**: The IndexedDB wrapper.

```js
// Access utils directly through gg
if (gg.utils.isString("test")) { ... }

// Use the database
gg.cdb.open("MyDatabase");
```

---

## 📄 License

See the [LICENSE](./LICENSE) file for details.
