---
description: >-
  ลูป (Loop) คือ รูปแบบการทำงานซ้ำ
  ซึ่งชุดคำสั่งจะทำงานวนซ้ำตามจำนวนรอบหรือเงื่อนไขที่กำหนดไว้
  คำสั่งพื้นฐานสำหรับการทำซ้ำในภาษา Swift ประกอบด้วย for loop และ while loop
---

# Loops

### For loop

คำสั่ง `for` จะถูกใช้เพื่อสั่งให้โปรแกรมดำเนินการตามคำสั่งที่อยู่ในบล็อก {...} แบบวนซ้ำตามจำนวนรอบที่กำหนดไว้ ซึ่งมักใช้คู่กับ Range Operator เพื่อระบุขอบเขตของการนับรอบการทำงานผ่าน **ตัววนซ้ำ (iterator)**&#x20;

![ผังงานของคำสั่ง for](<.gitbook/assets/Untitled Diagram-2 (1).png>)

ตัวอย่างการใช้คำสั่ง `for`

```swift
let count = 1...10
for i in count {
  print("Number is \(i)")
}


for number in 1...3 {
	print("Hello world! for round No. \(number)")
}


let message = "Hello, Thiti"
for char in message {
    print(char)
}


let minutes = 60
for tickMark in 0..<minutes {
    // render the tick mark each minute (60 times)
}


```

ในบางกรณี หากเราไม่จำเป็นต้องใช้งานค่าของตัววนซ้ำในการทำงานตามชุดคำสั่งใน Scope ของ {...} เราสามารถเขียนคำสั่งได้ ดังนี้

```swift
let base = 3
let power = 10
var answer = 1

for _ in 1...power {
    answer *= base   
}

print("\(base) to the power of \(power) is \(answer)")
```

การใช้คำสั่ง `stride(from: to: by: )` เพื่อการเพิ่มสเต็ปการนับ

```swift
for i in stride(from: 0, to: 50, by: 5) {
    print(i) 
}
// 0,5,10,15,20,25,30,35,40,45 


for j in stride(from: 50, to: 0, by: -5) {
    print(j)
}
// 50,45,40,35,30,25,20,15,10,5
```

การใช้คำสั่ง `where` เพื่อกำหนดเงื่อนไขเพิ่มเติมในการทำงาน

```swift
let programmingLanguages = ["Swift", "Java", "Obj-C", "JavaScript", "Kotlin", "Python"]
for language in programmingLanguages {
      print(language)
}
//Swift, Java, Obj-C, JavaScript, Kotlin, Python

for language in programmingLanguages where language.starts(with: "J") {
     print(language)
}
//Java, JavaScript
```

### While loop

คำสั่ง `while` จะถูกใช้เพื่อสั่งให้โปรแกรมดำเนินการตามคำสั่งที่อยู่ในบล็อก {...} แบบวนซ้ำ จนกว่าเงื่อนไขที่กำหนดจะมีค่าเป็นเท็จ (false) ซึ่งมีการใช้งานอยู่ 2 รูปแบบ คือ `while` และ `repeat...while`

![ผังงานของคำสั่ง while และ repeat ... while](<.gitbook/assets/Untitled Diagram-3 (1).png>)

ตัวอย่างการใช้คำสั่ง `while`

```swift
var currentLevel: Int = 0
var finalLevel: Int = 5

while (currentLevel <= finalLevel) {
    if (finalLevel >= currentLevel) {
        print("You have play in level \(currentLevel)")
        currentLevel += 1
    }
}

print("outside of while loop")
```

ตัวอย่างการใช้คำสั่ง `repeat...while`

```swift
var currentLevel: Int = 0
var finalLevel: Int = 5

repeat {
    if (currentLevel <= finalLevel) {
        print("You have play in level \(currentLevel)")
        currentLevel += 1
    }
} while (currentLevel <= finalLevel)

print("outside of while loop")
```

### คำสั่ง Continue

คำสั่ง `continue` เป็น **Control Transfer Statements** ที่ใช้เพื่อบอกให้ loop หยุดและเริ่มต้นรอบใหม่อีกครั้ง ตัวอย่างเช่น

```swift
var intialLevel: Int = -5, 
var finalLevel: Int = 2
var currentLevel: Int = intialLevel

while currentLevel < finalLevel {
    if intialLevel < 0 {
        print("Starting level must be positive")
        intialLevel = 0
        currentLevel = intialLevel
        continue //หยุดการทำงานและเริ่มต้นรอบใหม่
    }
    currentLevel += 1
    print("next level")
}

print("outside of while loop")

//Starting level must be positive
//next level
//next level
//outside of while loop
```

### คำสั่ง break

คำสั่ง `break` เป็น **Control Transfer Statements** ที่ใช้เพื่อบอกให้หยุดการทำงานและกระโดดออกจาก Loop ทันที ตัวอย่างเช่น&#x20;

```swift
var currentLevel:Int = 1
var finalLevel:Int = 2
var isLifeAvailable = true

while (isLifeAvailable) {
    
    if currentLevel > finalLevel {
        print("Game Completed. No level remaining")
        break //หยุดการทำงานและกระโดดออกจาก Loop
    }
    //play game and go to next level
    currentLevel += 1
    print("next level")
}

print("outside of while loop")
//next level
//next level
//Game Completed. No level remaining
//outside of while loop
```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language (Swift 5.2 beta)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-2-beta/id1002622538), Apple Inc., 2020
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.



{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง**\
**ผู้เขียน** ธิติ ธีระเธียร  \
**วันที่เผยแพร่**  วันที่ 9 กุมภาพันธ์ 2563\
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/loops](https://ajthiti.gitbook.io/swift/loops)\
**เงื่อนใขในการใช้งาน**\
****This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}
