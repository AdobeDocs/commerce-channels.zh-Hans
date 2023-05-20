---
title: 價格範圍
description: 使用Commerce定價範圍，根據多個網站或全域管理定價。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 價格範圍

[!DNL Commerce] 提供您專屬的設定 [定價範圍](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} 位於核心Commerce使用手冊中。

如果您將目錄價格範圍從 `Global` 至 `Website`，所有價格型別屬性也會變更為 `Website`. 另請參閱 [新增網站](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

選擇網站價格時，有兩個價格來源：

- 網站價格
- 預設（後援）價格

針對Amazon銷售管道整合，根據您的 [清單規則](./listing-rules.md)，您可以將多個網站的產品對應至單一網站 [!DNL Amazon Marketplace] 國家/地區(定義於 [存放區整合](./store-integration.md))。 不過，此對應會介紹當產品存在於多個不同價格的網站上時，應該發佈哪種價格的問題。
