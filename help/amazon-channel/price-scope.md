---
title: 价格范围
description: 使用商务定价范围可根据多个网站或全球范围管理定价。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# 价格范围

[!DNL Commerce] 为 [定价范围](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;}设置为 `Global` 或 `Website`. 如果定价设置为 `Global`，则所有网站都有一个价格来源。 如果定价设置为 `Website`，则您的网站可能会因不同的价格而有所不同，并且还具有回退默认定价值。 请参阅 [目录价格](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price)核心商务用户指南中的{target=&quot;_blank&quot;}。

如果您将目录价格范围从 `Global` to `Website`，则所有价格类型属性也将更改为 `Website`. 请参阅 [添加网站](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target=&quot;_blank&quot;}。

选择网站价格时，有两个价格来源：

- 网站价格
- 默认（回退）价格

对于Amazon销售渠道集成，基于 [列表规则](./listing-rules.md)，您可以将多个网站中的产品映射到单个网站 [!DNL Amazon Marketplace] 国家/地区(在 [存储集成](./store-integration.md))。 但是，此映射将介绍当产品存在于价格不同的多个网站上时应发布价格的问题。
