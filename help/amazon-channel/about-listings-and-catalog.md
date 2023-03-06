---
title: 关于Amazon和Commerce目录
description: Amazon Sales Channel可将您的Amazon列表导入Commerce后端，并持续与产品和销售同步。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 关于Amazon和 [!DNL Commerce] 目录

您的Adobe Commerce或Magento Open Source后端包含一个目录，其中包含所有产品和相关设置及信息（图像、选项、价格等）以及订单和发货配置。 您的 [!DNL Amazon Seller Central] 帐户还具有目录和订单配置，通过 [!DNL Amazon Marketplace].

为了更好地管理和查看产品目录和通过一个位置进行的销售，Amazon sales channel会将您的Amazon列表导入您的 [!DNL Commerce] 后端，持续与产品和销售同步，并报告问题和趋势。 它支持与多个集成 [!DNL Amazon Seller Central] 帐户，通过单个界面跟踪多个店面的所有数据。

## 产品属性

Adobe Commerce和Magento Open Source使用产品管理目录同步 [属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 以定义产品设置和数据。 Amazon还使用属性，通过载入进行映射。 期间 [预设置任务](./amazon-pre-setup-tasks.md) 对于Amazon sales channel，您可以定义其他Amazon属性（如果需要），以确保在将Amazon列表导入到您的渠道时产品映射正确。 [!DNL Commerce] 目录。 这些属性包括UPC、EAN、ISBN和ASIN ([!DNL Amazon Standard Identification Number])。 通过载入，产品可以在Amazon和之间同步 [!DNL Commerce] 使用您的属性的目录。 正确映射您的 [!DNL Commerce] 和Amazon产品可确保产品信息、订单和库存的持续同步。

如果您没有为目录创建或配置这些属性，则应添加 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} and values to your products before onboarding. When an Amazon attribute is imported, it can be used for search, navigation, price rules, and much more. See [What Do ASIN, UPC, EAN, ISBN, SKU and Other Barcodes Mean?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

新用户引导后，您可以随时管理和更新产品属性和Amazon映射。

## 产品列表

Amazon列表是您通过销售的每个产品的产品页 [!DNL Amazon Marketplace]，显示通过属性映射的产品描述、价格、图像等。 在新用户引导期间，您可以配置 [!DNL Commerce] 产品可以自动发布到Amazon列表。 您还可以通过将现有Amazon列表映射到您的 [!DNL Commerce] 产品。

创建列表后 [!DNL Commerce] 产品，则会提交到Amazon以供审批。 大多数成功的列表会在几小时内获得批准。 如果您的列表获得批准，它将显示在 [!DNL Amazon Marketplace] 客户立即订购的商品。 此 [!DNL Amazon Sales Channel] 扩展提供了一组用于查看Amazon列表的选项卡。 根据问题或所需数据，您应查看 [!DNL Amazon Seller Central] 说明这些列表的特定详细信息。

- [活动](./active-listings.md)：列出通过市场可用的已批准产品列表。

- [准备列出](./ready-to-list.md)：列出符合列表规则要求并准备好发布到Amazon的产品。

- [不活动](./inactive-listings.md)：列出由于特定原因（例如品牌策略问题）被阻止、已关闭并需要重新粘贴等原因而在市场中不可用的产品。

- [不合格](./ineligible-listings.md)：根据上市规则，列出无法在商城中积极上市的产品(例如 `0` 数量或销售日期)。

- [未完成](./incomplete-listings.md)：列出缺少必需信息的产品。 更新产品数据以供另一审阅。

- [已结束](./ended-listings.md)：列出符合列出条件但手动从Amazon中移除的产品清单。 您可以重新列出这些产品。

## 正在同步数据

Adobe Commerce和Magento Open Source在您的 [!DNL Amazon Seller Central] 帐户和 [!DNL Commerce] 后端。 持续更新通过以下方式提供单个源 [!DNL Commerce] 管理和维护库存、完成订单、跟踪销售以及减少制造费用和重复工作。 报告会捕获最新数据，以便跟踪趋势并解决在两个系统之间捕获的通信问题。

所有同步操作都由管理 [cron作业](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}，设置为每5分钟更新一次 [预设置任务](./amazon-pre-setup-tasks.md).
