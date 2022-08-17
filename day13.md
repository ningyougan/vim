语法：末行模式 :[range]s[ubstitute]/<pattern>/<string>/[flags]
1、匹配范围 range：
- $：当前行到尾行
- %：全文
- number,number：行号范围
2、待替换字符 pattern
3、替换的字符 string
4、flags：
- g：s默认替换每行的第一个目标字符，指定flags g 替换所有的目标字符
- c：进入选择模式，输入以下字符执行不同的功能
-- y：替换当前字符
-- n：跳过当前字符
-- a：替换所有字符
-- q：不执行强制退出
-- l：替换当前字符并退出
5、可视化模式下选择后替换自动输入 range
6、多选：
- gb：选取当前字符，多次按键同时选择，便于批量替换

:s/done/todo
:%s/done/todo

v :s/done/todo