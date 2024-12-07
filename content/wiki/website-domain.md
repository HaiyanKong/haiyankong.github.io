---
title: "Vercel + Cloudflare 绑定域名"
slug: "website-domain"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

> 本文内容：使用 Cloudflare 给 Vercel 部署的网站绑定域名
> 
> 本文发布于 2024-01-25，部分内容可能过期了

# 购买域名

在 [Namesilo](https://www.namesilo.com/) 购买域名，购买过程很简单，可以使用支付宝支付。详细步骤可以参考教程：[namesilo域名注册和cloudflare域名解析教程](https://zhuanlan.zhihu.com/p/625843308)

# 将域名添加到 Cloudflare

将域名添加到 Cloudflare，该部分的大多数步骤都是直接点击 Continue 即可，其中最关键的步骤是返回域名购买处的域名管理中心（图 1）修改 DNS 记录，将原本显示的所有地址删除掉（图 2），添加 Cloudflare 的服务器（图 3）。接下来是“漫长（大概十几分钟？）”的等待时间，等待托管的域名生效。详细步骤可以参考教程：

- [namesilo域名注册和cloudflare域名解析教程](https://zhuanlan.zhihu.com/p/625843308)
- [如何在国内访问vercel部署应用？（“登录Cloudflare控制台并添加站点”部分）](https://zhuanlan.zhihu.com/p/666912903)

{{<figure src="/wiki/website-domain-1.png" caption="Figure 1">}}

{{<figure src="/wiki/website-domain-2.png" caption="Figure 2">}}

{{<figure src="/wiki/website-domain-3.png" caption="Figure 3">}}

# 在 Cloudflare 添加域名解析记录

在 Cloudflare 添加`CNAME`类型的解析，也就是把购买的域名定向到 XXX.vercel.app，并打开 proxy 服务（图 4 & 图 5）。详细步骤可以参考教程：[如何在国内访问vercel部署应用？（“去Cloudflare添加域名解析记录”部分）](https://zhuanlan.zhihu.com/p/666912903)

{{<figure src="/wiki/website-domain-4.png" caption="Figure 4">}}

{{<figure src="/wiki/website-domain-5.png" caption="Figure 5">}}

# Cloudflare 配置 SSL

防止后续访问时出现“重定向次数过多”的问题，提前在 Cloudflare 修改站点的加密模式，如图 6 所示。详细步骤可以参考教程：

- [使用 vercel + cloudflare 管理域名（“cloudflare 配置 ssl”部分）](https://caoayu.top/Blog/软件使用/vercel-cf/#cloudflare-ssl)
- [Vercel + Cloudflare = 重定向次数过多？Cloudflare + Vercel err_too_many_redirects 解决方法](https://zhuanlan.zhihu.com/p/621476520)

{{<figure src="/wiki/website-domain-6.png" caption="Figure 6">}}

# 在 Vercel.app 配置域名

如图 7 所示，添加即可。详细步骤可以参考教程：[如何在国内访问vercel部署应用？（“对部署好的vercel应用添加除了自带域名的新域名解析”部分）](https://zhuanlan.zhihu.com/p/666912903)

{{<figure src="/wiki/website-domain-7.png" caption="Figure 7">}}

# 参考资料

- [Namesilo](https://www.namesilo.com/)
- [Cloudflare](https://www.cloudflare.com/zh-cn/)
- [Vercel](https://vercel.com/)
- [namesilo域名注册和cloudflare域名解析教程](https://zhuanlan.zhihu.com/p/625843308)
- [如何在国内访问vercel部署应用？](https://zhuanlan.zhihu.com/p/666912903)
- [使用 vercel + cloudflare 管理域名](https://caoayu.top/Blog/软件使用/vercel-cf/)
- [Vercel + Cloudflare = 重定向次数过多？Cloudflare + Vercel err_too_many_redirects 解决方法](https://zhuanlan.zhihu.com/p/621476520)
