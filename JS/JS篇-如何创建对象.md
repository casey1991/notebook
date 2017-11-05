# JS篇-如何创建对象

### 普通语法创建对象

```javascript
var o ={a:1}
```

### 使用构造函数创建对象

当new 作用于函数时，就使用了构造函数创建对象

```javascript
function Method(){
  this.num = [];
}
Method.prototype = {
  addNum: function(num){
    this.num.push(num);
  }
}
var m = new Method();
```

### 使用Object.create创建对象

ECMAScript5引入的新方法,

```javascript
var o = {a: 1};
var b = Object.create(o);
```

### 使用class关键字

```javascript
class obj{
  constructor(){}
}
```