# GitHub doc for markdown

This document is an exercise for [the GitHub doc](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

> 本仓库用来当作我个人的 markdown 语法参考，绝大部分内容都是 GitHub 官方文档的中文翻译。
> 欢迎大家分享自己对 markdown 的理解，和大家一起学习！

## Headings

最多可以加 6 个 # 在标题文本前。

<!-- markdownlint-disable-next-line -->
# The largest heading

## The second largest heading

<!-- markdownlint-disable-next-line -->
###### The smallest heading

## 给文本加样式

你可以在评论字段和 .md 文件中，使用加粗，斜体，删除线

### 加粗

语法：
`** **` 或
`__ __`  

`**This is bold text**`
<!-- markdownlint-disable-next-line -->
**This is bold text**  

### 斜体

语法：
`* *` 或 `_ _`  
`*This text is italicized*`  
*This text is italicized*

### 删除线

语法：
`~~ ~~`  
`~~This was mistaken text~~`  
~~This was mistaken text~~

### 粗体里面带斜体

`** **` + `_ _`  
`**This text is _extremely_ important**`  
**This text is _extremely_ important**  

### 既粗又斜

`*** ***`  
`***All this text is important***`  
***All this text is important***

### 引用文本

语法：> 打头  
`> Text that is a quote`  
> Text that is a quote  

小贴士：查看对话的时候，可以通过高亮文本，然后输入 r 来自动引用文本。通过点击 ... 然后点击 Quote reply 来引用整个评论。

### 引用代码

#### 行内引用

在一句话中，使用 ` 来引用代码或命令。  
反引号中的文本不会被格式化。

快捷键：`ctrl` + `e`  

#### 代码块

将代码独立成块的话，可以使用3个反引号。  

Some basic Git commands are:

```console
git status
git add
git commit
```

### 链接

[链接文本]  
(URL)  

快捷键：`ctrl` + `k`  

操作方式：复制URL链接，选中文本，按下快捷键  

`This site was built using [GitHub Pages](https://pages.github.com/).`  
`This site was built using [GitHub Pages](https://pages.github.com/).  

### 相对链接

在渲染出来的 markdown 文件中，定义相对链接和图片路径来帮助读者定位库中的其它文件。

相对链接相对的是当前文件，即 markdown 文件的所在位置。
比如说，你在库的根路径中，又一个 README 文件，
另一个文件位于 docs/CONTRIBUTING.md ,
那么，README 中，指向 CONTRIBUTING.md 的相对链接，应该是这样的：
  
`[Contribution guidelines for this project](docs/CONTRIBUTING.md)`  
[Contribution guidelines for this project](docs/CONTRIBUTING.md)

GitHub会根据你当前所在的分支，自动转换相对链接或图片路径。  
你可以使用所有的相对链接操作符，比如 `./` 和 `../`  

相对链接对于克隆了你的库的用户会更便利。
绝对链接很可能无法在克隆的库中使用，
我们推荐使用相对链接来引用库中的其它文件。  

### 图片

语法： `![文本](URL)`  
  
GitHub 支持将图片嵌入到 issue，pull request，discussions，comments 和 `.md` 文件。你可以展示一张库里的图片，添加一个在线图片的链接，或者是上传一张图片。  

小贴士：展示库中图片的时候，要使用相对链接，而不是绝对链接。  

例子：  

1、在相同分支的 .md 文件中展示图片
`/assets/images/electrocat.png`  

2、另一个分支的 .md 文件展示图片
`/../main/assets/images/electrocat.png`  

3、在库的 issues, pull requests, comments 中展示图片  
`../blob/main/assets/images/electrocat.png`  

4、在另一个库中的 `.md` 文件中展示图片  
`/../../../../github/docs/blob/main/assets/images/electrocat.png`  

5、在 issues, pull requests, comments 中，展示另一个库的图片  
`../../../github/docs/blob/main/assets/images/electrocat.png?raw=true`  

最后2个相对链接，如果图片在私库中，查看者只有对那个私库有读权限的时候，才能正常显示。  

### 在指定主题中显示图片

在 markdown 中，可以通过在图片 URL 的末尾，加上  
`#gh-dark-mode-only` 或 `#gh-light-mode-only`  
来指定一个主题，图片仅显示于这个主题中。  

我们区别了亮和暗两个色彩模式，所以只有2个选项可用。  
可以使用这2个选项来展示专门为暗背景或亮背景优化了的图片。  
这对于透明 PNG 图片特别有用。

1、暗主题  
`![GitHub Light](https://github.com/github-light.png#gh-dark-mode-only)`  

2、亮主题  
`![GitHub Dark](https://github.com/github-dark.png#gh-light-mode-only)`  

### 列表

#### 无序列表

语法：行首 `-` 或 `*`  

```markdown
- George Washington
- John Admas
- Thomas Jefferson
```

- George Washington
- John Admas
- Thomas Jefferson

#### 有序列表

<!-- markdownlint-disable-next-line-->
语法：行首 `数字. `

```markdown
1. James Madison
2. James Monroe
3. John Quincy Adams
```

1. James Madison
2. James Monroe
3. John Quincy Adams  

### 嵌套列表

在一个列表项下，将一个或多个列表项进行缩进，  
就可以创建嵌套列表了。  

语法：嵌套行的 `-` 或 `*` 对其上一行的文本头

```markdown
1. First list item
   - First nested list item
     - Second nested list item
```

1. First list item
   - First nested list item
     - Second nested list item

#### 如果不用等宽字体，如何判断嵌套缩进的字符数？

数一数，上一行正文前面有多少个字符，做相应的缩进即可，多少个字符对应多少个空格。

### 任务列表

语法：  
行首加 `- [x]` 或 `- [ ]`  

```markdown
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
```

- [x] #739
- [ ] <https://github.com/octo-org/octo-repo/issues/740>
- [ ] Add delight to the experience when all tasks are complete :tada:

如果任务的文字以 `(` 开头，需要使用 `\` 将其回退。  

`- [ ] \(Optional) Open a followup issue`  

### 提及个人和团队

语法：`@用户名` 或 `@团队名`  

团队例子： `@organization/team-name`  

此操作会触发通知，让他们关注到你的对话。  
如果编辑了一个评论，提及名字的人也会收到通知。  

`@github/support What do you think about these updates?`  

@github/support What do you think about these updates?  

当你 @ 一个父级团队的时候，子团队的成员也会接收到通知，
来简化多个团队之间的交流。  

输入 @ 以后带出的列表，只会显示库的协作者和帖子的参与者。  

### 引用 issues 和 pull requests

语法：输入 `#` 调起库中的 issues 和 pull requests  
输入 issue 或 pull request 的号码或标题，都可以进行过滤，  
然后输入 tab 或 回车 补完高亮的结果。  

### 引用外部资源

如果仓库配置了自定义的自动链接引用，那么指向一个 JIRA issue 或 Zendesk ticket 的引用，会转换为短链接。  

### 使用 emoji

语法：`:Emoji代码:`  

```markdown
@octocat :+1: This PR looks great - it's ready to merge! :shipit:
```  

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

输入 `:` 会调起建议列表  

### 脚注

语法：

- 引用
  - `[^脚注id]`
- 脚注本身
  - `[^脚注id]: 脚注内容`

```markdown
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.
```

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.

脚注的位置，无论你写在文章的哪里，都会在 markdown 的底部进行渲染。

### 通过评论来隐藏内容

语法：HTML comment 语法  

```markdown
<!-- This content will not appear in the rendered Markdown -->
```  

### 忽略 markdown 格式

语法：在 markdown 字符前，使用 `\` 来回退 markdown 格式  

```markdown
Let's rename \*our-new-project\* to \*our-old-project\*
```

Let's rename \*our-new-project\* to \*our-old-project\*  

### 禁用 markdown 渲染

查看 markdown 文件的时候，可以点击文件顶部的 <> 来禁用 markdown 渲染，并查看文件的源码。  
