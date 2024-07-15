---
title: 查看Amazon订单
description: 在Adobe Commerce或Magento Open Source管理员中查看您的Amazon Marketplace订单。
feature: Sales Channels, Orders
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 查看Amazon订单

可通过两种方式查看您的Amazon订单：_[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_。

这两个选项都会显示从Amazon收到的基本订单信息，包括：

- 购买日期
- 订单号
- 状态
- 购买者姓名
- 总计
- 订单注释

_[!UICONTROL All Orders]_视图为订单搜索添加了筛选选项。

>[!NOTE]
>
>除&#x200B;_[!UICONTROL Order Notes]_列外，_[!UICONTROL Amazon orders]_&#x200B;表中填充了从Amazon接收的订单信息。 _订单备注_&#x200B;列由[!DNL Commerce]在订单处理过程中更新。

## 最新订单

您可以在[存储仪表板](./amazon-store-dashboard.md)的&#x200B;_[!UICONTROL Recent Orders]_部分中查看最近的订单。

![最近的订单](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### 查看最近的Amazon订单

1. 在商店信息卡上单击&#x200B;**[!UICONTROL View Store]**。

1. 在&#x200B;_[!UICONTROL Recent Orders]_部分中查看您的订单。

1. 要查看订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单号。

   此时将打开订单的&#x200B;_[!UICONTROL Amazon Order Details]_页面。

## 查看所有订单

您可以在&#x200B;_[!UICONTROL Amazon orders]_页面上查看您的所有Amazon订单（也称为_[!UICONTROL All Orders]_&#x200B;视图）。 Amazon订单表类似于商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分，但允许您查看所有Amazon订单，并使用以下筛选选项缩小订单列表：

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon订单](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### 查看所有Amazon订单

1. 在商店信息卡上单击&#x200B;**[!UICONTROL View Store]**。

1. 单击&#x200B;_[!UICONTROL Recent Orders]_部分中的&#x200B;**[!UICONTROL All Orders]**。

1. 要缩小列表范围或搜索特定订单号，请完成&#x200B;**[!UICONTROL Filter by]**&#x200B;参数并单击&#x200B;**[!UICONTROL Apply filters]**。

1. 要查看订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单号。

   此时将打开订单的&#x200B;_[!UICONTROL Amazon Order Details]_页面。

## 使用过滤器

您可以将过滤器应用于&#x200B;_[!UICONTROL Filter by]_部分中的订单列表。 进行选择并单击&#x200B;**[!UICONTROL Apply filters]**。 应用的筛选器显示在订单网格上方。

用于查看Amazon订单的![筛选器](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### 更改应用的筛选器

- 您可以在&#x200B;_[!UICONTROL Filter by]_部分中添加或更改您的筛选器。 单击&#x200B;**[!UICONTROL Apply filters]**以更新订单列表和显示在订单网格上方的筛选器选项。

- 您可以通过单击筛选器的`x`来逐个删除筛选器，也可以通过单击&#x200B;**[!UICONTROL Clear all filters]**&#x200B;来逐个删除所有筛选器。 删除筛选器将更新订单列表和显示在订单网格上方的筛选器选项。

- 如果订单列表较长，则可以使用网格下方的分页控件来查看更多订单。

>[!TIP]
>
>有关订单视图的一些提示：
>
>- 如果您有多个Amazon商店集成，则可能需要在商店视图之间切换时刷新页面视图，才能更新当前商店的订单列表和分页视图。
>- 按列排序时，排序仅适用于当前列表视图。 最佳实践是筛选列表，然后对查看的页面进行排序。
>- 根据视图窗口的宽度，您可能会在列中看到重叠文本。 要展开要换行的文本列，请加宽窗口视图。
>- 按&#x200B;_[!UICONTROL Total]_过滤时，按整数过滤。 输入小数可能会造成结果错误。

### 默认列

| 列 | 描述 |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | 仅在&#x200B;_[!UICONTROL All Orders]_视图中可用。<br>根据以下条件缩小订单列表：<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | 从Amazon收到的购买日期。 |
| [!UICONTROL Order Number] | 由Amazon生成并从接收的订单编号。 要查看Amazon订单详情屏幕，请单击链接。 |
| [!UICONTROL Status] | Amazon收到的订单状态。 选项： `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | 从Amazon收到的下订单人员的姓名。 |
| [!UICONTROL Grand Total] | 从Amazon收到的订单的总货币值。 |
| [!UICONTROL Order Notes] | 订单在[!DNL Commerce]中处理时记录的最近操作。 此信息包括但不限于订单导入错误和订单处理更新。<br>**注意**：此字段已由[!DNL Commerce]在订单处理过程中更新。 |
