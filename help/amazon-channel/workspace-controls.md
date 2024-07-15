---
title: Amazon sales channel - Workspace控件
description: AmazonSales Channel提供了工作区控件，可帮助您查找列表、查看信息以及轻松应用操作。
feature: Sales Channels
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Workspace控件

Amazon Sales Channel [主页](./amazon-sales-channel-home.md)有一些常见的工作区控件，包括筛选器、默认视图、列和导出。 并非所有页面都具有相同的控制选项。

![AmazonSales Channel工作区控件示例](assets/amazon-workspace-controls.png){width="600" zoomable="yes"}

## 操作

_[!UICONTROL Actions]_选择器提供了一个用户可用于页面的操作列表。 选中后，该操作将应用于所有选定项目。 要将操作应用于特定项目，请选中每个项目第一列中的复选框，然后选择_[!UICONTROL Actions]_&#x200B;下的选项。

例如，当选择器显示在&#x200B;_[!UICONTROL Attributes]_页面上时，它包含_[!UICONTROL Re-import Product Attribute Values]_&#x200B;操作。 选择此操作将会ping相应的[!DNL Amazon Seller Central]帐户，并刷新左侧列中检查的每个Amazon存储项目的[!DNL Commerce]数据。

![操作菜单示例](assets/amazon-sales-channel-home-actions-option.png){width="500"}

## 过滤器

_[!UICONTROL Filters]_控件显示用于缩小表中显示的数据范围的选项。 筛选器选项基于在“列”控件中选择的列。 筛选器选项仅显示在列控件中启用的列。

筛选器控件可以包括用于缩小指定日期的数据范围的动态日历、具有预定义选择的列的下拉菜单以及可能包含自定义数据的自由文本字段。

以下示例显示了用于筛选订单列表的设置，以仅显示满足以下条件的订单：

- 2019年1月2日至2019年7月2日期间下达的订单，以及
- 具有名为`Smith`的买家的订单，并且
- 状态为`Shipped`的订单。

设置筛选选项后，单击&#x200B;**[!UICONTROL Apply Filters]**&#x200B;以筛选列出的数据。 单击“取消”退出“筛选器”控件而不应用。

![筛选器控件示例](assets/workspace-controls-filters.png){width="600" zoomable="yes"}

将筛选器应用于数据后，将显示&#x200B;**[!UICONTROL Active Filters]**&#x200B;信息。 您可以单击![清除筛选器图标](assets/x-icon-clear-filters.png)图标以清除特定筛选器选项，或单击&#x200B;**[!UICONTROL Clear All]**&#x200B;以清除所有应用的筛选器。

![活动筛选器示例](assets/applied-filters-line.png){width="700"}

## 视图

“视图”控件基于页面的默认列，因此将其命名为“默认视图”。 可以使用“列”控件添加或删除可用列。 自定义列时，您随后可以将视图另存为视图控件中的自定义视图。

在页面显示中添加或删除列后：

1. 单击&#x200B;**[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**。

1. 输入视图的名称。

1. 要保存自定义视图，请单击箭头图标。

![查看控件示例](assets/workspace-controls-view.png)

在此示例中，_订单ID_&#x200B;列被添加到列控件中并另存为自定义视图。 请注意，保存自定义视图名称后，视图名称已从&#x200B;_默认视图_&#x200B;更改为输入的名称。

您可以在&#x200B;_[!UICONTROL View]_菜单中选择所需的视图来切换视图。

如果要删除或更改自定义视图的名称，请单击铅笔图标。 然后，您可以输入其他名称，也可以单击垃圾桶图标以删除自定义视图。 无法删除默认视图。

## 列

列控件允许您在页面显示中添加或删除数据列。 每个Amazon Sales Channel页面都有一个预设的数据列组合，但大多数页面都有可用的其他列。 如果没有可用的其他列，您仍可以从显示中删除默认列。

以下示例显示了Columns控件。 勾选选项对应于页面上显示的列标题。

- 要向页面中添加数据列，请选中复选框。
- 要从页面中删除数据列，请勿选中复选框。

![列控件示例](assets/workspace-controls-columns.png){width="400"}

复选框更改会立即显示。 如果进行更改并退出页面，则该页面将返回到默认列显示。 对于您定期进行的更改，您可以在“视图”控件中将列更改另存为自定义视图。 然后，您可以在视图控件中进行切换，而无需手动添加或删除列。

您可以单击&#x200B;**[!UICONTROL Reset]**&#x200B;将选项设置回默认设置，也可以单击&#x200B;**[!UICONTROL Cancel]**&#x200B;退出而不进行更改。

## 导出

导出选项允许您将数据导出到数据文件，而数据文件可以导入到第三方软件或单独的数据库中。 导出的数据仅限于显示的数据。 如果需要，请确保在使用导出控制之前添加或删除列。

准备导出数据时，请选择导出格式选项并单击&#x200B;**[!UICONTROL Export]**。

- CSV — 包含纯文本数据的逗号分隔值文件
- Excel XML — 一种基于XML的电子表格数据格式（通常用于Excel用户）

生成的数据文件会自动保存到您指定的文件夹以供下载。

![导出控制](assets/workspace-controls-export.png){width="250"}
