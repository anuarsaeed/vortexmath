# digitalRoot
Library for getting digital root from numbers and letters. 
You can also pass a array of inputs and get array of outputs, give letters numeric value and get their digital root.

The digital root of a positive integer is found by summing the digits of the integer. If the resulting value is a single digit then that digit is the digital root. If the resulting value contains two or more digits, those digits are summed and the process is repeated. This is continued as long as necessary to obtain a single digit.

I am going to add additional functionality to this library in the future. Open to any new ideas.
## Install

Via Composer

``` bash
$ composer require "anuar/digitalroot"
```

## Usage examples

``` php
$digitalRoot = new \digitalRootSrc\digitalRootBuilder();

// You may pass strings or integers. The output will be converted to string type.
$my_input = "23081996";

// Returns the digital root(single digit).
// Output: [
//            "client_input" => "23081996",
//            "digital_root" => "2"
//         ]
$digitalRoot->getDigitalRoot($my_input);

// Returns the digital root complete calculation.
// Output: [
//            "client_input" => "23081996",
//            "digital_root" => "2",
//            "digits" => [2,5,5,4,5,5,5,2],
//            "numeric" => "25545552"
//         ]
$digitalRoot->getDigitalRootCompleteCalculation($my_input);

// Pass array and returns array of digital roots.
// Output: ["2", "3"]
$digitalRoot->getdigitalRootBulk(["23081996","43434336"]);

// You can also give letters numeric value and get their digital root.
// Then you need to pass second parameter which gives each letter numeric value.
// Output: [
//            'client_input' => "abc12",
//            'digital_root' => "9"
//         ]
$digitalRoot->getDigitalRoot("abc12", ["A" => 1, "B" => 2, "C" => 3]);
