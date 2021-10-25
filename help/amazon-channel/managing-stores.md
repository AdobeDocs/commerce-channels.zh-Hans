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

查看Amazon销售渠道主页时， _Amazon商店_ 默认情况下，视图会打开。

![Amazon商店视图](assets/amazon-sales-channel-home-tabs.png)

的 _[!UICONTROL Amazon Stores]_“视图”显示每个Amazon存储区的“存储卡”以及一些基本的统计和管理选项。 每张卡片中显示的摘要信息包括每个商店状态、创建日期、上次更新日期、需要注意的列表(例如：未完成的列表)和分配的 [!DNL Commerce] 网站。

查看 _[!UICONTROL Amazon Store]_查看，每个商店卡允许您：

- 打开商店 [仪表板](./amazon-store-dashboard.md)，单击 **[!UICONTROL View Store]**.

- 要更改存储状态或删除存储，请单击 **[!UICONTROL Action]** 并选择：

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]**  — 选择将存储的状态更改为 `Active` 或 `Inactive`，分别为。

      更改 `Inactive` 存储到 `Active` 状态可使用商店当前的商店设置（如列表设置、价格规则和覆盖）激活商店的列表和订单活动。

      从 `Active` to `Inactive` 状态会暂停商店的列表和订单活动。 非活动商店会保留所有商店设置和清单，但会暂时停止定价、数量和订单管理的同步，直到该商店被更改为 `Active` 状态。 此功能允许您在区域级别控制您的商店活动，而无需重新创建或重新集成Amazon商店，或丢失历史订单和销售数据。

   - **[!UICONTROL Delete]**  — 选择删除不再需要的存储。

      选择您希望删除现有Amazon商店及其与 [!DNL Amazon Seller Central] 帐户。 删除帐户会从Amazon销售渠道中删除该商店，以及与该商店相关的所有帐户设置、列表、日志和其他信息。 删除后无法检索该存储，必须创建新存储。

>[!NOTE]
>要在集成期间更改分配给存储的网站，您必须删除该存储，并使用存储集成期间定义的不同网站再次添加该存储。

| 存储卡 | 描述 |
|--- |--- |
| 顶部 | 包括： <br>存储的区域图标，在 [存储集成](./store-integration.md).<br> 分配的 _[!UICONTROL Magento Website]_，在存储集成期间定义。<br>的_[!UICONTROL Status]_ 你的店。 选项： **[!UICONTROL Active]**  — 商店集成已通过Amazon完成和验证，可用于销售活动。 **[!UICONTROL Inactive]**  — 商店集成已完成，但尚未使用或可用于销售活动。 When `Inactive`，则Amazon销售会暂停。 When `Active`、销售收入和其他要保存的设置，以在激活之前进行更新。<br>的 *[!UICONTROL Last Updated]* Amazon商店设置最近更改的日期。<br>的 *[!UICONTROL Created]* 在Amazon销售渠道中创建Amazon商店的日期。 |
| 中段 | 包括最近30天的商店活动摘要图表，并包括需要注意的任何列表以及相应的警报。 |
| 底部 | 包括“查看存储”和“操作”选项。<br>打开商店 [仪表板](./amazon-store-dashboard.md)，单击 **[!UICONTROL View Store]**.<br>要激活、停用或删除存储，请单击 **[!UICONTROL Actions]**. |
