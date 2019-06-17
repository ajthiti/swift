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
* `addNumber(firstNumber: 3 , secondNumber: 15)` คือ การเรียกใช้ฟังก์ชัน พร้อมกับส่งอาร์กิวเมนต์ \(Argument\) จำนวน 2 ค่า คือ 3 และ 5 ไปเพื่อเป็นพารามิเตอร์สำหรับใช้ในการประมวลผลของฟังก์ชัน และรับผลลัพธ์ที่ได้มาเก็บไว้ในตัวแปร ชื่อ totResult

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

