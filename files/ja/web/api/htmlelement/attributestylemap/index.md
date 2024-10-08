---
title: "HTMLElement: attributeStyleMap プロパティ"
short-title: attributeStyleMap
slug: Web/API/HTMLElement/attributeStyleMap
l10n:
  sourceCommit: bba05bf24a714715f3517cf1296274dd41d6e811
---

{{APIRef("CSSOM")}}

**`attributeStyleMap`** は {{domxref("HTMLElement")}} インターフェイスの読み取り専用のプロパティで、生きた {{domxref("StylePropertyMap")}} を返します。これには、要素のインライン スタイル属性で定義されているか、スクリプト経由で {{domxref("HTMLElement")}} インターフェイスの {{domxref("HTMLElement.style", "style")}} プロパティを使用して割り当てられた、要素のスタイルプロパティのリストが入ります。

一括指定プロパティは展開されます。`border-top: 1px solid black` を設定すると、代わりに個別指定プロパティ ({{cssxref("border-top-color")}}, {{cssxref("border-top-style")}}, {{cssxref("border-top-width")}}) が設定されます。

{{domxref("HTMLElement.style", "style")}} プロパティと `attributeStyleMap` プロパティの主な違いは、`style` プロパティが {{domxref("CSSStyleDeclaration")}} オブジェクトを返すのに対し、`attributeStyleMap` プロパティは {{domxref("StylePropertyMap")}} オブジェクトを返すことです。

このプロパティ自身は書き込みできませんが、`style` プロパティを通じて返す {{domxref("CSSStyleDeclaration")}} オブジェクトと同様に、このプロパティが返す {{domxref("StylePropertyMap")}} オブジェクトを通じてインラインスタイルを読み書きすることができます。

## 値

生きた {{domxref("StylePropertyMap")}} オブジェクトです。

## 例

次のコードは `style` 属性と `attributeStyleMap` プロパティの関係を示しています。

```html
<div style="white-space: pre-line;">
  <div id="el" style="border-top: 1px solid blue; color: red;">要素の例</div>
  <div id="output"></div>
</div>
```

```css
#el {
  font-size: 16px;
}
```

```js
const element = document.getElementById("el");
const output = document.getElementById("output");

for (const property of element.attributeStyleMap) {
  output.textContent += `${property[0]} = ${property[1][0].toString()}\n`;
}
```

{{EmbedLiveSample("Examples", "200", "200")}}

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- {{domxref("HTMLElement.style")}}
- {{domxref("SVGElement.attributeStyleMap")}}
- {{domxref("MathMLElement.attributeStyleMap")}}
