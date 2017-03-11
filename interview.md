### interview
---
1. python性能优化？
	1.1 代码编写方面
	for i in list: print(i)   for i in range(len(list)): print(list[i])
	[x ** 2 for x in range(6)]    map(lambda x: x ** 2, range(6))
	import os  linesep_ = os.linesep #定义全局变量，接收os.linesep，暂时记录，避免多次查询os模块中的linesep变量
