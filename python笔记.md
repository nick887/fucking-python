# python笔记
## 0. ZEN OF PYTHON
>Beautiful is better than ugly.  
>Explicit is better than implicit.  
>Simple is better than complex.  
>Complex is better than complicated.  
>Flat is better than nested.  
>Sparse is better than dense.  
>Readability counts.  
>Special cases aren't special enough to break the rules.  
>Although practicality beats purity.  
>Errors should never pass silently.  
>Unless explicitly silenced.  
>In the face of ambiguity, refuse the temptation to guess.  
>There should be one-- and preferably only one --obvious way to do it.  
>Although that way may not be obvious at first unless you're Dutch.  
>Now is better than never.  
>Although never is often better than *right* now.  
>If the implementation is hard to explain, it's a bad idea.  
>If the implementation is easy to explain, it may be a good idea.  
>Namespaces are one honking great idea -- let's do more of those  


## 1 数据类型
### 1.0字符串处理
* 删除空白
> ``` string.rstrip() ```去除右边空白
> ```string.lstrip()```去除左边空白
> ```string.strip()```去除左右空白
> 修改字符串使字符串去除两边空白```string=string.strip()```其他同理
* 大小写修改
> ```string.title()```单词首字母大写
> ```string.upper()```全部大写
> ```string.lower()```全部小写
* 字符串转化
> ```str(a)```将其他类型转化为字符串类型
* print字符串格式
> ```print("string")```括号中字符串可以加双引号也可以加单引号
### 1.1列表
* 列表访问
> 元素下标为0，1，2、、、
> 可以倒序访问，即```list[-1]```
* 列表增加
> ```list.append(object)```将新元素增加到列表末尾
> ```list.insert(index,object)```在下标index元素前添加元素object
* 列表删除
> ```del list[index]```删除下标为index的元素
> ```a=list.pop()```删除list末尾元素并将删除元素赋值给a
> ```a=list.pop(index)```删除下标为index元素并赋值给a
> ```list.remove(object)```删除列表中出现的第一个指定对象
* 列表组织
	- > ```list.sort()```对列表排序
	  > ```list.sort(reverse=True)```对列表反向排序
	  >  ```list.sorted()```输出一个排好序的列表，不改变原列表值
	- > ```list.reverse()```将列表反转
	- > ```len(list)```获取列表长度	  
### 1.2操作列表
* 列表遍历
> ```for item in list```
* 函数range()
> ```for i in range(i,j,x)```range为一个从i到j-1，步长为x，数字组成的列表
* 列表统计计算
> ```python
> max(list)//列表最大值
> min(list)//列表最小值
> sum(list)//列表和
> ```
* 列表解析
> 一种方便的构造列表的方法
> ```a=[value** for i value in range(1,10)]```
> 使代码更加简洁
* 列表切片
> ```python
> list[x:]//下标为x-1元素至末尾元素
> list[:x]//开头至下标为x-1元素
> list[x,y]//下标为x-1至y-1元素
> //x,y可以为负数
> ```
* 列表复制
> ```python
> a=b[:]//注意不可以使用a=b,a=b相当于给b一个别名a，未申请新的空间储存b的复制
> ```
### 1.3 元组
* 元组定义
> ```python
>  a= (object1,object2,object3,...)
> ```
> 元组的访问```a[index]```
* 元组赋值
> 元组中的元素不可被赋值，例```a[0]=250```
> 元组可以被赋值，例```a=(250,250)```

## 2 控制语句
### 2.0 if语句
* if语句格式
	* if结构
	```python
	if condition :
	...
	```
	* if-else结构
	```python
	if condition :
	....
	else :
	.....
	```
	* if-elif-else结构
	```python
	if condition :
	....
	elif condition1:
	.....
	elif condition2:
	......
	.....
	```
* if 语句检查多个条件
	* 与条件
	> ``` python
	> if condition1 and condition2 :
	> ..........
	> ```
	* 或条件
	> ``` python
	> if condition1 or condition2 :
	> ..........
	> ```
* 关键字 in
> in 判断元素是否在列表中
> ``` python
> if item in list ://在列表中
> ...........
> if item not in list://不在列表中
> .................
> ```

## 3 字典
* 字典的书写
字典中的基本元素由键值对组成，形式如下：
``` python
a={'x':'value1','y'='value2',....}
```
 * 访问字典
类似与访问列表，下标改为键值
```python
a['x']
```
* 增加键值对
通过赋值语句可以实现增加，若字典中存在则改变值  
不存在则增加此键值对
```python
a['x']=b
```
* 删除键值对
```python
del a['x']//删除键为'x'的键值对
```
* 遍历字典
  * 遍历字典元素
  ```python
  for i,j in a.items()//i为键，j为值
  ```
  * 遍历字典键
  ```python
  for i in a.keys()//注意此时的遍历以及将键值sorted
  ```
  * 遍历字典值
  ```python
  for i in a.values()
  ```
  * set()函数
  当列表中的值重复的较多，而我们不需要这样的重复的无效数据时可以使用set(list)函数  
  此函数通过列表输入生成一个集合类型，集合与列表类似，不同在于集合不含有重复元素
  ```python
  for i in set(a.values())
  ```
  * 嵌套字典
   * 列表嵌套字典
     ```python
     [{},{},{},...]
     ```
   * 字典嵌套列表
     ```python
     {
     a:[x,y,z,...],
     ...........
     }
     ```
   * 字典中有字典
     ```python
     {{},{},{},....}
     ```


## 3 交互输入与while
### 3.0 函数input()
>```a=input(string)//其中string为提示语不赋值给a```
>a为字符串类型值
### 3.1 函数int()
>```a=int(b)```
>将b转换为整数类型赋值给a
### 3.2 while结构
>```python
>while condition:
>	........
>```
>``` while list :```可同于判断列表是否为空
### 3.3 删除特定值元素
> ```python
>  while a in list :
> ......
> ```
## 4 函数
### 4.0 函数结构
>```python
>def abc():
>	.......
>```
### 4.1 关键字实参
>```python
>def abc(a,b):
>	.....
>abc(a=c,b=d)
>```
>在这种情况下不需要考虑顺序
### 4.2 默认值
>```python
>def abc(a,b=d):
>	......
>abc(x)
>```
>此时a赋值x，b为默认值d，注意需要把a放在第一位
### 4.3禁止函数修改列表
> ```python
> def abc(list)
> 	.....
> abc(list[:])
> ```
> 这种表示方法表示只能访问不能修改，传入的是list的副本
### 4.4 传递任意数量的参数
>```python
>def abc(*a)
>	.....//实际上a为一个列表类型，他的值由传入实参构成
>```
>a可以接受任意数量参数写入一个以a命名的元祖中
>注意：使用任意数量形参需要把形参写到最后
### 4.5 传递任意数量键值对参数
>```python
>def abc(**a)
>	......//实际上a是一个字典型值，他的值有传入实参构成
>abc(a='b',c='d')
>```
>
### 4.6函数模块
>```python
>import a//a.function()
>import a as b//b.function()
>from a import function//function()
>from a import *//function()
>```
## 5 类
### 5.0 类的定义
> ```python
> class Dog():
> 	def __init__(self,a,b):
> 		self.x=a
> 		self.y=b
> 	def function(self)
> 		......
> 	............
> ```
 ### 5.1类中元素与方法的使用
> ```python
> class Fuck():
> def __init__(self,a,b):
>    self.name=a
>    self.age=b
> def show(self):
>    print(self.name+"\n"+str(self.age)+"\n")
> wo=Fuck("nmd",12)
> print(wo.name)//使用元素
> wo.show()//使用方法
> ```
### 5.2类中元素的修改
> ```python
> class Fuck():
> def __init__(self):
>    self.name=""
> def change(self,name)
>    self.name=name
> wo=Fuck()
> wo.changr("fuck")//通过方法修改
> wo.name="fuck"//通过直接访问修改
> ```
### 5.3类的继承