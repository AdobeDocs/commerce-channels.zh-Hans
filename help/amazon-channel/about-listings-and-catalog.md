---
title: 关于Amazon和商务目录
description: Amazon销售渠道会将您的Amazon列表导入Commerce后端，并会持续与产品和销售同步。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# 关于Amazon和[!DNL Commerce]目录

您的Adobe商务或Magento Open Source后端包含一个目录，其中包含所有产品以及关联的设置和信息（图像、选项、价格等）以及订购和发运配置。 您的[!DNL Amazon Seller Central]帐户还具有目录和订单配置，可通过[!DNL Amazon Marketplace]严格跟踪您的销售情况。

为了通过一个位置更好地管理和查看您的产品目录和销售，Amazon销售渠道会将您的Amazon列表导入[!DNL Commerce]后端，并持续与产品和销售同步，并报告问题和趋势。 它支持与多个[!DNL Amazon Seller Central]帐户的集成，通过单个界面跟踪多个店面的所有数据。

## 产品属性

Adobe商务和Magento Open Source管理目录同步时，使用产品[attributes](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}定义产品设置和数据。 Amazon还使用属性，以通过载入进行映射。 在为Amazon销售渠道执行[预设设置任务](./amazon-pre-setup-tasks.md)期间，您可以定义其他Amazon属性（如果需要），以确保在将Amazon列表导入[!DNL Commerce]目录时正确映射产品。 这些属性包括UPC、EAN、ISBN和ASIN([!DNL Amazon Standard Identification Number])。 通过载入，产品可使用您的属性在Amazon和[!DNL Commerce]目录之间同步。 正确映射[!DNL Commerce]和Amazon产品可确保产品信息、订单和库存的持续同步。

如果您尚未为目录创建或配置这些属性，则应在载入之前向产品添加[!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}和值。 导入Amazon属性后，该属性可用于搜索、导航、价格规则等。 有关这些属性的更多信息，请参阅[Amazon:什么是UPC、EAN、ISBN和ASIN?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

入门后，您可以随时管理和更新产品属性和Amazon映射。

## 产品列表

Amazon列表是您通过[!DNL Amazon Marketplace]销售的每个产品的产品页面，显示产品描述、价格、图像等通过属性映射的信息。 在入门过程中，您可以配置[!DNL Commerce]产品，以将其自动发布到Amazon列表。 您还可以通过将现有Amazon列表映射到[!DNL Commerce]产品来导入这些列表。

创建[!DNL Commerce]产品列表后，这些产品将提交Amazon以供审批。 大多数成功的列表会在几小时内获得批准。 如果您的列表获得批准，它将显示在[!DNL Amazon Marketplace]中，以供客户立即订购。 [!DNL Amazon Sales Channel]扩展提供了一组用于查看Amazon列表的选项卡。 根据问题或所需数据，您应查看[!DNL Amazon Seller Central]帐户，以了解这些列表的具体详细信息。

- [活动](./active-listings.md):列出通过市场提供的已批准产品清单。

- [准备列表](./ready-to-list.md):列出符合列表规则要求并可发布到Amazon的产品。

- [不活动](./inactive-listings.md):列出因特定原因（如品牌问题）、关闭和需要重新展示等而被阻止而无法在市场上提供的产品。

- [不合格](./ineligible-listings.md):根据上市规则，列出无法在市场上主动列出的产品(如数量 `0` 或销售日期)。

- [不完整](./incomplete-listings.md):列出缺少必需信息的产品。更新产品数据以供其他审阅。

- [已结束](./ended-listings.md):列出符合列表条件但手动从Amazon中删除的产品清单。您可以重新列出这些产品。

## 正在同步数据

Adobe商务和Magento Open Source在[!DNL Amazon Seller Central]帐户和[!DNL Commerce]后端之间传递产品和订单数据。 持续更新通过[!DNL Commerce]提供单一来源来管理和维护您的库存，执行订单，跟踪销售，并减少开销和工作重复。 报表可捕获用于跟踪趋势和解决两个系统之间存在的通信问题的最新数据。

所有同步都由[cron作业](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}管理，在[预设设置任务](./amazon-pre-setup-tasks.md)中设置为每五分钟更新一次。
