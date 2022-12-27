---
title: "Website update record using git"
date: 2022-12-20
author: Haiyan Kong
slug: en221220websiteupdate
draft: false
toc: false
categories: tutrial
tags: website
---

# update

- update your website

```
cd /d/Hugo/quickstart
bash deploy.sh
```

- deploy.sh   contains:

```
git add .
msg="updating site on $(date)"
git commit -m "$msg"
git push origin master
```

## error solution

- git error: Internet

```
git config --global --unset http.proxy
git config --global --unset https.proxy
```

```
git push
```

- git error: failed to push some refs to ‘https://github.com/…

```
git pull --rebase origin master
```

# clone

- clone project from GitHub

```
git clone --recursive link
```
