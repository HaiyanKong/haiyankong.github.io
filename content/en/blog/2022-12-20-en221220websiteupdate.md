---
title: "Website Update Record [draft]"
date: 2022-12-20
author: Haiyan Kong
slug: en221220websiteupdate
draft: false
toc: false
categories:
  - record
tags:
  - tutrial
  - English
---

**update**
```
cd /d/Hugo/quickstart
bash deploy.sh
git config --global --unset http.proxy
git config --global --unset https.proxy
git push
```

**clone**
```
git clone --recursive link
```

**deploy.sh** ***contains:***
```
git add .
msg="updating site on $(date)" 
git commit -m "$msg"
git push origin master
```