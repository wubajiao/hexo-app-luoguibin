---
title: php define()与defined()函数区别
date: 2017-07-13 14:58:45
tags: php
categories: 后端
toc: true
---

有时经常混淆define() 和 defined(), 记录一下两者的用法。
<!-- more -->

# define() 
常量类似变量，不同住处在于：

* 常量在设定之后，它的值无法更改
* 常量名不需要开头的美元符号$
* 作用域不影响对常量的访问
* 常量值只能是字符串或者数字

语法：define(name,value,case_insensitive)


| 属性名 | 解释 | 
| --- | --- |
| name | 必需，常量的名称 | 
| value | 必需，设置常量的值 | 
| case_insensitive | 可选，规定常量的名称是否对大小写敏感。若设置为 true，则对大小写不敏感。默认是 false（大小写敏感） |

比如：
``` javascript
<?php
　　define("myWebsite","http://wuhaidong.me",true);
　　echo constant("mywebsite");    // constant()返回一个常量的值
?>
```
输出： http://wuhaidong.me

# defined()
常量定义之后，可以用 defined() 函数来判断是否定义了某个常量。defined()函数是检查某常量是否存在，如果存在，则返回ture,否则，返回false

``` javascript
<?php
　　define("myWebsite","http://wuhaidong.me");
　　echo defined("myWebsite");
?>
```
输出：true









