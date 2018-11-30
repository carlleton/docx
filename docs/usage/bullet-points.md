# 项目符号点

## 示例

要制作一个项目符号，只需将一个段落执行项目符号方法`.bullet()`：

```js
var text = new docx.TextRun("Bullet points");
var paragraph = new docx.Paragraph(text).bullet();

var text2 = new docx.TextRun("Are awesome");
var paragraph2 = new docx.Paragraph(text2).bullet();

doc.addParagraph(paragraph);
doc.addParagraph(paragraph2);
```

### 这将产生:

*   Bullet points
*   Are awesome
