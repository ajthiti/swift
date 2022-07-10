---
description: Closure คือ กลุ่มของคำสั่ง ซึ่งสามารถถูกประกาศและถูกใช้ในส่วนต่างๆ ของโค้ด
---

# Closure

การใช้ Closure ในภาษา Swift นั้น มีความคล้ายกับการใช้งาน Lambda expression ในการเขียนโปรแกรมด้วยภาษา java หรือ C# ซึ่งจะช่วยให้เราสามารถเขียนคำสั่งได้สั้นและง่ายขึ้น รูปแบบทั่วไปของ Closure มีลักษณะดังนี้

```swift
{ 
    (parameter type, parameter type) -> return ReturnType in
    // คำสั่งเพื่อระบุการทำงานของ closure
    
}
```

ตัวอย่างการลดรูปการเขียนคำสั่งโดยใช้ Closure

```swift
//ตัวอย่างในการใช้งาน Function Type
func addTwoInt(_ firstInt: Int, _ secondInt: Int) -> Int {
    return firstInt + secondInt
}


var myFunc: (Int, Int) -> Int 
myFunc = addTwoInt
print(myFunc(7, 5))    // 12
```

เราอาจสามารถลดรูปได้ดังนี้

```swift
var myFunc =  {
    (firstInt: Int, secondInt: Int) -> Int in
    return firstInt + secondInt
}

print(myFunc(7, 5))    // 12
```

#### (1) การใช้ Closure ในรูปแบบที่ไม่มีการส่งค่ากลับ

```swift
let sayHello: () -> Void = {
    print("Hello!")
}
```

#### (2) การใช้ Closure ในแบบพารามิเตอร์

```swift
func mathOperate(firstNumer: Double, secondNumer: Double, with: (Double, Double) -> Double) -> Double {
    return with(firstNumer,secondNumer)
}

let max = mathOperate(firstNumer: 10.0, secondNumer: 5.0, with: {
    (firstNumber, secondNumber) in
        if firstNumber > secondNumber {
            return firstNumber
        } else {
            return secondNumber
        }
} )
```

## แหล่งข้อมูลอ้างอิง

* [The Swift Programming Language (Swift 5.5)](https://books.apple.com/th/book/the-swift-programming-language-swift-5-5-beta/id1002622538), Apple Inc., 2019. Available on: Apple Book Store.
* [App Development with Swift](https://books.apple.com/th/book/app-development-with-swift/id1465002990), Apple Inc., 2017. Available on: Apple Book Store.

{% hint style="info" %}
**รายละเอียดเพื่อการอ้างอิง**\
**ผู้เขียน** ธิติ ธีระเธียร  \
**วันที่เผยแพร่**  วันที่ 27 มิถุนายน 2564.\
**เข้าถึงได้จาก** [https://ajthiti.gitbook.io/swift/closure](https://ajthiti.gitbook.io/swift/closure)\
**เงื่อนใขในการใช้งาน**\
****This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).
{% endhint %}
