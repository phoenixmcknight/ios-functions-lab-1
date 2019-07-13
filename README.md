# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(x:Double ) -> Double {
let Cost = x + nyTax
return Cost

}
var TotalCost = totalWithTax(x: itemCost)
print(TotalCost)

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(x:Int ) -> Int {
let Cost = x + Int(nyTax)
return Cost

}
var TotalCostAfterTax = totalWithTax(x: Int(itemCost))
print(TotalCostAfterTax)


## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
func HowIsItOutside (x: Int) -> String {
let Warm = ("It's really warm.")
let Cold = ("It's cold out.")
if x >= 85 {
return Warm
} else if x <= 40 {
return Cold
} else {
return "Weather is moderate."

}

}

var WhatIsItLike = HowIsItOutside(x: 72)
print(WhatIsItLike)

## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

func min2(a: Int, b: Int) -> Int {

if a < b {
return a
} else {
return b
}
}
var ThisIsTheSmallestNumber = min2(a: 1, b: 2)
print(ThisIsTheSmallestNumber)

## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

func lastDigit(_ number: Int) -> Int {
return number % 10
}
var LastDigit1 = lastDigit(12345)
print(LastDigit1)


## Question 5

Write a function that takes in any two positive integers and return the sum.

func Sum (x: Int, y: Int) -> Int {
var result = 0
if x > 0 && y > 0 {
result = x + y
}
return result
}
var sum1 = Sum(x: 1, y: 2)
print(sum1)


## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

func grades (x: Int) -> String {
switch x {
case 100:
return "A+"
case 90...99:
return "A"
case 80...89:
return "B"
case 70...79:
return "C"
case 65...69:
return "D"

default:
return "F"
}
}
let grade = grades(x: 45)
print(grade.uppercased())


## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

func calculator (num1:Int, Num2:Int,Operator:String) -> Int? {
var answer = 0
switch Operator {
case "+":
answer = num1 + Num2
case "-":
answer = num1 - Num2
case "x":
answer = num1 * Num2
case "/":

answer =  num1 / Num2
default:
return nil
}
return answer
}

let answer1 = calculator(num1: 0, Num2: 5, Operator: "/")
print(answer1!)


## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

let myFinalCost = totalWithTip() //Fill in the arguments
```

let mealCost = 45
let tipPercentage = 0.15
func totalWithTip (x:Double) -> Double {
let Total =  Double(mealCost) + Double(tipPercentage)
return Total
}
var myFinalCost = totalWithTip(x: 45)
print(myFinalCost)


Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

let myFinalCostWithTipAndTax = totalWithTipAndTax() //Fill in the arguments in function
```

let mealCost = 45
let tipPercentage = 0.15
let taxPercentage = 0.09
func totalWithTip (x:Double) -> Double {
let Total =  Double(mealCost) + Double(tipPercentage) + Double(taxPercentage)
return Total
}
let myFinalCostWithTipAndTax = totalWithTip(x: 45)
print(myFinalCostWithTipAndTax)
## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

func repeatPrint (message: String, count: Int) -> String {
let message1 = String(repeating: message, count: count)
return message1
}
let RepeatPrint2 = repeatPrint(message: "+", count: 10)
print(RepeatPrint2)


## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

var number = [Int]()
func first(_n:Int) -> [Int] {
for num in 1..._n {
number.append(num)
}
return number
}
let output = first(_n: 3)
print(output)

## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)

func numbers (num:Int)  {
for n in 1...num {
if n % 3 == 0 && n % 5 == 0  {
print("FizzBuzz")

} else if n % 5 == 0 {
print("Buzz")

} else if n % 3 == 0 {
print("Fizz")

} else {
print(n)
}
}
}
let numbers1 = numbers(num: 15)
print(numbers1)

## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

func reverse (numbers:[Int]) -> [Int] {
var numbers1 = [Int]()
for num in numbers {
numbers1 = [num] + numbers1
}

return numbers1
}
let numbers2 = reverse(numbers: [1,2,3])
print(numbers2)


## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.

func mostFrequentInt(in arr: [Int]) -> Int {
var frequencyDict = [Int: Int]()
for num in arr {
//if we haven't seen it (1) else whatever it was before + 1
if let currentValue = frequencyDict[num] {
frequencyDict[num] = currentValue + 1
} else {
frequencyDict[num] = 1
}
}
var mostFrequent = (number: -1, occurances: -1)
for (number, occurances) in frequencyDict {
if occurances > mostFrequent.occurances {
mostFrequent = (number, occurances)
}
}
return mostFrequent.number
}

print(mostFrequentInt(in: [4,2,5,2,4,2,4,5,2,1,1,1,1,1,1]))


## Question 14

Write a function that sums all the even indices of an array of Ints.

func sumEven (s: [Int]) -> [Int] {
var sum1 = [Int]()
for sum in s where sum % 2 == 0 {
sum1.append(Int(sum))
}
return sum1
}
let sumEven1 = sumEven(s:[1,2,3,4,5,6])
print(sumEven1.reduce(0,+))


## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`


## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

## Question 17

Write a function that determines if a value is inside of array.

func value (x:[Int]) -> [String] {
var myArray: [Int] = [1,2,3,4,5]
var Truth = [String]()
for num in myArray  {
if [num] == x {
Truth = ["\(x.first!) is inside of the array."]
} else {
Truth = ["\(x.first!) is not inside the array"]
}
}
return Truth
}
let myNew = value(x: [7])
print(myNew)

## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

let dieRoll = Int(arc4random_uniform(6) + 1)
func EvenOrOdd (x:Int) -> Bool {

var value1 = Bool()
if x % 2 == 0 {
value1 = true
} else if x % 2 != 0 {
value1 = false
}
return value1
}
let EvenOrOdd2 = EvenOrOdd(x: dieRoll)
print(EvenOrOdd2)


## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

func min2(a: [Int]) -> Int {
var value = 0
a.sorted()
value = a.sorted().last!


return value
}
var ThisIsTheBiggestNumber = min2(a:[11,12,5,4,3,10])
print(ThisIsTheBiggestNumber)

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]
func min2(a: [Int]) -> Int {
var value = 0
a.sorted()
value = a.sorted().last!


return value
}
var ThisIsTheBiggestNumber = min2(a:myArray)
print("\(ThisIsTheBiggestNumber) is the biggest number")

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]
func min2(a: [Int]) -> String {
var value = 0
a.sorted()
value = a.sorted().last!
if value % 2 == 0 {
return ("\(value) is even")
} else {
return("\(value) is odd")
}


}
var ThisIsTheBiggestNumber = min2(a:myArray)
print("The largest number \(ThisIsTheBiggestNumber).")

## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."
func characters (x:String) -> Int {
var characters1 = String()
for i in x where i != " " {
characters1.append(i)
}
return characters1.count
}
let CharactersFunc = characters(x: myString)
print(CharactersFunc)


## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```

Sample output: `3`

let testString = "This is a test string for your code"

func match(a:String) -> Int {
var count = 0
let targetCharacter: Character = "i"

for i in a {
if i == targetCharacter {
count += 1
}

}
return count
}
let match1 = match(a: testString)
print(match1)


## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```

Output: `13`

let inputString = "This one is a little more complicated"

func match(a:String) -> Int {
var count = 0
let targetCharacters: [Character] = ["a","e","i","o","u"]
for c in targetCharacters {
for i in a {
if i == c {
count += 1
}

}
}
return count

}
let match1 = match(a:inputString )
print(match1)


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.

let inputArray2 = [3,1,4,1,3,2,6,1,9]
func unique (a:[Int]) -> Int {

var unique1 = Set(a)
print(a)
print(unique1.sorted())


return unique1.count



}
var unique1 = unique(a: inputArray2)
print(unique1)


## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

func binary(arr:[Int]) -> Decimal {
    var index = 0
    var empty = Decimal()
    for x in arr {
        empty += Decimal(x) * pow(2,index)
        index += 1
        
    }
    return empty
}
let binary2 = binary(arr: [1,0,1,1,1,0,1])
print(binary2)



## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`

func timedifference (firstHour firstHour:Int, firstMinute firstMinute:Int, secondHour secondHour:Int, secondMinute secondMinute:Int) -> String {
var firstTime = 0
var secondTime = 0
if firstHour < 24 && firstMinute < 60 && secondHour < 24 && secondMinute < 60 {
firstTime = (firstHour * 60) + firstMinute
secondTime = (secondHour * 60) + secondMinute
return String(abs(firstTime - secondTime))
} else {
return "invalid time entry"
}
}
let time = timedifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)
print("the result is \(time) minutes")

## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

func filterOdd(arr:[Int]) -> [Int] {
var evenArray = [Int]()
for i in arr {
if i % 2 == 0 {
evenArray.append(i)
}
}
return evenArray
}
let evenNumbers = filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])
print(evenNumbers)


## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

func doubleIt(arr:[Int]) -> [Int] {
var empty = [Int]()
for x in arr {
empty.append(x*2)

}
return empty
}

let DoubleIt2 = doubleIt(arr: [1, 2, 3, 4])
print(DoubleIt2)


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

func MultiplyIt(arr:[Int], n:Int) -> [Int] {
var empty = [Int]()
for x in arr {
empty.append(x*n)

}
return empty
}

let MultiplyIt2 = MultiplyIt(arr: [1, 2, 3, 4], n:4)
print(MultiplyIt2)


## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

func unwrap(arr:[Int?]) -> [Int] {
var empty = [Int]()
for n in arr where n != nil {
empty.append(n!)

}
return empty
}

let unwrap2 = unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])
print(unwrap2)


## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`


## Question 31

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`


## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)

func reverse(rev1:String) -> String {

var string2 = ""
var answer = ""
for num in rev1 {
string2 = String(num) + string2
if string2.lowercased() == rev1.lowercased() {
answer = "\(rev1) is a palindrome."
} else {
answer = "\(rev1) is not a palindrome."
}
}
return answer
}

let palindrome = reverse(rev1: "racecar")
print(palindrome)

## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)

func pangram(rev1:String) -> String {
let alphabet = "abcdefghijklmnopqrstuvwxyz"
var answer = ""
let alphabet2 = Set(alphabet)
if  Set(rev1).isSubset(of: alphabet2) {
answer = "\"\(rev1)\" is a pangram"
} else {
answer = "\"\(rev1)\" is not a pangram"
}
return answer
}
let pangram1 = pangram(rev1: "The dog walks around the park every day.")
print(pangram1)


## Question 34

Write your own `min()` and `max()` functions for an Array of Ints

MIN 
func min(array:[Int]) -> Int {
var empty = [Int]()
for num in array {
empty.append(num)
}
return empty.sorted().first!
}
let min1 = min(array: [10,2,3,4,5,6,7,8,1])
print(min1)

MAX

func Max(array:[Int]) -> Int {
var empty = [Int]()
for num in array {
empty.append(num)
}
return empty.sorted().last!
}
let Max1 = Max(array: [10,2,3,4,5,6,7,8,1])
print(Max1)

## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.

func common(array1:[Int],array2:[Int]) -> [Int] {
var empty = [Int]()
empty += Set(array1).intersection((Set(array2)))
return empty
}
let common2 = common(array1: [1,2,3,5,8,10], array2: [2,5,7,10])
print(common2)



## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.


## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`
