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


