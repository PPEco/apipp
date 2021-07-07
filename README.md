# ApiPP
Library to simplify writing API

## Installation
```shell
composer require ppeco/apipp
```

## Example
```php
use apipp\ApiPP;

require_once "vendor/autoload.php";

ApiPP::create()
    ->method("hello_world", function(ApiPP $apiKit) {
        return "Hello, world!";
    })
    ->method("hwp", function(ApiPP $apiKit) {
        [$someKey] = $apiKit->get(["key"]);
        return "Key: $someKey";
    })
    ->start();
```
