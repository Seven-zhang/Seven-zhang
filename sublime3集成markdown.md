# sublime3集成markdown
## 1、sublime 安装支持markdown的插件
- #### *安装Markdown Editing和Markdown Preview 插件*

    markdown Editing插件支持markdown编写，Preview插件支持浏览器预览

>自定义快捷键，点击 Preferences --> 选择 Key Bindings User，输入：

```
    { "keys": ["alt+m"], "command": "markdown_preview", "args":{"target": "browser", "parser":"markdown"} },
```
>设置语法高亮和mathjax支持，Preferences -> Package Settings -> Markdown Preview -> Setting - User中添加如下参数：

```
{
    "enable_mathjax": true,
    "enable_highlight": true,
}
```

- #### *安装Monokai Extended & Markdown Extended插件*
    Monokai Extended插件扩展了Monokai主题，Markdown Extended插件支持代码高亮

## 2、markdown简单语法
### 代码块
如果要标记一小段行内代码，你可以用反引号把它包起来（`）

例如：

```
Use the `printf()` function.
```
效果如下：

Use the `printf()` function.

代码块有两种方式，一种用\```包含代码，另一种用四个空格或tab在每行代码前

例如：

    ```
    public void test(){
    System.out.println("helloword");
    }
    ```
效果如下：

```
    public void test(){
    System.out.println("helloword");
    }
```
### 代码块高亮
添加一个可选的语言标识符

例如：
    ```java
    public void test(){
        System.out.println("helloword")
    }
    ```
效果如下：
```java
    public void test(){
    System.out.println("helloword");
    }
```
### table表格
你可以创建表格，通过符号-分开第一行和其他行，通过|分开各个列
```
one  | two
---- | ---
123  | 456
789  | 000
```

效果如下：

one  | two
---- | ---
123  | 456
789  | 000

在标题行包含:，你可以使得表格向左对齐，向右对齐，居中，:在最左边表示左对齐，:在最右边表示右对齐，左右两边都有:表示居中

```
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```
效果如下：

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |


### 粗体和斜体
用两个\*\*包含一段文本表示粗体，用一个\*包含一段文本表示斜体

例如：

```
**当我跑步时** *我谈些什么*
```
**当我跑步时** *我谈些什么*

### 列表

Markdown 支持有序列表和无序列表。

无序列表使用星号、加号或是减号作为列表标记：
```
- one
- two
- three
```
效果如下：

- one
- two
- three

有序列表则使用数字接着一个英文句点：
```
1.  one
2.  two
3.  three
```
效果如下：

1.  one
2.  two
3.  three

### 标题
在文本前面加上 #
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
效果如下：

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

### 链接和图片
插入链接不需要其他按钮，你只需要使用 `[显示文本](链接地址)`
```
[markdown简单语法](http://www.jianshu.com/p/q81RER)
[atom编辑markdown](http://www.jianshu.com/p/f3fd881548ad)
```
效果如下：

[markdown简单语法](http://www.jianshu.com/p/q81RER)

[atom编辑markdown](http://www.jianshu.com/p/f3fd881548ad)

插入图片不需要其他按钮，你只需要使用 `![](图片链接地址)`
```
![](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg)
```
效果如下：

![](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg)

### 引用
在你希望引用的文字前面加上 >,> 和文本之间要保留一个字符的空格
```
> 一盏灯， 一片昏黄； 一简书， 一杯淡茶
```
效果如下：

> 一盏灯， 一片昏黄； 一简书， 一杯淡茶
