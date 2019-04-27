---
description: >-
  ตัวดำเนินการเป็นเครื่องหมายหรือกลุ่มของเครื่องหมายที่ใช้ในการทำการอย่างใดอย่างหนึ่ง
  เช่น การกำหนดค่า การประมวลผลทางคณิตศาสตร์ หรือการเปรียบเทียบทางตรรกะ เป็นต้น
---

# Operators

**ตัวดำเนินการ \(Operator\)** คือ สัญลักษณ์ที่ใช้ในคำสั่งหรือนิพจน์เพื่อกำหนดกระบวนการการทำงานของโปรแกรม ในการเขียนโปรแกรม เราสามารถใช้ตัวดำเนินการเพื่อทำสิ่งต่างๆ ดังนี้

การกำหนดค่าให้กับตัวแปรหรือค่าคงที่ \(Assign a value\)

```swift
let favoriteActor = "Tom Cruise"  //กำหนดค่าให้ตัวแปร
favoriteActor = "Bradl Pitt"      //แก้ไขค่าที่อยู่ในตัวแปร
```

การดำเนินการทางคณิตศาสตร์ \(Basic Arithmetic\)

```swift
var firstScore = 52
var secondScore = 24
var thirdScore = 35

let totalScore = firstScore + secondScore + thirdScore  //การบวก
let diffScore = firstScore - secondScore  //การลบ
let powerScore = totalScore * 2           //การคูณ
let agvScore = Double(totalScore) / 4     //การหาร
let modScore = thirdScore % 3             //การหารเอาเศษ
```

การดำเนินการกำหนดค่าเชิงประกอบ \(Compound Assignment\)

```swift
var myScore: Int = 20
myScore += 3    // myScore = myScore + 3
myScore -= 5    // myScore = myScore - 5
myScore *= 2    // myScore = myScore * 2
myScore /= 2    // myScore = myScore / 2
```

การดำเนินการแบบเปรียบเทียบ \(Comparison Operators\) โดยจะทำการเปรียบเทียบค่าที่ถูกเก็บในตัวแปร 2 ตัวแปร เช่น ค่าของตัวแปร a และ ค่าของตัวแปร b โดยจะได้ผลลัพธ์จากการทำงานเป็น true หรือ false

* การใช้ == ในการเปรียบเทียบว่า a และ b มีค่าเท่ากัน ใช่หรือไม่ เช่น  a == b 
* การใช้ !=  ในการเปรียบเทียบว่า a และ b มีค่าไม่เท่ากัน ใช่หรือไม่ เช่น a != b
* การใช้ &gt; ในการเปรียบเทียบว่า a มีค่ามากกว่า b หรือไม่ เช่น a &gt; b
* การใช้ &lt; ในการเปรียบเทียบว่า a มีค่าน้อยกว่า b หรือไม่ เช่น a &lt; b
* การใช้ &gt;= ในการเปรียบเทียบว่า a มีค่ามากกว่าหรือเท่ากับ b หรือไม่ เช่น a &gt;= b
* การใช้ &lt;= ในการเปรียบเทียบว่า a มีค่าน้อยกว่าหรือเท่ากับ b หรือไม่ เช่น a &lt;= b

ตัวอย่างการใช้ตัวดำเนินการแบบเปรียบเทียบ เช่น

```swift
let a: Int = 7
let b: Int = 10
if (a >= b) {
    print("a มีค่ามากกว่าหรือเท่ากับ b")
 } else {
    print("a มีค่าน้อยกว่า b")
 }
```

การดำเนินการแบบตรรกะ \(Logical Operator\) เป็นการดำเนินการกับข้อมูลประเภท Boolean \(true หรือ false\) ด้วยเครื่องหมาย ! \(NOT\), && \(AND\) หรือ \|\| \(OR\) โดยจะได้ผลลัพธ์การทำงานดังนี้

| a | b | !a | a && b | a \|\| b |
| :---: | :---: | :---: | :---: | :---: |
| true | true | false | true | true |
| true | false | false | false | true |
| false | true | true | false | true |
| false | false | true | false | false |

