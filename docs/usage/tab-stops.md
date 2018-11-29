# 制表符

> 制表符很重要，如果您不清楚它们是什么，[这里有一个链接解释](https://en.wikipedia.org/wiki/Tab_stop)。它可以实现并排文本，无需table或者不断按空格键。

**注意**: 目前，制表位的测量单位对于人类而言是反直觉的。它使用OpenXML自己的测量系统。例如，2268大致翻译为3厘米。因此，在将来，我可能会考虑将其更改为百分比甚至厘米。

![Word 2013 标签](http://www.teachucomp.com/wp-content/uploads/blog-4-22-2015-UsingTabStopsInWord-1024x577.png "Word 2013 Tab Stops")

只需在下面列出的段落中调用相关方法即可。然后只需`tab()`向文本对象添加方法调用。添加多个`tabStops`意味着您必须链接`tab()`直到`tabStop`选择所需的。示例如下所示。

## 示例

```js
var paragraph = new docx.Paragraph().maxRightTabStop();
var leftText = new docx.TextRun("Hey everyone").bold();
var rightText = new docx.TextRun("11th November 2015").tab();
paragraph.addRun(leftText);
paragraph.addRun(rightText);
```
上面的示例将在同一行上创建左对齐文本和右对齐文本。外行解决这个问题的方法是使用文本框或表格。YUK！

```js
var paragraph = new docx.Paragraph();
paragraph.maxRightTabStop();
paragraph.leftTabStop(1000);
var text = new docx.TextRun("Second tab stop here I come!").tab().tab();
paragraph.addRun(text);
```

以上显示了两个制表位的使用，以及如何选择/使用它。

## 左制表符
```js
paragraph.leftTabStop(2268);
```
2268是距离左侧的距离。

## 居中制表符
```js
paragraph.centerTabStop(2268);
```
2268是距离左侧的距离。

## 居右制表符
```js
paragraph.rightTabStop(2268);
```
2268是距离左侧的距离。

## 最大右侧制表符
```js
paragraph.maxRightTabStop();
```
这将在右侧的边缘创建制表位。方便对齐和左对齐文本在同一行。
