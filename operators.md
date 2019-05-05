---
description: >-
  ตัวดำเนินการเป็นเครื่องหมายหรือกลุ่มของเครื่องหมายที่ใช้ในการทำการอย่างใดอย่างหนึ่ง
  เช่น การกำหนดค่า การประมวลผลทางคณิตศาสตร์ หรือการเปรียบเทียบทางตรรกะ เป็นต้น
---

# Operators

**ตัวดำเนินการ \(Operator\)** คือ สัญลักษณ์ที่ใช้ในนิพจน์หรือคำสั่งเพื่อกำหนดกระบวนการการทำงานของโปรแกรม ในการเขียนโปรแกรม เราสามารถใช้ตัวดำเนินการเพื่อทำสิ่งต่างๆ ดังนี้

### **การกำหนดค่าให้กับตัวแปรหรือค่าคงที่ \(Assign a value\)**

```swift
let favoriteActor = "Tom Cruise"  //กำหนดค่าให้ตัวแปร
favoriteActor = "Bradl Pitt"      //แก้ไขค่าที่อยู่ในตัวแปร
```

### **การดำเนินการทางคณิตศาสตร์ \(Basic Arithmetic\)**

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

เครื่องหมาย + \(Additional operator\) นอกจากจะถูกใช้เพื่อดำเนินการกับตัวเลขแล้ว ยังสามารถใช้ในการเชื่อมต่อข้อความ \(Concatenation\) ได้ด้วย ตัวอย่างเช่น 

```swift
var sayHi: String = "สวัสดีครับ คุณ"
var friendName: String = "สมชาย"
print (sayHi + friendName)     //สวัสดีครับ คุณสมชาย
```

### **การดำเนินการด้วยตัวดำเนินการกำหนดค่าเชิงประกอบ \(Compound Assignment\)**

```swift
var myScore: Int = 20
myScore += 3    // myScore = myScore + 3
myScore -= 5    // myScore = myScore - 5
myScore *= 2    // myScore = myScore * 2
myScore /= 2    // myScore = myScore / 2
```

### **การดำเนินการด้วยตัวดำเนินการเปรียบเทียบ \(Comparison Operators\)** 

ตัวดำเนินการกลุ่มนี้จะทำหน้าที่ในการเปรียบเทียบค่าที่ถูกเก็บในตัวแปร 2 ตัวแปร เช่น ค่าของตัวแปร a และ ค่าของตัวแปร b โดยจะได้ผลลัพธ์จากการทำงานเป็นข้อมูลมูลประเภท Boolean \(true หรือ false\) ตัวดำเนินการเปรียบเทียบ ประกอบด้วย

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

### **การดำเนินการด้านตรรกะ \(Logical Operator\)** 

ตัวดำเนินการที่ใช้เพื่อประมวลผลทางตรรกศาสตร์กับข้อมูลประเภท Boolean \(true หรือ false\) ตัวดำเนินการในกลุ่มนี้ประกอบด้วย 

* Logical NOT  \( ! \)  
* Logical AND \( && \)
* Logical OR \( \|\| \)

โดยหากกำหนดให้ a และ b เป็นตัวแปรประเภท Boolean แล้ว จะได้ผลลัพธ์การดำเนินการด้วยตัวดำเนินการด้านตรรกะ ดังนี้

| a | b | !a | a && b | a \|\| b |
| :---: | :---: | :---: | :---: | :---: |
| true | true | false | true | true |
| true | false | false | false | true |
| false | true | true | false | true |
| false | false | true | false | false |

ตัวอย่างการใช้ตัวดำเนินการด้านตรรกะ เช่น

```swift
if (doorCode && retinaScan) || doorKey || password {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
```

### ลำดับในการทำงานของตัวดำเนินการ \(Order of operations\)

ตัวดำเนินการแต่ละตัวต่างก็มีลำดับความสำคัญ \(Precedence\) ของการทำงานก่อนหลังแตกต่างกันไป โดยตัวดำเนินการที่มีความสำคัญสูงจะทำงานก่อนตัวดำเนินการที่มีความสำคัญต่ำ 

```swift
let x = 2, y = 3, z = 5
var result = x + y * z              // Equals 17
var anotherResult = (x + y) * z     // Equals 25
```

ความสำคัญของตัวดำเนินการในภาษา Swift สามารถเรียงลำดับได้ ดังนี้

* Logical NOT  \( ! \)
* Multiplication \( \* \)
* Division \( / \)
* Module \( % \)
* Addition \( + \)
* Substraction \( - \)
* Less than \( &lt; \)
* Less than or equal \( &lt;=\)
* More than \( &gt; \)
* More than or equal \( &gt;=\)
* Equal \( == \)
* Not be equal \( != \)
* Logical AND \( && \)
* Logical OR \( \|\| \)

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language \(Swift 5.0\)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-0/id881256329), Apple Inc., 2018. Available on: Apple Book Store.
* [App Development with Swift](https://itunes.apple.com/WebObjects/MZStore.woa/wa/viewBook?id=1219117996), Apple Inc., 2017. Available on: Apple Book Store.



{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง  
ผู้เขียน** ธิติ ธีระเธียร    
**วันที่เผยแพร่**  วันที่ 27 เมษายน 2562.  
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/operators](https://ajthiti.gitbook.io/swift/operators)  
**เงื่อนใขในการใช้งาน**  
This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}

