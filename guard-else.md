---
description: >-
  Guard เป็นคำสั่งเงื่อนไขที่มีความคล้ายกับ If
  มักถูกใช้เพื่อการตรวจจับข้อผิดพลาดที่อาจเกิดขึ้นกับโปรแกรม
  โดยการทำงานตามคำสั่งภายในขอบเขตที่กำหนดเมื่อเงื่อไขเป็นเท็จ
---

# Guard-else

ตามปกติ เรามักใช้ if ในการสร้างชุดคำสั่งเพื่อดักจับความผิดพลาดที่อาจเกิดขึ้นในโปรแกรม ตัวอย่างเช่น การตรวจสอบการป้อนจำนวนเงินที่จะถอนออกจากเครื่อง ATM&#x20;

```swift
var balance: Int = 1000

func atmwithdrawMoneyl (amount: Int) {
    if amount <= 0 {
        print("จำนวนเงินไม่ถูกต้อง")
        return
    } else if amount > balance {
        print("ยอดเงินคงเหลือไม่เพียงพอ")
        return
    } else if amount % 100 != 0 {
        print("โปรดระบุยอดเงินที่ต้องการเป็นจำนวนเต็มร้อย")
        return
    } else {
        balance = balance - amount
    }
}
```

เมื่อใช้คำสั่ง guard-else ในการตรวจสอบ จะสามารถเขียนคำสั่งได้ดังนี้

```swift
var balance: Int = 1000

func atmwithdrawMoneyl (amount: Int) {
    guard amount > 0 else {
        print("จำนวนเงินไม่ถูกต้อง")
        return
    }
    
      guard amount <= balance else {
        print("ยอดเงินคงเหลือไม่เพียงพอ")
        return
    }
    
    guard amount % 100 == 0 else {
        print("โปรดระบุยอดเงินที่ต้องการเป็นจำนวนเต็มร้อย")
        return
    }
    
      balance = balance - amount
    
}
```



## แหล่งข้อมูลอ้างอิง

* **การเขียนโปรแกรม Swift และ iOS ฉบับพื้นฐาน**. บัญชา ปะสีละเตสัง. ซีเอ็ดยูเคชั่น. 2561

{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง**\
**ผู้เขียน** ธิติ ธีระเธียร  \
**วันที่เผยแพร่**  วันที่ 10 กรกฏาคม 2565\
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/guard-else](https://ajthiti.gitbook.io/swift/guard-else)\
**เงื่อนใขในการใช้งาน**\
****This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}
