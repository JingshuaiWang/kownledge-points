### function
---
1. 在函数体或者模块或者类的内部用 """ 文档字符串（docstring）""" 描述此函数体或者模块或者类的功能，最完善的注释可以让使用者直接通过文档字符串，就可以错作此函数体或者模块或者类。函数名.__doc__ 或者 类名.__doc__或者mode.__doc__ 打印出来。

2. 函数的返回值为 None 或者其它值。

3. 函数定义好之后，若不调用，则不会执行函数。

4. 函数的名称应该能尽可能反应出此函数的功能。

5. 函数外的变量名称与函数内部的变量名称可相同，分别存储在不同的作用域中，系统查找变量按照局部空间，全局空间的顺序查找。

6. 若函数内部希望使用外部变量，则需要在函数内部用 global 声明该外部变量

7. 定义函数的时候可以为参数设置默认值，成为默认参数，默认参数放在参数列表的第一位，其余为可选参数，python 并不能保证可选参数一定会出现。

8. 在顶层或者全局作用域定义的函数可以被其他函数内部直接调用。

9. capture一个错误时候，可以使用 raise捕获，然后用Except exception as e 可以打印出错误(e),这个e就是我们捕获的错误。

11. 函数内部嵌套函数，系统会形成函数调度栈，当前执行的函数位于栈顶，执行到return的时候，把此函数移除栈顶，然后把其它函数压栈到栈顶。

#### 内建函数builtIn function
---
1. print()
	```
	print("1", "2", "3");
	print("hello world", "%d---%s"%(3, "wuge"));
	print("hello world",);
	print('{} is a good man'.format("wuge"));
	```
2. range()
	```
	for i in range([0],len("wuge"),[step]):
		print(i);
	```
3. enumerate()#内建类，接收一个可迭代对象，然后返回一个迭代器，可调用next(iterator)
	```
	for i, v in enumerate("wuge"):
		print(i,v);
	```
4. reversed() #内建类，接收一个可迭代对象，返回一个迭代器，可调用next(iterator)
	```
	for i in reversed("wuge"):
		print(i);
	```
5. dir([parameter]) 传参数情况下，显示参数的属性。不传参数的情况下，显示全局变量名字。

6. help([parameter]) 显示对象的文档字符串。若不传参，则进入交互式帮助界面

7. open(filename,"r"/"a"/"w"/"rU"/"bU") #rU以只读方式打开，并提供通用换行符支持U universal

8. type(obj) 返回对象的类型

9. str(obj) 把对象转化为字符串类型

10. len(obj) 返回对象的长度

11. int(obj) 把对象转化为int类型

12. id(obj) 读取obj的内存地址

12. compile(code,filename,mode) 如：compile("for i in range(10): print(i)","","exec")  然后返回的对象为代码对象，
	代码对象可被exec()或者eval()或者single()函数执行，视code中语句而定，若含有表达式语句，则采用eval.若含有交互式命令，则采用single()

14. hex(num) #将数字转换为16进制，并以字符串的形式返回

15. otc(num) #将数字转换成8进制，并以字符串的形式返回

16. chr(num) #将一个数字转换为ascill对应的字符

17. odr(str) #将字符转换成ascill对应的数字，范围为1~255

18. abs(num) #求取绝对值并返回

19. divmode(num1, num2) #(num1//num2, num1%num2)

20. pow(num1, num2) #num1**num2

21. tuple(iterobj) #把可迭代对象转换成元组

22. list(iterobj) #把可迭代对象转换成列表

23. len(obj) #返回对象的长度，有几个字符组成。obj为非数字类对象

24. max(num1, num2, num3....) #求几个数字的最大值

25. min(num1, num2, num3....) #求几个数字的最小值

26. sorted(iter, reverse = False) #为可迭代对象排序，reverse默认为False，设置为True，则倒序。

27. sum(iterable, start = 0) #把可迭代对象相加，并加上start值，然后返回。iterable不可为str。

28. zip("ab", "cd", "ef"....) #把参数的首元素连接起来返回一个zip对象，调用__next__(),可得到连接首元素后的元组。

29. str.upper() #把str字母全部替换成大写

30. str.lower() #把str字母全部替换成小写

31. str.capitalize() #把str的首字母转换成大写

32. str.center(width) #把str扩充之长度为width，居中，左右两边设置空格。

33. str1.count(str2,start = 0, step = num) #返回str2在str1中出现的次数

34. b'str'.decode('utf-8') #以utf-8编码格式对b'str'解码

35. str.encode('utf-8') #以utf-8编码格式对str进行编码

36. str.find(str1) #查找str1是否在str中，并返回在str中的索引。

37. list.remove("e") #移除list中的e元素

38. list.pop(index) #通过索引移除列表中元素，并返回移除的元素

39. list.count("wuge") #"wuge"在列表中有多少个

40. del list[0] #移除列表中的第一个元素

50. del list #删除list的命名空间，使之不存在

51. iter(iterable) #接收可迭代对象，返回迭代器

52. dict_.keys() dict_.values() dict_items()

53. map(func, iterable) #接收一个函数和可迭代对象返回一个迭代器

54. filter(func or none, seq) #通过函数设定的规则，遍历序列

55. 匈牙利命名风格 o 代表object, i代表integer, a代表array, s代表string, f代表float, fn代表函数function, re代表正则表达

56. import os os是操作系统接口模块，通过它我们可以完成操作系统级别的任务，比如在不同平台上访问文件。

57. 句柄可操作的函数:read()和readlines()和write()和writelines()，pyhon不会强制加上或者去除换行符。需要程序员自己操作,去除换行操作符，用trip().

58. 若不用f.close()方法关闭一个文件，则有可能丢失输出到缓冲区的数据。


