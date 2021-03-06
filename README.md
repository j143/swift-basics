# swift-basics
Some basic operations in Swift

```swift
print("Hello from Swift!")
```

### Values

```swift
var myVariable = 70
myVariable = 80
let myConstant = 24
```

Type does not need to be specified explicitly.

```swift
let implicitInt = 12
let implicitDouble = 21.2
let explicitDouble: Double = 23
```

Type conversion does not happen implicitly, we need
to make instances explicitly for the desired type.


```swift
let info = "The distance of moon "
let distance = 1000000000000
print(info + String(distance))
```

And for simpler way to include values in strings

```swift
let planets = 9
let subplanets = 12
print("There are more than \(planets) planets.")
print("There are more than \(planets + subplanets) celestial objects.")
```

Multiline quotation

```swift
let quotation = """
  Even though there's whitespace to the left,
  the actual lines have no indentation.
    of course, this line will have it.
  Double quotes can be used
  """
  
print(quotation)
```

Lists and key-value pairs

```swift
var plants = ["rose", "tulip", "neem", "meswak"]
plants[1] = "A frangranced flower"

var marks = [
  "Kate": "23",
  "Mahi": "27",
]

marks["Deepti"] = "26"
print(marks)
```

Operations over lists

```swift
plants.append("spring")
print(plants)
```

```swift
let emptyArray = [String]()
let emptyDictionary = [String: Float]()
```

### Control Flow

`for`, `while`, `repeat-while` to make loops and
`if` and `switch` as conditionals

```swift
let playerScores = [12, 12, 20, 35]
var teamScore = 0

for score in playerScores {
  if score > 20 {
    teamScore += 2
  } else {
    teamScore += 1
  }
}

print(teamScore)
```

And optional values?

```swift
var optionalName: String? = "Menhan Crest"
var greeting = "Hi!"
if let name = optionalName {
  greeting = "Hello, \(name)"
}

print(greeting)
```

### Functions and closures

`func` to declare a function. `->` used to separate parameter
names and types from the function return type.

```swift
func wish(name: String, event: String) -> String {
  return "Hi \(name), Happy \(event)."
}

print(wish(name: "Kiran", event: "Birthday"))
```

tuples

```swift
func findStats(points: [Int]) -> (min: Int, max: Int, sum: Int) {
  var min = points[0]
  var max = points[0]
  var sum = 0
  
  for score in points {
    if score > max {
      max = score
    } else if score < min {
      min = score
    }
    sum += score
  }
  
  return (min, max, sum)
}

let stats = findStats(points: [7, 20, 72, 1])
print(stats.sum)
print(stats.2)
```


Nested functions

```swift
func addition() -> Int {
  var x = 12
  func add() {
    x += 1
  }
  add()
  return x
}

print(addition())
```
