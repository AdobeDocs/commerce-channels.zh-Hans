---
title: 创建和编辑覆盖
description: 使用AmazonSales Channel覆盖将您所做的更改应用于单个Amazon列表或多个列表。
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# 创建和编辑覆盖

您可以为列表创建和覆盖，也可以编辑或删除已应用于列表的覆盖。 覆盖为特定列表设置定义的值。

## 为单个列表创建覆盖

的 _[!UICONTROL Create Override]_查看_[!UICONTROL Inactive]_, _[!UICONTROL Active]_和_[!UICONTROL Ineligible]_ 选项卡。

1. 查看 _[!UICONTROL Products Listings]_页面(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_和_[!UICONTROL Ineligible]_ 选项卡。

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Create Override]**打开产品列表覆盖页面。

   ![创建Amazon列表覆盖](assets/amazon-select-create-override.png)

1. 为确保您查看的列表正确，请验证 _[!UICONTROL Listing Details]_.

1. 确定要创建的覆盖类型。

   您可以为列表定义单个改写类型或任何类型组合（价格、处理时间、条件、销售者附注）。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入定义的时间值（以天为单位） **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 并为 **[!UICONTROL Condition Override]**.
   - **卖家说明**  — 单击 **[!UICONTROL Change Seller Notes]** 输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 单击 **[!UICONTROL Save Listing Override]**.

   的 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表状态将更改为 `Relist in Progress`. 所做的更改将随下次数据同步一起发布到Amazon（在您的cron设置中配置）。 此列表也会添加到_[!UICONTROL Overrides]_ 选项卡。

以下示例显示了定义新价格的覆盖 `$55`，新的处理时间 `1 day`，新条件 `Used; Like New`和新的卖家票据文本。

![Amazon列表覆盖示例](assets/amazon-overrides-edit.png)

## 编辑或删除单个列表的覆盖 {#edit-override-single-listing}

的 _[!UICONTROL Edit Overrides]_查看_[!UICONTROL Overrides]_ 选项卡。

1. 查看 _[!UICONTROL Product Listings]_页面(_[!UICONTROL Overrides]_ 选项卡。

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   的 _[!UICONTROL Product Listing Overrides]_页面。

   ![选择Amazon列表覆盖](assets/amazon-select-edit-overrides.png)

1. 要确保覆盖正确的列表，请验证 _[!UICONTROL Listing Details]_.

1. 编辑 _[!UICONTROL Override]_设置，为要更改的类型（“价格”、“处理时间”、“条件”、“卖家附注”）定义部分。

   若要使覆盖类型保持相同，请选择 `No Change To <override type>` （默认）。 此设置会保持先前定义的覆盖值不变。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入定义的时间值（以天为单位） **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 选择正确的选项 **[!UICONTROL Condition Override]**.
   - **卖家说明**  — 单击 **[!UICONTROL Change Seller Notes]** 输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 要删除覆盖类型，请单击 **删除** 适用于要删除的每种类型。 如果未删除，则之前定义的值将保留在覆盖中。

1. 单击 **[!UICONTROL Save Listing Override]**.

   的 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表状态将更改为 `Relist in Progress`. 所做的更改将随下次数据同步一起发布到Amazon（在您的cron设置中配置）。 如果列表尚未列出，则还会将列表添加到_[!UICONTROL Overrides]_ 选项卡。

借用 _创建覆盖_ 示例。 以下示例显示对之前创建的覆盖的编辑，该覆盖定义了 `$50`，删除“处理时间”改写，并保留以前的“条件”和“卖家附注”改写。

![编辑或删除覆盖](assets/amazon-overrides-edit-2.png)
__

## 编辑或删除多个列表的覆盖 {#edit-override-multiple-listings}

的 _[!UICONTROL Edit Listing Overrides]_操作在_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_&#x200B;和 _[!UICONTROL Ineligible]_选项卡。

>[!NOTE]
>
>由于您正在修改多个列表的覆盖，因此 _[!UICONTROL Listing Details]_部分不会像修改单个列表时一样显示。

1. 查看 _[!UICONTROL Products Listings]_页面(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_&#x200B;和 _[!UICONTROL Ineligible]_选项卡。

1. 选中每个要修改的列表左侧列中的复选框。

1. 在 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Edit Listing Overrides]**.

   的 _[!UICONTROL Product Listing Overrides]_页面。

   ![选择Amazon列表覆盖](assets/amazon-actions-edit-listing-overrides.png)

1. 编辑 _[!UICONTROL Override]_设置，为要更改的类型（“价格”、“处理时间”、“条件”、“卖家附注”）定义部分。

   要保持覆盖相同，请选择 `No Change To <override type>` （默认）。 此设置会保持先前定义的覆盖值不变。

   - **价格**  — 单击 **[!UICONTROL Change Listing Price]** 输入您定义的价格值 **[!UICONTROL Price Override]**.
   - **处理时间**  — 单击 **[!UICONTROL Change Handling Time]** 并输入定义的时间值（以天为单位） **[!UICONTROL Handling Time Override]**.
   - **条件**  — 单击 **[!UICONTROL Change Condition]** 选择正确的选项 **[!UICONTROL Condition Override]**.
   - **卖家说明**  — 单击 **[!UICONTROL Change Seller Notes]** 输入注释文本 **[!UICONTROL Seller Notes Override]**.

1. 要删除覆盖类型，请单击 **[!UICONTROL Remove]** 适用于要删除的每种类型。 如果未删除，则之前定义的值将保留在覆盖中。

1. 单击 **[!UICONTROL Save Listing Override]**.

   的 _[!UICONTROL Product Listing Overrides]_页面关闭。 列表的状态将更改为 `Relist in Progress`. 所做的更改将随下次数据同步一起发布到Amazon（在您的cron设置中配置）。 如果列表尚未列出，则还会将列表添加到_[!UICONTROL Overrides]_ 选项卡。

### 覆盖类型

| 覆盖 | 描述 |
|--- |--- |
| [!UICONTROL Price Override] | 价格覆盖可定义列表的价格。 在删除覆盖之前，此覆盖优先于所有自动设置。<br><br>要覆盖产品的价格，请选择 **[!UICONTROL Change Listing Price]** 并输入 **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | 处理时间覆盖定义处理和发运产品所花费的时间（以天为单位）。 处理时间覆盖优先于所有自动和默认的处理时间设置，直到删除覆盖为止。<br><br>中存在的值 _[!UICONTROL Handling Time Override]_框中，选择自定义的 [列表设置](./listing-settings.md) 或您定义的覆盖处理时间。 如果删除处理时间覆盖，则列表将默认为列表设置中定义的处理时间。<br><br>要定义处理时间覆盖，请选择&#x200B;**[!UICONTROL Change Handling Time]**并输入的新处理时间（以天为单位）**[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | 要覆盖列表条件，请选择 **[!UICONTROL Change Condition]** 并从 **条件覆盖**. |
| [!UICONTROL Seller Notes Override] | 适用于目录中使用以下条件定义的产品 `New`，可以添加销售者注释，以进一步详细说明您的产品及其条件，以便向潜在购买者提供。 您可以为 `New` 条件产品，但Amazon不显示注释。<br><br>要改写销售者附注，请选择 **[!UICONTROL Change Seller Notes]** 并输入新注释 **[!UICONTROL Seller Notes Override]**. |
