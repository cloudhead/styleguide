# JavaScript

## Identifiers

- **RULE**: Identifiers bound to constructors **must** start with a capital.

```javascript
  // GOOD

  var User = function (name, age) {
      this.name = name;
      this.age = age;
  };
  var user = new User('bob', 32);

```


```javascript
  // BAD

  var user = function (name, age) {
      this.name = name;
      this.age = age;
  };
  var u = new user('bob', 32);

```

- **RULE**: Identifiers bound to a variable or function **must** start with a *minuscule*.
- **RULE**: Identifiers bound to a variable or function **must** be CamelCased or lowercase,
  depending on their length.

```javascript
  // GOOD

  var someKindOfProcess = function () {};
  var tmpvar = 42;

```


```javascript
  // BAD

  var some_kind_of_process = function () {};
  var somekindofprocess = function () {};

```

## Variable declarations

- **RULE**: Variables **must** always be declared, prior to use.
- **RULE**: Variable declarations **should** appear at the top of functions,
  and not inside other blocks. The exception is *for* loops.

> Variable declarations are moved up to the top of the function scope anyway,
> so that's where they belong.


```javascript
  // GOOD

  function (a, b) {
      var k;

      if (a == b) {
          k = true;
      }
      ...
  }

  for (var i = 0; i < l; i ++) { ... }

```


```javascript
  // BAD

  function (a, b) {
      if (a == b) {
          var k = true;
      }
      ...
  }

```

## Control-flow

- **RULE**: Control-flow statements, such as `if`, `while` and `for` **must** have a space between the keyword and the left parenthesis.

> They aren't functions, and thus better distinguished like this.

```javascript
  // GOOD

  if (a) {
      return true;
  }

```

```javascript
  // BAD

  if(a) {
      return true;
  }

```

## Functions

- **RULE**: Anonymous functions **must** have a space between the `function` keyword and the left parenthesis.

> To emphasise the lack of identifier and differentiate them with named functions.


```javascript
  // GOOD

  function (a, b) {}

```


```javascript
  // BAD

  function(a, b) {}

```

- **RULE**: Named functions **must not** have a space between the function name and the left parenthesis.
- **RULE**: Function calls **should not** have a space between the function name and the left parenthesis.


```javascript
  // GOOD

  function add(a, b) {}

```


```javascript
  // BAD

  function add (a, b) {}

```

## Semicolons

- **RULE**: Semicolons `;` **must** be added at the end of every statement, **except** when the next character is a closing bracket `}`.
  In that case, they may be omitted.


```javascript
  // GOOD

  var f = function add(a, b) {
      if (a == b) { return a * 2 }   // No `;` here.
      return a + b;
  };

```


```javascript
  // BAD

  var f = function add (a, b) {
      return a + b
  }

```

## Braces

- **RULE**: Braces **should** be used in all circumstances. They **may** be omitted
  around simple statements.


```javascript
  // GOOD

  if (x) { return true }

```

```javascript
  // BAD

  if (x)
    while (1)
      i ++;
  else
    ...
```


```javascript
  // OK

  if (x) return true;

```

```javascript
  // OK

  if (x)
      return true;

```
- **RULE**: Opening Braces **must never** be on a line of their own.

> Vertical screen space is precious.

```javascript
  // GOOD

  if (x) {
      return true;
  }

```


```javascript
  // BAD

  if (x)
  {
      return true;
  }

```

```javascript
  // BAD

  if (x) {
      return true; }

```


