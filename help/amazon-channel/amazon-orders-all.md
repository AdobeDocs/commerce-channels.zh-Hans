---
title: 查看Amazon订单
description: 在“Amazon商务”或“Magento Open Source管理员”中查看您的Adobe Marketplace订单。
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 查看Amazon订单

有两种方法可查看您的Amazon订单：_[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_。

这两个选项都会显示从Amazon收到的基本订单信息，包括：

- 购买日期
- 订单编号
- 状态
- 买方名称
- 总计
- 订单说明

_[!UICONTROL All Orders]_视图为订单搜索添加筛选选项。

>[!NOTE]
>
>除了&#x200B;_[!UICONTROL Order Notes]_列，_[!UICONTROL Amazon orders]_&#x200B;表中填充了从Amazon收到的订单信息。 _Order Notes_&#x200B;列在订单处理过程中由[!DNL Commerce]更新。

## 最近订单

您可以在[存储功能板](./amazon-store-dashboard.md)的&#x200B;_[!UICONTROL Recent Orders]_部分查看最新订单。

![最近订购](assets/amazon-recent-orders-imported.png)

### 查看最近的Amazon订单

1. 单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在&#x200B;_[!UICONTROL Recent Orders]_部分查看您的订单。

1. 要查看订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单编号。

   此时将打开订单的&#x200B;_[!UICONTROL Amazon Order Details]_页面。

## 查看所有订单

您可以在&#x200B;_[!UICONTROL Amazon orders]_页面上查看所有Amazon订单（也称为_[!UICONTROL All Orders]_&#x200B;视图）。 “Amazon订单”表类似于商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分，但允许您查看所有Amazon订单，并通过以下筛选选项缩小订单列表：

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon订单](assets/amazon-orders-list-all.png)

### 查看所有Amazon订单

1. 单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

1. 单击&#x200B;_[!UICONTROL Recent Orders]_部分中的&#x200B;**[!UICONTROL All Orders]**。

1. 要缩小列表或搜索特定订单编号，请完成&#x200B;**[!UICONTROL Filter by]**&#x200B;参数并单击&#x200B;**[!UICONTROL Apply filters]**。

1. 要查看订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单编号。

   此时将打开订单的&#x200B;_[!UICONTROL Amazon Order Details]_页面。

## 使用过滤器

您可以在&#x200B;_[!UICONTROL Filter by]_部分将过滤器应用于订单列表。 选择并单击&#x200B;**[!UICONTROL Apply filters]**。 您应用的过滤器显示在订单网格的上方。

![用于查看Amazon订单的过滤器](assets/amazon-orders-filter-view.png)

### 更改应用的过滤器

- 您可以在&#x200B;_[!UICONTROL Filter by]_部分添加或更改过滤器。 单击&#x200B;**[!UICONTROL Apply filters]**以更新订单列表以及显示在订单网格上方的过滤器选项。

- 您可以通过单击过滤器的`x`一次删除过滤器，也可以通过单击&#x200B;**[!UICONTROL Clear all filters]**&#x200B;一次删除所有过滤器。 删除过滤器会更新订单列表以及显示在订单网格上方的过滤器选项。

- 如果订单列表较长，您可以使用网格下方的分页控件查看更多订单。

>[!TIP]
>
>有关订单视图的一些提示：
>
>- 如果您有多个Amazon存储集成，则在存储视图之间切换时，可能需要刷新页面视图，以更新当前存储的订单列表和分页视图。
>- 按列排序时，排序仅适用于当前列表视图。 最佳做法是过滤列表，然后对您正在查看的页面进行排序。
>- 根据视图窗口的宽度，您可能会在列中看到重叠的文本。 要展开要换行的文本的列，请扩大窗口视图。
>- 按&#x200B;_[!UICONTROL Total]_过滤时，按整数过滤。 输入小数量可能会导致结果中出现错误。


### 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Filter by] | 仅在&#x200B;_[!UICONTROL All Orders]_视图中可用。<br>根据以下信息缩小订单列表：<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | 从Amazon收到的购买日期。 |
| [!UICONTROL Order Number] | 由生成并从Amazon接收的订单号。 要查看Amazon Order Details（订单详细信息）屏幕，请单击链接。 |
| [!UICONTROL Status] | 订单的状态，由Amazon接收。 选项：`Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | 从Amazon收到的下单人的姓名。 |
| [!UICONTROL Grand Total] | 从Amazon收到的订单的货币总值。 |
| [!UICONTROL Order Notes] | 在[!DNL Commerce]中处理订单时记录的最新操作。 信息包括但不限于订单导入错误和订单处理更新。<br>**注意**:在订单处理过程中， [!DNL Commerce] 此字段会由更新。 |
