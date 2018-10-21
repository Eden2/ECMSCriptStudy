# 介绍
ECMAScript是Javascript的规范，JavaScript是ECMAScript语言的方言，JavaScript 
实现了多数 ECMA-262 中描述的 ECMAScript 规范，但存在少数差异。
## 基础
### 变量 变量命名规则：
* 第一个字符必须是字母，下划线或美元符号$
* 余下的字符可以是下划线、美元符号或者任何字母或者数字字符

匈牙利类型标记法：首字母小写表示类型，接下来字母大写。
如果把关键字作为变量名会报identifier expected

### 变量类型 ECMAScript中，变量可以存在两种类型的值，即原始值和引用值
原始类型：5种 即 Undefined、Null、Boolean、Number 和 String，用typeof 运算符可以输出类型，null被认为是对象的占位符，但从技术上来说，他仍然是原始值
对变量或值调用 typeof 运算符将返回下列值之一：
	•	undefined - 如果变量是 Undefined 类型的
	•	boolean - 如果变量是 Boolean 类型的
	•	number - 如果变量是 Number 类型的
	•	string - 如果变量是 String 类型的
	•	object - 如果变量是一种引用类型或 Null 类型的
    
	
下面的代码段测试该变量的值是否等于 undefined：
```
var oTemp;
alert(oTemp == undefined);
这段代码将显示 "true"
```
1. undefined 是声明了变量但未对其初始化时赋予该变量的值,undefined 实际上是从值 null 派生来的。
2. null 则用于表示尚未存在的对象。如果函数或方法要返回的是对象，那么找不到该对象时，返回的通常是null。
3. 

###  每行编码结尾的分号可有可无
### Numbel
当计算生成的数大于 Number.MAX_VALUE 时，它将被赋予值 Number.POSITIVE_INFINITY，意味着不再有数字值。
同样，生成的数值小于 Number.MIN_VALUE 的计算也会被赋予值 Number.NEGATIVE_INFINITY，也意味着不再有数字值。
如果计算返回的是无穷大值，那么生成的结果不能再用于其他计算。
NaN，表示非数（Not a Number）。这种情况发生在类型（String、Boolean 等）转换失败时
### String类型
*  arrayObject.toString()
*  booleanObject.toString()  输出true flase
*  dateObject.toString()     时间输出当前时间 Mon Aug 27 2018 13:57:52 GMT+0800 (CST)
*  NumberObject.toString()   number类型转为字符串，当调用该方法的对象不是Number时抛出TypeError异常。
*  array.toLocaleString() 
*  date.toLocaleString()     本地时间区表示2018/8/27 下午2:05:11
*  Number.toLocaleString()
*  stringObject.valueOf()    valueOf() 方法可返回 String 对象的原始值。原始值是由从 String 对象下来的所有对象继承的。valueOf() 方法通常由 JavaScript 在后台自动进行调用，而不是显式地处于代码中。
*  parseInt() 把非数字的值转化为数字
只有对 String 类型调用这些方法，它们才能正确运行；对其他类型返回的都是 NaN。
"12345red" == 12345
"0xA"      == 10
"56.9"     == 56
"red"      == NaN
### 类型转换
parseInt() 可以把二进制、八进制、十六进制或其他任何进制的字符串转换成整数
```
var iNum1 = parseInt("AF", 16);	//返回 175
var iNum1 = parseInt("10", 2);	//返回 2
var iNum2 = parseInt("10", 8);	//返回 8
var iNum3 = parseInt("10", 10);	//返回 10

```
parseFloat()转换成一个浮点数，如果对字符串解析直到到达数字的末端为止，然后以数字返回该数字
```
document.write(parseFloat("10")) 
document.write(parseFloat("10.00")) 
document.write(parseFloat("10.33")) 
document.write(parseFloat("34 45 66")) 
document.write(parseFloat(" 60 ")) 
document.write(parseFloat("40 years"))
document.write(parseFloat("He was 40"))

输出：
10
10
10.33
34
60
40
NaN

```
从首字母开始解析，首字母解析不出来就直接返回NaN了

### 引用类型
引用类型通常叫做类class，遇到引用值，所处理的就是对象。
下面的代码创建 Object 对象的实例：
```
var newObj = new Object()
```
Bool对象
Boolean 对象是 Boolean 原始类型的引用类型。
```
var oBoolObj = new Boolean(true)
```
String对象
String 对象是 String 原始类型的对象表示法，它是以下方式创建的：
```
var oStringObject = new String("hello world");

```
concat()方法
