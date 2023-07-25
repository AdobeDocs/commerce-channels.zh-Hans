---
title: 创建和编辑Amazon sales channel覆盖
description: 使用AmazonSales Channel覆盖可将您的更改应用于单个Amazon列表或多个列表。
feature: Sales Channels, Products, Configuration
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 0%

---

# 创建和编辑覆盖

您可以创建和覆盖列表，也可以编辑或删除已应用于列表的覆盖。 覆盖为特定列表设置定义的值。

## 为单个列表创建覆盖

此 _[!UICONTROL Create Override]_可在查看列表时执行操作_[!UICONTROL Inactive]_， _[!UICONTROL Active]_、和_[!UICONTROL Ineligible]_ 选项卡。

1. 查看列表 _[!UICONTROL Products Listings]_页面(_[!UICONTROL Inactive]_， _[!UICONTROL Active]_、和_[!UICONTROL Ineligible]_ 选项卡)。

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Create Override]**以打开“产品列表改写”页。

   ![创建Amazon列表覆盖](assets/amazon-select-create-override.png){width="220"}

1. 要确保您查看的是正确的列表，请验证 _[!UICONTROL Listing Details]_.

1. 确定正在创建的覆盖类型。

   您可以为清单定义单个改写类型或类型组合（“价格”、“处理时间”、“条件”、“卖方备注”）。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 并输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入以下项目的定义时间值（以天为单位）： **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 并为选择正确的选项 **[!UICONTROL Condition Override]**.
   - **卖方备注**  — 单击 **[!UICONTROL Change Seller Notes]** 并输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 单击 **[!UICONTROL Save Listing Override]**.

   此 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表的状态更改为 `Relist in Progress`. 更改将使用您的下一个数据同步（在cron设置中配置）发布到Amazon。 该列表还将添加到_[!UICONTROL Overrides]_ 选项卡。

以下示例显示了一个覆盖，该覆盖定义了一个新的价格： `$55`，的新处理时间 `1 day`，的新条件 `Used; Like New`和新的卖家备注文本。

![Amazon列表覆盖示例](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## 编辑或移除单个列表的覆盖 {#edit-override-single-listing}

此 _[!UICONTROL Edit Overrides]_可在查看列表时执行操作_[!UICONTROL Overrides]_ 选项卡。

1. 查看列表 _[!UICONTROL Product Listings]_页面(_[!UICONTROL Overrides]_ 选项卡)。

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   此 _[!UICONTROL Product Listing Overrides]_页面打开。

   ![选择Amazon列表覆盖](assets/amazon-select-edit-overrides.png){width="125"}

1. 要确保覆盖正确的列表，请验证 _[!UICONTROL Listing Details]_.

1. 要编辑您的 _[!UICONTROL Override]_设置，为要更改的类型（价格、处理时间、条件、卖方备注）定义部分。

   要使覆盖类型保持不变，请选择 `No Change To <override type>` （默认）。 此设置使以前定义的覆盖值保持不变。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 并输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入以下项目的定义时间值（以天为单位）： **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 并选择正确的选项 **[!UICONTROL Condition Override]**.
   - **卖方备注**  — 单击 **[!UICONTROL Change Seller Notes]** 并输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 要删除覆盖类型，请单击 **移除** 用于您要删除的每个类型。 如果未删除，则先前定义的值将保留在覆盖中。

1. 单击 **[!UICONTROL Save Listing Override]**.

   此 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表的状态更改为 `Relist in Progress`. 更改将使用您的下一个数据同步（在cron设置中配置）发布到Amazon。 如果尚未列出，则也会将列表添加到_[!UICONTROL Overrides]_ 选项卡。

正在附带 _创建覆盖_ 示例。 以下示例显示对之前创建的覆盖的编辑，该编辑定义了以下内容的新价格 `$50`，删除处理时间覆盖，并保留以前的条件和卖方票据覆盖。

![编辑或删除覆盖](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## 编辑或删除多个列表的覆盖 {#edit-override-multiple-listings}

此 _[!UICONTROL Edit Listing Overrides]_操作可在_[!UICONTROL Inactive]_， _[!UICONTROL Active]_，_[!UICONTROL Overrides]_、和 _[!UICONTROL Ineligible]_选项卡。

>[!NOTE]
>
>由于您正在修改多个列表的覆盖，因此 _[!UICONTROL Listing Details]_部分不按修改单个列表时的方式显示。

1. 查看列表 _[!UICONTROL Products Listings]_页面(_[!UICONTROL Inactive]_， _[!UICONTROL Active]_，_[!UICONTROL Overrides]_、和 _[!UICONTROL Ineligible]_选项卡)。

1. 选中左侧列中的复选框，以选中要修改的每个列表。

1. 下 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Edit Listing Overrides]**.

   此 _[!UICONTROL Product Listing Overrides]_页面打开。

   ![选择Amazon列表覆盖](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. 要编辑您的 _[!UICONTROL Override]_设置，为要更改的类型（价格、处理时间、条件、卖方备注）定义部分。

   要使覆盖保持不变，请选择 `No Change To <override type>` （默认）。 此设置使以前定义的覆盖值保持不变。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 并输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入以下项目的定义时间值（以天为单位）： **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 并选择正确的选项 **[!UICONTROL Condition Override]**.
   - **卖方备注**  — 单击 **[!UICONTROL Change Seller Notes]** 并输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 要删除覆盖类型，请单击 **[!UICONTROL Remove]** 用于您要删除的每个类型。 如果未删除，则先前定义的值将保留在覆盖中。

1. 单击 **[!UICONTROL Save Listing Override]**.

   此 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表的状态更改为 `Relist in Progress`. 更改将使用您的下一个数据同步（在cron设置中配置）发布到Amazon。 如果尚未列出，则也会将列表添加到_[!UICONTROL Overrides]_ 选项卡。

### 覆盖类型

| 覆盖 | 描述 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | 价格覆盖定义了列表的价格。 此覆盖优先于所有自动设置，直到覆盖被删除。<br><br>要覆盖产品价格，请选择 **[!UICONTROL Change Listing Price]** 并输入新的价格 **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | 处理时间覆盖定义处理和发运产品所需的时间（以天为单位）。 处理时间覆盖优先于所有自动和默认处理时间设置，直到覆盖被删除。<br><br>中存在的值 _[!UICONTROL Handling Time Override]_框是在 [列表设置](./listing-settings.md) 或您定义的覆盖处理时间。 如果删除了处理时间覆盖，则列表将默认为列表设置中定义的处理时间。<br><br>要定义处理时间改写，请选择&#x200B;**[!UICONTROL Change Handling Time]**并输入的新处理时间（以天为单位）**[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | 要覆盖列表条件，请选择 **[!UICONTROL Change Condition]** 并从中选择新条件 **条件覆盖**. |
| [!UICONTROL Seller Notes Override] | 对于目录中的产品，其定义条件不是 `New`，可添加卖家注释，向潜在买家进一步详细说明您的产品及其条件。 您可以为输入卖方备注覆盖 `New` 条件产品，但Amazon不显示注释。<br><br>要覆盖卖方备注，请选择 **[!UICONTROL Change Seller Notes]** 并输入新注释 **[!UICONTROL Seller Notes Override]**. |
