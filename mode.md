###mode
---
1. 模块是类和函数或者可执行代码的组合

2. 导入模块 import mode_name

3. darwin 达尔文 是mac ox 系统的组成部分

4. PEP: 一个PEP就是一个python增强提案(python enancement proposal),新版特性被增加到python中的方式。需通过python开发社区和、PEP作者和实现者、Guido van Rossum的一致同意才可加入到新版python.

5. PEP8:python编码规范。

7. \ 可以让一个过长的语句分解成多行

8. 典型的模块的内部结构
	#起始行（Unix），python3中不需要定义
	#文档注释
	#模块导入
	#定义变量  也遵循使用此变量的函数或者类最近的地方定义
	#定义类
	#定义函数
	#主程序

9.如果模块被导入到其它模块那么__name__ = 模块名字。如果模块没有被导入到其它模块，那么__name__ = "__main__"

