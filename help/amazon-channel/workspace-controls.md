---
title: Amazon sales channel — 工作区控件
description: AmazonSales Channel提供工作区控件，可帮助您查找列表、查看信息以及轻松应用操作。
feature: Sales Channels
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# 工作区控件

Amazon销售渠道 [主页](./amazon-sales-channel-home.md) 具有一些常见的工作区控件，包括筛选器、默认视图、列和导出。 并非所有页面都具有相同的控制选项。

![AmazonSales Channel工作区控制示例](assets/amazon-workspace-controls.png){width="600" zoomable="yes"}

## 操作

此 _[!UICONTROL Actions]_选择器提供了用户可用于页面的操作列表。 选中后，该操作将应用于所有选定项目。 要将操作应用于特定项目，请选中每个项目第一列中的复选框，然后选择下的选项_[!UICONTROL Actions]_.

例如，当选择器显示在 _[!UICONTROL Attributes]_页面上，它包含_[!UICONTROL Re-import Product Attribute Values]_ 操作。 选择此操作将试通 [!DNL Amazon Seller Central] 帐户并刷新 [!DNL Commerce] 左侧列中勾选了每个Amazon存储项的数据。

![“操作”菜单示例](assets/amazon-sales-channel-home-actions-option.png){width="500"}

## 筛选器

此 _[!UICONTROL Filters]_控件显示用于缩小表中显示的数据范围的选项。 过滤器选项基于在“列”控件中选择的列。 筛选选项仅显示在列控件中启用的列。

过滤器控件可以包括用于缩小指定日期的数据范围的动态日历、具有预定义选择的列的下拉菜单以及可能包含自定义数据的自由文本字段。

以下示例显示了用于筛选订单列表的设置，以仅显示满足以下条件的订单：

- 2019年1月2日至2019年7月2日期间下达的订单，以及
- 买方名为的订单 `Smith`、和
- 状态为“ ”的订单 `Shipped`.

设置好筛选选项后，单击 **[!UICONTROL Apply Filters]** 以筛选列出的数据。 单击“取消”退出“筛选器”控件而不应用。

![过滤器控件示例](assets/workspace-controls-filters.png){width="600" zoomable="yes"}

将过滤器应用于数据后， **[!UICONTROL Active Filters]** 将显示信息。 您可以单击 ![“清除过滤器”图标](assets/x-icon-clear-filters.png) 图标以清除特定的过滤器选项，或单击 **[!UICONTROL Clear All]** 以清除所有应用的筛选器。

![活动过滤器示例](assets/applied-filters-line.png){width="700"}

## 视图

“视图”控件基于页面的默认列，因此被命名为“默认视图”。 您可以使用“列”控件添加或删除可用列。 自定义列时，您随后可以将视图另存为视图控件中的自定义视图。

在页面显示中添加或删除列后：

1. 单击 **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. 输入视图的名称。

1. 要保存自定义视图，请单击箭头图标。

![查看控件示例](assets/workspace-controls-view.png)

在此示例中， _订单ID_ 列会添加到列控件中并另存为自定义视图。 请注意，保存自定义视图名称后，视图名称会从 _默认视图_ 输入名称。

您可以通过在视图之间选择所需的视图来切换 _[!UICONTROL View]_菜单。

如果要删除或更改自定义视图的名称，请单击铅笔图标。 然后，您可以输入其他名称，也可以单击垃圾桶图标以删除自定义视图。 无法删除默认视图。

## 列

列控件允许您在页面显示中添加或删除数据列。 每个Amazon Sales Channel页面都有一个预设的数据列组合，但大多数页面都有可用的其他列。 如果没有可用的其他列，您仍可以从显示中删除默认列。

以下示例显示了Columns控件。 选中选项对应于页面上显示的列标题。

- 要向页面中添加数据列，请选中复选框。
- 要从页面中删除数据列，请不要选中复选框。

![列控件示例](assets/workspace-controls-columns.png){width="400"}

复选框更改会立即显示。 如果进行更改并退出该页面，则该页面将返回到默认列显示。 对于您定期进行的更改，可以将列更改保存为视图控件中的自定义视图。 然后，您可以在视图控件中切换，而无需手动添加或删除列。

您可以单击 **[!UICONTROL Reset]** 以将选项设置回默认设置，或者您可以单击 **[!UICONTROL Cancel]** 退出而不进行更改。

## 导出

导出选项允许您将数据导出到数据文件，而数据文件可以导入到第三方软件或单独的数据库中。 导出的数据仅限于显示的数据。 如果需要，请确保在使用导出控制之前添加或删除列。

准备导出数据时，请选择导出格式选项并单击 **[!UICONTROL Export]**.

- CSV — 包含纯文本数据的逗号分隔值文件
- Excel XML — 基于XML的电子表格数据格式（通常用于Excel用户）

生成的数据文件会自动保存到您指定的文件夹以供下载。

![导出控制](assets/workspace-controls-export.png){width="250"}
