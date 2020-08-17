Obsidian is a Markdown-based note-taking and knowledge base app. 
Obsidian 是一个基于 Markdown 的笔记与知识库软件。

We currently support the formats below:<br>
目前，我们支持以下几种语法格式：

---

### Headers 标题

# This is a heading 1
## This is a heading 2
### This is a heading 3 
#### This is a heading 4
##### This is a heading 5
###### This is a heading 6

# 这是一号标题
## 这是二号标题
### 这是三号标题
#### 这是四号标题
##### 这是五号标题
###### 这是六号标题

---

### Emphasis 着重标记

*This text will be italic*<br>
_This will also be italic_<br>

*这是宋体字*<br>
_这也是宋体字_

**This text will be bold**<br>
__This will also be bold__<br>

**这是粗体**<br>
__这也是粗体__

_You **can** combine them_<br>
_你**可以**把它们结合起来使用_

---

### Lists 列表

- Item 1
- Item 2
  - Item 2a
  - Item 2b

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

- 项目一
- 项目二
  - 项目二 - 1
  - 项目二 - 2

1. 项目一
2. 项目二
3. 项目三
   1. 项目三 - 1
   2. 项目三 - 2

--- 

### Images 图片

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

---

### Links 链接

http://obsidian.md - automatic!<br>
[Obsidian](http://obsidian.md)

Markdown style links can be used to refer to either external objects, such as web pages, or an internal page or image. If there are spaces in the url, they can be escaped by either using `%20` as a space, such as [Export options](Pasted%20image), or by enclosing the target in `<>`, such as [Slides Demo](<Slides Demo>).

---

### Blockquotes 引用

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961

> 人类的赞歌就是勇气的赞歌。

\- *JoJo 的奇妙冒险，1989*


---

### Inline code 行内代码

Text inside `backticks` on a line will be formatted like code. 

被`反引号`括起来的文字会被解释为代码。


---

### Code blocks 代码块

Syntax highlight is supported with the language specified after the first set of backticks. We use prismjs for syntax highlighting, a list of supported languages can be found [at their site](https://prismjs.com/#supported-languages)

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
    
    Text indented with a tab is formatted like this, and will also look like a code block in preview. 
    
	缩进的文字被修饰成这样。同样，它在预览中看起来像代码块。

---

### Task list 任务清单

- [x] #tags, [links](), **formatting** supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
- [ ] tasks can be clicked in Preview to be checked off

- [x] #标签, [链接]() 的样式在这里同样支持。
- [x] 它使用列表语法；同时支持有序列表和无序列表。
- [x] 这是一个已完成的项目。
- [ ] 这是未完成的。
- [ ] 任务可以在预览模式下被勾选完成。
---

### Tables 表格

You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`:

First Header | Second Header
------------ | ------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

---

Tables can be justified with a colon | Another example with a long title
:----------------|-------------:
because of the `:` | these will be justified

If you put links in tables, they will work, but if you use Piped Links, the pipe must be escaped with a `\` to prevent it being read as a table element.

First Header | Second Header
------------ | ------------
[[Format your notes\|Formatting]]	|  [[Keyboard shortcuts\|hotkeys]]	

---

### Strikethrough 删除线

Any word wrapped with two tildes (like ~~this~~) will appear crossed out.

---

### Footnotes 脚注

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: meaningful!

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

You can also use inline footnotes. ^[notice that the carat goes outside of the brackets on this one.]

### Math
$$\begin{vmatrix}a & b\\
c & d
\end{vmatrix}=ad-bc$$

You can also do inline math like $e^{2i\pi} = 1$ .

## Obsidian specific

### Highlighting 荧光笔

Use two equal signs to ==highlight text==.

添加双等号来==使用荧光笔==。（可以在设置中自定义它的快捷键）

### Internal linking 内部链接

Link to a page: [[Internal link]].

链接到一个页面：[[像这样]]。

### Internal embeds 内联文件

Embed another file (read more about [[Embed files]]).

![[Obsidian]]


## Developer notes 开发者事项

We strive for maximum capability without breaking any existing formats, therefore we use a slightly unorthodox combination of flavors of markdown. It is broadly CommonMark, with the addition of some functionality from GitHub Flavored Markdown (GFM), some latex support, and our chosen embed syntax, which you can read more about at [[Accepted file formats]].
