# 文档（Document）

> `Document` 对象是你开始创造 `.docx` 的起点,这是字面上的文档。您可以将所有内容添加到
> `Paragraphs`然后添加到这个 `Document`对象,最后根据您的需要导出。

要创建一个新文档，如下简单实现：

```js
var doc = new docx.Document();
```

## 文档属性

您可以通过指定选项向Word文档添加属性，例如：

```js
var doc = new docx.Document({
    creator: "Dolan Miu",
    description: "My extremely interesting document",
    title: "My Document",
});
```

### 完整的选项列表：

```
creator
description
title
subject
keywords
lastModifiedBy
revision
```

您可以混合匹配您想要的任何属性，或不提供任何属性。
