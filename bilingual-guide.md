# 双语文档标准（暂行）

本标准为一般性标准，具体文档项目可能需要根据实际情况进行一些灵活变动。

## 语言代码

双语文档的语言代码为 `xx-yy` 的形式，其中 `xx` 为译文语言代码，`yy` 为原文语言代码。如英译中的文档转换为双语文档后，其语言代码为 `zh-en`；法语译中文的文档转换为双语文档后，其语言代码为 `zh-fr`。

## 各级标题

各级标题中文在左，英文在右，中间用 `|` 分隔符进行分隔。

### 举例：

原文：

```
# 快速入门
```

转换成双语：

```
# 快速入门 | Quick Start
```

## 段落

段落英文在上，中文在下。如果 `MarkDown` 文本一个换行就能使生成的网页内容换行，则中英文之间不需要隔空行；否则需要一个空行。

### 举例：

原文：

```
欢迎来到 React 文档！本章节将介绍你每天都会使用的 80% 的 React 概念。
```

转换后：

```
Welcome to the React documentation! This page will give you an introduction to the 80% of React concepts that you will use on a daily basis.
欢迎来到 React 文档！本章节将介绍你每天都会使用的 80% 的 React 概念。
```

## 列表

### 有序列表

有序列表采用英文在上，中文在下的形式。英文部分采用正常数字标识，中文部分则改为无序列表标识（如 `-` 或者 `*`）。

#### 举例

```
1. 仅针对当前着手，显示“You are at move #…”而不是按钮。
2. 重写 `Board` 以使用两个循环来制作方块而不是对它们进行硬编码。
3. 添加一个切换按钮，使可以按升序或降序对落子的步数进行排序。
```

转换后：

```
1. For the current move only, show "You are at move #..." instead of a button.
- 仅针对当前着手，显示“You are at move #…”而不是按钮。
2. Rewrite `Board` to use two loops to make the squares instead of hardcoding them.
- 重写 `Board` 以使用两个循环来制作方块而不是对它们进行硬编码。
3. Add a toggle button that lets you sort the moves in either ascending or descending order.
- 添加一个切换按钮，使可以按升序或降序对落子的步数进行排序。
```

### 无序列表

无序列表采用英文在上，中文在下的形式。中英部分采用统一符号。

#### 举例

```
* **程序设计**——使用同样的技术决定你是否应该创建一个新的函数或者对象。这一技术即 [单一功能原理](https://en.wikipedia.org/wiki/Single_responsibility_principle)，也就是说，一个组件理想情况下应仅做一件事情。但随着功能的持续增长，它应该被分解为更小的子组件。
* **CSS**——思考你将把类选择器用于何处。(然而，组件并没有那么细的粒度。)
* **设计**——思考你将如何组织布局的层级。
```

转换后：

```
* **Programming**--use the same techniques for deciding if you should create a new function or object. One such technique is the [single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle), that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents. 
* **程序设计**——使用同样的技术决定你是否应该创建一个新的函数或者对象。这一技术即 [单一功能原理](https://en.wikipedia.org/wiki/Single_responsibility_principle)，也就是说，一个组件理想情况下应仅做一件事情。但随着功能的持续增长，它应该被分解为更小的子组件。
* **CSS**--consider what you would make class selectors for. (However, components are a bit less granular.)
* **CSS**——思考你将把类选择器用于何处。(然而，组件并没有那么细的粒度。)
* **Design**--consider how you would organize the design's layers.
* **设计**——思考你将如何组织布局的层级。
```

## 表格

表格中，表头内的文字采用左中文，右英文的形式，中间用 `/` 符号隔开。表身内的内容采用左中文，右英文的形式，中间用 `<br>`（用于换行）符号隔开。

### 举例

```
| 语法/Syntax          | 导出语句/Export statement                           | 导入语句/Import statement                         |
| -----------    | -----------                        | -----------                       |
| 默认/Default  | 示例一<br>Example One |示例二<br>Example Two|
| 具名/Named  | 示例三<br>Example Three  | 示例四<br>Example Four |
```

## 引用块/警告块

引用块/警告块格式按引用块内部内容决定。但是要记得保持同一个内容的两种语言在同一个引用块/警告块内。

### 举例

原文：

```
> [!NOTE]
> 
> To reduce the potential confusion between default and named exports, some teams choose to only stick to one style (default or named), or avoid mixing them in a single file. Do what works best for you!
```

转换后：

```
> [!NOTE]
> 
> To reduce the potential confusion between default and named exports, some teams choose to only stick to one style (default or named), or avoid mixing them in a single file. Do what works best for you!
> 
> 为了减少在默认导出和具名导出之间的混淆，一些团队会选择只使用一种风格（默认或者具名），或者禁止在单个文件内混合使用。这因人而异，选择最适合你的即可！
```

## 代码块

代码块暂时只转换注释内容。占据整行的注释采用上英文下中文的格式，行内注释采用左中文右英文的格式。如果是块级注释，则两种语言的注释包围在同一个块内。如果是左注释符号，右注释内容型的编程语言，则英文行内注释左边仍保留注释符号；如果是注释被注释符号左右包围，则中英文行内注释内容都包围在注释符号内。

### 举例

原文:

```
export default function MyApp() {
  // 示例注释
  return (
    <div>
      <h1>欢迎来到我的应用</h1>
      <MyButton title="我是一个按钮" /> // 示例行内注释
    </div>
  );
}
```


```
export default function MyApp() {
  // Example Comment
  // 示例注释
  return (
    <div>
      <h1>欢迎来到我的应用</h1>
      <MyButton title="我是一个按钮" /> // 示例行内注释 // Example Inline Comment
    </div>
  );
}
```

## 链接

链接内文字改为上英文，下中文。如果是内部链接，则两种语言的链接所指向的路径均改为双语版本路径。

### 举例

原文：

```
[示例链接](/zh/example)
```

转换后：

```
[Example Link](/zh-en/example)
[示例链接](/zh-en/example)
```

## 图片

图片不用变两份，但 alt 文本要转换成左中文右英文中间隔 `|` 的双语形式，如果可以请通过编辑图片将图片内文本弄成上英文下中文。

### 示例

原文：

```
![示例图片](/exampleImage.jpg)
```

转换后：

```
![示例图片 | Example Image](/exampleImage.jpg)
```

## 无需翻译的情况

有时一段文字会不需要翻译，比如函数名称、API 等。这时可以看情况决定。比如在列表中，如果只有一个条目不需要翻译，那么为了整齐，仍然将该条目复制成两份；如果所有条目都不需要翻译，那么就不需要复制条目了。

## 总结

这些规则看着很繁多，其实有很多规律可循。比如段落文本是上英下中，这是双语字幕的常见模式；比如标题左中文右英文，这是为了让 TOC 中的中文内容能够被看到，而不会因为标题太长而被隐藏；标题中间隔 `|`，是为了防止中文标题末尾是英文单词而导致混淆。本标准仍有很多需要完善和考虑不周的地方，也欢迎大家指出。
