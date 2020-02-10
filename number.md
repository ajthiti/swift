---
description: >-
  ตัวเลข เป็นข้อมูลพื้นฐานที่มีอยู่หลายแบบ เช่น Int, UInt, Double และ Float
  ซึ่งมักถูกใช้บ่อยในการเขียนโปรแกรมและการประมวลผลทางสถิติ ในภาษา Swift
  มีคุณสมบัติการรักษาสภาพของตัวแปร ดังนั้น จึงจำเป็นที่เรา
---

# Number

### Integer

Integer เป็นตัวแปรหรือค่าคงที่ ซึ่งใช้เก็บข้อมูลประเภทตัวเลขจำนวนเต็มทั้งค่าบวกและค่าลบ รวมถึงเลขศูนย์ ซึ่งตัวเลขเรานั้นจะต้องไม่มีทศนิยม เช่น 25, -3 หรือ 0 เป็นต้น

* ค่าเริ่มต้น คือ 0
* ขนาดข้อมูล 32 หรือ 64 บิต ขึ้นอยู่กับแพลตฟอร์มที่ใช้งาน 
* ช่วงของข้อมูล ตั้งแต่ -2,147,483,648 ถึง 2,147,483,647 \(สำหรับแบบ 32 บิต\) หรือตั้งแต่ -9223372036854775808 ถึง 9223372036854775807 \(สำหรับแบบ 64 บิต\)
* There are many variants of Integer type.e.g. `UInt`, `Int8`, `Int16` etc. The most common one you use is of `Int`.
* If you have a requirement to specify the size/type of integer a variable/constant can hold, you can store it more specifically using `UInt`, `Int8`, `Int16` etc. which we are going to explore below.

