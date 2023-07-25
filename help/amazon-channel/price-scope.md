---
title: Amazon销售渠道 — 价格范围
description: 使用Commerce定价范围根据多个网站或全局管理定价。
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 价格范围

[!DNL Commerce] 为提供配置 [定价范围](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) 将设置为 `Global` 或 `Website`. 如果将定价设置为 `Global`，所有网站都有一个单一的价格来源。 如果将定价设置为 `Website`，您的网站可能会因各种渠道的不同而有所差异，并且还有一个后备默认定价值(请参阅 [价格范围](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html))。

如果您将目录价格范围从 `Global` 到 `Website`，则所有价格类型属性也会更改为 `Website`. 参见 [添加网站](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

在选择网站价格时，有两个价格来源：

- 网站价格
- 默认（回退）价格

对于Amazon sales channel集成，根据您的 [上市规则](./listing-rules.md)，您可以将多个网站中的产品映射到单个 [!DNL Amazon Marketplace] 国家/地区(定义于 [存储集成](./store-integration.md))。 但是，此映射引入了一个问题：如果产品存在于多个网站上且价格不同，则应发布哪个价格。
