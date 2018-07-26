gg
==

A JavaScript and DOM utility library.

# API
## gg(selector, supplantee)
Return a collection of matched elements found in the DOM.
## Factory
`gg(selector, supplantee)`
#### Parameters:
Name | Type | Description
---- | ---- | -----------
selector | String, Node, NodeArray, GG Object | A string containing a selector expression, a DOM element, an array of DOM elements, or a gg factory object.
supplantee | Object (optional) | The object to supplant into the selector.
#### Methods
`typeOf(value)` _-> {string}_
> Determines the type of its argument.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be tested.
<br/>
`isArray(array)` _-> {boolean}_
> Determines if its argument is an array.
##### Parameters
Name | Type | Description
---- | ---- | -----------
array | Any | The value to be tested.
<br/>
`isBoolean(bool)` _-> {boolean}_
> Determines if its argument is a boolean.
##### Parameters
Name | Type | Description
---- | ---- | -----------
bool | Any | The value to be tested.
<br/>
`isFunction(func)` _-> {boolean}_
> Determines if its argument is a function.
##### Parameters
Name | Type | Description
---- | ---- | -----------
func | Any | The value to be tested.
<br/>
`isNull(nul)` _-> {boolean}_
> Determines if its argument is null.
##### Parameters
Name | Type | Description
---- | ---- | -----------
nul | Any | The value to be tested.
<br/>
`isNumber(number)` _-> {boolean}_
> Determines if its argument is a number.
##### Parameters
Name | Type | Description
---- | ---- | -----------
number | Any | The value to be tested.
<br/>
`isObject(object)` _-> {boolean}_
> Determines if its argument is an object.
##### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>
`isString(string)` _-> {boolean}_
> Determines if its argument is a string.
##### Parameters
Name | Type | Description
---- | ---- | -----------
string | Any | The value to be tested.
<br/>
`isUndefined(undef)` _-> {boolean}_
> Determines if its argument is undefined.
##### Parameters
Name | Type | Description
---- | ---- | -----------
undef | Any | The value to be tested.
<br/>
`isArrayLike(object)` _-> {boolean}_
> Determines if its argument is an array-like object.
##### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>
`isBuffer(buffer)` _-> {boolean}_
> Determines if its argument is an arraybuffer.
##### Parameters
Name | Type | Description
---- | ---- | -----------
buffer | Any | The value to be tested.
<br/>
`isEmpty(object)` _-> {boolean}_
> Determines if its argument is an object with no enumerable properties.
##### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested.
<br/>
`isGG(object)` _-> {boolean}_
> Determines if its argument is a gg object.
##### Parameters
Name | Type | Description
---- | ---- | -----------
object | Any | The value to be tested
<br/>
`isNan(nan)` _-> {boolean}_
> Determines if its argument is NaN.
##### Parameters
Name | Type | Description
---- | ---- | -----------
nan | Any | The value to be tested.
<br/>
`isNode(node)` _-> {boolean}_
> Determines if its argument is a DOM element.
##### Parameters
Name | Type | Description
---- | ---- | -----------
node | Any | The value to be tested
<br/>
`isTypedArray(array)` _-> {boolean}_
> Determines if its argument is a typed array.
##### Parameters
Name | Type | Description
---- | ---- | -----------
array | Any | The value to be tested
<br/>
`toArray(value)` _-> {boolean}_
> Converts its argument to an array or typed array.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>
`toCamelCase(string)` _-> {boolean|string}_
> Converts a hyphenated string to camel case. Returns false if its argument is not a string.
##### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>
`toCodesFromString(string)` _-> {array}_
> Converts a string to an array of Unicodes. Its argument is first passed to `toArray`.
##### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>
`toFloat(value, digits)` _-> {number|string}_
> Converts a value to a floating point number with an optional number of decimals. Automatically removes commas and returns 0 if the result is NaN.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
digits | Number (optional) | The number of decimals.
<br/>
`toHyphenated(string)` _-> {boolean|string}_
> Converts a hyphenated string to camel case. Returns false if its argument is not a string.
##### Parameters
Name | Type | Description
---- | ---- | -----------
string | String | The value to be converted.
<br/>
`toInt(value, radix)` _-> {number}_
> Converts a value to an integer using the specified radix (defaults to 10). Automatically removes commas and returns 0 if the result is NaN.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | String, Number | The value to be converted.
radix | Number (optional) | The radix to use.
<br/>
`toUint8(value)` _-> {uint8array}_
> Converts its argument to an uint8array. If its argument is a number, the returned uint8array has a length equal to it.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>
`toBuffer(value)` _-> {arraybuffer}_
> Converts its argument to an arraybuffer by passing it to `toUint8`. If its argument is a number, the returned arraybuffer has a length equal to it.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to be converted.
<br/>
`toStringFromCodes(array)` _-> {string}_
> Converts an array of Unicodes to a string. Its argument is first passed to `toArray`.
##### Parameters
Name | Type | Description
---- | ---- | -----------
array | Array | The value to be converted.
<br/>
`arrSlice(value)` _-> {array}_
> Shorthand for Array.prototype.slice.call(value).
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The `this` value to call Array.prototype.slice() with.
<br/>
`betterview(buffer, offset, length)` _-> {better}_
> An upgraded DataView.
##### Parameters
Name | Type | Description
---- | ---- | -----------
buffer | Any | The value passed to `toBuffer` before storing; usually an array, arraybuffer, or string.
offset | Number (optional) | The offset, in bytes, to the first byte in the specified buffer for the new view to reference. If not specified, the view of the buffer will start with the first byte.
length | Number (optional) | The number of elements in the byte array. If unspecified, length of the view will match the buffer's length.
<br/>
`copy(value)` _-> {any}_
> Copies its argument by value.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to copy.
<br/>
`each(items, func, thisarg)` _-> {any}_
> Loops through `items`, converting it to an array if necessary, passing each item and its index/key to `func`.  `func`'s this argument is set to `thisarg` or `items` if none was passed.  Essentially a `forEach` method with the capability to handle objects and their keys, as well as nodes.
##### Parameters
Name | Type | Description
---- | ---- | -----------
value | Any | The value to copy.
<br/>
- **gg.each**
- **gg.ease**
- **gg.emitter**
- **gg.equal**
- **gg.extend**
- **gg.inherits**
- **gg.inArray**
- **gg.noop**
- **gg.supplant**
- **gg.uuid**
- **gg.getById**
- **gg.getPosition**
- **gg.getStyle**
- **gg.setImmediate**
- **gg.select**
- **gg.selectAll**
- **gg.create**
- **gg.scrollIntoView**
- **gg.scrollToTop**
- **gg.keyboardHandler**
- **gg.mouseHandler**
- **gg.removeKeyboardHandlers**
- **gg.removeMouseHandlers**
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