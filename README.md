---
description: >-
  การประกาศตัวแปรหรือค่าคงที่
  เป็นการกำหนดชื่อที่ใช้ในการอ้างอิงถึงพื้นที่หน่วยความจำ
  พร้อมทั้งระบุชนิดของข้อมูลที่ถูกจัดเก็บไว้ในพื้นที่ดังกล่าว
---

# Constants, Variables and Types

## ค่าคงที่และตัวแปร

**ค่าคงที่ \(Constant\)** คือ ข้อมูลที่ถูกจัดเก็บในหน่วยความจำและไม่มีการเปลี่ยนแปลงค่า เราสามารถประกาศค่าคงที่ได้ด้วยคีย์เวิร์ด let

```swift
//Defined "Constant" using the let keyword
let name = "Thiti Theerathean"
let pi = 3.14
```

**ตัวแปร \(Variable\)** คือ ข้อมูลที่จัดเก็บในหน่วยความจำ ซึ่งสามารถเปลี่ยนแปลงได้ในระหว่างการทำงานของโปรแกรม เราสามารถประกาศตัวแปรได้ด้วยคีย์เวิร์ด var

```swift
//Defined "Variable" using the var keyword
var score = 0
score = 10
```

การตั้งชื่อค่าคงที่และตัวแปร จะเป็นรูปแบบ **Camel Case** คือ การเขียนคำติดกันโดย**ไม่เว้นวรรค**และตัวอักษรแรกของคำเป็นตัวพิมพ์ใหญ่ เรียกอีกอย่างว่า Upper Camel Case เช่น HelloWorld หรือ myFirstName เป็นต้น โดย **ไม่ใช้** ตัวเลขหรือสัญลักษณ์ทางคณิตศาสตร์นำหน้าชื่อ

## ประเภทของข้อมูล

ประเภทของข้อมูลพื้นฐาน \(Basic Data Type\) ในเบื้องต้น สามารถแบ่งออกได้เป็น 4 ชนิด ดังนี้

* ข้อมูลประเภทตัวเลขจำนวนเต็ม \(Integer\) ใช้คีย์เวิร์ด Int
* ข้อมูลประเภทตัวเลขทศนิยม \(Double\) ใช้คีเวิร์ด Double
* ข้อมูลประเภทข้อความ \(String\) ใช้คีเวิร์ด String
* ข้อมูลประเภทตรรกะ \(Boolean\) ใช้คีเวิร์ด Bool

แม้ว่าภาษา Swift จะสามารถกำหนดประเภทของข้อมูลให้กับตัวแปรหรือค่าคงที่ได้อัตโนมัติ โดยจะอ้างอิงจากค่าแรกที่ถูกกำหนดให้กับตัวแปรหรือค่าคงที่นั้น \(Type Inference\) แต่ผู้พัฒนายังสามารถกำหนดประเภทของข้อมูลด้วยตนเอง \(Type Annotation\) ได้อีกด้วย

```swift
//Type Annotation
let playerName: String = "Julian"
var myNumber: Int = 39
var clubMember: Bool = true
var temperature: Double = 30.7
```

นอกจากประเภทของข้อมูลพื้นฐานแล้วนักพัฒนายังสามารถสร้างประเภทของข้อมูลขึ้นมาใช้เองได้ หรือเรียกว่า "User definded data type"

```swift
enum Gender {
    case male
    case female
}

var sex: Gender = .male
    
```

รวมทั้งยังมีรูปแบบในการพัฒนาแอพที่มีความปลอดภัยจากความผิดพลาดในระหว่างการทำงาน \(Run time error\) ด้วยคุณสมบัติการเรียกร้องให้กำหนดค่า \(Required Value\) ซึ่งจะไม่ยอมให้นักพัฒนาประกาศตัวแปรเป็น ค่าว่าง \(nil\) และคุณสมบัติการรักษาสภาพของตัวแปร \(Type Safety\)

```swift
var wholeNumber = 30
var numberWithDecimals = 17.5

wholeNumber = numberWithDecimals //error: Cannot assign value of type 'Double' to type 'Int'
```

แต่นักพัฒนาก็สามารถแปลงประเภทของตัวแปรได้ด้วยเช่นกัน

```swift
var myIntNumber = 30
var myDoubleNumber = 7.5

var result: Double = Double(myIntNumber) + myDoubleNumber
```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language \(Swift 5.0\)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-0/id881256329), Apple Inc., 2018. Available on: Apple Book Store.
* [App Development with Swift](https://itunes.apple.com/WebObjects/MZStore.woa/wa/viewBook?id=1219117996), Apple Inc., 2017. Available on: Apple Book Store.

