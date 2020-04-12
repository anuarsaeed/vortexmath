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

// Returns the digital root(single digit).
// Output: [
//            "client_input" => "23081996",
//            "digital_root" => "2"
//         ]
$digitalRoot->getDigitalRoot("23081996");


// Returns the digital root complete calculation.
// Output: [
//            "client_input" => "299493218",
//            "digital_root" => 2,
//            "digital_root_from" => "Summary from splitting double digit value and adding both digits togather."
//            "full_calculation" => [
//                "string" => "2 9 11 1 1 2 9 11 1 1 2 4 6 9 15 1 5 6 3 9 2 11 1 1 2 1 3 8 11 1 1 2",
//                "array" => [2,9,11,1,1,2,9,11,1,1,2,4,6,9,15,1,5,6,3,9,2,11,1,1,2,1,3,8,11,1,1,2]
//            ],
//            "single_digit_summaries" => [
//                "string" => "6 9 3",
//                "array" => [6,9,3]
//            ],
//            "double_digit_summaries" => [
//                "string" => "11 11 15 11 11",
//                "array" => [11,11,15,11,11]
//            ],
//            "double_digit_summaries_separated_digits" => [
//                "string" => "1 1 1 1 1 5 1 1 1 1",
//                "array" => [1,1,1,1,1,5,1,1,1,1]
//            ],
//            "double_digit_summaries_separated_digits_summaries" => [
//               "string" => "2 2 6 2 2",
//               "array" => [2,2,6,2,2]
//            ],
$digitalRoot->getDigitalRootCompleteCalculation("299493218");


// Pass array and returns array of digital roots.
// Output: [
//           "23081996' => "2",
//           "43434336" => "3"
//         ]
$digitalRoot->getdigitalRootBulk(["23081996","43434336"]);


// You can also give letters numeric value and get their digital root.
// Then you need to pass second parameter which gives each letter numeric value.
// Output: [
//            'client_input' => "abc12",
//            'digital_root' => "9"
//         ]
$digitalRoot->getDigitalRoot("abc12", ["A" => 1, "B" => 2, "C" => 3]);
