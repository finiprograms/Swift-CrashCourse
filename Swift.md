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
* Has better performance speed than arrays (fast inserstion, lookup, deletion)
```swift
var ages = [21, 55, 21, 43, 23]

//var agesSet: Set<Int> = []

var agesSet = Set(ages)
print(agesSet) // [55, 23, 43, 21]

agesSet.insert(101)
agesSet.contains(101) // True //Constant Time LookUp
print(agesSet)
```
* In order for something to go in a Set it has to conform to **hashable**. 
 * Basic Swift types automatically conform to Hashable.
 * It comes into play when creating your own types Ex. var sean: Person = Person(named: "Sean")
 * 
* **Hashable:** A protocol that provides a **hashValue** to our object. **The hashValue** is used to compare two instances. 

## Dictionary
* A collection whose elements are key-value pairs
* A type of hash table, providing fast access to the entries it contains
 ** Each entry in the table is identified using its key, which is a hashable type such as a string or number. You use that key to retrieve the corresponding value, which can be any object
```swift
let devices: [String: String] = [
    "phone": "iphone",
    "laptop": "2016 MacBook Pro",
    "tablet": "2018 iPad Pro",] //key: value

    devices["laptop"]   //2016 Macbook Pro //Constant Time LookUp
```

## Functions
* Functions are self-contained chunks of code that perform a specific task. 
* You give a function a name that identifies what it does, and this name is used to “call” the function to perform its task when needed.

```swift
func printInstructors(name: String) {
    print(name)
}

printInstructors(name: "Joe")

func add(firstNumber: Int, to secondNumber: Int) -> Int {
   
    let sum = firstNumber + secondNumber
    return sum
}

add(firstNumber: 18, to: 216) //call site

func add(firstNumber: Int, secondNumber: Int) -> Int {
   
    let sum = firstNumber + secondNumber
    return sum
}

add(firstNumber: 18, secondNumber: 12) //call site
```

## if/else
* The if/else statement executes a block of code if a specified condition is true. If the condition is false, another block of code can be executed.
```swift
var isDarkModeOn = true
if isDarkModeOn == true {
    print("That's how it should be.")
}

if isDarkModeOn {
    print("That's how it should be.")
} else {
    print("You are a psycho")
}

var myHighScore = 555
var yourHighScore = 444

if myHighScore > yourHighScore {
    print("I win")
} else {
    print("You win")
}

var highscore = 111
if highscore > 500 {
    print("You're the best")
} else if highscore > 250 {
    print("You're average")
} else if highscore > 100 {
    print("You need improvement")
} else {
    print("Yikes")
}
```
## For
* A for loop is used for iterating over a collection (that is either a list, a tuple, a dictionary, a set, or a string) or doing something x number of times
```swift
let allStars = ["James", "Davis", "Harden", "Doncic", "Leonard"]

for player in allStars {
    print(player)
}

for i in 0..<25 { //0-24
    print(i)
}

var randomInts: [Int] = []

for _ in 0..<25 {
    let randomNumber = Int.random(in: 0...100) //runs 25 times
    randomInts.append(randomNumber)
}

print(randomInts)
```
## enum (enumerations)
* A group of values that are related 
* Raw values can be strings, characters, or any of the integer or floating-point number types. Each raw value must be unique within its enumeration declaration.
```swift
enum Phone {
    case iphone11Pro
    case iphoneSE
    case pixel
    case nokia
}

func getBrandonsOpinion(on phone: Phone){
    if phone == .iphone11Pro {
        print("This will be my next phone.")
} else if phone == .iphoneSE {
        print("I dislike this phone size. It makes design hard")
} else if phone == .pixel {
        print("Hardware is great, android is no no")
} else {
    print("Can't be broken. Classic.")
}
}

getBrandonsOpinion(on: .iphone11Pro)

enum Phone: String {
    case iphone11Pro = "This will be my next phone."
    case iphoneSE = "I dislike this phone size. It makes design hard"
    case pixel = "Hardware is great, android is no no"
    case nokia = "Can't be broken. Classic."
}

func getBrandonsOpinion(on phone: Phone){
    print(phone.rawValue) 
}

    getBrandonsOpinion(on: .iphone11Pro)
```
## Swit
