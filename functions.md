---
description: >-
  ฟังก์ชัน (Function) คือ บล็อกของชุดคำสั่งสำหรับการทำงานเฉพาะอย่าง
  โดยแต่ละฟังก์ชันจะถูกกำกับด้วยชื่อเรียก ซึ่งใช้ในการอ้างอิง
---

# Functions

### การสร้างฟังก์ชัน

โดยทั่วไป ฟังก์ชันจะประกอบด้วย **ชื่อเรียก\(name\)**, **ค่าสำหรับการทำงาน \(parameters\)** และ**ค่าที่ส่งกลับ \(return\)** ซึ่งการนิยาม \(defining\) การทำงานของฟังก์ชันสามารถทำได้ ดังนี้

```swift
func functionName (parameters) -> ReturnType {
  // คำสั่งเพื่อระบุการทำงานของฟังก์ชัน
  
}
```

ตัวอย่างการสร้างฟังก์ชันอย่างง่ายเพื่อการหาผลรวมของตัวเลข 2 ตัว และการเรียกใช้งาน

```swift
func addNumber(firstNumber: Int, secondNumber: Int) -> Int {
    let result = firstNumber + secondNumber
    return result
}

var totResult = addNumber(firstNumber: 3, secondNumber: 15)
print(totResult) // 18
```

* `addNumber`  คือ ชื่อฟังก์ชัน \(functionName\) ซึ่งใช้กำกับเพื่อการเรียนใช้งานฟังก์ชัน
* `firstNumber: Int` และ `secondNumber: Int`  คือ พารามิเตอร์ \(parameters\) ซึ่งประกอบไปด้วยชื่อและประเภทของพารามิเตอร์ที่จะรับเข้ามาเพื่อใช้ในการทำงานตามคำสั่งภายในฟังก์ชัน
* `-> Int` คือ ประเภทของค่าที่จะส่งกลับหลังจากการทำงานตามคำสั่งเสร็จสิ้น โดยจะต้องสอดคล้องกับที่ระบุไว้ที่ return
* `addNumber(firstNumber: 3 , secondNumber: 15)` คือ การเรียกใช้ฟังก์ชัน พร้อมกับส่งอาร์กิวเมนต์ \(Argument\) จำนวน 2 ค่า คือ 3 และ 5 ไปเพื่อเป็นพารามิเตอร์สำหรับใช้ในการประมวลผลของฟังก์ชัน และรับผลลัพธ์ที่ได้มาเก็บไว้ในตัวแปร ชื่อ totResult  \* อาร์กิวเมนต์  คือ ข้อมูลที่ส่งให้กับพารามิเตอร์ของฟังก์ชัน

### ฟังก์ชันที่ไม่มีพารามิเตอร์และไม่มีการรีเทิร์นค่า

```swift
func displayPi() {
  print("3.1415926")
}

displayPi()  // 3.1415926
```

### ฟังก์ชันที่มีพารามิเตอร์แต่ไม่มีการรีเทิร์นค่า

```swift
func triple(value: Int) {
  let result = value * 3
  print("If you multiply \(value) by 3, you'll get \(result).")
}

triple(value: 10)  // If you multiply 10 by 3, you'll get 30.
```

### ฟังก์ชันที่มีพารามิเตอร์มากกว่า 2 ตัว แต่ไม่มีการรีเทิร์นค่า

```swift
func sayHello(to: String, and: String) {
   print("Hello! \(to) and \(and).")
}

sayHello(to: "Thiti", and: "Looknam")  // Hello! Thiti and Looknam.
```

### ฟังก์ชันที่มีการรีเทิร์นค่า

```swift
func multiply(firstNumber: Int, secondNumber: Int) -> Int {
   let result = firstNumber * secondNumber
   return result
}

var result = multiply(firstNumber: 3, secondNumber: 5)
print(result)  // 15
```

### การใช้พารามิเตอร์แบบ External และ Local name 

```swift
func sayHello(to person: String, and anotherPerson: String) {
   print("Hello! \(person) and \(anotherPerson).")
}

sayHello(to: "Thiti", and: "Looknam")  // Hello! Thiti and Looknam.
```

หากเราต้องการเรียกใช้ฟังก์ชัน โดยละเว้นการระบุชื่ออาร์กิวเมนต์ \(Omiting label\) สามารถทำได้ โดยใช้เครื่องหมาย  `_`  ระบุไว้แทนชื่อพารามิเตอร์ของฟังก์ชัน

```swift
func sayHello(_ person: String, _ anotherPerson: String) {
   print("Hello! \(person) and \(anotherPerson).")
}

sayHello("Thiti", "Looknam")  // Hello! Thiti and Looknam.
```

### การกำหนดค่าเริ่มต้นให้กับพารามิเตอร์

เราสามารถกำหนดค่าเริ่มต้น \(default value\) ให้กับพารามิเตอร์ได้ ซึ่งหากเราไม่มีการผ่านค่าไปยังฟังก์ชัน ฟังก์ชันก็จะใช้ค่าดังกล่าวแทนทันที

```swift
func power(number: Int, by: Int = 2) -> Int {
  var result = 1
  for _ in 1...by {
     result = result * number
  }
  return result
}

let firstResult = power(number: 5)  // 25
let secondResult = power(number: 3, by: 4)  // 81
```

### การกำหนดพารามิเตอร์แบบ Optional

หากมีพารามิเตอร์บางตัวที่ไม่ได้ถูกใช้ในการทำงานทุกครั้ง เราอาจกำหนดให้สามารถผ่านค่า nil มายังพารามิเตอร์ดังกล่าวได้ กล่าวคือ เราสามารถกำหนดให้พารามิเตอร์ดังกล่าวเป็นแบบ Optional โดยใช้เครื่องหมาย ? กำกับไว้หลังชนิดของข้อมูลที่จะรับเข้ามายังฟังก์ชัน

```swift
func rectArea(width: Double, height: Double?) -> String {
    if height != nil {
        return "สี่เหลี่ยนมีพื้นที่ทั้งหมด \(width * height!) ตารางเมตร"
    } else {
        return "สี่เหลี่ยนมีพื้นที่ทั้งหมด \(width * width) ตารางเมตร"
    }
}

var myArea = rectArea(width: 5.0, height: 3.0)
print(myArea)  // สี่เหลี่ยนมีพื้นที่ทั้งหมด 15.0 ตารางเมตร

myArea = rectArea(width: 5.0, height: nil)
print(myArea)  // สี่เหลี่ยนมีพื้นที่ทั้งหมด 25.0 ตารางเมตร
```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language \(Swift 5.0\)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-0/id881256329), Apple Inc., 2018. Available on: Apple Book Store.
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.

{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง  
ผู้เขียน** ธิติ ธีระเธียร    
**วันที่เผยแพร่**  วันที่ 17 มิถุนายน 2562.  
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/conditional-statement](https://ajthiti.gitbook.io/swift/functions)  
**เงื่อนใขในการใช้งาน**  
This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}

