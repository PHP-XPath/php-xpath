# Class

Указывает на `class` конструкцию.
Указывает на всё объявление `class`, включая все его дочерние элементы.

### Contexts

- [Namespace](namespaces.md)

##### Пример

Xpath:
`C`

Кодовая база:
```php
<?php

namespace A\B;

// start
class C {}
// end
```

или

```php
<?php

namespace A\B {
    // start
    class C {}
    // end
}
```

## Methods

Указывает на все методы внутри класса, удовлетворяющие фильтрам.

##### Пример

- `C[methods]`

## Properties

Указывает на все свойства внутри класса, удовлетворяющие фильтрам.

##### Пример

- `C[properties]`

## Constants

Указывает на все константы внутри класса, удовлетворяющие фильтрам.

##### Пример

- `C[constants]`

## Targeting

Ссылка на `class` указывает только на определение класса, которое находится внутри контекста.


File 1:
```
src/Domain/Auth/User.php
```
Content:
```php
<?php

namespace Domain\Auth;

class User {}
```

File 2:
```
src/Domain/Forum/User.php
```
Content:
```php
<?php

namespace Domain\Forum;

class User {}
```

Class `User` будет указывать на два класса в обоих `namespace`.

В контексте `\Domain\Auth`, класс `User` будет указывать только на 1 класс.
Полная запись будет определяться конкатенацией через обратную косую черту: `\Domain\Auth\User`.
