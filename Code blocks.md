# GitHub doc for markdown about [code block](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)

在单独划分出来的代码块中，分享代码示例，并启用语法高亮。  

## 划分代码块

语法：用`` ``` ``包裹代码  

GitHub官方推荐在代码块的前后，各安排一行空行，以便原始格式更加便于阅读。  

````javascript
```

function test() {
  console.log("notice the blank line before this function?");
}

```
````

```javascript
        function test() {
          console.log("notice the blank line before this function?");
        }
```

如果要在列表里面，保留代码块的格式，需要将未独立划分的代码块，进行缩进8个空格。  

如果要在独立划分代码块中，显示 3 个 backticks 的话，将它们包裹在4个 backticks 中。

`````markdown
````
```
Look! You can see my backticks.
```
````
`````

<!-- markdownlint-disable-next-line -->
````
```
Look! You can see my backticks.
```
````

### 语法高亮

在独立划分代码块中，可以添加一个可选的语言标识符，来开启语法高亮。

比如，Ruby 代码的语法高亮：

````markdown
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
````

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
