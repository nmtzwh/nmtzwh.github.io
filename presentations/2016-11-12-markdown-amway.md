---
layout: presentation
title: Markdown amway
permalink: /presentation/
---

# 简介Markdown

好，开始介绍，这个博客唯一可以吸引到博主的亮点--Markdown（其实我觉得主题很简洁很美啊）。

首先，我们平时写的网页元素，都是由Markup，即：html语言写成的。其特点就是标签化的语句：

```markup
<html>
<body>
<h1>My First Heading</h1>
<p>My first paragraph.</p>
</body>
</html>
```

虽然html很利于排版，但是直接写起来很不方便，于是就有了markdown这种语法，可以很方便地“翻译”成html，同时兼容html输入。具体的教程，可以参考[这个cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)，或者[Ghost的帮助](https://help.ghost.org/hc/en-us/articles/224410728-Markdown-Guide)

---
class: inverse

# 基础知识

章节设置也很简单，比如：各级标题就用`#`表示，记得之后要加**空格**

```markdown
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag
```

对文字进行一些格式化（注意！与文字间没有空格）：

```markdown
斜体： *asterisks* or _underscores_
加粗： **asterisks** or __underscores__
同时加粗和斜体： **asterisks and _underscores_**
划掉(误，应该是左右各两个波浪线~）： ~~text~~
```

---

# 列表

```markdown
1. 数字加`.`，然后空格，表示一级有序列表；
3. 自动加1，与写的具体数字无关；
  1. 下一级列表，开头空2格
  2. 下一级列表

列表间由普通文字段落隔开，否则会连接在一起。

* 无序的列表可以用这三种符号加空格表示 asterisks
- Or minuses
+ Or pluses
```

---

# 超链接

`[显示的字符](https://www.google.com)`

插入图片的格式为（在Ghost中只需`![]()`，然后上传图片）：

`![名称](图片路径)`

特殊用法：页内跳转的链接这么写`[传送门](#portal)`，然后在目标处设置锚点`<a name="portal"></a>`。

---

# 快捷键

下表是Ghost里常用的快捷键：

| Result                                   | Markdown         | Shortcut           |
| ---------------------------------------- | ---------------- | ------------------ |
| **Bold**                                 | **text**         | Ctrl/⌘ + B         |
| *Emphasize*                              | *text*           | Ctrl/⌘ + I         |
| ~~Strike-through~~                       | ~~text~~         | Ctrl + Alt + U     |
| [Link](http://support.ghost.org/markdown-guide/) | [title](http://) | Ctrl/⌘ + K         |
| `Inline Code`                            | `code`           | Ctrl/⌘ + Shift + K |
| Image                                    | ![alt](http://)  | Ctrl/⌘ + Shift + I |
| List                                     | * item           | Ctrl + L           |
| Blockquote                               | > quote          | Ctrl + Q           |
| H1                                       | # Heading        |                    |
| H2                                       | ## Heading       | Ctrl/⌘ + H         |
| H3                                       | ### Heading      | Ctrl/⌘ + H (x2)    |

---

# 额外

简单吧！！！而且格式化之后排版很优雅。

如果你像我一样，有着各种奇怪的需求，这里是附加的功能（嗯，不是Ghost官方支持的）。

**代码块高亮**

因为时常要贴一些代码，所以对不同语言的高亮支持是必须的。这里采用[prism.js](http://prismjs.com/)实现，使用方法就是在代码块加入语言的名称，比如：


```python
import sys, math

def hash_fraction(m, n):
    ...
    if m < 0:
        hash_value = -hash_value
    if hash_value == -1:
        hash_value = -2
    return hash_value
```

***

### 公式

**LaTeX公式**

用MathJax实现，两种用法，行内的话就用单个`$`（似乎还有Bug），单行的用俩。比如：

```markdown
我们假设
$$\sigma = 1, \mu = 0$$

可以得到标准正态分布的概率密度函数：
$$G(x) = \dfrac{1}{\sqrt{2\pi}}e^{-\dfrac{x^2}{2}}$$
```

我们假设
$$\sigma = 1, \mu = 0$$

可以得到标准正态分布的概率密度函数：
$$G(x) = \dfrac{1}{\sqrt{2\pi}}e^{-\dfrac{x^2}{2}}$$
