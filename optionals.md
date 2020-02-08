---
description: >-
  การป้องกันการเกิดความผิดพลาดซึ่งเกิดจากการไม่พร้อมใช้งานของตัวแปรที่ยังไม่ได้มีการกำหนดค่าหรือมีค่าเป็น
  "ค่าว่าง" (nil)
---

# Optionals

ตัวแปรที่มี **ค่าว่าง \(nil\)** หรือ ตัวแปรที่ยังไม่ถูกกำหนดค่า \(Not set\) เมื่อถูกเรียกใช้งานอาจส่งผลให้เกิดความผิดพลาดในการทำงานของโปรแกรมและสร้างประสบการณ์การใช้งานที่ไม่ดีกับผู้ใช้ ซึ่งภาษา Swift นั้น จะไม่อนุญาตให้มีการกำหนดค่า nil ให้กับตัวแปรที่ถูกสร้างขึ้นตามปกติทั่วไป

```swift
var userInput: String = nil   //'nil' cannot initialize specified type 'String'
```

**Optional** คือ การกำหนดให้ทราบว่าตัวแปรอาจมีสถานะที่ไม่มีค่า \(Not set\) หรือมีโอกาสเป็นค่าว่าง \(nil\) ได้ โดยปกติแล้ว Optional จะถูกใช้งานกับตัวแปรเท่านั้น เนื่องจากหากนำมาใช้กับค่าคงที่แล้ว เมื่อมีการกำหนดให้ค่าคงที่ดังกล่าวเป็น nil ก็จะไม่สามารถเปลี่ยนแปลงค่าได้อีก การกำหนดให้ตัวแปรเป็น Optional ทำได้โดยใส่เครื่องหมาย ? กำกับลงไปดังนี้

```swift
var userInput: String? = nil
```

เมื่อมีการกำหนดค่าให้กับตัวแปรแบบ Optional แล้ว การจะนำค่าดังกล่าวมาใช้งานนั้นจำเป็นจะต้อง Unwrap ค่าที่ถูกเก็บไว้ออกมาเสียก่อน โดยการใส่เครื่องหมาย ! กำกับในส่วนท้ายชื่อของตัวแปร เรียกวิธีการนี้ว่า **Force unwarpping**  

```swift
var userInput: String?
userInput = "Thiti"
print(userInput)  // Optional("Thiti")

let inputData1:String = userInput!  // Need the '!' to unwrapped
print(inputData1)  // Thiti

let inputData2:String = userInput!  // Need the '!' to unwrapped
print(inputData2)  // Thiti
```

เนื่องจากในการนำค่าจาก Optional ไปใช้งานนั้น เราจะต้องทำการ Force unwarpping ทุกครั้ง ดังนั้น ถ้าเรามีความมั่นใจว่า Optional ที่ถูกสร้างขึ้น หลังจากที่ได้กำหนดค่าให้แล้ว Optional ดังกล่าวจะไม่มีค่าเป็น nil อีกต่อไป เราสามารถกำหนดให้ทำการ unwarp โดยอัตโนมัติได้ด้วยการระบุเครื่องหมาย ! ไว้ในส่วนท้ายของการประกาศตัวแปรเป็นแบบ Optional แทนการใช้เครื่องหมาย ? วิธีการนี้เรียกว่า **Implicitly Unwrapped Optional**

```swift
var userInput: String!
userInput = "Thiti"
print(userInput)  // Optional("Thiti")

let inputData1:String = userInput  // No need '!' to unwrapped
print(inputData1)  // Thiti
```

อย่างไรก็ตาม หาก Optional เกิดมีค่าเป็น nil จะส่งผลให้เกิดการทำงานผิดพลาดขึ้นได้ เพื่อป้องกันความผิดพลาดดังกล่าวที่อาจเกิดขึ้น จึงควรมีการตรวจสอบค่าที่ถูกเก็บไว้ก่อนนำไปใช้งาน ดังนี้

**วิธีที่ 1 :** การตรวจสอบว่าตัวแปรไม่เป็นค่า nil ด้วยคำสั่ง if

```swift
if userInput != nil {
    let inputData: String = userInput
    print(inputData)
}
```

**วิธีที่ 2 :** การใช้ Optional Binding เพื่อลองกำหนดค่าลงในตัวแปรใหม่ด้วยคำสั่ง if let

```swift
if let inputData: String = userInput {
    print(inputData)
}
```

นอกจากนี้ ยังสามารถใช้เครื่องหมาย ?? ซึ่งเรียกว่า **Nil Coalescing Operator** ในการกำหนดค่าโดยปริยาย \(default\) ให้กับข้อมูลได้ดังนี้

```swift
var inputAge: Int!
var myAge: Int = inputAge ?? 0    //if inputAge = nil then assign 0 to myAge
print(myAge)
```

หรือการใช้ ? และ ! ร่วมกับ as ในการแปลงชนิดของข้อมูล \(Type casting\) 

```swift
var temp: Any = "12"

if let myNumber = temp as? Int {
    print(myNumber)
} else {
    print("Can't convert to Int")
}
```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language \(Swift 5.0\)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-0/id881256329), Apple Inc., 2018. Available on: Apple Book Store.
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.



{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง  
ผู้เขียน** ธิติ ธีระเธียร    
**วันที่เผยแพร่**  วันที่ 26 เมษายน 2562.  
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/optionals](https://ajthiti.gitbook.io/swift/optionals)  
**เงื่อนใขในการใช้งาน**  
This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}

