---
title: 手动发布Amazon列表
description: 如果需要，您可以从Commerce管理员手动发布已结束的Amazon列表。
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 手动发布Amazon列表

您可以手动发布一个或多个已结束的Amazon列表。

1. 在“ ”上查看一个或多个列表 _[!UICONTROL Ended]_选项卡 [产品列表](./managing-product-listings.md) 页面(_[!UICONTROL Inactive]_， _[!UICONTROL Active]_，或_[!UICONTROL Ineligible]_ 选项卡)。

1. 在左栏中，单击以选中要重新发布的每个列表。

1. 下 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Publish Product to Amazon]**.

1. 单击 **[!UICONTROL OK]** 在确认消息中。

   此时会显示一条消息，确认正在处理选定的列表以发布到Amazon。

   列表信息会根据您的cron设置发布到Amazon。 列表信息会在下次数据同步时发送到Amazon。 在Amazon回复列表确认之前，手动发布的列表将保留在 _准备列出_ 制表符 `List in Progress` 状态。 从Amazon收到列表确认后，列表将移至 _活动_ 制表符 `Active` 状态。
