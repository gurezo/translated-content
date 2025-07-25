---
title: columns
slug: Web/CSS/columns
---

CSS 属性 **`columns`** 用来设置元素的列宽和列数。

{{InteractiveExample("CSS Demo: columns")}}

```css interactive-example-choice
columns: 2;
```

```css interactive-example-choice
columns: 6rem auto;
```

```css interactive-example-choice
columns: 12em;
```

```css interactive-example-choice
columns: 3;
```

```html interactive-example
<section id="default-example">
  <p id="example-element">
    London. Michaelmas term lately over, and the Lord Chancellor sitting in
    Lincoln's Inn Hall. Implacable November weather. As much mud in the streets
    as if the waters had but newly retired from the face of the earth, and it
    would not be wonderful to meet a Megalosaurus, forty feet long or so,
    waddling like an elephantine lizard up Holborn Hill.
  </p>
</section>
```

```css interactive-example
#example-element {
  min-width: 21rem;
  text-align: left;
}
```

它是一个[简写属性](/zh-CN/docs/Web/CSS/CSS_cascade/Shorthand_properties)，可在单个方便的声明中设置 {{cssxref('column-width')}} 和 {{cssxref("column-count")}} 属性。与所有简写属性一样，任何省略的子值都将设置为其[初始值](/zh-CN/docs/Web/CSS/CSS_cascade/Value_processing#初始值)。

## 语法

```css
/* Column width */
columns: 18em;

/* Column count */
columns: auto;
columns: 2;

/* Both column width and count */
columns: 2 auto;
columns: auto 12em;
columns: auto auto;

/* Global values */
columns: inherit;
columns: initial;
columns: unset;
```

`columns` 属性可以按任何顺序指定为下面列出的一个或两个值。

### 取值

- `<'column-width'>`
  - : 理想的列宽，定义为 {{cssxref("&lt;length&gt;")}} 或 `auto` 关键字。实际宽度可以更宽或更窄以适合可用空间。See {{cssxref("column-width")}}。
- `<'column-count'>`
  - : 元素内容应分成的理想列数，定义为 {{cssxref("&lt;integer&gt;")}} 或 `auto` 关键字。如果此值和列的宽度都不是 `auto` ，则它仅指示允许的最大列数。请参阅 {{cssxref("column-count")}} 。

### 正式语法

{{csssyntax}}

## 例子

### HTML

```html
<p class="content-box">
  This is a bunch of text split into three columns using the CSS `columns`
  property. The text is equally distributed over the columns.
</p>
```

### CSS

```css
.content-box {
  columns: 3 auto;
}
```

### Result

{{EmbedLiveSample('例子', 'auto', 120)}}

## 规范

{{Specifications}}

{{cssinfo}}

## 浏览器兼容性

{{Compat}}
