# jstdg7
JavaScript: The Definitive Guide (7th Edition) 学习笔记

函数

```javascript
function plus1(x) {
    return x + 1;
}

plus1(3)	// 4

let square = function(x) {
    return x * x;
}

square(plus1(3))	// 16
```

ES6 及之后，简洁语法使用 `=>` 箭头函数

```javascript
const plus1 = x => x + 1;
const square = x => x * x;
plus1(3) // 4
square(plus1(3)) // 16
```

自定义对象方法

```javascript
let points = [
    {x: 0, y: 0},
    {x: 1, y: 1}
];

// 关键字 this 是方法所在的对象，也就是前面定义的数组 points
points.dist = function() {
    let p1 = this[0];
    let p2 = this[1];
    let a = p2.x - p1.x;
    let b = p2.y - p1.y;
    return Math.sqrt(a * a + b * b); // 毕达哥拉斯定理
};

points.dist() // Math.sqrt(2)
```

