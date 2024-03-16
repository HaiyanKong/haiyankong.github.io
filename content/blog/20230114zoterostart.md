---
title: "Zotero installation and settings"
date: 2023-01-14
author: Haiyan Kong
slug: 20230114/zoterostart
draft: false
tags: zotero
---

{{< alert "circle-info" >}}
**Summary**: 
Zotero installation and settings. Recording for sharing and also reference for myself if re-install new Zotero in future. 
{{< /alert >}}

## Installation

Download the package in the [Zotero website](https://www.zotero.org/support/beta_builds) (This version is Zotero 7 beta, but if you want to install Zotero 6, you can click [here](https://www.zotero.org/download/)) and install.

## Basic Settings

Click the **Settings**(Zotero 6 is **Preference**) in **Edit**, and then: 

### General

My settings showed in Figure 1.

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-1.jpg" caption="Figure 1.General settings" width="500">}}

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-1-1.jpg" caption="Figure 1.1.Filename Format settings" width="500">}}

```
{{ year suffix }}{{ authors max="1" name="family" join="_" suffix="_" case="hyphen" }}{{ title truncate="30" case="hyphen" }}
```

### Sync

My settings showed in  Figure 2, I used [InfiniCLOUD](https://infini-cloud.net/en/index.html) for cloud store items and pdf files in my Zotero. The free plan in InfiniCLOUD (Figure 2.1) is enough for these literature files storage (I think).

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-2.jpg" caption="Figure 2.Sync settings" width="500">}}

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-2-1.jpg" caption="Figure 2.1.InfiniCLOUD" width="500">}}

### Export

My settings showed in Figure 3.

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-3.jpg" caption="Figure 3.Export settings" width="500">}}

### Cite

My settings showed in Figure 4.

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-4.jpg" caption="Figure 4.Cite settings" width="500">}}

### Advanced

My settings showed in Figure 5 & 6.

*Note: “Data Dictionary Location” means the place in your computer you want to store your Zotero data (everything in Zotero, such as items info, items pdf attachments, other attachments, and ...).*

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-5.jpg" caption="Figure 5.Advanced settings1" width="500">}}

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-6.jpg" caption="Figure 6.Advanced settings2" width="500">}}

## Advanced Settings: Add-on

Click the **Add-on** in **Tools**. Figure 7 showed the add-on extensions I used. All of them are excellent add-on extensions!

*Note: Figure 7.1 recorded the Better BibTex Settings in my Zotero.*

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-7.jpg" caption="Figure 7.Add-on" width="500">}}

{{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-7-1.jpg" caption="Figure 7.1.Better BibTex Settings" width="500">}}

```
[year][auth:lower]'_'[shorttitle1_0:lower]
```

```
year + auth(n=0,m=1,creator="*",initials=false).fold.lower + "'_'" + shorttitle(1,0).lower
```

## Basic function

- Export references

  - Method 1: After selecting an item, click Edit

  {{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-8.jpg" caption="Figure 8" width="300">}}

  ​		***Copy citation (复制引注)***

  ​		(Beffel & Nuttall, 2020)

  ​		**copy reference list (复制参考文献表)**

  ​		Beffel, J. H., & Nuttall, A. K. (2020). Influences of parentification and benefit finding on prosocial behavior among typically developing siblings of individuals with autism spectrum disorder. *Research in Developmental Disabilities*, *104*, 103694. https://doi.org/10.1016/j.ridd.2020.103694

  - Method 2: After selecting an item, right click

  {{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-9.jpg" caption="Figure 9" width="200">}}

  {{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-10.jpg" caption="Figure 10" width="300">}}

- Delete local files while deleting attachments

  {{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-11.jpg" caption="Figure 11" width="600">}}

- Show items from sub-collections

  {{<figure src="/blog/en/20230114zoterostart/20230114zoterostart-12.jpg" caption="Figure 12" width="300">}}

## Reference

- [Awesome Zotero Plugins](https://plugins.zotero-chinese.com/charts)
- [Zotero 插件下载](https://plugins.zotero-chinese.com/#/?id=zotero-插件下载)

{{< badge "edit" >}}
Update: 29 February 2023
{{< /badge >}}