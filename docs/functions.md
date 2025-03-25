# Function

Указывает на `function` конструкцию.
Указывает на все объявления функций или методов класса.
В случае метода включает в себя все дочерние элементы, такие как:
- Определение возвращаемого типа
- Определение параметров функции
- Определение тела функции
- Модификаторы доступа

### Contexts

- [Namespace](namespaces.md)
- [Classes](classes.md)

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


## Targeting

Ссылка на `function` указывает только на определение функции, которое находится внутри контекста.

File 1:
```
src/Utils/Std.php
```
Content:
```php
<?php

namespace App\Utils;

class Std {
  public function time() {}
}
```

File 2:
```
src/functions.php
```
Content:
```php
<?php

namespace App;

function time() {}
```

Function `time()` будет указывать на три функции:
- \App\Utils\Std::time()
- \App::time()
- time()

В контексте `\App`, функция `time()` будет указывать только на 1 функцию, внутри `src/functions.php`
В контексте `\App\Utils`, функция `time()` будет указывать только на 1 функцию, внутри класса `Std` в файле `src/Utils/Std.php`
В контексте `\`, функция `time()` будет указывать только на 1 функцию из стандартной библиотеки.
