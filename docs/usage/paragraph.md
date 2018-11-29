# 段落

> OpenXML中的所有内容 (文本, 图片, 图标等) 都以段落形式组织。

## 示例

您可以通过执行以下操作向锻炼添加更多文本：

```js
var paragraph = new docx.Paragraph(),
```

```js
var text = new docx.TextRun("Lorem Ipsum Foo Bar");
var paragraph = new docx.Paragraph();
paragraph.addRun(text);
```

```js
var paragraph = new docx.Paragraph("Short hand notation for adding text.");
```

创建段落后，必须将段落添加到`document`

```js
doc.addParagraph(paragraph);
```

## 样式

要创建样式，请参阅样式Wiki: https://github.com/dolanmiu/docx/wiki/Styling

![Word 2013 Styles menu](http://content.gcflearnfree.org/topics/233/style_apply_choose.png "Word 2013 Styles menu")

### 标题1 - 标题5

```js
paragraph.heading1();
paragraph.heading2();
paragraph.heading3();
paragraph.heading4();
paragraph.heading5();
```

### 标题

```js
paragraph.title();
```

## 文字对齐

段落的文本对齐方式：center、left、right、justified：

```js
paragraph.center();
```

```js
paragraph.left();
```

```js
paragraph.right();
```

```js
paragraph.justified();
```

### 示例

```js
paragraph.heading1().center();
```

它将创建一个名称为`heading 1`的样式，并且居中

## Thematic Break

要在页面中添加中断，只需在段落中添加一个`.thematicBreak()`：

```js
var paragraph = new docx.Paragraph("Amazing Heading").heading1().thematicBreak();
```

上面的示例将在标题下创建一个分页符。

## 分页符

要移至新页面（插入分页符），只需添加`.pageBreak()`一个段落：

```js
var paragraph = new docx.Paragraph("Amazing Heading").heading1().pageBreak();
```

上面的示例将创建一个标题，然后立即开始一个新页面。

### 分页前:

此选项（以单词提供）将确保段落将在新页面上开始（如果它尚未在新页面上）。

```js
var paragraph = new docx.Paragraph("Hello World on another page").pageBreakBefore();
```

![Page Break Before in Word](https://user-images.githubusercontent.com/34742290/40176503-df3a8398-59db-11e8-8b9c-d719f13aa8b4.png)

示例: https://github.com/dolanmiu/docx/blob/master/demo/demo15.js

## 分页控制

段落使用 `.keepLines()` 和 `.keepNext()` 两个方法限制段落内和段落之间的分页符。(请参阅 [this Microsoft article](https://support.office.com/en-us/article/Keep-lines-and-paragraphs-together-d72af534-926f-4c4b-830a-abfc2daa3bfa) 查看详情)
