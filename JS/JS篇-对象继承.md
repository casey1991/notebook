# JS篇-对象继承

js被描述为基于原型的语言，每个对象都有一个原型对象

```javascript
function Person(){
  
}
var person = new Person();
//Person.prototype以及person.__proto__分别代表什么？
//当person创建后其__proto__指向原型对象(这里是Object)
//Person.prototype将用来定义可以被继承的方法属性
```

### Call配合Object.create继承

```javascript
function Person(first,last,age,gender,interests){
  this.name ={
    first,
    last
  };
  this.age = age;
  this.gender = gender;
  this.interests = interests;
}
Person.prototype.greeting = function(){
  console.log('Hi I\'m '+this.name.first+'.');
}
function Teacher(first,last,age,gender,interests,subject){
  Person.call(this,first,last,age,gender,interests);
  this.subject = subject;
}
Teacher.prototype = Object.create(Person.prorotype);//继承Person的原型对象中的方法

Teacher.prootype.greeting = function(){
  //可以重写
}
```

### extends继承

ES5语法

```javascript
class Person(){
  greeting(){
    
  }
}
class Teacher extends Person{
  gretting(){
    super.gretting();
  }
}
```