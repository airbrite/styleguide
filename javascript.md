# Javascript Style Guide

Much of this is adapted from [Douglas Crockford](http://javascript.crockford.com/code.html) and [Airbnb](https://github.com/airbnb/javascript/tree/master/es5)

## React

[Airbnb React](https://github.com/airbnb/javascript/tree/master/react)

## jQuery

[YOU MIGHT NOT NEED JQUERY](http://youmightnotneedjquery.com/)

## Indentation

Tabs should be soft tabs of **2 spaces**.

## Quotations

Prefer `'` over `"`.

## Comparisons

Always use `===` and `!==`, **never** use `==` and `!=`.

## Semicolons

Use them.

* Always use semicolons for all functions, callbacks, and literals.
* Don't use semicolons for if, for, while, and other control blocks.

## Comments

For most inline comments, use `//`.

We also use JSDoc for function/method block commenting

Try to make your code simple and self documenting.
Use 20 lines as a guideline for considering breaking the method into pieces.

## Default Values

When initializing default values, use:

```js
objectids = null;
strings = '';
numbers = 0;
objects = {};
arrays  = [];
dates = null;
```

## Variables

### Caching

Anytime you access something more than once in the same method,
assign it to a variable.

Bad:

```js
return 'hi ' + this.get('name') + '. How are you doing, ' + this.get('name');
```

Good:

```js
var name = this.get('name');

return 'hi ' + name + '. How are you doing, ' + name;
```

### Naming

#### Instances

Use camelCase for variable and instance names.

Bad:

```js
var Bob = new UserModel();
var bob_jones = new UserModel();
```

Good:

```js
var bob = new UserModel();
var bobJones = new UserModel();
```

An exception to this is when directly accessing the database,
many fields stored in the database schema use underscores.

#### Classes

Use UpperCase for class names.

Bad:

```js
var user = Backbone.Model.extend();
var user_collection = Backbone.Collection.extend();
```

Good:

```js
var UserModel = Backbone.Model.extend();
var UserCollection = Backbone.Collection.extend();
```

#### Constants

ALL_CAPS underscored for constants.

Bad:

```js
MyConstant = 'apikey';
```

Good:

```js
MY_CONSTANT = 'apikey';
```

### Spacing

* One line per variable
* One `var` per var
* 80 character limit

Bad:

```js
var user = 'Bob',
    admin = 'Jack';

var wombat, kangaroo, koala;
```

Good:

```js
var user = 'Bob';
var admin = 'Jack';

var wombat;
var kangaroo;
var koala;
```

#### Functions, Variables, and Control statements

* Space before `{`
* Space after `if`
* Space after `function`

```js
var b = 0;
var c = 1;

function foo() {
  // No spaces
}

if (b) {
  // No spaces
}

switch(foo) {
  case 'bar':
    console.log('bar');
    break;
  case 'omg':
    console.log('omg');
    break;
  default:
    console.log(foo);
    break;
}
```

#### Wrapping Arguments

If arguments go past the 80 character line limit, add a newline after each just like an array.

Bad:

```js
function() {
...
}.property('foo', 'bar', 'baz', 'wombat', 'koala', 'coffee', 'tea', 'beer', 'whiskey');
```

Good:

```js
function() {
...
}.property(
  'foo',
  'bar',
  'baz',
  'wombat',
  'koala',
  'coffee',
  'tea',
  'beer',
  'whiskey'
);
```

### jQuery wrapped

All jQuery wrapped object variable names should prepend a `$`.

Bad:

```js
var user = $('#current-user');
var links = $('.links');
```

Good:

```js
var $user = $('#current-user');
var $links = $('.links');
```

## Control structures

### Early Return

Bad:

```js
if (foo) {
  return;
} else {
  return 'blah';
}
```

Good:

```js
if (foo) {
  return;
}

return 'blah';
```

### No one-line IF

Bad:

```js
if (foo) return;
```

Good:

```js
if (foo) {
  return;
}
```

## Ternary Operator

Use them for simple cases.

Bad:

```js
var foo = (this.model.get('products').length > 10 && bar < 1) ? true : false;
```

Good:

```js
var foo = productLength > 10 ? true : false;
```

## Leading Commas

No.

Bad:

```js
var a = [
    1
  , 2
  , 3
];

var b = {
    foo: 'bar'
  , baz: 'wombat'
};
```

Good:

```js
var a = [
  1,
  2,
  3
]

var b = {
  foo: 'bar',
  baz: 'wombat'
};
```

## Wrap JSON.parse with try/catch

Bad:

```js
var j = JSON.parse(myJson);
```

Good:

```js
try {
  var j = JSON.parse(myJson);
} catch(e) {
  console.error(e);
}
```

## Globals

Don't use them. We expose the namespace for each app.
