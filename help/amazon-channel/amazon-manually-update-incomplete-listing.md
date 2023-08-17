---
title: 更新Amazon必需信息
description: Amazon sales channel提供了“未完成”选项卡来监视缺少Amazon所需信息的Commerce目录产品。
feature: Sales Channels, Merchandising, Catalogs, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 更新必需信息（列表不完整）

列表显示在 _[!UICONTROL Incomplete]_选项卡包括 [!DNL Commerce] 目录产品符合您的上市规则中定义的Amazon资格要求，但在上市前缺少Amazon要求的信息。

## 更新所需信息(无法分配给Amazon列表) {#update-required-info-unable-to-assign-to-amazon-listing}

1. 查看列表 _[!UICONTROL Incomplete]_tab in [管理列表](./managing-product-listings.md).

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**要更新的列表。

1. 查看您尝试与Amazon列表匹配的目录产品信息（SKU和产品名称）。

1. 对象 **[!UICONTROL Assign ASIN]**，输入Amazon为要与目录产品匹配的列表分配的ASIN。

1. 要保存产品匹配项，请单击 **[!UICONTROL Save Listing Update]**.

该列表现在与您的目录匹配，随后该列表将根据您的cron和列表设置更新并发布到Amazon。 它也会从 _[!UICONTROL Incomplete]_选项卡。

![手动分配ASIN以不匹配列表](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## 更新所需信息（找到多个匹配项） {#update-required-info-multiple-matches-found}

1. 查看列表 _[!UICONTROL Incomplete]_tab in [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. 在 _操作_ 列，单击 **选择** > **更新必需信息** 要更新的列表。

1. 查看您尝试与Amazon列表匹配的目录产品信息（SKU和产品名称）。

1. 对象 **[!UICONTROL Select Correct Amazon Listing]**，为要与此产品匹配的列表选择正确的ASIN。

   此处列出的选项包括标识为可能匹配的目录产品。 如果这些选项都不正确，则可以选择 `Manually Enter Correct ASIN` 并手动输入产品的ASIN。

1. 如果手动输入ASIN，请为输入正确的ASIN **[!UICONTROL Manually Assign ASIN]**.

1. 要保存产品匹配项，请单击 **[!UICONTROL Save Listing Update]**.

![从多个可能的匹配项中手动选择ASIN](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## 更新所需信息（具有变体） {#update-required-info-has-variants}

1. 查看列表 _[!UICONTROL Incomplete]_tab in [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**要更新的列表。

1. 查看您尝试与Amazon列表匹配的目录产品信息（SKU和产品名称）。

1. 对象 **[!UICONTROL Select Correct Amazon Listing]**，为要与此产品匹配的列表选择正确的ASIN。

   此处列出的选项包括标识为可能匹配的目录产品。 如果这些选项都不正确，则可以选择 `Manually Enter Correct ASIN` 并手动输入产品的ASIN。

1. 如果手动输入ASIN，请为输入正确的ASIN **[!UICONTROL Manually Assign ASIN]**.

1. 要保存产品匹配项，请单击 **[!UICONTROL Save Listing Update]**.

## 更新所需信息（缺少条件） {#update-required-info-missing-condition}

1. 查看列表 _[!UICONTROL Incomplete]_tab in [管理列表](./managing-product-listings.md).

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**要更新的列表。

1. 查看您尝试与Amazon列表匹配的目录产品信息（SKU和产品名称）。

1. 对象 **[!UICONTROL Condition]**&#x200B;中，选择相应的条件。

   可用选项列表取决于您的 [产品列表条件](./product-listing-condition.md) 设置。

1. 要保存产品匹配项，请单击 **[!UICONTROL Save Listing Update]** .

![手动更新缺少的条件](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
