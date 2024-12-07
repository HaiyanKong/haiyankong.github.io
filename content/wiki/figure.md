---
title: "Figure"
slug: "figure"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

> 本文内容：画图备忘录

# 类型

## 箱形图

{{<figure src="/wiki/plot-box-plot1.png" caption="Figure 1">}}

- *Q* 0/4：[最小值](https://zh.wikipedia.org/wiki/最小值)（minimum）
- *Q* 1/4：第1[四分位数](https://zh.wikipedia.org/wiki/四分位数)（lower quartile）
- *Q* 2/4：[中位数](https://zh.wikipedia.org/wiki/中位數)（第2[四分位数](https://zh.wikipedia.org/wiki/四分位数)、median）
- *Q* 3/4：第3[四分位数](https://zh.wikipedia.org/wiki/四分位数)（upper quartile）
- *Q* 4/4：[最大值](https://zh.wikipedia.org/wiki/最大值)（maximum）

以第1四分位数（*Q*1/4）和第3四分位数（*Q*３/4）的数值作为箱型的上下限。

{{<figure src="/wiki/plot-box-plot2.png" caption="Figure 2">}}

- 下边界=5
- 第1四分位数（Q1）=7
- 中位数、第2四分位数（median、Q2）=8.5
- 第3四分位数（Q3）=9
- 上边界=10
- 四分位间距（interquartile range，简称IQR）=(Q3−Q1)=2（即ΔQ)

当有数值与第1与第3四分位数的范围差距1.5×IQR以上时，该值为离群值（outlier）。

数值位于范围外1.5×IQR到3×IQR范围的数值，称作适度离群值（mild outlier）。
数值位于范围外3×IQR以上的数值，称作极端离群值（extreme outlier）。

因此该图中的离群值有：

- 适度离群值（mild outlier） = 3.5
- 极端离群值（extreme outlier） = 0.5

### reference

[维基百科](https://zh.wikipedia.org/wiki/箱形图)

# 配色

Colormap setup for standardizing commonly-plotting oceanographic variables

Repo: https://github.com/matplotlib/cmocean

Link: https://matplotlib.org/cmocean/

# 系列

## Friends Don't Let Friends Make Bad Graphs

This is an *opinionated* essay about good and bad practices in data visualization. Examples and explanations are below.

Repo: https://github.com/cxli233/FriendsDontLetFriends
