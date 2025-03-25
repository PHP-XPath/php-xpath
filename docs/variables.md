# Variable

Указывает на `variable` конструкцию.
Указывает на все объявления переменных или свойств класса.
В случае свойства включает в себя все дочерние элементы, такие как:
- Определение типа
- Определение значения по умолчанию
- Модификаторы доступа

### Contexts

- [Namespace](namespaces.md)
- [Classes](classes.md)
- [Functions](functions.md)
  - [Parameters](functions.md#parameters)
  - [Body](functions.md#body)

##### Пример

Xpath:
`$prop1`

Кодовая база:
```php
<?php

namespace A\B;

class C {
    // start
    public $prop1 = 'foo';
    // end
    public $prop2 = 1;
}
```

или

```php
$prop1 = 5;
```

## Declared type

Указывает на определение типа свойства.

##### Пример

- `$prop1[type]`

## Default value

Указывает на определение значения свойства по умолчанию.

##### Пример

- `$prop1[defaultValue]`
