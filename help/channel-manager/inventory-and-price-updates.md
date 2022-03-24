---
title: 库存和价格更新
description: '"[!DNL Channel Manager] 同步商务商店和 [!DNL Walmart Marketplace] 以便您可以通过商务管理员管理您的销售渠道操作”'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# 库存和价格更新

渠道管理器跟踪已发布产品的库存和定价，并同步对渠道管理器和沃尔玛市场所做的更改，以反映产品清单中的当前库存数量和定价。**

## 库存更新

当库存级别发生更改时，渠道管理器会同步商务产品目录和沃尔玛市场之间的更新，以便渠道管理器和沃尔玛市场都显示当前库存数量。

在渠道管理器和Walmart Marketplace中显示库存更改最多可能需要5分钟。

* **更新产品目录中的库存数量** — 如果由于 [手动库存数量更改](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) 或订购退款或取消，渠道管理器会将更改同步到连接的销售渠道和 [!DNL Walmart Marketplace].

* **减少库存量以反映沃尔玛的订单** — 在Walmart Marketplace订单同步到渠道管理器后，渠道管理器会将更新发送到商务订单系统。 商务根据订单调整库存数量。 然后，更新的数量会同步到Walmart Marketplace。 可能是在同步操作完成之前，在渠道管理器和市场中显示的库存量存在一些差异。

>[!IMPORTANT]
>
> 在Walmart Marketplace订单与渠道管理器同步后，库存数量和其他订单处理信息将仅针对从Commerce启动的退款和取消进行更新。 如果从Walmart Marketplace退回或取消订单，则处理来自Commerce的更改，以确保商务库存数量和订单信息准确无误。

## 价格更新

当商务中的产品价格发生更改时，渠道管理器会将更新从商务产品目录同步到Walmart Marketplace。 显示库存更改最多可能需要5分钟。

### 管理已发布产品的定价

1. 从 [!UICONTROL Admin]，选择 **[!UICONTROL Catalog > Products]**.
1. 在产品网格中，找到要更新的产品并选择 **[!UICONTROL Edit]**.
1. 根据需要查看并更新价格。
1. **[!UICONTROL Save]** 改变。

渠道管理器会将任何价格更新同步到渠道商店，并 [!DNL Walmart Marketplace]. 此操作最多可能需要5分钟。

有关在Commerce中管理产品价格配置的详细信息，请参阅 [管理定价](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
