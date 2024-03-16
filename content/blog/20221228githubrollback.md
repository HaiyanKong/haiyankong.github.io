---
title: "Rollback in GitHub Desktop"
date: 2022-12-28
author: Haiyan Kong
slug: 20221228/githubrollback
draft: false
tags: github
---

{{<alert "circle-info" >}}
**Summary**: 
If you want to rollback project files to where they were before the last commit in GitHub Desktop, you can follow this blog.
{{< /alert >}}



**Step 1**

Choose **the project** you want to rollback in GitHub Desktop, as presented in Figure 1.

{{<figure src="/blog/en/20221228githubrollback/20221228githubrollback-1.png" caption="Figure 1" width="800">}}

**Step 2**

Click the **History** in Figure 2, find the newest commit, and click right mouse button, and choose **Revert changes in commit**.

{{<figure src="/blog/en/20221228githubrollback/20221228githubrollback-2.png" caption="Figure 2" width="800">}}

**Step 3**

If you completed step 2 successfully, you will see the changes like Figure 3 **green box**. These mean the project creates a new "commit" record rather than being restored immediately.

Click the **Changes**.

{{<figure src="/blog/en/20221228githubrollback/20221228githubrollback-3.png" caption="Figure 3" width="800">}}

**Step4**

Click the **Push origin**. Then you will get your original project before the committed.

{{<figure src="/blog/en/20221228githubrollback/20221228githubrollback-4.png" caption="Figure 4" width="800">}}

**Reference**

- [Rollback uncommitted changes in GitHub Desktop (or Github for Windows)](https://stackoverflow.com/questions/24975043/rollback-uncommitted-changes-in-github-desktop-or-github-for-windows)

- [GitHub Desktop rollback](https://jiming.blog.csdn.net/article/details/112615134?spm=1001.2101.3001.6650.17&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-17-112615134-blog-80140863.pc_relevant_3mothn_strategy_recovery&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-17-112615134-blog-80140863.pc_relevant_3mothn_strategy_recovery&utm_relevant_index=23)