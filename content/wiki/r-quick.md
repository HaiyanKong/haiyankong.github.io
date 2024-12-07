---
title: "R 速查"
slug: "r-quick"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

# 教程

- 格拉斯哥大学心理系教程 [psyTeachR↗](https://psyteachr.github.io/)
- 北京大学李东风R语言教程 [R语言教程↗](https://www.math.pku.edu.cn/teachers/lidf/docs/Rbook/html/_Rbook/index.html)
- https://nyu-cdsc.github.io/learningr/

# Packages

{{<figure src="/wiki/r-quick-11.png" caption="Figure 11">}}

{{<figure src="/wiki/r-quick-12.png" caption="Figure 12">}}

# Windows 中 R 相关的安装更新

## Update R

### Way1: direct code way

Run the following code in "Ri".

```r
install.packages("installr")
library(installr)
updateR() # updating R
```

Running “updateR()” will detect if there is a new R version available, and if so it will download+install it (etc.). Just press “next”, “OK”, and “Yes” on everything.

Attention: during updating, you will be prompted whether need to copy the R package installed in the old version to the new version (such as Figure 1 and Figure 2), pay attention to choose according to your needs.

{{<figure src="/wiki/r-quick-1.png" caption="Figure 1">}}

{{<figure src="/wiki/r-quick-2.png" caption="Figure 2">}}

### Way 2: update using GUI

First load installr base on the following code.

```r
install.packages("installr")
library(installr)
```

After running the above code, you will see new button "installr" (Figure 3), please click it and click "Update R". The next steps almost same as Way1.

{{<figure src="/wiki/r-quick-3.png" caption="Figure 3">}}

## Update R in Rstudio

After R updating, you can uninstall the old R version. Then if you next open R studio, you will see the windows like Figure 5. Just choose the "choose a special version of R", select the newest Rversion.

If you did not uninstall the old R version.You can also open "Rstudio", and then  click "Tools-Global" Options, choose "General". If the R version is the newest, means you complete the updating. If not, click Change, you will see figure 4, then click "choose a special version of R", choose the newest one.

{{<figure src="/wiki/r-quick-4.png" caption="Figure 4">}}

{{<figure src="/wiki/r-quick-5.png" caption="Figure 5">}}

## Update Rstudio

Click "Help" in "Rstudio", and choose "Check for Update". It will be directly linked to the official website of Rstudio, directly downloaded and installed.

{{<figure src="/wiki/r-quick-6.png" caption="Figure 6">}}

In addition, you can also check your R version by the following code.

```r
# Check version R
version
```

### Update R packages in Rstudio

Open Rstudio, in "Tool", choose "Check for Package Updates". If you get figure 7, means all your packages are newest version.

{{<figure src="/wiki/r-quick-7.png" caption="Figure 7">}}

{{<figure src="/wiki/r-quick-8.png" caption="Figure 8">}}

Otherwise, you can also use code to update all your R packages in Rstudio.

```r
# check packages
old.packages()
# update all the packages
update.packages()
```

## Install Rtools

https://cran.r-project.org/bin/windows/Rtools/

下载完成后一路点击 Next 安装即可；随后，需要将 R 和 Rtools 添加到 windows 系统环境变量中：打开“此电脑”，在空白处右击，依次在窗口点“属性”——“高级系统设置”——“高级”——“环境变量”，在“系统变量”中寻找 Path，需要在 Path 内添加 R 的 bin 目录路径，rtools 的目录，以及 rtools 的 usr/bin 目录。

{{<figure src="/wiki/r-quick-9.png" caption="Figure 9">}}

添加完环境变量后，就可以在 cmd 命令行下就可以打开 R。

{{<figure src="/wiki/r-quick-10.png" caption="Figure 10">}}

## Reference

- [A step by step (screenshots) tutorial for upgrading R on Windows↗](https://www.r-statistics.com/2015/06/a-step-by-step-screenshots-tutorial-for-upgrading-r-on-windows/)
- https://www.bilibili.com/read/cv18580753/
