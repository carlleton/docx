# 文本

段落中需要 `text run` 对象. 要创建文本:

```js
var text = new docx.TextRun("My awesome text here for my university dissertation");
paragraph.addRun(text);
```

文本对象具有改变文本显示方式的方法

## 强调重点

更多信息 [在这里](https://english.stackexchange.com/questions/97081/what-is-the-typography-term-which-refers-to-the-usage-of-bold-italics-and-unde)

### 加粗

```js
text.bold();
```

### 斜体

```js
text.italics();
```

### 下划线

```js
text.underline();
```

### 删除线

```js
text.strike();
```

### 双删除线

```js
text.doubleStrike();
```

### 上标

```js
text.superScript();
```

### 下标

```js
text.subScript();
```

### 全部大写

```js
text.allCaps();
```

### 小写

```js
text.smallCaps();
```

## 文本换行

有时您会希望将文本放在另一行文本下面但在同一段落中。

```js
text.break();
```

## 链接

如果要创建**粗体**和**斜体**的段落，该怎么办呢？

```js
paragraph.bold().italics();
```
