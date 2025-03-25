# Namespace

Указание на `namespace` конструкцию.
Указывает на всё выражение `namespace`, включая все его дочерние элементы.

### Contexts

Empty.

##### Пример

Xpath:
```
\A\B
```

Кодовая база:
```php
<?php

// start
namespace A\B;

class C {}
// end
```

или

```php
<?php

// start
namespace A\B {
    class C {}
}
// end
```

## Targeting

Ссылка на `namespace` указывает только на область, которую описывает ключевое слово `namespace`.

##### Пример

File 1:
```
src/Controller/A.php
```
Content:
```php
<?php

namespace App\Controller;

class A {}
```

File 2:
```
src/Controller/B.php
```
Content:
```php
<?php

namespace App\Controller;

class B {}
```

Namespace `\App\Controller` будет указывать на два пространства имен в обоих файлах.
