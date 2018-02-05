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
## Convert stdClass (decoded JSON) object to PHP array
```php
var_dump(convert($json));
    
array(2) {
  ["hello"]=>
  string(5) "world"
  ["properties"]=>
  array(2) {
    ["url"]=>
    string(50) "https://github.com/matejbukovsky/php-json-to-array"
    ["convert"]=>
    bool(true)
  }
}
```
## Return PHP code
```php
echo getCode(convert($json));

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
[phpFiddle](http://phpfiddle.org/main/code/5t9v-rxnf)
