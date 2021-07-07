# apikit
Kit for api servers

## Installation
```
composer require ppeco/apipp
```

## Example
```php
use levkopo\apikit\ApiKit;
ApiKit::create()
    ->method("hello_world", function(ApiKit $apiKit) {
        return "Hello, world!";
    })
    ->method("hwp", function(ApiKit $apiKit) {
        [$someKey] = $apiKit->params(["key"]);
        return "Key: $someKey";
    })
    ->start();
```
