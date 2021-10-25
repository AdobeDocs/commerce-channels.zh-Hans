---
title: 查看Amazon订单
description: 在Adobe Commerce或Magento Open Source管理员中查看您的Amazon Marketplace订单。
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 查看Amazon订单

有两种方法可查看您的Amazon订单： _[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_.

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
>除 _[!UICONTROL Order Notes]_列，_[!UICONTROL Amazon orders]_ 表格中填充有从Amazon收到的订单信息。 的 _订单说明_ 列更新者 [!DNL Commerce] 随顺序的流程。

## 最近订单

您可以在 _[!UICONTROL Recent Orders]_部分 [存储仪表板](./amazon-store-dashboard.md).

![最近订购](assets/amazon-recent-orders-imported.png)

### 查看最近的Amazon订单

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在 _[!UICONTROL Recent Orders]_中。

1. 要查看订单详细信息，请在 _[!UICONTROL Order Number]_列。

   的 _[!UICONTROL Amazon Order Details]_页面。

## 查看所有订单

您可以在 _[!UICONTROL Amazon orders]_页面(也称为_[!UICONTROL All Orders]_ 视图)。 Amazon订单表类似于 _[!UICONTROL Recent Orders]_区域，但允许您查看所有Amazon订单，并通过以下过滤选项缩小订单列表范围：

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon订单](assets/amazon-orders-list-all.png)

### 查看所有Amazon订单

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 单击 **[!UICONTROL All Orders]** 在 _[!UICONTROL Recent Orders]_中。

1. 要缩小列表或搜索特定订单编号，请完成 **[!UICONTROL Filter by]** 参数并单击 **[!UICONTROL Apply filters]**.

1. 要查看订单详细信息，请在 _[!UICONTROL Order Number]_列。

   的 _[!UICONTROL Amazon Order Details]_页面。

## 使用过滤器

您可以在 _[!UICONTROL Filter by]_中。 选择并单击&#x200B;**[!UICONTROL Apply filters]**. 您应用的过滤器显示在订单网格的上方。

![用于查看Amazon订单的过滤器](assets/amazon-orders-filter-view.png)

### 更改应用的过滤器

- 您可以在 _[!UICONTROL Filter by]_中。 单击&#x200B;**[!UICONTROL Apply filters]**更新订单列表和显示在订单网格上方的过滤器选项。

- 您可以通过单击 `x` (通过单击 **[!UICONTROL Clear all filters]**. 删除过滤器会更新订单列表以及显示在订单网格上方的过滤器选项。

- 如果订单列表较长，您可以使用网格下方的分页控件查看更多订单。

>[!TIP]
>
>有关订单视图的一些提示：
>
>- 如果您有多个Amazon存储集成，则在存储视图之间切换时，可能需要刷新页面视图，以更新当前存储的订单列表和分页视图。
>- 按列排序时，排序仅适用于当前列表视图。 最佳做法是过滤列表，然后对您正在查看的页面进行排序。
>- 根据视图窗口的宽度，您可能会在列中看到重叠的文本。 要展开要换行的文本的列，请扩大窗口视图。
>- 过滤依据 _[!UICONTROL Total]_，按整数过滤。 输入小数量可能会导致结果中出现错误。


### 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Filter by] | 仅在 _[!UICONTROL All Orders]_中。<br>根据以下信息缩小订单列表：<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | 从Amazon收到的购买日期。 |
| [!UICONTROL Order Number] | 由生成并从Amazon接收的订单号。 要查看Amazon Order Details（订单详细信息）屏幕，请单击链接。 |
| [!UICONTROL Status] | 订单的状态，由Amazon接收。 选项： `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | 从Amazon收到的下单人的姓名。 |
| [!UICONTROL Grand Total] | 从Amazon收到的订单的货币总值。 |
| [!UICONTROL Order Notes] | 在中处理订单时记录的订单最近的操作 [!DNL Commerce]. 信息包括但不限于订单导入错误和订单处理更新。<br>**注意**:此字段已更新为 [!DNL Commerce] 随顺序的流程。 |
