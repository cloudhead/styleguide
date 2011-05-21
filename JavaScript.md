# JavaScript

## Identifiers

- **RULE**: Identifiers bound to contructor functions **must** start with a capital.

### GOOD

```javascript

  var User = function (name, age) {
      this.name = name;
      this.age = age;
  };
  var user = new User('bob', 32);

```

### BAD

```javascript

  var user = function (name, age) {
      this.name = name;
      this.age = age;
  };
  var u = new user('bob', 32);

```

- **RULE**: Identifiers bound to a variable **must** be CamelCased, and start with a lowercase letter.

### GOOD

```javascript

  var someKindOfProcess = function () {};

```

### BAD

```javascript

  var some_kind_of_process = function () {};

```

## Variable declarations

- **RULE**: Always declare variables at the *top* of functions.
- **REASON:**: Variable declarations are moved up to the top of the function scope anyway,
so that's where they belong.

### GOOD

```javascript

  function (a, b) {
      var k;

      if (a == b) {
          k = true;
      }
      ...
  }

```

### BAD

```javascript

  function (a, b) {
      if (a == b) {
          var k = true;
      }
      ...
  }

```

## Functions

- **RULE**: Anonymous functions **should** have a space between the `function` keyword and the left parenthesis.
- **REASON**: To emphasise the lack of the anonimity and differentiate them with named functions.

### GOOD

```javascript

  function (a, b) {}

```

### BAD

```javascript

  function(a, b) {}

```

- **RULE**: Named functions **should not** have a space between the function name and the left parenthesis.
- **REASON**: See above.

### GOOD

```javascript

  function add(a, b) {}

```

### BAD

```javascript

  function add (a, b) {}

```

## Semicolons

- **RULE**: Semicolons `;` **must** be added at the end of every statement, **except** when preceding a closing bracket `}`.
- **REASON**: That's what Jesus would have wanted.

### GOOD

```javascript

  var f = function add(a, b) {
      if (a == b) { return a * 2 } // No `;` here.
      return a + b;
  };

```

### BAD

```javascript

  var f = function add (a, b) {
      if (a == b) { return a * 2; }
      return a + b
  }

```

## Braces

- **RULE**: Braces **must** be used in all circumstances.
- **REASON**: JavaScript uses braces to structure code.

### GOOD

```javascript

  if (x) { return true }

```

### BAD

```javascript

  if (x) return true;

```
```javascript

  if (x)
      return true;

```
- **RULE**: Braces **must never** be on a line of their own.
- **REASON**: It wastes screen space.

### GOOD

```javascript

  if (x) {
      return true;
  };

```

### BAD

```javascript

  if (x)
  {
    return true;
  }

```
```javascript

  if (x) {
      return true; }

```


