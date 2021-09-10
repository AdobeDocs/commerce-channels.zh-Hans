---
title: Amazon商店视图
description: 转到Amazon商店视图，以快速查看每个Amazon商店的基本统计信息和访问管理选项。
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon商店视图

查看Amazon销售渠道主页时，默认打开&#x200B;_Amazon商店_&#x200B;视图。

![Amazon商店视图](assets/amazon-sales-channel-home-tabs.png)

_[!UICONTROL Amazon Stores]_视图会为您的每个Amazon存储显示一个“存储卡”，以及一些基本的统计和管理选项。 每张卡片中显示的摘要信息包括每个商店状态、创建日期、上次更新日期、需要注意的列表(例如：列表不完整)和分配的[!DNL Commerce]网站。

查看&#x200B;_[!UICONTROL Amazon Store]_视图时，每个商店卡都允许您：

- 要打开存储[功能板](./amazon-store-dashboard.md)，请单击&#x200B;**[!UICONTROL View Store]**。

- 要更改存储状态或删除存储，请单击&#x200B;**[!UICONTROL Action]**&#x200B;并选择：

   - **[!UICONTROL Activate]** /  **[!UICONTROL Deactivate]**  — 选择将存储的状态分别 `Active` 更改 `Inactive`为或。

      将`Inactive`存储更改为`Active`状态会使用存储当前存储设置（如列表设置、价格规则和覆盖）激活存储的列表和订单活动。

      将存储状态从`Active`更改为`Inactive`状态会暂停存储的列表和订单活动。 非活动存储保留了所有存储设置和列表，但暂时停止定价、数量和订单管理的同步，直到该存储重新变为`Active`状态。 此功能允许您在区域级别控制您的商店活动，而无需重新创建或重新集成Amazon商店，或丢失历史订单和销售数据。

   - **[!UICONTROL Delete]**  — 选择删除不再需要的存储。

      选择您希望何时删除现有的Amazon商店及其与[!DNL Amazon Seller Central]帐户的集成设置。 删除帐户会从Amazon销售渠道中删除该商店，以及与该商店相关的所有帐户设置、列表、日志和其他信息。 删除后无法检索该存储，必须创建新存储。

>[!NOTE]
>要在集成期间更改分配给存储的网站，您必须删除该存储，并使用存储集成期间定义的不同网站再次添加该存储。

| 存储卡 | 描述 |
|--- |--- |
| 顶部 | 包括：<br>存储区域图标，在[存储集成](./store-integration.md)期间定义。<br> 在存储集 _[!UICONTROL Magento Website]_成过程中定义的分配。<br>你_[!UICONTROL Status]_ 店的。选项：**[!UICONTROL Active]** — 使用Amazon完成并验证了商店集成，可用于销售活动。 **[!UICONTROL Inactive]**  — 商店集成已完成，但尚未使用或可用于销售活动。当`Inactive`时，您的Amazon销售将暂停。 当`Active`时，将保存销售收入和其他设置以在激活之前进行更新。<br>对 *[!UICONTROL Last Updated]* Amazon商店设置进行最新更改的日期。<br>在 *[!UICONTROL Created]* Amazon销售渠道中创建Amazon商店的日期。 |
| 中段 | 包括最近30天的商店活动摘要图表，并包括需要注意的任何列表以及相应的警报。 |
| 底部 | 包括“查看存储”和“操作”选项。<br>要打开商店功 [能板](./amazon-store-dashboard.md)，请单 **[!UICONTROL View Store]**&#x200B;击。<br>要激活、取消激活或删除存储，请单击 **[!UICONTROL Actions]**。 |
