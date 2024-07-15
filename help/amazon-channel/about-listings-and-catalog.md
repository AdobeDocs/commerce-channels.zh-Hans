---
title: Amazon和Commerce目录
description: Amazon Sales Channel可将您的Amazon列表导入到Commerce后端，并不断与产品和销售同步。
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazon和[!DNL Commerce]目录

您的Adobe Commerce或Magento Open Source后端包括一个目录，其中包含所有产品和相关设置及信息（图像、选项、价格等）以及订单和送货配置。 您的[!DNL Amazon Seller Central]帐户还具有目录和订单配置，通过[!DNL Amazon Marketplace]严格跟踪您的销售。

为了更好地通过某个位置管理和审查产品目录和销售额，Amazon销售渠道会将您的Amazon列表导入您的[!DNL Commerce]后端，不断与产品和销售同步，并报告问题和趋势。 它支持与多个[!DNL Amazon Seller Central]帐户的集成，通过单个界面跟踪多个店面的所有数据。

## 产品属性

Adobe Commerce和Magento Open Source使用产品[属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)来定义产品设置和数据，从而管理目录同步。 Amazon还使用属性，通过载入进行映射。 在为Amazon销售渠道执行[预设置任务](./amazon-pre-setup-tasks.md)期间，您可以定义其他Amazon属性（如果需要），以确保在将Amazon列表导入[!DNL Commerce]目录时产品映射正确。 这些属性包括UPC、EAN、ISBN和ASIN ([!DNL Amazon Standard Identification Number])。 通过载入，产品使用您的属性在Amazon和[!DNL Commerce]目录之间同步。 [!DNL Commerce]和Amazon产品的正确映射可确保产品信息、订单和库存的持续同步。

如果您没有为目录创建或配置这些属性，则应在载入之前向产品添加[!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)和值。 导入Amazon属性后，该属性可用于搜索、导航、价格规则等。 查看[ASIN、UPC、EAN、ISBN、SKU和其他条形码的含义是什么？](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

新用户引导后，您可以随时管理和更新产品属性和Amazon映射。

## 产品列表

Amazon列表是您通过[!DNL Amazon Marketplace]销售的每种产品的产品页面，用于显示通过属性映射的产品描述、价格、图像等。 在新用户引导期间，您可以配置可自动将您的[!DNL Commerce]产品发布到Amazon列表。 您还可以通过将现有Amazon列表映射到[!DNL Commerce]产品来导入这些列表。

创建清单[!DNL Commerce]产品后，这些产品将提交到Amazon进行审批。 大多数成功的列表都会在几个小时内获得批准。 如果您的列表已获得批准，它将显示在[!DNL Amazon Marketplace]中，以供客户立即订购。 [!DNL Amazon Sales Channel]扩展提供了一组用于查看Amazon列表的选项卡。 根据问题或所需数据，您应该查看您的[!DNL Amazon Seller Central]帐户以获取有关这些列表的特定详细信息。

- [活动](./active-listings.md)：列出通过市场提供的已批准产品清单。

- [准备列出](./ready-to-list.md)：列出符合列出规则要求并准备发布到Amazon的产品。

- [不活动](./inactive-listings.md)：列出由于特定原因（如品牌策略问题）被阻止、已关闭且需要重新粘贴等原因而在商城中不可用的产品。

- [不符合条件](./ineligible-listings.md)：由于列表规则，列出无法在商城中主动列出的产品（如`0`数量或销售日期）。

- [不完整](./incomplete-listings.md)：列出缺少所需信息的产品。 更新产品数据以供另一审阅。

- [已结束](./ended-listings.md)：列出有资格列出但手动从Amazon中移除的产品清单。 您可以重新列出这些产品。

## 正在同步数据

Adobe Commerce和Magento Open Source在您的[!DNL Amazon Seller Central]帐户和[!DNL Commerce]后端之间传输产品和订单数据。 连续更新通过[!DNL Commerce]提供单个来源，用于管理和维护库存、完成订单、跟踪销售以及减少开销和重复工作。 报告会捕获最新数据，以便跟踪趋势并解决在两个系统之间捕获的通信问题。

所有同步操作都由[cron作业](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)管理，在[预设置任务](./amazon-pre-setup-tasks.md)中，设置为每五分钟更新一次。
