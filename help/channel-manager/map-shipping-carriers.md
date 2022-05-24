---
title: 映射运输承运人
description: 映射用于匹配的属性[DNL! 商务]产品到现有 [!DNL Walmart Marketplace] 列表和同步数据 [!DNL Channel Manager] 和 [!DNL Walmart].
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: aff38e59771fb973b789450b1a7b9552a7a809ff
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# 映射运输承运人

在您之前 [处理订单发运](process-orders.md#ship-an-order) 表示 [!DNL Walmart Marketplace] 订购，将沃尔玛首选的运输公司映射到 [!DNL Commerce] 以便在 [!DNL Walmart] 和 [!DNL Commerce].

未映射到首选运营商的商业运营商将标记为 *[!UICONTROL Other Carrier]* 在沃尔玛。

**先决条件**

在映射装运承运人之前，请完成以下任务：

1. 查看 [实时交货的承运人方法和装运最佳实践](https://sellerhelp.walmart.com/s/guide?article=000009473) 对沃尔玛市场来说。

1. 验证 [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) 和 [!UICONTROL Shipping Settings] 配置 [!DNL Commerce] 存储，以确保已优化 [!DNL Walmart Marketplace sales].

## 映射运输承运人

1. 在 [!UICONTROL Listings] 页面，选择 **[!UICONTROL Settings]**.

1. 从 **[!UICONTROL Map Attributes]**，选择 **[!UICONTROL Shipping Carriers]**.

   ![映射运输承运人](assets/map-shipping-carriers.png)

1. 对于 [!DNL Walmart] 列出首选运营商，选择 [!DNL Commerce] 承运人名称（如果承运人可用）。

1. 选择 **[!UICONTROL Save]** 以应用配置。
