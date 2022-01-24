# GitHub doc for markdown about [autolink](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls)

对 URL, issues, pull requests 和 commits 的引用会自动进行缩减，并转换成链接。  

## URLs

`Visit https://github.com`  

<!--
GitHub的官方文档上，这里是不需要加 <> 的。
但是光 https://github.com 违反了 markdownlint 的 MD034 规则，原因是，GitHub虽然会自动转换 URL ，但是很多 markdown parser 是不会的。所以加上 <> 以便 markdown 代码更加通用。
-->
Visit <https://github.com>  

## Issues 和 pull requests

在 GitHub 的对话中，对 issues 和 pull requests 的引用会自动转换成短链接。  

注意：自动链接的引用在仓库的 wiki 或 文件中，是不会创建的。  

引用类型 | 原始引用 | 短链接
-- | -- | --
Issue 或 pull request URL | `https://github.com/jlord/sheetsee.js/issues/26` | #26
`#` 加上 issue 或 pull request 编号 | `#26` | #26
`GH-`加上 issue 或 pull request 编号 | `GH-26` | GH-26
`Username/Repository#` 加上 issue 或 pull request 编号 | `jlord/sheetsee.js#26` | jlord/sheetsee.js#26
`Organization_name/Repository#` 加上 issue 或 pull request 编号 | `github/linguist#4039` | github/linguist#4039

如果再一个任务列表中，引用了 issue, pull request 或 discussion 的话，引用会自行展开，展示标题和状态。  

## Commit SHA

对 commit 的 SHA 的引用，会自动转换为短链接，指向 GitHub 上的 commit 。  

引用类型 | 原始引用 | 短链接
--|--|--
Commit URL | `https://github.com/jlord/sheetsee.js/commit/a5c3785ed8d6a35868bc169f07e40e889087fd2e` | a5c3785
SHA | `a5c3785ed8d6a35868bc169f07e40e889087fd2e` | a5c3785
User@SHA | `jlord@a5c3785ed8d6a35868bc169f07e40e889087fd2e` | a5c3785
`Username/Repository@SHA` | `jlord/sheetsee.js@a5c3785ed8d6a35868bc169f07e40e889087fd2e` | jlord/sheetsee.js@a5c3785

## 指向外部资源的自定义自动链接

如果仓库配置了自定义的自动链接引用的话，如果引用外部资源，比如 JIRA issue 或 Zendesk ticket，就会自动转换成短链接。如果想知道仓库中哪些自动链接可用，可以联系仓库管理员。
