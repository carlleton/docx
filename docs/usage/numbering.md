# 项目符号和有序编号

`docx.js`它的项目符号和有序编号非常灵活，允许用户在其样式和显示方面有很大的自由度。例如，可以使用阿拉伯数字，罗马数字甚至有序词（“一”，“二”，“三”……）来显示数字。该格式还支持在整个文档中重复使用项目符号/编号样式，因此使用相同样式的不同列表不需要重新定义它们。

由于这种灵活性，DOCX中的项目符号和有序编号涉及一些移动部件：
1. 文档级项目符号/编号定义（摘要）
2. 文档级项目符号/编号定义（具体）
3. 段落级项目符号/编号选择

## 文档级项目符号/编号定义（摘要）

每个文档都包含一组抽象编号系统定义，这些定义使用这些项目符号/编号定义段落的格式和布局。抽象编号系统定义如何为列表显示项目符号/数字，包括可能使用的任何子列表。因此，每个抽象定义包括一系列_级别_，从直观来看这些_级别_形成从0到顶级逐渐增大的序列，从中又形成了子列表，子子列表等。每个级别包括以下属性：

*   **level**: 这是堆栈中从0开始的索引
*   **numberFormat**: 表示应如何生成项目符号或编号。选项包括`bullet`(不用编号)，`decimal`(阿拉伯数字)，`upperRoman`,`lowerRoman`,`hex`和`hex`等等
*   **levelText**: 这是一个格式化的字符串，它使用`numberFormat`函数的输出并生成要在列表中的每个项之前插入的字符串。您可以使用`%1`,`%2`……来引用每个编号级别之前的数字。因此`%d)`具有数字格式的级别文本`lowerLetter`将导致序列"a)","b)"，...
*   以及其他一些，您可以在规范部分17.9.6中看到

## 文档级项目符号/编号定义（具体）

具体定义有点像是具体的子类抽象的定义。它们指定它们的父类，并被允许覆盖某些确定的级别定义。因此，两个列表仅在显示子子列表可以共享相同的摘要编号定义和具体定义略有不同。

## 段落级项目符号/编号选择

为了使用项目符号/有序编号（必须是具体的定义），段落需要选择它，类似将CSS class应用到dom元素上，使用具体的编号定义ID和级别编号应用到段落上。另外，MS Word和LibreOffice通常使用一个“ListParagraph”样式到一个编号的段落上。

## 在`docx`中使用项目符号/编号

`docx` 包含一个预定义的项目符号样式，您可以使用`para.bullets()`将它添加到您的段落中。如果您需要不同的项目符号或编号样式，您必须使用`docx.Numbering`这个类。

首先，您需要创建一个新的编号容器类，并使用它来创建抽象编号样式，定义您的级别，创建您的编号样式：

```js
const numbering = new docx.Numbering();

const abstractNum = numbering.createAbstractNumbering();
abstractNum.createLevel(0, "upperRoman", "%1", "start").addParagraphProperty(new Indent(720, 260));
abstractNum.createLevel(1, "decimal", "%2.", "start").addParagraphProperty(new Indent(1440, 980));
abstractNum.createLevel(2, "lowerLetter", "%3)", "start").addParagraphProperty(new Indent(2160, 1700));

const concrete = numbering.createConcreteNumbering(abstractNum);
```

然后，您可以使用对应项的`.setNumbering()`方法将具体样式应用于段落：

```js
topLevelP.setNumbering(concrete, 0);
subP.setNumbering(concrete, 1);
subSubP.setNumbering(concrete, 2);
```

最终，当您准备渲染文档的时候，你需要让输出端了解您的编号样式：

```js
const packer = new Packer(doc, undefined, undefined, numbering);
packer.pack(myOutput);
```
