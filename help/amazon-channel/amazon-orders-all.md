---
title: 查看Amazon订单
description: 在Adobe Commerce或Magento Open Source管理员中查看您的Amazon Marketplace订单。
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 查看Amazon订单

查看您的Amazon订单的方法有两种： _[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_.

这两个选项都会显示从Amazon收到的基本订单信息，包括：

- 购买日期
- 订单号
- 状态
- 买家姓名
- 总计
- 订单注释

_[!UICONTROL All Orders]_视图为订单搜索添加筛选选项。

>[!NOTE]
>
>除了 _[!UICONTROL Order Notes]_列，_[!UICONTROL Amazon orders]_ 表格中填充了从Amazon收到的订单信息。 此 _订单注释_ 列更新者 [!DNL Commerce] 随着订单的处理。

## 最近的订单

您可以在中查看最近的订单 _[!UICONTROL Recent Orders]_部分 [存储仪表板](./amazon-store-dashboard.md).

![最近的订单](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### 查看最近的Amazon订单

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在中查看订单 _[!UICONTROL Recent Orders]_部分。

1. Amazon要查看订单详细信息，请单击 _[!UICONTROL Order Number]_列。

   此 _[!UICONTROL Amazon Order Details]_此时将打开订单页面。

## 查看所有订单

您可以在以下网站查看所有Amazon订单： _[!UICONTROL Amazon orders]_页面(也称为_[!UICONTROL All Orders]_ 视图)。 Amazon的“订单”表类似于 _[!UICONTROL Recent Orders]_区域，但允许您查看所有Amazon订单，并使用以下筛选选项缩小订单范围：

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon订单](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### 查看所有Amazon订单

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 单击 **[!UICONTROL All Orders]** 在 _[!UICONTROL Recent Orders]_部分。

1. 要缩小列表范围或搜索特定订单编号，请填写 **[!UICONTROL Filter by]** 参数并单击 **[!UICONTROL Apply filters]**.

1. Amazon要查看订单详细信息，请单击 _[!UICONTROL Order Number]_列。

   此 _[!UICONTROL Amazon Order Details]_此时将打开订单页面。

## 使用过滤器

您可以在以下位置将过滤器应用于您的订单列表： _[!UICONTROL Filter by]_部分。 进行选择并单击&#x200B;**[!UICONTROL Apply filters]**. 应用的过滤器将显示在“订单”网格上方。

![用于查看Amazon订单的筛选器](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### 更改应用的筛选器

- 您可以在以下位置添加或更改您的筛选器： _[!UICONTROL Filter by]_部分。 单击&#x200B;**[!UICONTROL Apply filters]**以更新订单列表和显示在订单网格上方的筛选选项。

- 您可以通过单击 `x` ，或者一次单击全部 **[!UICONTROL Clear all filters]**. 删除过滤器会更新订单列表和出现在订单网格上方的过滤器选项。

- 如果订单列表较长，则可以使用网格下方的分页控件查看更多订单。

>[!TIP]
>
>有关订单视图的一些提示：
>
>- 如果您有多个Amazon商店集成，则可能需要在商店视图之间切换时刷新页面视图，以更新当前商店的订单列表和分页视图。
>- 按列排序时，排序仅适用于当前列表视图。 最佳实践是筛选列表，然后对查看的页面进行排序。
>- 根据视图窗口的宽度，您可能会看到列中重叠的文本。 要展开要换行的文本列，请加宽窗口视图。
>- 筛选条件为 _[!UICONTROL Total]_，按整数过滤。 输入小数可能会造成结果错误。


### 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Filter by] | 仅在 _[!UICONTROL All Orders]_视图。<br>根据以下条件缩小订单列表：<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | 从Amazon收到的购买日期。 |
| [!UICONTROL Order Number] | 由Amazon生成并从接收的订单编号。 要查看“Amazon订单详细信息”屏幕，请单击链接。 |
| [!UICONTROL Status] | Amazon收到的订单状态。 选项： `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | 从Amazon收到的下订单人员的姓名。 |
| [!UICONTROL Grand Total] | 从Amazon收到的订单总货币值。 |
| [!UICONTROL Order Notes] | 订单处理时记录的最近操作 [!DNL Commerce]. 信息包括但不限于订单导入错误和订单处理更新。<br>**注释**：此字段更新者 [!DNL Commerce] 随着订单的处理。 |
