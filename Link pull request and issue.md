# GitHub doc for markdown about [link pull request to an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)

将 pull request 链接到一个 issue ，可以看到 bug 修复的进度，并在 pull request 合并时，自动关闭 issue 。

## 关于链接的 issue 和 pull request

既可以手动将 issue 和 pull request 关联，也可以在 pull request 的描述中，使用所支持的关键词进行关联。  

当你将 pull request 和 它所解决的 issue 链接起来的时候，写作者就能看到某人正在处理这个 issue 。  

当你将已经建立了链接的 pull request 合并到仓库的默认分支的时候，它所链接的 issue 就会自动关闭了。  

## 使用关键词将 pull request 链接到 issue

在 默认分支的 pull request 的描述或提交消息中，使用所支持的关键词，就可以将 pull request 链接到 issue 。  

- close
- closes
- closed
- fix
- fixes
- fixed
- resolve
- resolves
- resolved

如果你在一个 pull request 中引用了另一个 pull request 的话，那个 pull requst 就会链接起来。合并引用人 pull request 的话，会关闭被引用的 pull request 。  

用来关闭链接项的关键词语法，会基于 issue 和 pull request 是否在同一个仓库中，而有所不同。

被链 issue | 语法 | 例子
--|--|--
同一个仓库中的 issue | 关键词 #ISSUE-NUMBER | `Closes #10`
另一个仓库中的 issue | 关键词 OWNER/REPOSITORY#ISSUE-NUMBER | `Fixes octo-org/octo-repo#100`
多个 issue | 每个 issue 都需要使用完整语法 | `Resolves #10, resolves #123, resolves octo-org/octo-repo#100`

只有手动链接的 pull request 可以被手动取消链接。如果你使用了关键词创建链接，又想要取消链接的话，必须编辑 pull request 描述来删掉关键词。  

另外，也可以在 commit message 中使用关闭关键词。当你将 commit 合并进默认分支的时候，issue 就会被关闭，但是包含那个 commit 的 pull request 并不会被列为被链 pull request 。  

## 手动链接 pull request 和 issue

所有拥有库写入权限的人，都可以手动给 pull request 链接 issue 。  
可以给 pull request 链接最多**10**个 issue 。Issue 和 pull request 必须在相同的仓库中。  

1. 在 GitHub.com 上，导航到仓库主页
2. 在仓库名下方，点击 **Pull requests**
3. 在 pull request 列表中，点击想要链接 issue 的 pull request
4. 在右边的侧边栏，点击 **Linked issues**
5. 点击想要链接给 pull request 的 issue
