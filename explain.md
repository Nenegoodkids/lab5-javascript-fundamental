# Week 5: JavaScript Fundamentals - Explain

## File

    01-variable.js
    02-functions.js
    03-control-flow.js
    04-loops.js
    05-integration.js

### 01-variable.js ผลลัพท์

D:\Work\Lab05-3>node 01-variables.js

=== Variables & Data Types Practice ===

Constants:
MAX_Users: 100
PI: 3.14159

Variable (let):

Count after increments: 2

=== Primitive Data Types ===
Numbers: 25 5.9 -10
Strings: John Doe
Booleans: isStudent: true isTeacher: false
null: null
undefined: undefined

=== Object Data Types ===
Array: [ 'apple', 'banana', 'orange' ]
First fruit: apple
Array length: 3
Object: { name: 'John', age: 25, city: 'Bangkok', isStudent: true }
Person name: John
Person age: 25

=== typeof Operator ===
typeof 25: number
typeof 'hello': string
typeof true: boolean
typeof undefined: undefined
typeof []: object
typeof {}: object
typeof (() => {}): function

=== Type Coercion ===
'5' + 2: 52
'5' - 2: 3
'5' \* 2: 10
true + 1: 2

Explicit coercion:
String(25): 25
Number('25'): 25
Boolean(1): true
Boolean(0): false
Boolean(''): false
Boolean('hello'): true

=== Challenge: Person Object ===
Student object:
{
firstName: 'Alice',
lastName: 'Smith',
age: 20,
gpa: 3.8,
courses: [ 'HTML', 'CSS', 'JavaScript' ],
isActive: true,
getFullName: [Function: getFullName],
getInfo: [Function: getInfo]
}
Full name: Alice Smith
Info: Alice Smith, Age: 20, GPA: 3.8
Courses: HTML, CSS, JavaScript

=== Truthy vs Falsy ===
Falsy values:
0: false
"": false
null: false
undefined: false
false: false
NaN: false

Truthy values:
1: true
hello: true
true: true
[]: true
{}: true
() => {}: true

✅ Activity 1 completed!

1.  การประกาศตัวแปร (const vs let)
    const: ใช้ประกาศค่าคงที่ (Constant) เช่น MAX_Users, PI ซึ่งค่าเหล่านี้จะไม่สามารถเปลี่ยนแปลงได้

let: ใช้ประกาศตัวแปรที่ค่าเปลี่ยนได้ เช่น count เริ่มต้นที่ 0 เมื่อใช้คำสั่ง count++ สองครั้ง ค่าจึงเพิ่มเป็น 2

2. ประเภทข้อมูลพื้นฐาน (Primitive Data Types)
   Numbers: แสดงตัวเลขทั้งจำนวนเต็ม (25), ทศนิยม (5.9) และติดลบ (-10)

Strings: ใช้ Template Literal (เครื่องหมาย backtick `...`) เพื่อแทรกตัวแปรลงในข้อความได้โดยตรง เช่น ${firstName} ${lastName} ทำให้ได้ผลลัพธ์ "John Doe"

Booleans: แสดงค่าความจริง (true) หรือเท็จ (false)

null & undefined:

null: คือค่าว่างที่ตั้งใจกำหนดให้ว่าง

undefined: คือตัวแปรที่ประกาศแล้วแต่ยังไม่ได้กำหนดค่า (let noValue;)

3. ข้อมูลประเภท Object (Object Data Types)
   Array: เก็บข้อมูลเป็นชุด การเข้าถึงข้อมูลตัวแรกใช้ index 0 (fruits[0] ได้ "apple") และใช้ .length เพื่อนับจำนวนสมาชิก

Object: เก็บข้อมูลเป็นคู่ Key-Value การเข้าถึงค่าใช้จุด (.) เช่น person.name

4. ตัวดำเนินการ typeof
   ใช้ตรวจสอบประเภทของข้อมูล สิ่งที่น่าสนใจในส่วนนี้คือ:

typeof [] ได้ผลเป็น "object" (นี่เป็นพฤติกรรมปกติของ JavaScript เพราะ Array ถือเป็น Object ชนิดหนึ่ง)

typeof (() => {}) ได้ผลเป็น "function"

5. การแปลงชนิดข้อมูล (Type Coercion)
   Implicit (อัตโนมัติ):

'5' + 2: เครื่องหมาย + เมื่อเจอกับ String จะทำการ ต่อข้อความ จึงได้ "52"

'5' - 2 และ '5' \* 2: เครื่องหมายทางคณิตศาสตร์อื่นๆ จะพยายามแปลง String เป็นตัวเลขก่อนคำนวณ จึงได้ 3 และ 10

true + 1: true มีค่าเท่ากับ 1 เมื่อบวก 1 จึงได้ 2

Explicit (ชัดเจน): การใช้ฟังก์ชัน String(), Number(), Boolean() เพื่อบังคับแปลงค่า

6. Challenge: Person Object (Object ที่มี Method)
   มีการสร้าง Object student ที่มีฟังก์ชันอยู่ข้างใน (เรียกว่า Method)

this keyword: ใน getFullName มีการใช้ this.firstName ซึ่ง this จะอ้างอิงถึงตัว Object student เอง ทำให้ดึงค่า Alice และ Smith มาแสดงได้

.join(", "): ใช้แปลง Array courses ให้เป็น String ข้อความเดียว โดยคั่นด้วยลูกน้ำ

7. Truthy vs Falsy
   ส่วนนี้แสดงให้เห็นว่าค่าใดบ้างเมื่อถูกแปลงเป็น Boolean แล้วจะเป็นจริงหรือเท็จ:

Falsy (เป็นเท็จ): ได้แก่ 0, "" (ข้อความว่าง), null, undefined, false, NaN

Truthy (เป็นจริง): คือค่าอื่นๆ ที่ไม่ใช่ Falsy รวมไปถึง Array ว่าง [] และ Object ว่าง {} ด้วย (สังเกตว่า [] เป็น true ซึ่งต่างจากบางภาษา)

### 02-functions.js ผลลัพท์

=== Functions & Arrow Functions Practice ===

Function Declaration:
Hello, John!
Hello, Alice!

Function Expression:
add(5, 3): 8
add(10, 20): 30

Arrow Function (full syntax):
multiply(4, 5): 20
Arrow Function (shorthand):
square(5): 25
double(10): 20
getRandom(): 42 <-- (ค่านี้จะเปลี่ยนไปเรื่อยๆ ระหว่าง 0-99)

Default Parameters:
Anonymous is 0 years old from Unknown
John is 0 years old from Unknown
John is 25 years old from Unknown
John is 25 years old from Bangkok

Rest Parameters:
sum(1, 2, 3): 6
sum(5, 10, 15, 20): 50
sum(): 0
sumWithReduce(2, 4, 6, 8): 20

Destructuring Parameters:
Alice, 22 years old, from Chiang Mai

Validation Function:
{ valid: false, message: 'Email is required' }
{ valid: false, message: 'Invalid email format' }
{ valid: false, message: 'Missing domain extension' }
{ valid: true, message: 'Email is valid' }

Returning Objects:
{
firstName: 'John',
lastName: 'Doe',
age: 30,
email: 'john.doe@example.com',
getFullName: [Function: getFullName],
getAge: [Function: getAge]
}
Email: john.doe@example.com
Full name: John Doe

Callback Function:
Original: [ 1, 2, 3, 4, 5 ]
Doubled: [ 2, 4, 6, 8, 10 ]
Squared: [ 1, 4, 9, 16, 25 ]

Challenge: Calculator
5 + 3 = 8
10 - 4 = 6
6 \* 7 = 42
20 / 4 = 5
2 ^ 10 = 1024
Using operate('add', 5, 3) = 8

✅ Activity 2 completed!

1. Function Expression & Arrow Functions (ส่วนที่ 2-3)
   Expression: การเก็บฟังก์ชันไว้ในตัวแปร (const add = function...)

Arrow Function (=>): นี่คือ Syntax ยอดนิยมที่สุดในปัจจุบัน

Implicit Return: ถ้ามีบรรทัดเดียว ไม่ต้องเขียน return และ {} เช่น const square = (x) => x \* x; (ค่าจะถูกส่งออกมาทันที)

2. Default Parameters (ส่วนที่ 4)
   ช่วยกัน Error ในกรณีที่คนเรียกฟังก์ชันลืมส่งค่ามา เช่น name = "Anonymous" ถ้าไม่ส่งชื่อมา จะใช้คำว่า Anonymous แทน

3. Rest Parameters ...args (ส่วนที่ 5) -- สำคัญมาก ⭐
   เครื่องหมาย ... (3 จุด) ตรงพารามิเตอร์ ทำหน้าที่ "รวบ" ค่าทั้งหมดที่ส่งเข้ามาให้กลายเป็น Array

ในโค้ด: sum(1, 2, 3) ตัว ...numbers จะแปลงเป็น [1, 2, 3] ทำให้เราวนลูปหาผลรวมได้ไม่ว่าจะส่งตัวเลขมากี่ตัวก็ตาม

4. Destructuring Parameters (ส่วนที่ 6) -- สำคัญมาก ⭐
   แทนที่จะรับ user แล้วมาเขียน user.name, user.age เราสามารถ "แตก" (Destructure) ตัวแปรตั้งแต่วงเล็บรับค่าเลย: function printUser({ name, age, city })

เทคนิคนี้ใช้บ่อยมากใน React (การรับ Props)

5. Validation & Early Return (ส่วนที่ 7)
   สังเกตว่าแทนที่จะเขียน if...else ซ้อนกันเยอะๆ โค้ดใช้วิธีเช็ค Error ก่อน ถ้าเจอ Error ให้ return ออกทันที ทำให้โค้ดอ่านง่ายและสะอาด (Clean Code)

6. Returning Objects & Shorthand (ส่วนที่ 8) -- สำคัญมาก ⭐
   Property Shorthand: ถ้าชื่อ key เหมือนกับชื่อตัวแปรที่รับมา ไม่ต้องเขียน firstName: firstName เขียนแค่ firstName, ได้เลย

Method Shorthand: เขียน getFullName() { ... } ได้เลย ไม่ต้องเขียน : function() { ... }

7. Callback Function (ส่วนที่ 9)
   คือการส่ง "ฟังก์ชัน" เข้าไปเป็น "พารามิเตอร์" ของฟังก์ชันอื่น

ในโค้ด processArray รับ callback เข้ามา แล้วเอาไปใช้กับข้อมูลแต่ละตัว (จำลองการทำงานของ .map() ใน JavaScript จริงๆ)

8. Challenge: Calculator (ส่วนที่ 10)
   เทคนิค this[operation] คือการเรียกใช้ฟังก์ชันใน Object แบบ Dynamic

this['add'](5, 3) มีค่าเท่ากับ calculator.add(5, 3)

### 03-control-flow.js ผลลัพท์

### 04-loops.js ผลลัพท์

### 05-integration.js ผลลัพท์
