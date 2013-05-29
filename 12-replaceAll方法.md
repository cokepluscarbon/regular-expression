#12.replaceAll方法

正则表达式，主要用来进行字符串操作，许多语言都内置了很多正则表达方法。而String类的<code>replaceAll(String regex, String replacement)</code>就在最常用的方法之一。像在Java中，String类的方法<code>replace(String target, String replacement)</code>跟<code>replaceAll(String regex, String replacement)</code>是不同的，前者只支持普通的字符串替换，后者则支持正则表达式替换。

例如：

```java
String text = "Hello World!"
String result = text.replaceAll(".*", "#########");
System.out.println(result); // 输出#########

String text = "Hello World!";
String result = text.replaceAll("\\s","#");
System.out.println(result); // 输出Hello#World!
```

需要注意的是，在Java中的转义符为<code>\\</code>，而正则表达式的<code>\\</code>用来 **将下一个字符标记为一个特殊字符、或一个原义字符、或一个向后引用、或一个八进制转义符** 。所以在Java中，要表示正则表达式的<code>\s</code>需要两个<code>\\</code>，即<code>\\\s</code>。

如果在Java的正则表达式中表示<code>\\</code>，那该怎么写呢？在Java中表示<code>\\</code>使用<code>\\\</code>，而在正则中表示<code>\\</code>也用<code>\\\</code>，所以在Java的正则中要表示\则需要使用四个<code>\</code>，即<code>\\\\\\\</code>。例如替换文本中的<code>\\</code>为#：

```
text.replaceAll("\\\\", "#");
```


