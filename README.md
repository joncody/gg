gg
==

A JavaScript and DOM utility library.

# API
For the sake of time and brevity:
- DOM Elements, Nodes = Node
- DOM NodeLists, HTMLCollections, Array-like objects =  ArrayLike, Array-like
- gg factory objects = gobject
- contents of iterables = item, element

# Table Of Contents
- [gg](#ggselector-supplanter)
- [gg.typeOf](#typeofvalue---string)
- [gg.arrSlice](#arrslicevalue-start-end---array)
- [gg.isArray](#isarrayvalue---boolean)
- [gg.isBoolean](#isbooleanvalue---boolean)
- [gg.isFunction](#isfunctionvalue---boolean)
- [gg.isNull](#isnullvalue---boolean)
- [gg.isNumber](#isnumbervalue---boolean)
- [gg.isObject](#isobjectvalue---boolean)
- [gg.isString](#isstringvalue---boolean)
- [gg.isUndefined](#isundefinedvalue---boolean)
- [gg.isArrayLike](#isarraylikevalue---boolean)
- [gg.isBuffer](#isbuffervalue---boolean)
- [gg.isEmpty](#isemptyvalue---boolean)
- [gg.isGG](#isggvalue---boolean)
- [gg.isNan](#isnanvalue---boolean)
- [gg.isNode](#isnodevalue---boolean)
- [gg.isTypedArray](#istypedarrayvalue---boolean)
- [gg.toArray](#toarrayvalue---boolean)
- [gg.toCamelCase](#tocamelcase---booleanstring)
- [gg.toCodesFromString](#tocodesfromstringvalue---array)
- [gg.toFloat](#tofloatvalue-decimals---numberstring)
- [gg.toHyphenated](#tohyphenatedvalue---booleanstring)
- [gg.toInt](#tointvalue-radix---number)
- [gg.toUint8](#touint8value---uint8array)
- [gg.toBuffer](#tobuffervalue---arraybuffer)
- [gg.toStringFromCodes](#tostringfromcodesvalue---string)
- [gg.betterview](#betterviewvalue-offset-length---better)
- [gg.copy](#copyvalue---any)
- [gg.each](#eachitems-executable-thisarg---any)
- [gg.emitter](#emittervalue---object)
- [gg.equal](#equalone-two---boolean)
- [gg.extend](#extendvalue-add-overwrite---object)
- [gg.inherits](#inheritsctor-superctor---function)
- [gg.inArray](#inarraylist-value---boolean)
- [gg.noop](#noop)
- [gg.supplant](#supplantvalue-supplanter---booleanstring)
- [gg.uuid](#uuid---string)
- [gg.getPosition](#getpositionnode---object)
- [gg.getStyle](#getstylenode-pseudo---object)
- [gg.setImmediate](#setimmediateexecutable---object)
- [gg.getById](#getbyidid-supplanter---node)
- [gg.select](#selectselector-supplanter-node---node)
- [gg.selectAll](#selectallselector-supplanter-node---arraylike)
- [gg.scrollIntoView](#scrollintoviewnode-easingexec)
- [gg.scrollToTop](#scrolltotopnode-easingexec)
- [gg.create](#createtag---gobjectnull)
- [gg.keyboardListener](#keyboardlisteneroptions)
- [gg.mouseListener](#mouselisteneroptions)
- [gg.removeKeyboardListeners](#removekeyboardlisteners)
- [gg.removeMouseListeners](#removemouselisteners)
- [gg.ease](#ease)
- [gg.cdb](#cdb)

## gg(selector, supplanter)
Return a collection of matched nodes found in the DOM.
## Factory
##### gg(selector, supplanter)
#### Parameters
Name | Type | Description
---- | ---- | -----------
selector | String, Node, ArrayLike, GObject | The value containing a string, selector expression, a Node, an Array-like, or a gobject.
supplanter | Object (optional) | The value to supplant into the selector.
#### Methods
##### typeOf(value) _-> {String}_
> Determines the type of its argument.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### arrSlice(value, start, end) _-> {Array}_
> Shorthand for Array.prototype.slice.call.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The "this" value for [Array.prototype.slice](https://www.w3schools.com/jsref/jsref_slice_array.asp).
start | Number (optional) | An integer that specifies where to start the selection (The first element has an index of 0). Use negative numbers to select from the end of an array. If omitted, it acts like 0.
end | Number (optional) | An integer that specifies where to end the selection. If omitted, all elements from the start position and to the end of the array will be selected. Use negative numbers to select from the end of an array.
<br/>

##### isArray(value) _-> {Boolean}_
> Determines if its argument is an array.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isBoolean(value) _-> {Boolean}_
> Determines if its argument is a boolean.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isFunction(value) _-> {Boolean}_
> Determines if its argument is a function.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isNull(value) _-> {Boolean}_
> Determines if its argument is null.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isNumber(value) _-> {Boolean}_
> Determines if its argument is a number.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isObject(value) _-> {Boolean}_
> Determines if its argument is an object.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isString(value) _-> {Boolean}_
> Determines if its argument is a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isUndefined(value) _-> {Boolean}_
> Determines if its argument is undefined.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isArrayLike(value) _-> {Boolean}_
> Determines if its argument is array-like.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isBuffer(value) _-> {Boolean}_
> Determines if its argument is an arraybuffer.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isEmpty(value) _-> {Boolean}_
> Determines if its argument is an object with no enumerable properties.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isGG(value) _-> {Boolean}_
> Determines if its argument is a gobject.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isNan(value) _-> {Boolean}_
> Determines if its argument is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isNode(value) _-> {Boolean}_
> Determines if its argument is a node.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isTypedArray(value) _-> {Boolean}_
> Determines if its argument is a TypedArray.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### toArray(value) _-> {Array}_
> Converts its argument to an Array.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toCamelCase(value) _-> {Boolean|String}_
> Converts a hyphenated string to camel case. Returns false if its argument is not a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String | The value to be converted.
<br/>

##### toCodesFromString(value) _-> {Array}_
> Converts a string to an array of Unicodes. Its argument is first passed through [toArray](#toarrayvalue---array).
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String | The value to be converted.
<br/>

##### toFloat(value, decimals) _-> {Number|String}_
> Converts a value to a floating point number with an optional number of decimals. Removes commas before conversion and returns 0 if its result is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
decimals | Number (optional) | The number of decimals.
<br/>

##### toHyphenated(value) _-> {Boolean|String}_
> Converts a camel case string to a hyphenated one. Returns false if its argument is not a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String | The value to be converted.
<br/>

##### toInt(value, radix) _-> {Number}_
> Converts a value to an integer using the specified radix. Removes commas before conversion and returns 0 if its result is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
radix | Number (optional, default: 10) | The radix to use.
<br/>

##### toUint8(value) _-> {Uint8Array}_
> Converts its argument to an uint8array. If its argument is a number, it returns an uint8array with an equal length.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toBuffer(value) _-> {ArrayBuffer}_
> Converts its argument to an arraybuffer by passing it through [toUint8](#touint8value---uint8array) and getting its buffer property. If its argument is a number, it returns an arraybuffer with an equal length.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toStringFromCodes(value) _-> {String}_
> Converts an array of Unicodes to a string. Its argument is first passed through [toArray](#toarrayvalue---array).
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Array | The value to be converted.
<br/>

##### betterview(value, offset, length) _-> {Better}_
> An upgraded [DataView](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/DataView).
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value passed through [toBuffer](#tobuffervalue---arraybuffer) before storing.
offset | Number (optional) | The offset, in bytes, to the first byte in the specified buffer for the new view to reference. If not specified, the view of the buffer will start with the first byte.
length | Number (optional) | The number of elements in the byte array. If unspecified, length of the view will match the buffer's length.
<br/>

##### copy(value) _-> {Any}_
> Copies its argument by value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to copy.
<br/>

##### each(items, executable, thisarg) _-> {Any}_
> Calls a provided function once for each element in a set of elements, in order. It returns the assigned "this" value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
items | GObject, Array, ArrayLike, TypedArray, Buffer, Object | The value to iterate over.
executable | Function | The function to be run for each element within the set.
thisarg | Any (optional) | The value to be passed to the function to be used as its "this" value. If empty, the iterated set of elements will be assigned to it.
<br/>

##### emitter(value) _-> {Object}_
> A client side port of Node.js' events.js.  Allows, enables, and returns an emitter object - one able to listen for and emit custom events.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Object (optional) | The object to turn into an emitter.
<br/>

##### equal(one, two) _-> {Boolean}_
> Determines if its two arguments are equal by value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
one | Any | A value to compare.
two | Any | A value to compare.
<br/>

##### extend(value, add, overwrite) _-> {Object}_
> Extends its first argument with its second.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Object | The value to extend.
add | Object | The extending value.
overwrite | Boolean (optional; default: true) | The value indicating if values with matching keys will be overwritten.
<br/>

##### inherits(ctor, superCtor) _-> {Function}_
> Its first argument prototypically inherits from its second.
###### Parameters
Name | Type | Description
---- | ---- | -----------
ctor | Function | The inheriting value.
superCtor | Function | The inherited value.
<br/>

##### inArray(list, value) _-> {Boolean}_
> Checks if its second argument is contained within its first.
###### Parameters
Name | Type | Description
---- | ---- | -----------
list | Array | The value to look through.
value | Any | The value to look for.
<br/>

##### noop()
> An empty function.

<br/>

##### supplant(value, supplanter) _-> {Boolean|String}_
> Does variable substitution on its first argument. It scans through its first argument looking for expressions enclosed in { } braces. If an expression is found, use it as a key on its second argument, and if the key has a string value or number value, it is substituted for the bracket expression and it repeats.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String | The value to scan.
supplanter | Object | The supplanting value.
<br/>

##### uuid() _-> {String}_
> Generates a universally unique identifier.

<br/>

##### getPosition(node) _-> {Object}_
> Gets its arguments absolute x and y coordinates.
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Node | The Node to get the position of.
<br/>

##### getStyle(node, pseudo) _-> {Object}_
> Shorthand for [window.getComputedStyle](https://www.w3schools.com/jsref/jsref_getcomputedstyle.asp).
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Node | The node to get the computed style of.
pseudo | String (optional; default: null) | The pseudo-element to get.
<br/>

##### setImmediate(executable) _-> {Object}_
> Shorthand for [window.setTimeout](https://www.w3schools.com/jsref/met_win_settimeout.asp) with 0 wait time.
###### Parameters
Name | Type | Description
---- | ---- | -----------
executable | Function | The function that will be run.
<br/>

##### getById(id, supplanter) _-> {Node}_
> Combines [supplant](#supplantstring-object---booleanstring) and [document.getElementById](https://www.w3schools.com/jsref/met_document_getelementbyid.asp), in that order.
###### Parameters
Name | Type | Description
---- | ---- | -----------
id | String | The value to scan.
supplanter | Object | The supplanting value.
<br/>

##### select(selector, supplanter, node) _-> {Node}_
> Combines [document.querySelector](https://www.w3schools.com/jsref/met_document_queryselector.asp) and [supplant](#supplantstring-object---booleanstring), in that order, where document is replaced by the optional third argument if provided.
###### Parameters
Name | Type | Description
---- | ---- | -----------
selector | String | The value to scan.
supplanter | Object | The supplanting value.
node | Node | The node to execute the query from.
<br/>

##### selectAll(selector, supplanter, node) _-> {ArrayLike}_
> Combines [document.querySelectorAll](https://www.w3schools.com/jsref/met_document_queryselectorall.asp) and [supplant](#supplantstring-object---booleanstring), in that order, where document is replaced by the optional third argument if provided.
###### Parameters
Name | Type | Description
---- | ---- | -----------
selector | String | The value to scan.
supplanter | Object | The supplanting value.
node | Node | The node to execute the query from.
<br/>

##### scrollIntoView(node, easingExec)
> Scrolls its first argument into view using its second argument as the easing function.
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Node | The node to scroll into view.
easingExec | Function (optional, default: ease.easeInOutSine) | The easing function to use when scrolling the page.
<br/>

##### scrollToTop(node, easingExec)
> Scrolls to the top of its first argument using its second argument as the easing function.
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Node | The node to scroll to the top of.
easingExec | Function (optional, default: ease.easeInOutSine) | The easing function to use when scrolling.
<br/>

##### create(tag) _-> {GObject|Null}_
> Case insensitive shorthand for [document.createElement](https://www.w3schools.com/jsref/met_document_createelement.asp). The new node is converted to a gobject before being returned. If its argument is not a correctly named node it returns null.
###### Parameters
Name | Type | Description
---- | ---- | -----------
tag | String | The name of the node to create.
<br/>

##### keyboardListener(options)
> Listens for keyboard key down events.
###### Parameters
Name | Type | Description
---- | ---- | -----------
options | Object | Each options key is a keyCode (Number, String) of the keyboard key to listen for when pressed down with one exception - "preventDefault": (Boolean). Optionally, five strings are recognized as keys: "enter", "leftarrow", "uparrow", "downarrow", and "rightarrow". Each options value is a function to run when its corresponding key is pressed down.
<br/>

##### mouseListener(options)
> Listens for mouse key down events.
###### Parameters
Name | Type | Description
---- | ---- | -----------
options | Object | Each options key is a button code (Number, String) of the mouse button to listen for when pressed down with one exception - "preventDefault": (Boolean). Optionally, three strings are recognized as keys: "left", "middle", and "right". Each options value is a function to run when its corresponding button is pressed down.
<br/>

##### removeKeyboardListeners()
> Removes all keyboard listeners.
<br/>

##### removeMouseListeners()
> Removes all mouse listeners.
<br/>

#### Attributes
##### ease
> A collection of easing functions that return a current value based on four parameters.
###### Parameters
Name | Type | Description
---- | ---- | -----------
t | Number | The current time.
b | Number | The initial value.
c | Number | The change in value.
d | Number | The total duration.
###### Properties
- linearTween
- easeInQuad
- easeOutQuad
- easeInOutQuad
- easeInCubic
- easeOutCubic
- easeInOutCubic
- easeInQuart
- easeOutQuart
- easeInOutQuart
- easeInQuint
- easeOutQuint
- easeInOutQuint
- easeInSine
- easeOutSine
- easeInOutSine
- easeInExpo
- easeOutExpo
- easeInOutExpo
- easeInCirc
- easeOutCirc
- easeInOutCirc
<br/>

##### cdb
> An emitter that is a small, SQL-like interface to indexedDB.
###### Methods
Name | Parameters | Description
---- | ---------- | -----------
open | <table><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>String</td><td>The name of the database to open.</td></tr><tr><td>version (optional, default: 1)</td><td>Number</td><td>The version of the database.</td></tr></tbody></table> | Opens a new database.
delete | <table><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>String</td><td>The name of the database to delete.</td></tr></tbody></table> | Deletes a database.
<br/>

## gobject
A gg factory object.

- **gobject.add**
- **gobject.addClass**
- **gobject.after**
- **gobject.append**
- **gobject.appendTo**
- **gobject.attr**
- **gobject.before**
- **gobject.children**
- **gobject.classes**
- **gobject.clone**
- **gobject.create**
- **gobject.data**
- **gobject.each**
- **gobject.eachRaw**
- **gobject.get**
- **gobject.hasClass**
- **gobject.html**
- **gobject.insert**
- **gobject.length**
- **gobject.off**
- **gobject.on**
- **gobject.once**
- **gobject.parents**
- **gobject.prepend**
- **gobject.prependTo**
- **gobject.prop/css/style**
- **gobject.raw**
- **gobject.remove**
- **gobject.remAttr**
- **gobject.remClass**
- **gobject.remData**
- **gobject.remHtml**
- **gobject.remProp/remCss/remStyle**
- **gobject.remText**
- **gobject.select**
- **gobject.selectAll**
- **gobject.subtract**
- **gobject.text**
- **gobject.togClass**
