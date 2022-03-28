---
title: 库存和价格更新
description: '''[!DNL Channel Manager] 同步商务商店和 [!DNL Walmart Marketplace] 以便您可以通过商务管理员管理您的销售渠道操作'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 库存和价格更新

[!DNL Channel Manager] 跟踪渠道商店中产品的库存和定价。 当库存或定价发生更改时，更新会同步到 [!DNL Channel Manager] 和 [!DNL Walmart Marketplace] 以反映产品清单中的当前库存数量和定价。

## 库存更新

当库存水平发生更改时，渠道管理器会同步商务和沃尔玛市场之间的更新，以确保渠道管理器和沃尔玛市场拥有正确的库存数量。

在渠道管理器和市场之间同步库存更新最多可能需要10分钟。

* **更新产品目录中的库存数量** — 当由于 [手动库存数量更改](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html)退款或取消，则渠道管理器会将更改同步到连接的渠道和 [!DNL Walmart Marketplace].

* **减少库存量以反映沃尔玛的订单** — 在Walmart Marketplace订单同步到渠道管理器后，渠道管理器会将更新发送到商务订单系统。 商务根据订单调整库存数量。 然后，更新的数量会同步到Walmart Marketplace。 在同步操作完成之前，您可能会看到渠道管理器和市场之间的数量差异。

>[!IMPORTANT]
>
> 在Walmart Marketplace订单与渠道管理器同步后，库存数量和订单信息将仅针对从Commerce启动的退款和取消进行更新。 如果从Walmart Marketplace退回或取消订单，则处理来自Commerce的更改以确保商务库存数量和订单信息的准确性。

## 价格更新

当商务中的产品价格发生更改时，渠道管理器会同步 [!DNL Commerce] 产品目录到 [!DNL Walmart Marketplace]. 市场最多可能需要五分钟才能显示价格变化。

### 管理已发布产品的定价

1. 从 [!UICONTROL Admin]，选择 **[!UICONTROL Catalog > Products]**.
1. 在产品网格中，找到要更新的产品并选择 **[!UICONTROL Edit]**.
1. 根据需要查看并更新价格。
1. **[!UICONTROL Save]** 改变。

有关在Commerce中管理产品价格配置的详细信息，请参阅 [管理定价](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
