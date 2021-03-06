# 1 介绍

Python类库包含很多不同的组件。

Python包含的数据类型，通常被认为是Python核心的一部分，如`numbers`和`list`。Python核心定义了这些数据类型的形式，并且约束了这些数据类型的语义，但不完全定义它们的语义。（另一方面，Python核心定义了这些数据类型的语法，拼写，优先级）。

Python类库还包含内置函数和异常，这些内置函数和异常无需在python文件头部使用`import`即可在 Python 代码里使用。这些内置函数一部分是在Python语言核心里定义，但是大多数非必须的核心语义只在此描述。

大量的Python类库都由模块的集合所组成。也有很多方法可以剖析这个集合。一些模块是由 C 语言编写，构建在Python解释器上；另外一些模块是由Python编写，以源码的方式导入。一些模块提供了特定于Python的接口，比如打印堆栈信息；一些模块提供了特定于指定的操作系统的接口，比如访问特定的硬件；另外一些模块提供了特定的域名接口，比如`www`域名。一些模块可以在Python的所有版本上使用；一些模块需要底层操作系统的支持；然而另一些模块只能在Python编译和安装的时候指定才可用。

本手册是“由内及外”地来说明。首先描述内置的数据类型，然后描述内置函数和异常，最后按照章节的方式描述模块。章节的顺序以及模块在章节中的顺序排名不分先后。

这就意味着，你如果从头开始阅读该手册，跳到下一章节感到无聊时，你可从概览找你需要的Python类库。当然，你没有必要像阅读小说一样来从头到尾阅读该文档，可以浏览内容列表，或者从索引页查找指定的函数，模块，具体条目。最后，如果你学习`random`相关内容，你可以选择`random`页（参见`random`模块）来阅读。无论你阅读本手册顺序如何，假如你狠熟悉该手册的剩余部分，最好从Build-in Functions章节开始。

我们开始吧！



