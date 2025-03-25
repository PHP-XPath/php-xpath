### Namespace

Указание на `namespace` конструкцию.
Указывает на всё выражение `namespace`, включая все его дочерние элементы.

##### Пример

Xpath:
`\A\B`

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
