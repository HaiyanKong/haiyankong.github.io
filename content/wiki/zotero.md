---
title: "Zotero"
slug: "zotero"
toc: true
tocBorder: true
---

> 本文内容：Zotero 备忘录

# Installation

Download the package in the [Zotero website](https://www.zotero.org/download/).

# Basic Settings

Click the **Settings** (Zotero 6 is **Preference**) in **Edit**, and then:

## General

My settings showed in Figure 1.

{{<figure src="/wiki/zotero-tip-1.jpg" caption="Figure 1.General settings">}}

{{<figure src="/wiki/zotero-tip-1-1.jpg" caption="Figure 1.1.Filename Format settings">}}

```
{{ year suffix }}{{ authors max="1" name="family" join="_" suffix="_" case="hyphen" }}{{ title truncate="30" case="hyphen" }}
```

## Sync

My settings showed in  Figure 2, I used [InfiniCLOUD](https://infini-cloud.net/en/index.html) for cloud store items and pdf files in my Zotero. The free plan in InfiniCLOUD (Figure 2.1) is enough.

{{<figure src="/wiki/zotero-tip-2.jpg" caption="Figure 2.Sync settings">}}

{{<figure src="/wiki/zotero-tip-2-1.jpg" caption="Figure 2.1.InfiniCLOUD">}}

## Export

My settings showed in Figure 3.

{{<figure src="/wiki/zotero-tip-3.jpg" caption="Figure 3.Export settings">}}

## Cite

My settings showed in Figure 4.

{{<figure src="/wiki/zotero-tip-4.jpg" caption="Figure 4.Cite settings">}}

## Advanced

My settings showed in Figure 5 & 6.

*Note: “Data Dictionary Location” means the place in your computer you want to store your Zotero data (everything in Zotero, such as items info, items pdf attachments, other attachments, and ...).*

{{<figure src="/wiki/zotero-tip-5.jpg" caption="Figure 5.Advanced settings1">}}

{{<figure src="/wiki/zotero-tip-6.jpg" caption="Figure 6.Advanced settings2">}}

## Advanced Settings: Add-on

Click the **Add-on** in **Tools**. Figure 7 showed the add-on extensions I used. All of them are excellent add-on extensions!

*Note: Figure 7.1 recorded the Better BibTex Settings in my Zotero.*

{{<figure src="/wiki/zotero-tip-7.jpg" caption="Figure 7.Add-on">}}

{{<figure src="/wiki/zotero-tip-7-1.jpg" caption="Figure 7.1.Better BibTex Settings">}}

```
[year][auth:lower]'_'[shorttitle1_0:lower]
year + auth(n=0,m=1,creator="*",initials=false).fold.lower + "'_'" + shorttitle(1,0).lower
```

# Basic function

## Output reference

- Export references

	- Method 1: After selecting an item, click Edit

	{{<figure src="/wiki/zotero-tip-8.jpg" caption="Figure 8">}}

	```
	  	***Copy citation (复制引注)***
	
	  	(Beffel & Nuttall, 2020)
	
	  	**copy reference list (复制参考文献表)**
	
	  	Beffel, J. H., & Nuttall, A. K. (2020). Influences of parentification and benefit finding on prosocial behavior among typically developing siblings of individuals with autism spectrum disorder. *Research in Developmental Disabilities*, *104*, 103694. <https://doi.org/10.1016/j.ridd.2020.103694>
	```

	- Method 2: After selecting an item, right click

	{{<figure src="/wiki/zotero-tip-9.jpg" caption="Figure 9">}}

	{{<figure src="/wiki/zotero-tip-10.jpg" caption="Figure 10">}}

- Delete local files while deleting attachments

	{{<figure src="/wiki/zotero-tip-11.jpg" caption="Figure 11">}}

- Show items from sub-collections

	{{<figure src="/wiki/zotero-tip-12.jpg" caption="Figure 12">}}

## See item in which group

Just select the item, and then press “Ctrl”.

# Reference

- [Awesome Zotero Plugins](https://plugins.zotero-chinese.com/charts)
- [Zotero 插件下载](https://plugins.zotero-chinese.com/#/?id=zotero-插件下载)
