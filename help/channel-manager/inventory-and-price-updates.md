---
title: 库存和价格更新
description: ‘[!DNL Channel Manager] 同步库存和价格更新 [!DNL Commerce] 存储和 [!DNL Walmart Marketplace] 这样您就可以从以下位置管理您的销售渠道运营 [!DNL Commerce] 管理员'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 更新库存和定价

[!DNL Channel Manager] 跟踪中产品的库存和定价 [!DNL Commerce] 产品目录并将更新同步到连接的销售渠道和 [!DNL Walmart Marketplace]. 同步操作可确保产品清单反映当前库存数量和定价。


>[!IMPORTANT]
>
>晚于 [!DNL Channel Manager] 安装和配置，所有库存、价格和订单更新会自动同步。 如果您已在沃尔玛商城销售，请确保禁用任何其他更新产品和订单数据的集成。 然后，验证 [!DNL Commerce] 店面数据准确，符合要求 [!DNL Walmart Marketplace] 连接之前 [!DNL Channel Manager] 进入实时商城商店。


## 库存更新

当产品库存水平发生变化时 [!DNL Commerce]， [!DNL Channel Manager] 将更新同步到 [!DNL Walmart Marketplace]. 库存更新最多可能需要10分钟时间才能在销售渠道中同步到 [!DNL Walmart marketplace].

* **更新产品目录中的库存数量** — 时间 [!DNL Commerce] 库存数量因以下原因发生变化： [手动库存数量更改](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html)、退款或取消， [!DNL Channel Manager] 将更改同步到连接的通道，并且 [!DNL Walmart Marketplace].

* **减少库存量以反映 [!DNL Walmart Marketplace] 订单** — 在 [!DNL Walmart Marketplace] 订单同步到 [!DNL Channel Manager]， [!DNL Channel Manager] 将更新发送至 [!DNL Commerce] 订购系统。 [!DNL Commerce] 根据订单调整库存数量。 然后，更新后的数量将同步到 [!DNL Walmart Marketplace]. 在同步操作完成之前，您可能会在sales channel清单和中看到不同的数量 [!DNL Walmart].

>[!IMPORTANT]
>
>之后 [!DNL Walmart Marketplace] 订单同步到 [!DNL Channel Manager]，库存数量和订单信息只更新自以下日期起动的退款和取消： [!DNL Commerce]. 如果订单从以下日期退回或取消： [!DNL Walmart marketplace]，处理以下项的更改： [!DNL Commerce] 以确保的准确性 [!DNL Commerce] 库存数量和订单信息。

## 价格更新

当产品价格发生变化时 [!DNL Commerce]， [!DNL Channel Manager] 将更新同步到 [!DNL Walmart Marketplace]. 价格变更最多需要5分钟才能显示在中 [!DNL Walmart Marketplace] 列表。

### 管理已连接产品的定价

1. 从 [!UICONTROL Admin]，选择 **[!UICONTROL Catalog > Products]**.
1. 在产品网格中，找到要更新的产品并选择 **[!UICONTROL Edit]**.
1. 根据需要复查并更新价格。
1. **[!UICONTROL Save]** 改变了。

有关管理产品价格配置的帮助，请参阅 [!DNL Commerce]，请参见 [管理定价](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
