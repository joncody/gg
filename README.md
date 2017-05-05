gg
==

An ECMASCRIPT 5 compliant JavaScript utility library.

## API

- gg.typeOf(_mixed_)
- gg.noop()
- gg.arrSlice(_mixed_)
- gg.isBoolean(_mixed_)
- gg.isNumber(_mixed_)
- gg.isString(_mixed_)
- gg.isArray(_mixed_)
- gg.isObject(_mixed_)
- gg.isFunction(_mixed_)
- gg.isNull(_mixed_)
- gg.isUndefined(_mixed_)
- gg.isArrayLike(_mixed_)
- gg.isTypedArray(_mixed_)
- gg.isBuffer(_mixed_)
- gg.isNode(_mixed_)
- gg.isEmpty(_object_)
- gg.toArray(_mixed_)
- gg.toUint8(_mixed_)
- gg.toBuffer(_mixed_)
- gg.inArray(_mixed_, _array_)
- gg.toCamelCase(_string_)
- gg.undoCamelCase(_string_)
- gg.getCodesFromString(_string_)
- gg.getStringFromCodes(_array_)
- gg.uuid()
- gg.supplant(_string_, _object_)
- gg.inherits(_function_, _function_)
- gg.each(_mixed_, _function_[, _mixed_])
- gg.extend(_object_, _object_[, _boolean_])
- gg.cloneNodeDeeper(_node_)
- gg.getById(_string_)
- gg.select(_string_)
- gg.selectAll(_string_)
- gg.keyboardHandler(_object_)
- gg.mouseHandler(_object_)
- gg.xhrReq(_object_)
- gg.readFiles(_object_)
- gg.create(_string_)

## Instance API
- gobject.get([_number_])
- gobject.getRaw([_number_])
- gobject.length()
- gobject.each(_function_)
- gobject.add(_node[s]_)
- gobject.subtract(_number_)
- gobject.data(_string_, _string_)
- gobject.remData(_string_)
- gobject.attr(_string_, _string_)
- gobject.remAttr(_string_)
- gobject.prop(_string_, _string_)
- gobject.css(_string_, _string_)
- gobject.style(_string_, _string_)
- gobject.remProp(_string_)
- gobject.remCss(_string_)
- gobject.remStyle(_string_)
- gobject.text(_string_)
- gobject.remText(_string_)
- gobject.html(_string_)
- gobject.remHtml(_string_)
- gobject.classes(_string_)
- gobject.addClass(_string_)
- gobject.remClass(_string_)
- gobject.togClass(_string_)
- gobject.hasClass(_string_)
- gobject.insert(_string_, _string_)
- gobject.prepend(_node[s]_)
- gobject.prependTo(_node[s]_)
- gobject.append(_node[s]_)
- gobject.appendTo(_node[s]_)
- gobject.after(_node[s]_)
- gobject.before(_node[s]_)
- gobject.remove([_node[s]_])
- gobject.parents()
- gobject.children()
- gobject.select(_string_)
- gobject.selectAll(_string_)
- gobject.clone([_boolean_[, _boolean_]])
- gobject.create(_string_)
- gobject.hide()
- gobject.show()
- gobject.on(_string_, _function_[, _boolean_])
- gobject.off(_string_[, _function_])
- gobject.once(_string_, _function_[, _boolean_])
