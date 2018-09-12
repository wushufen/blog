```javascript

// null
value === null // true
typeof value // object

// undefined
value === undefined // true
typeof value == 'undefined' // true

// string
typeof value == 'string' // true
value instanceof String // false

// number
typeof value == 'number' // true
value instanceof Number // false

// array
value instanceof Array // true
typeof value // object

// object
typeof: null {} [] /reg/ ...

// function
typeof value == 'function' // true
value instanceof Function // true

// regexp
value instanceof RegExp // true
typeof value // object

// date
value instanceof Date // true
typeof value // object

// *
Object.prototype.toString.call(value) // "[object _Type_]"

// typeOf
function typeOf(value){
    return toString.call(value).slice(8, -1).toLowerCase()
}

```
