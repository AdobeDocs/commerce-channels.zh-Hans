---
title: 价格范围
description: 使用Commerce定价范围根据多个网站或全局管理定价。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 价格范围

[!DNL Commerce] 为提供配置 [定价范围](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} 核心Commerce用户指南中的。

如果您将目录价格范围从 `Global` 到 `Website`，则所有价格类型属性也会更改为 `Website`. 参见 [添加网站](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

在选择网站价格时，有两个价格来源：

- 网站价格
- 默认（回退）价格

对于Amazon sales channel集成，根据您的 [上市规则](./listing-rules.md)，您可以将多个网站中的产品映射到单个 [!DNL Amazon Marketplace] 国家/地区(定义于 [存储集成](./store-integration.md))。 但是，此映射引入了一个问题：如果产品存在于多个网站上且价格不同，则应发布哪个价格。
