# Function

Указывает на `function` конструкцию.
Указывает на все объявления функций или методов класса.
В случае метода включает в себя все дочерние элементы, такие как:
- Определение возвращаемого типа
- Определение параметров функции
- Определение тела функции
- Модификаторы доступа

##### Пример

Xpath:
`method1()`

Кодовая база:
```php
<?php

namespace A\B;

class C {
    // start
    public function method1() {}
    // end
}
```

или

```php
function method1() {}
```

## Return type

Указывает на тип возвращаемого значения.

##### Пример

- `method1()[returnType]`
- `method1()[returnType][0]`

## Parameters

Указывает на принимаемые методом параметры.

##### Пример

- `method1()[parameters]`
- `method1()[parameters]$prop1`

## Body

Указывает на тип возвращаемого значения.

##### Пример

- `method1()[body]`
- `method1()[body]$variable`

