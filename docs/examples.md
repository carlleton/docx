# 示例

> 所有的示例都可以独立运行，可以在项目中的`/demo`目录中找到

以下所有示例都可以在本地运行，请运行以下命令：

```sh
npm run demo
```

该命令将在`/demo`目录运行`demo selector app`。它将提示您选择一个demo编号，该编号将在此目录运行demo

## 简单示例

一个简单基于`docx`库的hello world：

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo1.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo1.ts_

## 样式

### 使用JS设置样式

该示例显示了如何使用js自定义文档的样式

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo2.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo2.ts_

### 使用XMl设置样式

该示例显示了如何使用XML自定义文档的样式

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo13.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo13.ts_

## 编号

该示例显示了多级别编号

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo3.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo3.ts_

## 表格

简单表格示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo4.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo4.ts_

### 表格边框

设置表格的边框样式

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo20.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo20.ts_

## 图片

### 将图片添加到文档中

从文件系统路径导入图片

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo5.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo5.ts_

### 将图片添加到页眉页脚

以下示例显示了如何将图片添加到页眉页脚

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo9.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo9.ts_

### 缩放图片

以下示例显示了如何缩放图片

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo12.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo12.ts_

### 在添加到文档之前将图片添加到媒体

这是将图片添加到文档的最佳途径，因为您可以在两个位置使用相同的图片而不增加文档大小

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo23.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo23.ts_

### 添加图片到表格中

和之前相同，要将图片添加到表格中，您需要先添加`Media`对象

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo24.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo24.ts_

### 使用Base64的图片

如果您想替代为Base64格式的图片

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo18.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo18.ts_

## 边距

如何自定义边距，示例：

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo6.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo6.ts_

## 文档方向

定义文档的横向还是竖向，示例：

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo7.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo7.ts_

## 页眉页脚

添加页眉页脚示例：

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo8.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo8.ts_

## 多个页眉页脚

请检查`Sections`这个功能

## 分页功能

### 默认分页

添加分页示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo14.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo14.ts_

### 分页前

类似word中在段落之前添加分页示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo15.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo15.ts_

## 章节

章节示例。章节允许多个页眉页脚，允许多个横向竖向（`landscape`/`portrait`）在文档中。您也可以在不同章节使用不同的页码格式和首页设置。

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo16.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo16.ts_

## 脚注

添加脚注示例，适合参考

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo17.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo17.ts_

## 打包

## 缓冲输出

以下示例显示了如何使用缓冲区打包输出，然后将该缓冲区写入文件系统。

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo19.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo19.ts_


## 书签

在文档中使用书签创建内部超链接示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo21.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo21.ts_

## 双向文本

以下示例显示了如何为某些语言（如希伯来语）使用双向文本

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo22.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo22.ts_

## 橱窗

### 我的简历

添加页眉页脚示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo10.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo10.ts_

### 文档的样式和图片

自定义文档的外观并添加图片的示例

[Example](https://raw.githubusercontent.com/dolanmiu/docx/master/demo/demo11.ts ":include")

_Source: https://github.com/dolanmiu/docx/blob/master/demo/demo11.ts_
