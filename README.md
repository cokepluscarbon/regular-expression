正则元字符总结
==================

###匹配元字符

|字符      | 元字符         |匹配对象            |
|---------|----------------|------------------|
|.        |点号            | 匹配单个任意字符    |
|[...]    |字符组          | 匹配单个列出的字符  |
|[^...]   |排除型字符组     |匹配单个未列出的字符 |
|\char    |转义字符        |若char是元字符，或转义序列无特殊含义时，匹配char对应的字符 |

###计数元字符

|字符        | 元字符         |匹配对象            |
|---------|----------------|------------------|
|？       |问号             |匹配零或一次      |
|*        |星号            |匹配任意多次，包括零次  |
|+        |加号            |匹配至少一次 |
|{mix,max}|区间量词         |匹配至少mix次，最多max次 |

###位置元字符

|字符        | 元字符         |匹配对象            |
|---------|----------------|------------------|
|^       |脱字符            |匹配一行的开头位置   |
|$       |美元符            |匹配一行的结束位置  |
|\<      |单词分解符        |匹配单词的开头位置   |
|\>      |单词分解符        |匹配单词的结束位置   |

###其他元字符

|字符        | 元字符         |匹配对象            |
|---------|----------------|------------------|
||       |脱字符            |匹配任意分割的表达式  |
|(...)    |括号            |限定多选结构的范围，标注两次作用的元素，为反向引用“捕获”文本 |
|\num     |反向引用        |匹配第num个捕获括号的文本   |
