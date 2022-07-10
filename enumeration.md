---
description: >-
  Enumeration เป็นการกำหนด Type สำหรับชุดข้อมูลหนึ่งๆ
  ซึ่งมีความเกี่ยวข้องกันไว้ด้วยกัน เพื่อเป็นรายการที่ง่ายต่อการเรียกใช้
  และลดข้อผิดพลาดจากการกำหนดค่านอกขอบเขต
---

# Enumeration

การกำหนดค่า Enummeration เพื่อเป็นการสร้างชนิดข้อมูลแบบตัวเลือก สำหรับนำไปกำนดค่าที่เป็นไปได้ในเรื่องที่สนใจ เช่น ประเภททิศทางของเข็มทิศ เราจะทำได้ดังนี้\


```swift
enum CompassPoint {
   case north
   case east
   case south
   case west
}

var compassHeading:CompassPoint = .north

switch compassHeading {
  case .north:
    print("I am heading north")
  case .east:
    print("I am heading east.")
  case .south:
    print("I am heading south")
  case .west:
    print("I am heading west")
}

```



## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language (Swift 5.5)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-5-beta/id1002622538), Apple Inc., 2019. Available on: Apple Book Store.
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.

{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง**\
**ผู้เขียน** ธิติ ธีระเธียร  \
**วันที่เผยแพร่**  วันที่ 27 มิถุนายน 2565.\
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/closure](https://ajthiti.gitbook.io/swift/closure)\
**เงื่อนใขในการใช้งาน**\
****This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}
