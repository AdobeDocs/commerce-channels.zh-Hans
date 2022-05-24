---
title: 库存和价格更新
description: '''[!DNL Channel Manager] 同步商务商店和 [!DNL Walmart Marketplace] 以便您可以通过商务管理员管理您的销售渠道操作'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 71ad5e3bc9ff6b909943a161472e4db7d375683f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# 更新库存和定价

[!DNL Channel Manager] 跟踪 [!DNL Commerce] 产品目录和同步到连接的销售渠道和 [!DNL Walmart Marketplace]. 同步可确保产品清单反映当前库存数量和定价。

## 库存更新

当产品库存级别在 [!DNL Commerce], [!DNL Channel Manager] 同步到销售渠道和 [!DNL Walmart Marketplace]. 库存更新可能最多需要10分钟才能跨销售渠道同步到 [!DNL Walmart marketplace].

* **更新产品目录中的库存数量** — 当 [!DNL Commerce] 库存数量因 [手动库存数量更改](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html)退款或取消， [!DNL Channel Manager] 将更改同步到连接的渠道，并 [!DNL Walmart Marketplace].

* **减少库存量以反映 [!DNL Walmart Marketplace] 订购** — 在 [!DNL Walmart Marketplace] 订单同步到 [!DNL Channel Manager], [!DNL Channel Manager] 将更新发送到 [!DNL Commerce] 订单系统。 [!DNL Commerce] 根据订单调整库存数量。 然后，更新的数量会同步到 [!DNL Walmart Marketplace]. 在同步操作完成之前，您可能会在销售渠道列表中看到不同的数量， [!DNL Walmart].

>[!IMPORTANT]
>
>在 [!DNL Walmart Marketplace] 订单同步到 [!DNL Channel Manager]，则仅对从 [!DNL Commerce]. 如果订单被退回或取消，则 [!DNL Walmart marketplace]，处理 [!DNL Commerce] 以确保 [!DNL Commerce] 库存数量和订单信息。

## 价格更新

当产品价格在 [!DNL Commerce], [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace]. 价格变化最多可能需要五分钟才能显示在 [!DNL Walmart Marketplace] 列表。

### 管理已发布产品的定价

1. 从 [!UICONTROL Admin]，选择 **[!UICONTROL Catalog > Products]**.
1. 在产品网格中，找到要更新的产品并选择 **[!UICONTROL Edit]**.
1. 根据需要查看并更新价格。
1. **[!UICONTROL Save]** 改变。

有关管理中产品价格配置的帮助，请参阅 [!DNL Commerce]，请参阅 [管理定价](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
