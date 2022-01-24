# GitHub doc for markdown about [永久链接](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/creating-a-permanent-link-to-a-code-snippet)

## 指向代码的链接

这种类型的永久链接，只在自己的库中，会渲染为代码片段。  
在其它库中，永久链接会渲染成 URL 。  

1. 在 GitHub 上，定位到仓库的主页

2. 定位到你想链接的代码

   - 链接文件中的代码的话，导航到文件
   - 链接 pull request 中的代码的话，导航到 pull request ，点击 **± Files changed** 。然后，找到你想在评论中链接的代码所在的文件，点击 **View**

3. 选择是否是选中单独一行代码，还是多行代码：

   - 选择单独一行代码的话，可以点击行号来高亮这一行

   - 选择多行代码的话，点击这些代码所在范围的第1行的行号，来高亮这一行代码。然后，鼠标移动到代码所在范围的最后1行，按 `shift` ，然后点击行号，来高亮整个范围。

4. 左边点击 **...** ，在下拉菜单中，点击 **Copy permalink**

5. 导航到想要链接代码的对话

6. 在评论框中，粘贴 permalink ，并点击 **Comment**

## 指向 markdown 的链接

通过加载 markdown 文件而不渲染 markdown 的方式，来连接 markdown 文件中的某几行。  

语法：markdown 文件的 URL 后面，加上 `?plain=1` 参数，最后贴上 `#L` 来高亮某些行。

`github.com/<organization>/<repository>/blob/<branch_name>/README.md?plain=1#L14`

以上会高亮 README.md 的第14行代码
