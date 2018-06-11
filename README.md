# php-json-to-array-to-code
Convert JSON object to PHP array or render array as PHP code

## Usage
```php
require 'src.php';
$json = '{  
   "hello":"world",
   "properties":{  
      "url":"https://github.com/matejbukovsky/php-json-to-array",
      "convert":true
   },
   "test": ["first", "second", 0]
}';
```
## Return PHP code
```php
echo getCode(json_decode($json, TRUE));

[
    "hello" => "world",
    "properties" => [
        "url" => "https://github.com/matejbukovsky/php-json-to-array",
        "convert" => TRUE,
    ],
    "test" => [
        0 => "first",
        1 => "secons",
        2 => 0,
    ],
];
```
## Demo
[phpFiddle](http://phpfiddle.org/main/code/d6hy-8q53)
