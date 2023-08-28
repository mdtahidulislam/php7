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

// remove data
unset($foods['drinks']);


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

## OOP-Inheritance
* inherit method & propertise to child
* override parents method & propertise in child
* use protected

## OOP-Abstract Class
-- Can't initiate class. It forces to use method during extends. Can override abstract methods
* use abstract keyword before class, method
* only keep method without body
* must define & use method body on extended class

## OOP-final keyword
-- can't override method
## OOP-static method & property
* static method & property can be accesed without initaing instance(object) of class
* use static keyword before property & method
* acsess property outside of class: ClassName::$propertyName
* acsess method outside of class: ClassName::$methodName()
* acsess inside class: self::$propertyName, self::$methodName()
* method override - can't override directly. needs to add static keyword
* parent method call - parent::methodname()
## OOP-Constant in Class
* declaration - const CONSTNAME = value
* access - const has the static scope: self::CONSTNAME (inside), ClassName::CONSTNAME (outside)
