---
title: 映射装运承运人
description: '映射属性以匹配[DNL！ Commerce]产品到现有 [!DNL Walmart Marketplace] 列出并同步数据 [!DNL Channel Manager] 和 [!DNL Walmart].'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 映射装运承运人

在您之前 [处理订单发运](process-orders.md#ship-an-order) 对象 [!DNL Walmart Marketplace] 订单，将沃尔玛首选的航运公司映射到 [!DNL Commerce] 以便装运数据能够在 [!DNL Walmart] 和 [!DNL Commerce].

未映射到首选运营商的商务运营商将标记为 *[!UICONTROL Other Carrier]* 日期 [!DNL Walmart].

**先决条件**

在映射装运承运人之前，请完成以下任务：

1. 查看 [准时交货的承运人方法和运输最佳实践](https://sellerhelp.walmart.com/s/guide?article=000009473) 对象 [!DNL Walmart Marketplace].

1. 验证 [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) 和 [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) 中的配置 [!DNL Commerce] 存储，以确保您已针对以下项优化配置： [!DNL Walmart Marketplace sales].

## 映射装运承运人

1. 从 **[!UICONTROL Listings]** 或 **[!UICONTROL Orders]** 页面，选择 **[!UICONTROL Channel Settings]**.

1. 日期 **[!UICONTROL Channel Settings]**，选择 **[!UICONTROL Shipping Carriers]**.

   ![映射装运承运人](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. 针对每个 [!DNL Walmart] 已列出首选运营商，请选择 [!DNL Commerce] 运营商名称时（如果该运营商可用）。

1. 选择 **[!UICONTROL Save]** 以应用配置。

