# ApiPP
Library to simplify writing API

## Installation
```
composer require ppeco/apipp
```

## Example
```php
use apipp\ApiPP;

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
