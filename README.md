# Decorator Pattern - Coffee

โปรเจกต์นี้เป็นการประยุกต์ใช้ **Decorator Pattern** กับระบบสั่งกาแฟ โดยสามารถเพิ่มส่วนประกอบต่าง ๆ เช่น Milk, Sugar และ Whipped Cream ให้กับกาแฟได้แบบไดนามิก โดยไม่ต้องแก้ไขคลาสกาแฟเดิม

## Author

**นางสาวรสริน เมืองหงษ์**

**รหัสนักศึกษา:** 673380289-4
**Section:** 1

## Design Pattern

**Decorator Pattern**

โครงสร้างหลักของโปรแกรมประกอบด้วย

* `Coffee` — Interface สำหรับกำหนดโครงสร้างของกาแฟ
* `Espresso` — Concrete Component
* `Americano` — Concrete Component
* `CoffeeDecorator` — Abstract Decorator
* `MilkDecorator` — เพิ่ม Milk ให้กับกาแฟ
* `SugarDecorator` — เพิ่ม Sugar ให้กับกาแฟ
* `WhippedCreamDecorator` — เพิ่ม Whipped Cream ให้กับกาแฟ
* `Main` — ใช้สำหรับทดสอบการทำงานของโปรแกรม

## Project Structure

```text
DecoratorPattern/
├── src/
│   ├── coffee/
│   │   ├── Coffee.java
│   │   ├── Americano.java
│   │   └── Espresso.java
│   │
│   ├── decorator/
│   │   ├── CoffeeDecorator.java
│   │   ├── MilkDecorator.java
│   │   ├── SugarDecorator.java
│   │   └── WhippedCreamDecorator.java
│   │
│   └── Main.java
│
├── Report_Decorator_Pattern.pdf
├── .gitignore
└── README.md
```

### Folder Description

#### `src/coffee/`

เก็บคลาสหลักของกาแฟ ได้แก่

* `Coffee.java` — กำหนด Interface ของกาแฟ
* `Espresso.java` — กาแฟ Espresso
* `Americano.java` — กาแฟ Americano

#### `src/decorator/`

เก็บคลาส Decorator สำหรับเพิ่มส่วนประกอบให้กับกาแฟ ได้แก่

* `CoffeeDecorator.java` — Abstract Decorator
* `MilkDecorator.java` — เพิ่ม Milk
* `SugarDecorator.java` — เพิ่ม Sugar
* `WhippedCreamDecorator.java` — เพิ่ม Whipped Cream

#### `src/Main.java`

ใช้สำหรับสร้าง Test Case และแสดงผลลัพธ์ของโปรแกรม

## How to Run

เข้าไปที่โฟลเดอร์ `src`:

```bash
cd src
```

Compile โปรแกรม:

```bash
javac coffee/*.java decorator/*.java Main.java
```

Run โปรแกรม:

```bash
java Main
```

## Test Cases

โปรแกรมทดสอบทั้งหมด 3 กรณี

### Test Case 1

```text
Configuration: Espresso
Description: Espresso
Total Cost: $2.00
```

### Test Case 2

```text
Configuration: Espresso + Milk
Description: Espresso + Milk
Total Cost: $2.50
```

### Test Case 3

```text
Configuration: Americano + Milk + Sugar + Whipped Cream
Description: Americano + Milk + Sugar + Whipped Cream
Total Cost: $3.90
```

## Note

ไฟล์ `.class` เป็นไฟล์ที่สร้างขึ้นจากการ Compile และถูกกำหนดไว้ใน `.gitignore` จึงไม่ถูกติดตามโดย Git

