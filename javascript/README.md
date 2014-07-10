# Javascript Styleguide

## Comments

For most comments, use `//`. For comments over 4 lines, you can use `/* */`.

Try to make your code simple and self documenting. Use 20 lines as a guideline for considering breaking the method into pieces.


## Default Values

When initializing default values, use:

```js
objectids = null;
strings = '';
numbers = 0;`
objects = {};
arrays  = [];
```

## Variables

### Caching

Anytime you access something more than once, assign to a variable.

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
SuperConstant = 'apikey';
```

Good:

```js
SUPER_CONSTANT = 'apikey';
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

## Promises

Prefer promises over callbacks.

We use bluebird to wrap all network requests in promises via bootie.

## Indentation

Tabs should be soft tabs of **2 spaces**.


## Quotations

Prefer ' over "


## Comparisons

Always use === and !==

## Semicolons

- Always use semicolons for all functions, callbacks, and literals.
- Don't use semicolons for if, for, while, and other control blocks.

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
