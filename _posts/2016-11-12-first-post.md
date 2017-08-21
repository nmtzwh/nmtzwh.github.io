---
layout: post
title: "安利 Markdown"
date: 2016-11-12
---


## 简介

+ ### 什么是`Markdown`？
  1. 一种**纯文本**的排版语法；
  2. 容易渲染成HTML，并由浏览器显示；

+ ### 为什么要用`Markdown`？
  1. Just write what's on your mind
  2. Do some **basic styling**
  3. Easily **collaborate** with others
  4. Share with and show to everyone


+ ### 安利的要点：**简单、美观、条理**。


---

## 应用场景

1. 做笔记（会议笔记、邮件、阅读摘要……）：
   + 纯文本，便捷地做笔记，而不需要在意排版（它会帮你完成）；
   + 很有条理，不需要后期归纳；
   + 方便插入链接、引用；
   + ​
2. 写说明（程序的ReadMe档，操作说明……）：
   + 支持代码高亮等功能；
   + 支持to-do list的功能；
   + 插入LaTeX公式；
   + ​
3. 写博客（甚至小说、日记……）：
   + 与笔记同理；
   + ​
4. 演示文稿：
   + 可以直接由笔记生成演示文稿，避免重复工作；


---
## 工具

只要一个记事本软件即可编写markdown，但是为了得到渲染的HTML，我们需要一些软件：

+ [Typora](http://www.typora.io/)：实时渲染出漂亮的结果，可以转为PDF、WORD等；
+ [Atom](https://atom.io/)：本身是很优秀的文本编辑器，自带markdown的转换；
+ 其他具有Markdown代码高亮的编辑器 + [GitHub](https://github.com/) / [StackEdit](https://stackedit.io/)

其实未渲染的Markdown纯文本可读性也很强。

---

## 基础

最基础的，空一行表示分段。

章节设置也很简单，比如：各级标题就用`#`表示，记得之后要加**空格**

```markdown
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag
```

对文字进行一些格式化（注意，这些符号与文字间**没有空格**）：

```markdown
斜体： *asterisks* or _underscores_
加粗： **asterisks** or __underscores__
同时加粗和斜体： **asterisks and _underscores_**
划掉(左右各两个波浪线~）： ~~text~~
```

---

## 列表

```markdown
1. 数字加`.`，然后空格，表示一级有序列表；
3. 自动加1，与写的具体数字无关；
  1. 下一级列表，开头空2格
  2. 下一级列表
```

```markdown
* 无序的列表可以用这三种符号加空格表示 asterisks
- Or minuses
+ Or pluses
```

```markdown
- [x] To-do list
- [ ] second entry
- [ ] third entry
```

1. 数字加`.`，然后空格，表示一级有序列表；
2. 自动加1，与写的具体数字无关；
   1. 下一级列表，开头空2格
   2. 下一级列表


---

## 链接和图片

+ 插入超链接的格式为：
  - `[显示的字符](https://www.google.com)`
+ 插入图片的格式为：
  - `![名称](图片路径：相对、绝对路径，或者网址)`
+ 特殊用法：页内跳转的链接这么写`[传送门](#portal)`，在目标处设置锚点`<a name="portal"></a>`

引用也很方便，在本行前加上`>`符号即可：
> Delling, D., Goldberg, A. V., Pajor, T., & Werneck, R. F. (2011). Customizable route planning. Lecture Notes in Computer Science (Including Subseries Lecture Notes in Artificial Intelligence and Lecture Notes in Bioinformatics), 6630 LNCS, 376–387. http://doi.org/10.1007/978-3-642-20662-7_32

![实例图片](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png "Markdown icon")

---

## 表格

`Markdown`对表格的支持还不太好，直接用文本表达也比较麻烦：

```
| Result                                   | Markdown           |
| ---------------------------------------- | ------------------ |
| **Bold**                                 | `**text**`         |
| *Emphasize*                              | `*text*`           |
| ~~Strike-through~~                       | `~~text~~`         |
| [Link](http://support.ghost.org/markdown-guide/) | `[title](http://your-link-url)` |
| `Inline Code`                            | backticks          |
| Image                                    | `![alt](http://your-image-url or path-to-your-image)`  |
| List                                     | `* item`           |
| Blockquote                               | `> quote`          |
| H1                                       | `# Heading`        |
```

但是在[软件](http://www.typora.io/)和[网站](http://www.tablesgenerator.com/markdown_tables)的帮助下，作为笔记性质的表格还是可以使用的。

---


### 表格效果：

|                  Result                  |                 Markdown                 |
| :--------------------------------------: | :--------------------------------------: |
|                 **Bold**                 |                `**text**`                |
|               *Emphasize*                |                 `*text*`                 |
|            ~~Strike-through~~            |                `~~text~~`                |
| [Link](http://support.ghost.org/markdown-guide/) |     `[title](http://your-link-url)`      |
|              `Inline Code`               |                backticks                 |
|                  Image                   | `![alt](http://your-image-url or path-to-your-image)` |
|                   List                   |                 `* item`                 |
|                Blockquote                |                `> quote`                 |
|                    H1                    |               `# Heading`                |

---


## 代码

在要贴一些代码时，对不同语言的高亮是很方便的。用`Markdown`加入代码块是很容易实现的（前后各3 个 **backtick**  ），例如：

```c++
#include "G4VisExecutive.hh"
#include "G4UIExecutive.hh"

#include "Randomize.hh"

//....oooOO0OOooo........oooOO0OOooo........oooOO0OOooo........oooOO0OOooo......

int main(int argc,char** argv)
{
  // Detect interactive mode (if no arguments) and define UI session
  //
  G4UIExecutive* ui = 0;
  if ( argc == 1 ) {
    ui = new G4UIExecutive(argc, argv);
  }
#ifdef G4MULTITHREADED
  G4MTRunManager* runManager = new G4MTRunManager;
#else
  delete runManager;
}
```

---



## 公式

用MathJax实现，用2个$将LaTeX的公式包围即可。比如：

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

---

## 参考

`Markdown`的语法很简单，基本上30分钟能看完基本的介绍，但是要熟练使用，偶尔还是需要查查语法，以下是一些比较好的参考资料：

+ [Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
+ [Ghost的帮助](https://help.ghost.org/hc/en-us/articles/224410728-Markdown-Guide)
+ [Markdown官网](http://daringfireball.net/projects/markdown/)
+ [Ghost博客的帮助](https://help.ghost.org/hc/en-us/articles/224410728-Markdown-Guide)
+ [Typora软件的帮助](http://support.typora.io/Markdown-Reference/)

