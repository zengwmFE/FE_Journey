

### 原型对象是什么？
> 在javascript中，每定义一个对象（函数）时，对象中都会包含一些预定义的属性，其中函数对象的一个属性就是原型对象prototype,普通对象没有prototype,但有__proto__属性

![image](https://github.com/4lQuiorrA/FE_Journey/blob/master/image/js/prototype.png)


### 原型对象有什么用

> 面向对象开发、类的继承

**引申出构造函数**
- 使用new关键字调用的函数
- 构造函数可以实例化1个对象
- 返回值、默认返回类的实例
- 特殊情况
    1. 没有返回值（默认返回类的实例）
    2. 简单数据类型 （返回类的实例）
    3. 对象类型 （返回的对象）


### 原型链
![image](https://github.com/4lQuiorrA/FE_Journey/blob/master/image/js/__protot__.png)<br/>
**总结：**
1. 每个函数都有一个prototype的对象属性
2. 每个对象都有一个__proto__属性，该属性指向其父类的prototype

**那这个函数的prototype到底指向什么呢？**
> 其实，函数的 prototype 属性指向了一个对象，这个对象正是调用该构造函数而创建的实例的原型，也就是这个例子中的 person1 和 person2 的原型。<br>
> 可以这样理解：每一个JavaScript对象(null除外)在创建的时候就会与之关联另一个对象，这个对象就是我们所说的原型，每一个对象都会从原型"继承"属性。<br/>

![image](https://github.com/4lQuiorrA/FE_Journey/blob/master/image/js/Person.png)

### constructor

![image](https://github.com/4lQuiorrA/FE_Journey/blob/master/image/js/constructor.png)



**Object.constructor  === Function**