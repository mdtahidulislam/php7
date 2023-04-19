# PHP7

## Associative Array
``` php

$foods = array(
    'veg' => 'alu, potol',  
    'drinks' => 'coc, 7up'
);

// get full array
print_r($foods);

// get single elem
echo $foods['veg'];

// add items
$foods['drinks'] .= ', sprite, water';
echo $foods['drinks'];


// foreach loop
foreach($foods as $key => $val) {
    echo $key .'='. $val."\n";
};

// for loop by key/value
$keys = array_keys($foods);
print_r($keys);
$numKeys = count($keys);

for($i=0; $i<$numKeys; $i++) {
    $key = $keys[$i];
    echo $foods[$key]."\n";
};
```

## String to Array & Array to String
* str to array: explode(delimeter, string);
* str to array: preg_split(delimeter, string);
* array to str: join(delimeter, array);

