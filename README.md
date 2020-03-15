# digitalRoot
Library for getting digital root from numbers and letters. 
You can also pass a array of inputs and get array of outputs.

The digital root of a positive integer is found by summing the digits of the integer. If the resulting value is a single digit then that digit is the digital root. If the resulting value contains two or more digits, those digits are summed and the process is repeated. This is continued as long as necessary to obtain a single digit.


## Install

Via Composer

``` bash
$ composer require "anuar/digitalroot"
```

## Usage examples

``` php
$digitalRoot = new \digitalRootSrc\digitalRootBuilder();

// You may pass strings or integers. The output will be converted to string.
$my_input = "23081996";

// Returns the digital root(single digit)
// Output: "2"
$digitalRoot->getDigitalRoot($my_input);

// Returns the digital root complete calculation
$digitalRoot->getDigitalRootCompleteCalculation($my_input);

// Pass array and returns array of digital roots.
// Output: ["2", "3"]
$digitalRoot->getdigitalRootBulkResult(['23081996','43434336'])
