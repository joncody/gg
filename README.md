gg
==

A JavaScript and DOM utility library.

# API
## gg(selector, supplantee)
Return a collection of matched elements found in the DOM.
## Factory
##### gg(selector, supplantee)
#### Parameters:
Name | Type | Description
---- | ---- | -----------
selector | String, Node, NodeList, GG Object | A string containing a selector expression, a DOM element, an array of DOM elements, or a gg factory object.
supplantee | Object (optional) | The object to supplant into the selector.
#### Methods
##### arrSlice(value, start, end) _-> {array}_
> Shorthand for Array.prototype.slice.call.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The "this" value for Array.prototype.slice.
start | Number (Optional) | An integer that specifies where to start the selection (The first element has an index of 0). Use negative numbers to select from the end of an array. If omitted, it acts like "0".
end | Number (Optional) | An integer that specifies where to end the selection. If omitted, all elements from the start position and to the end of the array will be selected. Use negative numbers to select from the end of an array.
<br/>

##### typeOf(value) _-> {string}_
> Determines the type of its argument.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>

##### isArray(array) _-> {boolean}_
> Determines if its argument is an array.
###### Parameters
Name | Type | Description
---- | ---- | -----------
array | Any | The value to be tested.
<br/>

##### isBoolean(bool) _-> {boolean}_
> Determines if its argument is a boolean.
###### Parameters
Name | Type | Description
---- | ---- | -----------
bool | Any | The value to be tested.
<br/>

##### isFunction(func) _-> {boolean}_
> Determines if its argument is a function.
###### Parameters
Name | Type | Description
---- | ---- | -----------
func | Any | The value to be tested.
<br/>

##### isNull(nul) _-> {boolean}_
> Determines if its argument is null.
###### Parameters
Name | Type | Description
---- | ---- | -----------
nul | Any | The value to be tested.
<br/>

##### isNumber(number) _-> {boolean}_
> Determines if its argument is a number.
###### Parameters
Name | Type | Description
---- | ---- | -----------
number | Any | The value to be tested.
<br/>

##### isObject(object) _-> {boolean}_
> Determines if its argument is an object.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>

##### isString(string) _-> {boolean}_
> Determines if its argument is a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
string | Any | The value to be tested.
<br/>

##### isUndefined(undef) _-> {boolean}_
> Determines if its argument is undefined.
###### Parameters
Name | Type | Description
---- | ---- | -----------
undef | Any | The value to be tested.
<br/>

##### isArrayLike(object) _-> {boolean}_
> Determines if its argument is an array-like object.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>

##### isBuffer(buffer) _-> {boolean}_
> Determines if its argument is an arraybuffer.
###### Parameters
Name | Type | Description
---- | ---- | -----------
buffer | Any | The value to be tested.
<br/>

##### isEmpty(object) _-> {boolean}_
> Determines if its argument is an object with no enumerable properties.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>

##### isGG(object) _-> {boolean}_
> Determines if its argument is a gg object.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested
<br/>

##### isNan(nan) _-> {boolean}_
> Determines if its argument is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
nan | Any | The value to be tested.
<br/>

##### isNode(node) _-> {boolean}_
> Determines if its argument is a DOM element.
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Any | The value to be tested
<br/>

##### isTypedArray(array) _-> {boolean}_
> Determines if its argument is a typed array.
###### Parameters
Name | Type | Description
---- | ---- | -----------
array | Any | The value to be tested
<br/>

##### toArray(value) _-> {array}_
> Converts its argument to an array.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toCamelCase(string) _-> {boolean|string}_
> Converts a hyphenated string to camel case. Returns false if its argument is not a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>

##### toCodesFromString(string) _-> {array}_
> Converts a string to an array of Unicodes. Its argument is first passed through [toArray](#toarrayvalue---array).
###### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>

##### toFloat(value, digits) _-> {number|string}_
> Converts a value to a floating point number with an optional number of decimals. Automatically removes commas and returns 0 if its result is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
digits | Number (optional) | The number of decimals.
<br/>

##### toHyphenated(string) _-> {boolean|string}_
> Converts a hyphenated string to camel case. Returns false if its argument is not a string.
###### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>

##### toInt(value, radix) _-> {number}_
> Converts a value to an integer using the specified radix (defaults to 10). Automatically removes commas and returns 0 if its result is NaN.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
radix | Number (optional) | The radix to use.
<br/>

##### toUint8(value) _-> {uint8array}_
> Converts its argument to an uint8array. If its argument is a number, it returns an uint8array with an equal length.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toBuffer(value) _-> {arraybuffer}_
> Converts its argument to an arraybuffer by passing it through [toUint8](#touint8value---uint8array) and getting its buffer property. If its argument is a number, it returns an arraybuffer with an equal length.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>

##### toStringFromCodes(array) _-> {string}_
> Converts an array of Unicodes to a string. Its argument is first passed through [toArray](#toarrayvalue---array).
###### Parameters
Name | Type | Description
---- | ---- | -----------
array | Array | The value to be converted.
<br/>

##### betterview(buffer, offset, length) _-> {better}_
> An upgraded DataView.
###### Parameters
Name | Type | Description
---- | ---- | -----------
buffer | Any | The value passed through [toBuffer](#tobuffervalue---arraybuffer) before storing.
offset | Number (optional) | The offset, in bytes, to the first byte in the specified buffer for the new view to reference. If not specified, the view of the buffer will start with the first byte.
length | Number (optional) | The number of elements in the byte array. If unspecified, length of the view will match the buffer's length.
<br/>

##### copy(value) _-> {any}_
> Copies its argument by value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to copy.
<br/>

##### each(items, func, thisarg) _-> {any}_
> Calls a provided function once for each element in a set of elements, in order. It returns the assigned "this" value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
items | GG Object, Node, NodeList, Array, ArrayLike, TypedArray, Buffer, Object | The value to iterate over.
func | Function | The function to be run for each element within the set.
thisarg | Any (Optional) | The value to be passed to the function to be used as its "this" value. If empty, the iterated set of elements will be assigned to it.
<br/>

##### emitter(object) _-> {object}_
> A client side port of Node.js' events.js.  Allows and enables an object to listen for and emit custom events.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Object | The object to turn into an emitter.
<br/>

##### equal(one, two) _-> {boolean}_
> Determines if its two arguments are equal by value.
###### Parameters
Name | Type | Description
---- | ---- | -----------
one | Any | A value to compare.
two | Any | A value to compare.
<br/>

##### extend(object, add, overwrite) _-> {object}_
> Extends its first argument with its second.
###### Parameters
Name | Type | Description
---- | ---- | -----------
object | Object | The value to extend.
add | Object | The extending value.
overwrite | Boolean (Optional; Default: true) | The value indicating if values with matching keys will be overwritten.
<br/>

##### inherits(ctor, superCtor) _-> {function}_
> Its first argument prototypically inherits from its second.
###### Parameters
Name | Type | Description
---- | ---- | -----------
ctor | Function | The inheriting value.
superCtor | Function | The inherited value.
<br/>

##### inArray(array, value) _-> {boolean}_
> Checks if its second argument is contained within its first.
###### Parameters
Name | Type | Description
---- | ---- | -----------
array | Array | The value to scan through.
value | Any | The value to index.
<br/>

##### noop()
> An empty function.

<br/>

##### supplant(string, object) _-> {boolean|string}_
> Does variable substitution on its first argument. It scans through its first argument looking for expressions enclosed in { } braces. If an expression is found, use it as a key on its second argument, and if the key has a string value or number value, it is substituted for the bracket expression and it repeats.
###### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to scan.
object | Object | The supplanting value.
<br/>

##### uuid() _-> {string}_
> Generates a universally unique identifier.

<br/>

##### getById(id, object) _-> {node}_
> Combines [supplant](#supplantstring-object---booleanstring) and document.getElementById, in that order.
###### Parameters
Name | Type | Description
---- | ---- | -----------
id | String | The value to scan.
object | Object | The supplanting value.
<br/>

##### getPosition(el) _-> {object}_
> Gets its arguments absolute x and y coordinates.
###### Parameters
Name | Type | Description
---- | ---- | -----------
el | Node | The DOM element to get the position of.
<br/>

##### getStyle(node, pseudo) _-> {object}_
> Shorthand for window.getComputedStyle().
###### Parameters
Name | Type | Description
---- | ---- | -----------
node | Node | The DOM element to get the computed style of.
pseudo | String (Optional; Default: null) | The pseudo-element to get.
<br/>

##### setImmediate(fn) _-> {object}_
> Shorthand for window.setTimeout() with "0" wait time.
###### Parameters
Name | Type | Description
---- | ---- | -----------
fn | Function | The function that will be executed.
<br/>

##### select(selector, object, node) _-> {node}_
> Combines document.querySelector and supplant, in that order, where document is replaced by the optional third argument if provided.
###### Parameters
Name | Type | Description
---- | ---- | -----------
selector | String | The value to scan.
object | Object | The supplanting value.
node | Node | The top level element to execute the query from.
<br/>

##### selectAll(selector, object, node) _-> {nodelist}_
> Combines document.querySelectorAll and supplant, in that order, where document is replaced by the optional third argument if provided.
###### Parameters
Name | Type | Description
---- | ---- | -----------
selector | String | The value to scan.
object | Object | The supplanting value.
node | Node | The top level element to execute the query from.
<br/>

- **gg.create**
- **gg.scrollIntoView**
- **gg.scrollToTop**
- **gg.keyboardHandler**
- **gg.mouseHandler**
- **gg.removeKeyboardHandlers**
- **gg.removeMouseHandlers**
- **gg.ease**
- **gg.cdb**


#### Instance
```javascript
var gobject = gg(_string_[, _object_]);
```
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
