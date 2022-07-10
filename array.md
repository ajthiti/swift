---
description: >-
  อาร์เรย์ คือ คอลเล็กชันซึ่งสามารถเก็บข้อมูลประเภทเดียวกันแบบเป็นลำดับ
  โดยข้อมูลนั้นจะอยู่ในตัวแปรหรือค่าคงที่ตัวเดียวกัน ข้อมูลแต่ละตัวของอาร์เรย์
  เรียกว่า Element ซึ่งมี Index กำกับตำแหน่งของข้อมูล
---

# Array

### การสร้างและจัดเก็บข้อมูล

การกำหนดค่าในอาเรย์ของภาษา Swift จะใช้ เครื่องหมาย \[ ] โดยค่าที่จัดเก็บในอาร์ย์จะต้องมี Type เดียวกันตัวอย่างเช่น

```swift
var numbers: [Int] = [3,5,7,9,11]
var names = ["Anne","Gary","Keith"]
```

เนื่องจากอาร์เรย์มีการจัดเก็บค่าเป็นแบบคอลเล็กชั่นซึ่งมีลำดับที่แน่นอน การเข้าถึงอีลีเม็นต์ต่างๆ ในอาร์เรย์ จะใช้การระบุตำแหน่งของ Index โดยเริ่มจาก 0, 1, 2, 3, ...

```swift
var names = ["Anne","Gary","Keith"]
let firstPerson = names[0]
print(firstPerson)
// Anne

names[1] = Paul
print(names)
//["Anne","Paul","Keith"]
```

การเพิ่มหรือลบสมาชิกในอาร์เรย์สามารถทำได้ด้วยการใช้คำสั่ง append, Insert และ remove

```swift
var friends = ["Anne","Paul","Keith"]
friends.append("Joe")
print(friends)
//["Anne","Paul","Keith", "Joe"]

friends.insert("Bob", at: 0)
print(friends)
//["Bob","Anne","Paul","Keith", "Joe"]

let paul = friends.remove(at: 2)
let joe = friends.removelast()
 print(friends)
//["Bob","Anne","Keith"]

friends.removeAll()
print(friends)
//[ ]
```
