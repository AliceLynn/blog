#概述
Markdown 是一种**轻量级标记语言**，它允许人们使用易读易写的纯文本格式编写文档，然后转换成格式丰富的HTML页面。 —— 来自[[维基百科](https://zh.wikipedia.org/wiki/Markdown)]

简单的来说，**Markdown就是用“标记符号”表示“格式”**。Markdown语法标签与HTML语法标签是**一一对应**的，比如Markdown的二级标题标签##就对应着HTML中的`<h2>...</h2>`标记，而且**Markdown是兼容HTML语法的**，如果你比较喜欢 HTML 的`<a>` 或 `<img>`标签，可以直接在Markdown文档中使用这些标记，而不用 Markdown 提供的链接或是图像标签语法。

#段落与换行

一个 **Markdown 段落**是由一个或多个连续的文本行组成，它的前后要有**一个以上的空行**（空行的定义是显示上看起来像是空的，便会被视为空行。若某一行只包含空格和制表符，也会被视为空行）。Markdown 允许段落内的强迫换行（插入换行符），普通段落不该用空格或制表符来缩进。

##标题
Markdown 支持两种标题的语法，类 [Setext](http://docutils.sourceforge.net/mirror/setext.html) 和类 [atx](http://www.aaronsw.com/2002/atx/) 形式。
类 Setext 形式是用底线的形式，利用 =（最高阶标题）和 -（第二阶标题）。
```
This is an H1
=========
         
This is an H2
----------------
```

显示效果：
This is an H1
=========
         
This is an H2
----------------
  

类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，例如：

```
# 这是 H1  

## 这是 H2  

#### 这是 H4

```

显示效果：
# 这是 H1  

## 这是 H2  

#### 这是 H4

  
##区块引用 Blockquotes
Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上`>`，最好和文字之间保留一个空格。

Markdown 也允许你偷懒只在整个段落的第一行最前面加上`>`
```

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,  

> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.  

> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.  

> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

```
显示出来会变成：
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,  

> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.  

> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.  

> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的`>`，而且引用的区块内也可以使用其他的 Markdown 语法哟，标题，列表，代码区快都可以用，还是很方便很优雅的~

举例：
```
> ## she
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,  

>>  consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.  

> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.  

> 
>> >  Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
>>  id sem consectetuer libero luctus adipiscing.
```

真实显示是这样的
> ## she
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,  

>>  consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.  

> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.  

> 
>> >  Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
>>  id sem consectetuer libero luctus adipiscing.

## 列表

列表格式也很常用，在 Markdown 中，你只需要在文字前面加上 - 就可以了。当然啦，在`-`、`1.`和文本之间也要保留一个字符的空格才是标准语法。
例如：

```
- 这是第一行 
- 这是第二行
- 这是第三行 
```
实际显示：
- 这是第一行 
- 这是第二行
- 这是第三行 

如果想要展示一个有序列表，也可以在文字前面加上 1. 2. 3.，例如：
``` 
1.文本1
2.文本2 
3.文本3
``` 
实际显示：
1.文本1
2.文本2 
3.文本3
