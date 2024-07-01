# JavaScript và TypeScript Cơ bản

## JavaScript

### Biến và Kiểu dữ liệu

```javascript
// Khai báo biến và gán giá trị
let age = 30;
const name = "John";

// Kiểm tra kiểu dữ liệu của biến
console.log(typeof age);  // Output: number
console.log(typeof name); // Output: string
```
### Cấu trúc điều khiển và Vòng lặp
```javascript
// Cấu trúc điều khiển
let hour = 12;
if (hour < 12) {
    console.log("Good morning!");
} else if (hour < 18) {
    console.log("Good afternoon!");
} else {
    console.log("Good evening!");
}

// Vòng lặp
for (let i = 0; i < 5; i++) {
    console.log(i);  // In ra các số từ 0 đến 4
}
```
### Hàm
```javascript
// Hàm đơn giản
function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Alice"));  // Output: Hello, Alice!

// Hàm arrow
const square = (x) => x * x;
console.log(square(5));  // Output: 25
```
### Mảng và Đối tượng
```javascript
// Mảng
let numbers = [1, 2, 3, 4, 5];
console.log(numbers[2]);  // Output: 3

// Đối tượng
let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    greet: function() {
        return `Hello, ${this.firstName} ${this.lastName}!`;
    }
};
console.log(person.greet());  // Output: Hello, John Doe!
```
### Xử lý ngoại lệ
```javascript
try {
    // Code có thể gây lỗi
    let result = 10 / 0;
    console.log(result);  // Nếu không có lỗi, in ra Infinity
} catch (error) {
    console.error("Error:", error.message);
} finally {
    console.log("Finally block executed.");  // Luôn được thực thi sau try-catch
}
```
## TypeScript

### Kiểu dữ liệu và Biến
```javascript
// Biến và kiểu dữ liệu
let age: number = 30;
const name: string = "John";

// Kiểu union
let id: number | string;
id = 123;    // Hợp lệ
id = "456";  // Hợp lệ
```
### Hàm và Interface
```javascript
// Hàm và type annotations
function add(x: number, y: number): number {
    return x + y;
}
console.log(add(5, 3));  // Output: 8

// Interface
interface Person {
    firstName: string;
    lastName: string;
    age: number;
}

// Class implements interface
class Student implements Person {
    constructor(public firstName: string, public lastName: string, public age: number) {}

    greet(): string {
        return `Hello, ${this.firstName} ${this.lastName}!`;
    }
}

let student = new Student("Alice", "Smith", 25);
console.log(student.greet());  // Output: Hello, Alice Smith!
```
### Generics
```javascript
// Generics
function identity<T>(arg: T): T {
    return arg;
}

let output1 = identity<string>("Hello");
let output2 = identity<number>(123);

console.log(output1);  // Output: Hello
console.log(output2);  // Output: 123
```
