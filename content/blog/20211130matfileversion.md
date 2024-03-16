---
title: "MATLAB Warning: Saving Variables to Older MAT-File Versions"
date: 2021-11-30
author: Haiyan Kong
slug: 20211130/matfileversion
draft: false
tags: matlab
---

{{<alert "circle-info" >}}
**Summary**: 
This blog will present a solution to address the MATLAB warning: "Variable cannot be saved to a MAT-file with a version older than 7.3."
{{< /alert >}}

When using MATLAB to save variables, you might encounter a warning message similar to the one below:

```MATLAB
Warning: The variable 'a' cannot be saved to a MAT-file with a version
older than 7.3.
```

To resolve this issue, you can follow these steps:

- Open MATLAB and click on Preferences.

- Navigate to the General tab and select MAT-Files.

- Choose the first option: "MATLAB Version 7.3 or later (save -v7.3)."



{{<figure src="/blog/en/20211130matfileversion/20211130matfileversion-1.png" caption="Figure 1" width="400">}}
