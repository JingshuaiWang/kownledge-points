### 正则表达式函数
---
1. match_result =  match(pattern,string,flag=0)

2. match_result.end()  返回匹配的字符串的最后一个索引

3. match_result.start() 返回匹配的字符串的第一个索引

4. match_result.group() 返回匹配对象，若有子组，则.group(0) = .group()  .group(1)表示第一个子组  .group(2)表示第二个子组

5. match_result.groups() 返回全部子组的元组，若是匹配整个字符串，则返回一个空元组
match_result.span()

6. re.fdl(pattern,string) 把成功匹配的多个匹配对象放在数组中返回
7. re.finditer(pattern,string) 把匹配的对象存储在迭代器中返回
8. re.sub(pattern,reply,string) 用 repy 替换 string 中的 pattern,然后返回
9. re.subn(pattern,repy,string) 同上，只不过返回一个匹配成功的总数
10. re.split(pattern,string,maxsplit) 返回一个列表


正则表达式：
1. literal 字面匹配
2. re1|re2 匹配re1|re2
3. . 匹配任何一个字符
4. ^ 匹配字符串起始部分
5. $ 匹配字符串终止部分
6. * 匹配0次或者多次前面出现的正则表达式
7. + 匹配一次或者多次前面出现的正则表达式
8. ？匹配零次或者1次前面出现的正则表达式
9. {n} 匹配n 次前面出现的正则表达式
10. {n，m} 匹配 n 到 m 次前面出现的正则表达式
11. [...]  以从左到右的顺序匹配来自字符集的任一一个字符串
12. \d 匹配任何一个十进制数字
13. \w 匹配任何一个字母数字字符
14. \s 匹配任何一个空格字符



