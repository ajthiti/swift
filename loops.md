---
description: >-
  ลูป (Loop) คือ รูปแบบการทำงานซ้ำ
  ซึ่งชุดคำสั่งจะทำงานวนซ้ำตามจำนวนรอบหรือเงื่อนไขที่กำหนดไว้
  คำสั่งพื้นฐานสำหรับการทำซ้ำในภาษา Swift ประกอบด้วย for , while และ repeat
---

# Loops

### การใช้คำสั่ง for

คำสั่ง `for` จะถูกใช้เพื่อสั่งให้โปรแกรมทำคำสั่งที่อยู่ในบล็อก {...} ซ้ำตามจำนวนรอบที่กำหนด ซึ่งมักใช้คู่กับ Range Operator เพื่อระบุขอบเขตของการนับรอบผ่าน **ตัววนซ้ำ \(iterator\)** 

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

ในกรณีที่ต้องการเพิ่มสเต็ปการนับให้มีค่ามากกว่าหรือน้อยกว่า 1 สามารถทำได้ โดยใช้คำสั่ง `stride(from: to: by: )`

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

รวมทั้งสามารถกำหนดเงื่อนไขเพิ่มเติมในการทำงานได้โดยใช้คำสั่ง where

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

### การใช้คำสั่ง while



### การใช้คำสั่ง repeat

