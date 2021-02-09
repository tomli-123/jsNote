[TOC]

## 1.":" 后面的value都是字面量

```
可以是整型、小数、列表（数组）、字符串
```

------

## 2."="后面的value可以是表达式、字面量

```
可以是整数、长整数、浮点数、大浮点数、字符串、布尔、正则表达式、变量类型、nil类型、列表、列表LIst的赋值方式(一般使用"=”这样就不会报错，因为等号已经将":“的功能包含了)
```

------

## 3.nil类型

```
任何类型都比nil类型要大，用户传入null，将会自动被当作nil处理，nil打印为null
```

------

## 4.注意

```
set list.a : null 表示设置下标a属性为null
set list:a = null 表示删除下标

set map.a : null 表示 设置a属性是null
set map.a = null  表示删除a属性
set map.a = "null" 表示设置a属性是null
```

------

## 5.string.uuid() 自动生成uuid

```
UUID可以让分布式系统中的所有元素，都能有唯一的辨识信息，而不需要通过中央控制端来做辨识信息的指定。这样就不需要考虑数据创建时的名称重复问题。
```

------

## 6.GBK

```
GBK全称《汉字内码扩展规范》，即中文码
```

------

## 7.file.xlsx

```
用来编写xlsx文件 参数：name文件名 r/w/rw权限 [utf-8]|gbk编码
```

------

## 8.buffer.txt

```
用来缓存文件 参数： r/w/rw权限 [utf-8]|gbk编码
```

------

## 9.as

```
return下的as
返回值类型 重定向 http.file文件的返回形式 可选值有file和stream
```

------

## 10.当下载文件时请求方式为download

------

## 11.return：stream以文件流形式返回

```
   以文件流形式读文件
   {set:"stream", "=":"file('001.jpg','r')"},
   {return:"stream",as:"http.stream"}  
   以文件流形式写文件
   {set:"ostream", "=":"buffer.txt('w','utf8')"},
   {write:{format:"txt",content:""/*Q$={hello world!
   }=Q$*/},by:"ostream"},
   {return:"is.valueOf(string.valueOf(ostream))",
   as:"http.stream"}
```

------

## 12.return: with

```
可用来设置response Headers中的content-type。将来会支持设置response Headers中的任意属性
```

------

## 13.return: of

```
当as的值是http.file时，of 用来设置返回的文件名
{set:"name", "=":"'testWriteXlsx'+'.xlsx'"},
{return:"file",of:"name",as:"http.file"}
```

