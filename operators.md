---
description: >-
  ตัวดำเนินการเป็นเครื่องหมายหรือกลุ่มของเครื่องหมายที่ใช้ในการทำการอย่างใดอย่างหนึ่ง
  เช่น การกำหนดค่า การประมวลผลทางคณิตศาสตร์ หรือการเปรียบเทียบทางตรรกะ เป็นต้น
---

# Operators

**ตัวดำเนินการ (Operator)** คือ สัญลักษณ์ที่ใช้ในนิพจน์หรือคำสั่งเพื่อกำหนดกระบวนการทำงานของโปรแกรม ในการเขียนโปรแกรม เราสามารถใช้ตัวดำเนินการเพื่อทำสิ่งต่างๆ ดังนี้

### **การกำหนดค่าให้กับตัวแปรหรือค่าคงที่ (Assign a value)**

```swift
var favoriteActor = "Tom Cruise"  //กำหนดค่าให้ตัวแปร
favoriteActor = "Bradl Pitt"      //แก้ไขค่าที่อยู่ในตัวแปร
```

### **การดำเนินการทางคณิตศาสตร์ (Basic Arithmetic)**

```swift
let firstScore = 52
let secondScore = 24
let thirdScore = 35

var totalScore = firstScore + secondScore + thirdScore  //การบวก
var diffScore = firstScore - secondScore  //การลบ
var powerScore = totalScore * 2           //การคูณ
var agvScore = Double(totalScore) / 4     //การหาร
var modScore = thirdScore % 3             //การหารเอาเศษ
```

เครื่องหมาย + (Additional operator) นอกจากจะถูกใช้เพื่อดำเนินการกับตัวเลขแล้ว ยังสามารถใช้ในการเชื่อมต่อข้อความ (Concatenation) ได้ด้วย ตัวอย่างเช่น&#x20;

```swift
var sayHi: String = "สวัสดีครับ คุณ"
var friendName: String = "สมชาย"
print (sayHi + friendName)     //สวัสดีครับ คุณสมชาย
```

### **การดำเนินการด้วยตัวดำเนินการกำหนดค่าเชิงประกอบ (Compound Assignment)**

```swift
var myScore: Int = 20
myScore += 3    // myScore = myScore + 3
myScore -= 5    // myScore = myScore - 5
myScore *= 2    // myScore = myScore * 2
myScore /= 2    // myScore = myScore / 2
```

### **การดำเนินการเพื่อเปรียบเทียบ (Comparison Operators)**&#x20;

ตัวดำเนินการกลุ่มนี้จะทำหน้าที่ในการเปรียบเทียบค่าที่ถูกเก็บในตัวแปร 2 ตัวแปร เช่น ค่าของตัวแปร a และ ค่าของตัวแปร b โดยจะได้ผลลัพธ์จากการทำงานเป็นข้อมูลมูลประเภท Boolean (true หรือ false) ตัวดำเนินการเปรียบเทียบ ประกอบด้วย

* การใช้ `==` ในการเปรียบเทียบว่า a และ b มีค่าเท่ากัน ใช่หรือไม่ เช่น  a == b&#x20;
* การใช้ `!=`  ในการเปรียบเทียบว่า a และ b มีค่าไม่เท่ากัน ใช่หรือไม่ เช่น a != b
* การใช้ `>` ในการเปรียบเทียบว่า a มีค่ามากกว่า b หรือไม่ เช่น a > b
* การใช้ `<` ในการเปรียบเทียบว่า a มีค่าน้อยกว่า b หรือไม่ เช่น a < b
* การใช้ `>=` ในการเปรียบเทียบว่า a มีค่ามากกว่าหรือเท่ากับ b หรือไม่ เช่น a >= b
* การใช้ `<=` ในการเปรียบเทียบว่า a มีค่าน้อยกว่าหรือเท่ากับ b หรือไม่ เช่น a <= b

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

### **การดำเนินการด้านตรรกะ (Logical Operator)**&#x20;

ตัวดำเนินการที่ใช้เพื่อประมวลผลทางตรรกศาสตร์กับข้อมูลประเภท Boolean (true หรือ false) ตัวดำเนินการในกลุ่มนี้ประกอบด้วย&#x20;

* Logical NOT  ( `!` ) &#x20;
* Logical AND ( `&&` )
* Logical OR ( `||` )

โดยหากกำหนดให้ a และ b เป็นตัวแปรประเภท Boolean แล้ว จะได้ผลลัพธ์การดำเนินการด้วยตัวดำเนินการด้านตรรกะ ดังนี้

|   a   |   b   |   !a  | a && b | a \|\| b |
| :---: | :---: | :---: | :----: | :------: |
|  true |  true | false |  true  |   true   |
|  true | false | false |  false |   true   |
| false |  true |  true |  false |   true   |
| false | false |  true |  false |   false  |

ตัวอย่างการใช้ตัวดำเนินการด้านตรรกะ เช่น

```swift
if (doorCode && retinaScan) || doorKey || password {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
```

### ลำดับในการทำงานของตัวดำเนินการ (Order of operations)

ตัวดำเนินการแต่ละตัวต่างก็มีลำดับความสำคัญ (Precedence) ของการทำงานก่อนหลังแตกต่างกันไป โดยตัวดำเนินการที่มีความสำคัญสูงจะทำงานก่อนตัวดำเนินการที่มีความสำคัญต่ำ&#x20;

```swift
let x = 2, y = 3, z = 5
var result = x + y * z              // Equals 17
var anotherResult = (x + y) * z     // Equals 25
```

ความสำคัญของตัวดำเนินการในภาษา Swift สามารถเรียงลำดับได้ ดังนี้

* Logical NOT  ( `!` )
* Multiplication ( `*` )
* Division ( `/` )
* Module ( `%` )
* Addition ( `+` )
* Substraction ( `-` )
* Less than ( `<` )
* Less than or equal ( `<=`)
* More than ( `>` )
* More than or equal ( `>=`)
* Equal ( `==` )
* Not be equal ( `!=` )
* Logical AND ( `&&` )
* Logical OR ( `||` )

## ตัวดำเนินการอื่นๆ

**Ternary conditional operator** เป็นตัวดำเนินการที่มีการตรวจสอบเงื่อนไขเพื่อการตัดสินใจในการทำงาน ซึ่งมีรูปแบบการใช้งาน คือ `condition ? a : b` โดยถ้าเงื่อนไขเป็น true ผลลัพธ์จะเป็น a แต่ถ้าเป็น false ผลลัพธ์จะเป็น b&#x20;

```swift
let myLuckyNumber = 35
(myLuckyNumber % 2 == 0) ? print("จำนวนคู่") : print("จำนวนคี่") 
```

**Nil-coalescing operator** เป็นตัวดำเนินการที่ใช้สำหรับตรวจสอบค่า Optional ซึ่งมีรูปแบบการใช้งาน คือ `optional ?? default` โดยหากพบว่ามีการกำหนดค่าใน Optional ก็จะทำการ Unwrap แต่ถ้าหากเป็น nil ก็จะกำหนดค่า default เข้าไปแทนที่

```swift
var petName: String?
print("สัตว์เลื้องของฉันชื่อว่า \(petName ?? "Daisy").")
```

**Range Operator** เป็นตัวดำเนินการเพื่อใช้ในการกำหนดช่วงของข้อมูล ซึ่งมักถูกใช้ร่วมกับการเขียน[คำสั่งแบบกำหนดเงื่อนไข (Condition Statement) ](conditional-statement.md)และ [ลูป (Loop)](loops.md) โดยสามารถแบ่งออกเป็นประเภทต่างๆ ได้ดังนี้

(1)  Closed range operator ( a...b ) เป็นการกำหนดช่วงของข้อมูลโดยเริ่มตั้งแต่ค่า a ไปจนถึงค่า b เช่น

```swift
// 1...3 Defines a range containing values 1, 2 and 3
for value in 1...3 {
	print(value)
}
```

(2) Half-Open range operator (a..\<b) เป็นการกำหนดช่วงของข้อมูลโดยเริ่มตั้งแต่ค่า a ไปจนถึงค่า b แต่ไม่นับค่า b เช่น

```swift
// 1..<3 Defines a range containing values 1,2
for value in 1..<3 {
	print(value)
}
```

(3) One-Sided range operator เป็นการกำหนดช่วงของข้อมูล โดยการระบุค่าแรกหรือค่าสุดท้ายของช่วงข้อมูลเพียงอย่างใดอย่างหนึ่ง เช่น

```swift
let setA = ..<2
print(setA.contains(-1))  //true
print(setA.contains(2))   //false

let setB = 2...
print(setB.contains(100)) //true
print(setB.contains(1))   //false

```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language (Swift 5.0)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-0/id881256329), Apple Inc., 2018. Available on: Apple Book Store.
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.



{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง**\
**ผู้เขียน** ธิติ ธีระเธียร  \
**วันที่เผยแพร่**  วันที่ 27 เมษายน 2562.\
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/operators](https://ajthiti.gitbook.io/swift/operators)\
**เงื่อนใขในการใช้งาน**\
****This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}
