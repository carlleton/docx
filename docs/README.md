<p align="center">
    <img alt="clippy the assistant" src="https://i.imgur.com/pwCV6L8.png">
</p>

<p align="center">
    使用JS/TS通过固有API轻松生成 .docx 文件. 适用于Node 和 浏览器。 :100:
</p>

---

# 欢迎

## 安装

```sh
npm install --save docx
```

你可以使用 `require` 或者 `import` 引入:

```js
let docx = require("docx");
```

```js
import * as docx from "docx";
```

## 基础用法

```js
var docx = require("docx");

// Create document
var doc = new docx.Document();

// Add some content in the document
var paragraph = new docx.Paragraph("Some cool text here.");
// Add more text into the paragraph if you wish
paragraph.addRun(new docx.TextRun("Lorem Ipsum Foo Bar"));
doc.addParagraph(paragraph);

// Used to export the file into a .docx file
var exporter = new docx.LocalPacker(doc);

exporter.pack("My First Document");

// Done! A file called 'My First Document.docx' will be in your file system if you used LocalPacker
```

## 荣誉成员

[@felipeochoa](https://github.com/felipeochoa)

[@h4buli](https://github.com/h4buli)

<p align="center">
    <img alt="clippy the assistant" src="http://i60.tinypic.com/339pvtt.png">
</p>

---

Made with 💖
