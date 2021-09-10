---
title: 板载AmazonSales Channel
description: 了解预设置任务、入门步骤，以及Amazon如何在Adobe商务和Magento Open Source中与AmazonSales Channel配合使用。
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html: 
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# 载入Amazon销售渠道

本节介绍预设置任务、入门步骤，以及有关Amazon如何在Adobe商务和Magento Open Source中与Amazon销售渠道配合使用的一些关键概念。

[!DNL Amazon Sales Channel]扩展支持多个Amazon存储。 对于在Amazon美国/加拿大/墨西哥地区运营的单个[!DNL Amazon Seller Central]帐户，请创建三家Amazon商店（分别为美国销售、墨西哥销售和加拿大销售）。 这三家商店中的每一家在其创建期间定义市场所在的国家/地区。 如果您有多个[!DNL Amazon Seller Central]帐户，则每个[!DNL Amazon Seller Central]帐户可能最多拥有三个Amazon存储区。 如果你在英国也卖，你会有第四家Amazon店。

>[!TIP]
>
>北美或欧洲(UK)地区的[!DNL Amazon Seller Central][专业卖家帐户](https://sell.amazon.com/){target=&quot;_blank&quot;}是必需的。 Amazon每月收取订购费和销售费。 请参阅[Amazon:选择您的销售计划](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}。<br><br>
>入门过程很简单 — 创建您的商店，然后将其连接到您的[!DNL Amazon Seller Central]帐户。
>连接您的商店后，Amazon渠道会尝试导入您的Amazon列表，并根据您的[属性映射](./attributes-view.md).<br><br>将它们与目录匹配
>您的Amazon销售渠道设置会影响您的Amazon列表。 您的初始列表、定价和产品设置均默认为您。 在您的商店连接到[!DNL Amazon Seller Central]帐户后，您可以修改[商店设置](./ob-store-review.md)（列表、定价、订单和报告）。

| 步骤 | 发生的情况 |
|--- |--- |
| [预设置任务](./amazon-pre-setup-tasks.md) | 在载入之前，必须确保您拥有一个已批准的活动[!DNL Amazon Seller Central]帐户。 此外，还有一些[!DNL Commerce]要求和建议，需在入门前完成。 |
| [验证Amazon API密钥](./amazon-verify-api-key.md) | 访问Amazon销售渠道时，[!DNL Commerce]会自动检查并验证您在存储配置中添加的Amazon API密钥。 如果您的API密钥尚未添加或无效，系统会提示您[添加或更新Amazon API密钥](./amazon-verify-api-key.md)。 |
| [存储集成](./store-integration.md) | 此步骤包括创建Amazon销售渠道商店，然后将其连接到您的[!DNL Amazon Seller Central]帐户。 您需要[!DNL Amazon Seller Central]帐户（用于创建卖家帐户的电子邮件或电话）的主登录凭据才能完成此步骤。 |
| [创建列表规则](./ob-create-listing-rule.md) | 连接Amazon销售渠道商店后，系统会提示您创建列表规则。 我们鼓励执行此步骤，但您也可以跳过此步骤以开始列表导入过程。 您还可以访问[存储并列出存储[功能板](./amazon-store-dashboard.md)上的设置](./ob-store-review.md)。 |
