---
title: ES6中新增的方式方法
date: 2020-10-04 13:52:48
tags:
---
### rest参数：用于把多余的参数放入数组里面 rest就是一个真正的数组，数组可以使用的方法都可以使用

``` bash 
    function add(...values){
      var sum = 0;
      for( item of values){
        sum += item;
      }
     return sum
    }
    console.log( add(1,2,3,4));  //10
    console.log(add(1,2,3,4,5));  //15
```
我们利用rest参数，可以向函数中传入任意个参数
***
BUT，rest参数只能作为函数中最后一个参数使用，即后面不能跟其他参数

### ES6中函数允许有默认值
``` bash 
    function func(x,y='cole'){
      console.log(x,y);
    }
    func('dylan')    //dylan cole
    func('dylan','babara') //dylan babara
    func('dylan','') //dylan
```
### 解构赋值
``` bash 
    function fn({x,y=2}){
      console.log(x,y);
    }
    fn({x:1});  //1 2
    fn({x:1,y:3});  //1 3
    fn({});  //undefined 2
    fn();  //Uncaught TypeError: Cannot destructure property 'x' of 'undefined' as it is undefined.
```

### 箭头函数
``` bash
    var f = v => v;
    // 相当于
    var f = function(v){
      return v;
    }
  // 如果箭头函数不需要参数或需要多个参数，就使用一个圆括号代表参数部分
    var f = () => v;
    // 相当于
    var f = function(){
      return v;
    }
```    
    
    
