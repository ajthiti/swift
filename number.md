---
description: >-
  ตัวเลข เป็นข้อมูลพื้นฐานที่มีอยู่หลายแบบ เช่น Int, UInt, Double และ Float
  ซึ่งมักถูกใช้บ่อยในการเขียนโปรแกรมและการประมวลผลทางสถิติ ในภาษา Swift
  มีคุณสมบัติการรักษาสภาพของตัวแปร ดังนั้น จึงจำเป็นที่เรา
---

# Number

### Integer

Integer คือ ตัวแปรหรือค่าคงที่ ซึ่งใช้เก็บข้อมูลประเภทตัวเลขจำนวนเต็มซึ่งประกอบด้วย ค่าบวกค่าลบ และเลขศูนย์ ซึ่งตัวเลขเหล่านั้นจะต้องไม่มีทศนิยม ตัวอย่างเช่น 25, -3 หรือ 0 เป็นต้น

ค่าเริ่มต้นของ Integer คือ 0 และสามารถเลือกใช้งานได้อยู่ 2 รูปแบบใหญ่ๆ คือ 

*  แบบมีเครื่องหมาย \(signed integer\) ซึ่งประกอบด้วย จำนวนเต็มลบ จำนวนศูนย์ และจำนวนเต็มบวก เช่น `Int`, `Int8`,`Int16`,`Int32`เป็นต้น
* แบบไม่มีเครื่องหมาย \(unsigned integer\) ซึ่งประกอบด้วย จำนวนศูนย์และจำนวนเต็มบวกเท่านั้น เช่น `UInt`, `UInt8`,`UInt16`,`UInt32`เป็นต้น

คำสั่งสำหรับการหาค่า max และ min ของ Integer เพื่อดูช่วงของข้อมูล

```swift
print(Int.min)
print(Int.max)
```

* `Int8` และ `UInt8` มีขนาดของข้อมูลเท่ากับ 8 บิต 
  * ช่วงข้อมูลของ `Int8` คือ -128 ถึง 127 
  * ช่วงข้อมูลของ `UInt8` คือ 0 ถึง 255 
* `Int16` และ `UInt16` มีขนาดของข้อมูลเท่ากับ 16 บิต 
  * ช่วงข้อมูลของ `Int16` คือ -32,768 ถึง 32,767 
  * ช่วงข้อมูลของ `UInt16` คือ 0 ถึง 65,535
* `Int32` และ `UInt32` มีขนาดของข้อมูลเท่ากับ 32 บิต 
  * ช่วงข้อมูลของ `Int32` คือ -2,147,483,648 ถึง 2,147,483,647 
  * ช่วงข้อมูลของ `UInt32` คือ 0 ถึง 4,294,967,295
* `Int` และ `UInt` มีขนาดของข้อมูลเท่ากับ 64 บิต 
  * ช่วงข้อมูลของ `Int` คือ  -9,223,372,036,854,775,808 ถึง 9,223,372,036,854,775,807 
  * ช่วงข้อมูลของ `UInt` คือ 0 ถึง 18,446,744,073,709,551,615

### Floating-Point Number

Floating-Point Number คือ ตัวแปรหรือค่าคงที่ ซึ่งใช้เก็บข้อมูลตัวเลขแบบมีทศนิยม เช่น 3.14,  0.4127 หรือ -273.15 เป็นต้น ซึ่งค่าเริ่มต้นของข้อมูล คือ 0.0 และมีให้เลือกใช้อยู่ 2 รูปแบบ คือ

* `Float` มีขนาด: 32 บิต, ความแม่นยำ ≥6 decimal digits
* `Double` มีขนาด: 64 บิต, ความแม่นยำ ≥15 decimal digits

```swift
//Float data type
let floatingScore: Float = 100.232
print(floatingScore)

//Double data type
let doubleScore: Double = 100.232321212121
print(doubleScore)
```

### Numeric Type Conversion

การแปลงค่าระหว่าง Integer และ Integer

```swift
let daysInYear: Int16 = 365
let daysInJanuary: UInt8 = 31
let totalDays = daysInYear + Int16(daysInJanuary)

let littleUInt16 = 120
let littleUInt8: UInt8 = UInt8(littleUInt16)

let bigUInt16 = 1440
let bitUInt8: UInt8 = UInt8(bigUInt16) // Compiler error.
```

การแปลงค่าระหว่าง Integer และ Floating-Point number

```swift
let startingRatio = 1  // กำหนดเป็น Int
let frationalRatio = 0.61803398875 //กำหนดเป็น Double

let goldenRatio = Double(startingRatio) +  frationalRatio
// goldenRatio มีค่าเท่ากับ 1.61803398875 และเป็น Double

let integerGoldenRatio = Int(goldenRatio)
//goldenRatio มีค่าเท่ากับ 1 และเป็น Int
```

### การดำเนินการกับตัวเลข

* คำสั่ง `round(จำนวน)` ใช้ในการประมาณค่าด้วยการปัดเศษทศนิยม โดยหากเศษมีค่ามากกว่า 0.5 จะปัดขึ้นเป็นจำนวนเต็มถัดไป แต่หากเศษน้อยกว่า 0.5 จะปัดทิ้ง
* คำสั่ง `floor(จำนวน)` ใช้ในการปัดทศนิยมทิ้งเป็นจำนวนเต็มที่อยู่ข้างล่างของจำนวนที่ระบุ
* คำสั่ง `ceil(จำนวน)` ใช้ในการปัดทศนิยมขึ้นเป็นจำนวนเต็มที่อยู่ข้างบนของจำนวนที่ระบุ
* คำสั่ง `trunc(จำนวน)` ใช้ในการตัดเศษทศนิยมทิ้งโดยไม่มีการปัดค่าจำนวนเต็ม
* คำสั่ง `abs(จำนวน)` ใช้ในการหาค่าสัมบูรณ์ \(absolute\)
* คำสั่ง `sqrt(จำนวน)` ใช้ในการหารากที่ 2
* คำสั่ง `pow(เลขฐาน,เลขชี้กำลัง)` ใช้หาค่าเลขยกกำลัง
* คำสั่ง `drand48()` ใช้ในการสุ่มตัวเลขจาก 0.0 ถึง 1.0
* คำสั่ง `arc4random()` ใช้ในการสุ่มตัวเลขจากข้อมูลชนิด UInt32
* คำสั่ง `arc4random_uniform(ขอบเขตบน)` ใช้ในการสุ่มตัวเลขชนิด UInt32 ตั้งแต่ 0 จนถึงขอบเขตบนที่กำหนด - 1 เช่น `arc4random_uniform(10)` คือ การสุ่มเลขจาก 0 ถึง 9

### NumberFormatter

เราสามารถจัดรูปแบบการแสดงผลของตัวเลขได้โดยใช้ NumberFormatter ซึ่งมีตัวอย่างการใช้งานดังนี้

```swift
let numFormat = NumberFormatter()
numFormat.numberStyle = .decimal  //ระบุว่าต้องการจัดรูปแบบเป็นเลขฐาน 10

//การจัดรูปแบบการแสดงตัวเลขเป็นข้อความด้วย string(for:)
if let result = numFormat.string(from: 10459) {
    print(result)   // 10,459
}

print(numFormat.string(from: 2956)!) //2,956
print(numFormat.string(from: 1352.567985)!) //1,352.568

//กรณีต้องการระบุจำนวนทศนิยมที่ใช้แสดงผล
numFormat.maximumFractionDigits = 2
print(numFormat.string(from: 1352.567985)!) //1,352.57

numFormat.minimumFractionDigits = 3
print(numFormat.string(from: 13.2)!) //13.200

```

สามารถศึกษาเกี่ยวกับ NumberFormatter เพิ่มเติมได้ที่ [https://developer.apple.com/documentation/foundation/numberformatter](https://developer.apple.com/documentation/foundation/numberformatter)

