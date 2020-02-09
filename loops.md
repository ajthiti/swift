---
description: >-
  ลูป (Loop) คือ รูปแบบการทำงานซ้ำ
  ซึ่งชุดคำสั่งจะทำงานวนซ้ำตามจำนวนรอบหรือเงื่อนไขที่กำหนดไว้
  คำสั่งพื้นฐานสำหรับการทำซ้ำในภาษา Swift ประกอบด้วย for loop และ while loop
---

# Loops

### For loop

คำสั่ง `for` จะถูกใช้เพื่อสั่งให้โปรแกรมดำเนินการตามคำสั่งที่อยู่ในบล็อก {...} แบบวนซ้ำตามจำนวนรอบที่กำหนดไว้ ซึ่งมักใช้คู่กับ Range Operator เพื่อระบุขอบเขตของการนับรอบการทำงานผ่าน **ตัววนซ้ำ \(iterator\)** 

![&#xE1C;&#xE31;&#xE07;&#xE07;&#xE32;&#xE19;&#xE02;&#xE2D;&#xE07;&#xE04;&#xE33;&#xE2A;&#xE31;&#xE48;&#xE07; for](.gitbook/assets/untitled-diagram-2%20%281%29.png)

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

คำสั่ง `while` จะถูกใช้เพื่อสั่งให้โปรแกรมดำเนินการตามคำสั่งที่อยู่ในบล็อก {...} แบบวนซ้ำ จนกว่าเงื่อนไขที่กำหนดจะมีค่าเป็นเท็จ \(false\) ซึ่งมีการใช้งานอยู่ 2 รูปแบบ คือ `while` และ `repeat...while`

![&#xE1C;&#xE31;&#xE07;&#xE07;&#xE32;&#xE19;&#xE02;&#xE2D;&#xE07;&#xE04;&#xE33;&#xE2A;&#xE31;&#xE48;&#xE07; while &#xE41;&#xE25;&#xE30; repeat ... while](.gitbook/assets/untitled-diagram-3%20%281%29.png)

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

