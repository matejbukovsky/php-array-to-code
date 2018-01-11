# php-json-to-array
Convert JSON object to PHP array

## Usage
    require 'src.php';
    $json = '{  
       "hello":"world",
       "properties":{  
          "url":"https://github.com/matejbukovsky/php-json-to-array",
          "convert":true
       }
    }';
    var_dump(convert($json));
    
## RESULT
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
