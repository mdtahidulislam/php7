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

## Associative Array to String
``` PHP
$students = array(
    'name' => 'tahidul',
    'class' => 6,
    'roll' => 1
);
/**
* join method just convert value to string
* so it is not useable
*/
$studentsArrayToStr = join(', ', $students);
print_r($studentsArrayToStr);

// solution 1: serialize & unsexrialize
$studentsArrayToStr1 = serialize($students);
print_r($studentsArrayToStr1);

$studentsArrayToStrUnserial = unsexrialize($studentsArrayToStr1);
print_r($studentsArrayToStrUnserial);

// solution 2: json_encode & json_decode
$studentsArrayTojsonencode = json_encode($students);
print_r($studentsArrayTojsonencode);

$studentsArrayTojsonDecode = json_decode($studentsArrayTojsonencode, true);
print_r($studentsArrayTojsonDecode);
```
