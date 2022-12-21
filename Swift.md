## Types
* Int: An integer number
  * var highScore: Int = 0
* Float: 32 bit floating point number (6 decimal places)
  * Ex. 2.4, 3.14
* Double: 64 bit floating point number (15 decimal places)
  * var precentComplete: Double = 0.76
* String: Textual Data
  * var userThought: String = "I hope this course is good."
* Boolean: True/False
  * var isDarkModeOn: Bool = true
* Character: a 16 bit Unicode chracter
  * Ex. "s"
* Swift Inference: If you don't specify the type of value you need, Swift uses type inference to work out the appropriate type. Type inference enables a compiler to deduce the type of a particular expression automatically when it compiles your code, simply by examining the values you provide. 
  * var myName = "Sean"
  * var highScore = 0

## Variables & Constants
* They capture a value so you can use that value throught your code base.
* Variable: Can be changed
  * var highScore = 0
    * highScore = 55
* Constant: Defined as a fixed value, cannot be changed 
  * let highScore = 0

## Array
* Containter or list of objects
* 0 index 
  * var ages: [Int] = []
```swift
  var ages = [21, 55, 19, 47, 22, 37, 88]
  
  ages.count 
  ages.first        //prints 21
  ages.last         //prints 88
  ages[4] 
  
  ages.append(99)
  ages 
  print(ages)       //[21, 55, 19, 47, 22, 37, 88, 99]
  
  ages.append(99)
  ages.sort()
  ages.reverse()
  ages.shuffle()
  print(ages)

```

## Set
* Similiar to an array, collection of items
* Unordered and No duplicates 
* Has better performance speed than arrays
```swift
var ages = [21, 55, 21, 43, 23]

//var agesSet: Set<Int> = []

var agesSet = Set(ages)
print(agesSet) // [55, 23, 43, 21]
```

