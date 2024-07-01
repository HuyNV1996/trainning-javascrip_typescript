# Thủ thuật xử lý mảng trong JavaScript

## Lặp qua mảng

### For Loop

```javascript
let numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);  // In ra từng phần tử của mảng
}
```
### ForEach
```javascript
numbers.forEach(function(number) {
    console.log(number);  // In ra từng phần tử của mảng
});
```
## Xử lý và biến đổi mảng
### Filter
```javascript
let evenNumbers = numbers.filter(function(number) {
    return number % 2 === 0;
});
console.log(evenNumbers);  // Output: [2, 4]
```
### Map
```javascript
let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});
console.log(doubledNumbers);  // Output: [2, 4, 6, 8, 10]
```
### Reduce
```javascript
let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});
console.log(doubledNumbers);  // Output: [2, 4, 6, 8, 10]
```
## Sắp xếp và tìm kiếm trong mảng
### Sort
```javascript
let sortedNumbers = numbers.sort(function(a, b) {
    return a - b;
});
console.log(sortedNumbers);  // Output: [1, 2, 3, 4, 5]
```
### Find
```javascript
let foundNumber = numbers.find(function(number) {
    return number > 3;
});
console.log(foundNumber);  // Output: 4
```
## Xoay vòng và đảo ngược mảng
### Reverse
```javascript
let reversedNumbers = numbers.reverse();
console.log(reversedNumbers);  // Output: [5, 4, 3, 2, 1]
```
### Slice
```javascript
let slicedNumbers = numbers.slice(1, 3);  // Lấy từ index 1 đến index 2
console.log(slicedNumbers);  // Output: [2, 3]
```
## Kiểm tra và thao tác với mảng
### Includes
```javascript
let isIncluded = numbers.includes(3);
console.log(isIncluded);  // Output: true
```
### Concat
```javascript
let moreNumbers = [6, 7, 8];
let combinedNumbers = numbers.concat(moreNumbers);
console.log(combinedNumbers);  // Output: [1, 2, 3, 4, 5, 6, 7, 8]
```
# Các bài toán thực tế có thể áp dụng.
## Lặp qua mảng và tính tổng
**Bài toán**: Tính tổng các phần tử trong mảng.
```javascript
let numbers = [1, 2, 3, 4, 5];

// Sử dụng phương thức reduce để tính tổng
let sum = numbers.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
}, 0);

console.log("Tổng các phần tử trong mảng:", sum);  // Output: 15
```
## Lọc các phần tử thỏa mãn điều kiện.
**Bài toán**: Lọc ra các số chẵn từ mảng.
```javascript
let numbers = [1, 2, 3, 4, 5];

// Sử dụng phương thức filter để lọc các số chẵn
let evenNumbers = numbers.filter(function(number) {
    return number % 2 === 0;
});

console.log("Các số chẵn trong mảng:", evenNumbers);  // Output: [2, 4]
```
## Biến đổi các phần tử của mảng.
**Bài toán**: Nhân đôi giá trị của mỗi phần tử trong mảng.
```javascript
let numbers = [1, 2, 3, 4, 5];

// Sử dụng phương thức map để nhân đôi giá trị của mỗi phần tử
let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});

console.log("Mảng gốc:", numbers);
console.log("Mảng sau khi nhân đôi:", doubledNumbers);  // Output: [2, 4, 6, 8, 10]
```
## Tìm phần tử đầu tiên thỏa mãn điều kiện
**Bài toán**: Tìm số lớn hơn 3 đầu tiên trong mảng.
```javascript
let numbers = [1, 2, 3, 4, 5];

// Sử dụng phương thức find để tìm số lớn hơn 3 đầu tiên
let foundNumber = numbers.find(function(number) {
    return number > 3;
});

console.log("Số lớn hơn 3 đầu tiên trong mảng:", foundNumber);  // Output: 4
```
## Sắp xếp mảng
**Bài toán**: Sắp xếp mảng theo thứ tự giảm dần.
```javascript
let numbers = [5, 2, 8, 1, 3];

// Sử dụng phương thức sort để sắp xếp mảng
let sortedNumbers = numbers.sort(function(a, b) {
    return b - a;
});

console.log("Mảng sau khi sắp xếp giảm dần:", sortedNumbers);  // Output: [8, 5, 3, 2, 1]
```
## Kết hợp các mảng
**Bài toán**: Kết hợp hai mảng và loại bỏ các phần tử trùng lặp.
```javascript
let numbers1 = [1, 2, 3];
let numbers2 = [3, 4, 5];

// Sử dụng phương thức concat và Set để kết hợp mảng và loại bỏ phần tử trùng lặp
let combinedNumbers = [...new Set(numbers1.concat(numbers2))];

console.log("Mảng kết hợp và loại bỏ trùng lặp:", combinedNumbers);  // Output: [1, 2, 3, 4, 5]
```
## Đảo ngược mảng
**Bài toán**: Đảo ngược thứ tự các phần tử trong mảng.
```javascript
let numbers = [1, 2, 3, 4, 5];

// Sử dụng phương thức reverse để đảo ngược mảng
let reversedNumbers = numbers.reverse();

console.log("Mảng sau khi đảo ngược:", reversedNumbers);  // Output: [5, 4, 3, 2, 1]
```