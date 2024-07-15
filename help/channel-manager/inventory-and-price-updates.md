---
title: 库存和价格更新
description: “[!DNL Channel Manager]”在 [!DNL Commerce] 商店和 [!DNL Walmart Marketplace] 之间同步库存和价格更新，以便您可以从 [!DNL Commerce] 管理员管理销售渠道操作
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 更新库存和定价

[!DNL Channel Manager]跟踪[!DNL Commerce]产品目录中的产品的库存和定价，并将更新同步到连接的销售渠道和[!DNL Walmart Marketplace]。 同步操作可确保产品清单反映当前的库存数量和定价。


>[!IMPORTANT]
>
>安装和配置[!DNL Channel Manager]后，所有库存、价格和订单更新将自动同步。 如果您已经在沃尔玛商店销售，请确保禁用任何其他更新产品和订单数据的集成。 然后，在将[!DNL Channel Manager]连接到实时市场商店之前，验证[!DNL Commerce]店面中的库存库存水平和价格是否准确并与[!DNL Walmart Marketplace]中的数据匹配。


## 清单更新

当[!DNL Commerce]中的产品库存水平更改时，[!DNL Channel Manager]将更新同步到[!DNL Walmart Marketplace]。 库存更新最多可能需要10分钟时间才能在销售渠道中同步到[!DNL Walmart marketplace]。

* **产品目录中的库存数量更新** — 当[!DNL Commerce]库存数量因[手动库存数量更改](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html)、退款或取消而发生更改时，[!DNL Channel Manager]将更改同步到连接的渠道和[!DNL Walmart Marketplace]。

* **减少库存数量以反映[!DNL Walmart Marketplace]个订单** — 在[!DNL Walmart Marketplace]个订单同步到[!DNL Channel Manager]后，[!DNL Channel Manager]将更新发送到[!DNL Commerce]订单系统。 [!DNL Commerce]根据订单调整库存数量。 然后，更新后的数量将同步到[!DNL Walmart Marketplace]。 在同步操作完成之前，您可能会在销售渠道清单和[!DNL Walmart]中看到不同的数量。

>[!IMPORTANT]
>
>将[!DNL Walmart Marketplace]订单同步到[!DNL Channel Manager]后，将只更新从[!DNL Commerce]启动的退款和取消的库存数量和订单信息。 如果从[!DNL Walmart marketplace]退款或取消订单，则处理从[!DNL Commerce]进行的更改以确保[!DNL Commerce]库存数量和订单信息的准确性。

## 价格更新

当[!DNL Commerce]中的产品价格更改时，[!DNL Channel Manager]将更新同步到[!DNL Walmart Marketplace]。 价格更改最多可能需要五分钟才能显示在[!DNL Walmart Marketplace]列表中。

### 管理已连接产品的定价

1. 从[!UICONTROL Admin]中选择&#x200B;**[!UICONTROL Catalog > Products]**。
1. 在产品网格中，找到要更新的产品并选择&#x200B;**[!UICONTROL Edit]**。
1. 根据需要查看和更新价格。
1. **[!UICONTROL Save]**&#x200B;更改。

有关在[!DNL Commerce]中管理产品价格配置的帮助，请参阅[管理定价](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html)。
