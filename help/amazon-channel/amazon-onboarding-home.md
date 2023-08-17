---
title: 板载 [!DNL Amazon Sales Channel]"
description: 了解预设置任务、载入步骤以及Amazon如何在Adobe Commerce和Magento Open Source中与AmazonSales Channel配合使用。
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 载入 [!DNL Amazon Sales Channel]

本节介绍Amazon如何在Adobe Commerce和Magento Open Source中与Amazon销售渠道配合使用的预设置任务、入门步骤以及一些关键概念。

此 [!DNL Amazon Sales Channel] 扩展支持多个Amazon存储。 对于单个 [!DNL Amazon Seller Central] 在Amazon美国/加拿大/墨西哥地区运营的帐户创建了三家Amazon商店（分别为美国销售、墨西哥销售和加拿大销售创建一家）。 这三家商店中的每一家都在创建期间定义了市场国家/地区。 如果您有多个 [!DNL Amazon Seller Central] 帐户，则可能每个最多可以拥有三个Amazon商店 [!DNL Amazon Seller Central] 帐户。 如果您还在英国销售，您将拥有第四家Amazon商店。

>[!TIP]
>
>A [专业卖方帐户](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>载入非常简单 — 创建您的商店，然后将其连接到您的 [!DNL Amazon Seller Central] 帐户。
>连接商店后，Amazon渠道会尝试导入您的Amazon列表，并根据您的网站上的 [属性映射](./attributes-view.md).<br><br>
>您的Amazon销售渠道设置会影响您的Amazon列表。 您的初始列表、定价和产品设置均默认为您设置。 您可以修改您的 [商店设置](./ob-store-review.md) （列表、定价、订购和报告） [!DNL Amazon Seller Central] 帐户。

| 步骤 | 发生什么情况 |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [预设置任务](./amazon-pre-setup-tasks.md) | 在加入之前，您必须确保已激活并批准 [!DNL Amazon Seller Central] 帐户。 还有一些 [!DNL Commerce] 载入前完成的要求和建议。 |
| [验证Amazon API密钥](./amazon-verify-api-key.md) | 访问Amazon销售渠道时， [!DNL Commerce] 自动检查并验证您在商店配置中添加的Amazon API密钥。 如果您的API密钥尚未添加或无效，系统会提示您输入 [添加或更新您的Amazon API密钥](./amazon-verify-api-key.md). |
| [存储集成](./store-integration.md) | 此步骤包括创建一个Amazon sales channel商店，然后将其连接到您的 [!DNL Amazon Seller Central] 帐户。 您需要的主要登录凭据用于 [!DNL Amazon Seller Central] 此步骤的帐户（用于创建卖方帐户的电子邮件或电话）。 |
| [创建列表规则](./ob-create-listing-rule.md) | 连接Amazon sales channel store后，系统会提示您创建列表规则。 我们鼓励执行此步骤，但您也可以跳过此步骤以开始列表导入流程。 您还可以访问 [存储和列表设置](./ob-store-review.md) 在商店中 [仪表板](./amazon-store-dashboard.md). |
