# this指向问题

```js
//1. 全局作用域或者普通函数中this指向全局对象window（注意定时器里面的this指向window）
console.log(this);
function fn() {
    console.log(this);
}
fn();
window.setTimeout(function() {
    console.log(this);
}, 1000);

//2. 方法调用中谁调用this指向谁
var o = {
    sayHi: function() {
        console.log(this);
    }
}
o.sayHi();
var btn = document.querySelector('button');
btn.onclick = function() {
    console.log(this);
}

//3. 构造函数中this指向构造函数的实例
function Fun() {
    console.log(this);
}
var fun = new Fun();
```

