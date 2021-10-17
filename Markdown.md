# 1 Introduction（介绍）
Markdown is a text-to-HTML conversion tool for web writers. Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML).


Markdown 是一个面向网络作者的文本到 HTML 的转换工具。Markdown 允许您使用易于阅读、易于编写的纯文本格式进行编写，然后将其转换为结构上有效的 XHTML（或 HTML）。

Markdown is not a replacement for HTML, or even close to it. Its syntax is very small, corresponding only to a very small subset of HTML tags. The idea is not to create a syntax that makes it easier to insert HTML tags. In my opinion, HTML tags are already easy to insert. The idea for Markdown is to make it easy to read, write, and edit prose. HTML is a publishing format; Markdown is a writing format. Thus, Markdown’s formatting syntax only addresses issues that can be conveyed in plain text.

Markdown 不是 HTML 的替代品，甚至不是 HTML 的替代品。它的语法非常小，**仅对应于 HTML 标签的一个非常小的子集**。这个想法不是创建一种语法，使插入 HTML 标签变得更容易。在我看来，HTML 标签已经很容易插入了。**Markdown 的想法是让阅读、编写和编辑散文变得容易**。**HTML 是一种发布格式；Markdown 是一种书写格式**。因此，Markdown 的格式化语法仅解决了可以以纯文本形式传达的问题。

官网： <https://daringfireball.net/projects/markdown/>


# 2 语法

[2.1 段落](#21-段落)

[2.2 标题](#22-标题)

[2.3 块引用](#23-块引用)

[2.4 列表](#24-列表)

[2.5 代码块](#25-代码块)

[2.6 分割线](#26-分割线)

[2.7 链接](#27-链接)

[2.8 强调](#28-强调)

[2.9 代码](#29-代码)

[2.10 图片](#210-图片)

## 2.1 段落

定义：一行或多行连续的硬包装文本，段落中一个换行符相当于空格，段落间由一个或多个空行分隔。

硬包装文本 (hard-wrapped text) ：根据屏幕宽度，会自动进行换行的文本。

空行：只包含空格或制表符的行。

硬中断 (hard breaks) ：在段落内进行换行，使用两个或多个空格结束一行，然后键入"LF"

正常的段落不应该用空格或制表符缩进。




## 2.2 标题
两种样式：

### 2.2.1 "Settext" 样式：

使用 `=` 和 `-` 标记一级和二级标题:

    一级标题
    =======

    二级标题
    -------

效果：

> 一级标题
> =======
>
> 二级标题
> -------


## 2.2.2 "atx" 样式：

使用`#`，可表示1-6级标题:

    # 一级标题
    ## 二级标题
    ### 三级标题
    #### 四级标题
    ##### 五级标题
    ###### 六级标题

效果：

> # 一级标题
> ## 二级标题
> ### 三级标题
> #### 四级标题
> ##### 五级标题
> ###### 六级标题




## 2.3 块引用

可以使文本的左侧使用竖线连接起来，表示一个大块。

在段落的每行或者只在第一行使用符号 `>` ,还可使用多个嵌套引用：

    > ## 一级引用块标题
    >
    > 一级引用块
    > 
    > 1. 一级引用块列表
    > 2. 一级引用块列表
    >
    > > ### 二级引用块标题
    > >
    > >     二级引用块代码块
    > >     二级引用块代码块

    效果：
    > ## 一级引用块标题

效果：

> > 一级引用块
> > 
> > 1. 一级引用块列表
> > 2. 一级引用块列表
> >
> > > ### 二级引用块标题
> > >
> > >     二级引用块代码块
> > >     二级引用块代码块




## 2.4 列表

对段落文字自动悬挂缩进。


### 2.4.1 无序列表
以 `*`, `+`, `-` 为开头；后接最少一个空格，最多三个空格；再接段落：

    *   Red
    *   Green
    *   Blue

    +   Red
    +   Green
    +   Blue

    -   Red
    -   Green
    -   Blue

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.

效果：

> *   Red
> *   Green
> *   Blue
> 
> +   Red
> +   Green
> +   Blue
> 
> -   Red
> -   Green
> -   Blue
> 
> *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
> Aliquam hendrerit mi posuere lectus.Vestibulum enim wisi,
> viverra nec, fringilla in, laoreet vitae, risus.


### 2.4.2 有序列表

以数字加句点为开头；后接最少一个空格，最多三个空格；再接段落：

    1.  Bird
    2.  McHale
    3.  Parish

效果：

> 1.  Bird
> 2.  McHale
> 3.  Parish




## 2.5 代码块

代码块的文本内容不经过解释器，直接显示。

代码块中的每一行缩进至少4个空格或1个制表符：

        void main()
        {
        printf("Hello, Markdown.");
        }

效果：

>     void main()
>     {
>     printf("Hello, Markdown.");
>     }




## 2.6 分割线

在单独一行放置三个或以上的 `*`, `-`, `_` ,可以形成分割线：

    * * *

    ***

    *****

    - - -

    ---------------------------------------

    _ _ _

效果：

> * * *
> 
> ***
> 
> *****
> 
> - - -
> 
> ---------------------------------------
> 
> _ _ _




## 2.7 链接

页面内跳转(非官方支持)：
1. 以#开头
2. 包含 `.`, `_` `:`直接忽略掉，
3. 空格使用 `-` 横杠符号替代
4. 大写字母转换成小写

### "inline" 样式

    [### "inline" 样式](#"inline"-样式 "Title")

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

    See my [About](./about/) page for details.

效果：

> [### "inline" 样式](#"inline"-样式 "Title")
>
> This is [an example](http://example.com/ "Title") inline link.
> 
> [This link](http://example.net/) has no title attribute.
> 
> See my [About](./about/) page for details.


### "reference" 样式

    This is [an example][id] reference-style link.

    [id]: http://example.com/  "Optional Title Here"

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

    [google]: http://google.com/        "Google"
    [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
    [msn]:    http://search.msn.com/    "MSN Search"

效果：

> This is [an example][id] reference-style link.
> 
> [id]: http://example.com/  "Optional Title Here"
> 
> I get 10 times more traffic from [Google][] than from
> [Yahoo][] or [MSN][].
> 
>   [google]: http://google.com/        "Google"
>   [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
>   [msn]:    http://search.msn.com/    "MSN Search"




## 2.8 强调

斜体：用一个 '*' 或 '_' 将元素包裹。

粗体：用两个 '*' 或 '_' 将元素包裹。

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

效果：

> *single asterisks*
> 
> _single underscores_
> 
> **double asterisks**
> 
> __double underscores__




## 2.9 代码

使用反引号 `` ` `` 将其包裹。与预先格式化的代码块不同，代码表示普通段落中的代码：

    Use the `printf()` function.

    ``There is a literal backtick (`) here.``

效果：

> Use the `printf()` function.
>
>``There is a literal backtick (`) here.``




## 2.10 图片

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

    ![Alt text][id]

    [id]: url/to/image  "Optional title attribute"
