---
title: "Hugo-Sewing Markdown Style"
date: 2024-05-15
author: Your Name
slug: hugo-sewing-markdown-style
draft: false
categories:
  - Hugo-Sewing
---

# Reference

- [https://hugo-ht.vercel.app/cn/2021/01/07/first-post-cn/](https://hugo-ht.vercel.app/cn/2021/01/07/first-post-cn/)

# H1 Markdown Style

## H2 Markdown Style
### H3 Markdown Style
#### H4 Markdown Style
##### H5 Markdown Style
###### H6 Markdown Style

## List 

- Water
- Water
	1. Water
	2. Water
- Water
  - Water
  - Water
  	1. Water
  	2. Water

## Table

| Water | *Water* | Water |
|---------|---------|---------|
| Water | Water | Water |
| **Water** | Water | Water |
| Water | Water | Water |

## Footnotes

What I cannot create, I do not understand[^1]. — Richard Feynman

## Quotes

> Je <del>memos</del>, donc je suis. — René Descartes fans

{{< blockquote author="René Descartes" link="https://github.com/eallion/memos.top" title="Source" >}}

<p>Je <del>memos</del>, donc je suis.</p>

{{< /blockquote >}}



## Math

For example, 

`$1 + 1 = 3$`

You can add Tags & References:

`$$p(x) = \frac{1}{\sigma \sqrt{2 \pi}} exp \left(-\frac{1}{2}\left[\frac{x-\mu}{\sigma}\right]^2\right)\tag{1.1}\label{eq1.1}$$`

Aligning equations are also possible, 

`\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}`

## Codes

You can type codes, like `this`. Or:

```javascript
// This is Javascript:
water = [1, 2, 3, 4, 5]
let a = 0;
for (let i = 0; i < 5; i++){
	if (water[i] > 3) {
		a += 1
	}
}
// How much is `a` now?
```


## Images

{{<figure src="/blog/hugo-sewing3.jpg" title="Title" caption="Caption" width="500">}}

[^1]: [Reference](https://hugo-ht.vercel.app/cn/2021/01/07/first-post-cn/)
