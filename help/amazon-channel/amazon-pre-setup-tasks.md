---
title: 预设置任务
description: 在AmazonSales Channel中集成Adobe商务或Magento Open Source商店之前，请查看要完成的所需任务。
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# 预设置任务

在[存储集成](./store-integration.md)之前，您必须确保[!DNL Amazon Seller Central]帐户和[!DNL Commerce]帐户已准备好进行集成。 要成功集成，需要执行一些预设设置任务。

在Amazon销售渠道中设置第一家Amazon商店时，会显示设置任务列表。 建议您在[添加Amazon商店](./store-integration.md)之前查看这些任务。 添加第一家商店后，您可以在Amazon销售渠道[主页](./amazon-sales-channel-home.md)的“学习和准备”视图中查看这些任务。

## 1.在[!DNL Commerce]中启用后台任务

在[!DNL Commerce]和Amazon之间同步的所有产品和数据都由[cron作业](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}管理。 完成添加或更新列表以及接收订单等任务后，cron作业会在您的[!DNL Commerce]后端和[!DNL Amazon Seller Central]帐户之间发送和接收数据。

- [ [!DNL Commerce] Enablecron](https://docs.magento.com/user-guide/system/cron.html) {target=&quot;_blank&quot;}。

- 为获得最佳性能，[将 [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;}设置为每五分钟运行一次。

## 2.创建[!DNL Amazon Seller Central]帐户

在开始设置Amazon销售渠道之前，您必须拥有有效的[!DNL Amazon Seller Central]帐户。 如果您在[北美（美国、加利福尼亚、MX）](https://sell.amazon.com/){target=&quot;_blank&quot;}或[欧洲（英国）](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;}区域没有现有的Amazon卖家帐户，则可以完成Amazon卖家帐户设置过程。

Amazon销售渠道要求[!DNL Amazon Seller Central]上的[!DNL Professional Seller]帐户。 Amazon每月收取订购费和销售费。 请参阅[Amazon:选择您的销售计划](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}。

## 3.确保您是已批准的Amazon卖家

要集成，您必须拥有已批准的[!DNL Amazon Seller Central]帐户。 您的帐户不得对产品或类别有任何限制。 某些产品和类别在创建列表之前需要获得批准。 查看Amazon的类别和产品批准政策，以确保产品已获得批准。 请参阅[Amazon:需要批准的类别和产品](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;}（需要卖家中心登录）。

此外，还务必确保您已在[!DNL Amazon Seller Central]帐户中配置了以下内容：

- 确保您的回访政策与Amazon回访政策一样好或更好。 请参阅[Amazon:返回策略](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}。

- 确保已配置您的税设置。 请参阅[Amazon:税收策略](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;}（需要卖方中央登录）。

- 确保正确配置您的装运方法。 要设置向客户提供[!DNL Commerce]以履行Amazon订单的发运方法，请更新[Amazon:在您的[!DNL Amazon Seller Central]帐户中发送设置](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;}。

## 4.确保为您的商店配置了增值税

（主要由英国卖家使用。） Amazon建议注册[Amazon VAT计算服务](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}。 如果您选择其他方法，则需负责增值税合规性。

>[!NOTE]
>
>Amazon可能需要10-14天才能验证和激活您的增值税计算服务帐户。

## 5.增加自动目录匹配数

在入门过程中，Amazon销售渠道会使用产品属性将您现有的Amazon列表（如果适用）与[!DNL Commerce]目录中的现有产品进行匹配。 入门后，这些产品属性将用于将您的[!DNL Commerce]目录项发布到Amazon列表，并在[!DNL Commerce]和Amazon之间同步产品数据。

要使最大数量的[!DNL Commerce]产品自动与Amazon列表匹配，您应为[!DNL Commerce]目录创建一组产品属性。 在设置Amazon销售渠道商店之前，您应添加[!DNL Commerce]产品属性以匹配以下Amazon属性，例如：ASIN、EAN、ISBN、UPC或GCID。 请参阅[在 [!DNL Commerce]](./ob-creating-magento-attributes.md)中创建产品属性。

## 6.配置货币和兑换（根据需要）

如果Amazon存储使用的货币与为[!DNL Commerce]存储配置的货币不同，请[启用货币](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}并设置[货币兑换率](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}。

## 7.创建“产品条件”属性（根据需要）

如果您的Amazon列表包含多个产品条件（如&#x200B;_new_、_used_&#x200B;或&#x200B;_like new_），请创建[!DNL Commerce]属性并分配条件值。 在入门期间，您必须将此属性映射到Amazon Condition产品属性。 请参阅[为Amazon创建属性](./ob-creating-magento-attributes.md)。

## 8.配置[!DNL Amazon Seller Central]发运方法

要设置要用于执行Amazon订单的发运方法，请参阅[!DNL Amazon Seller Central]帐户中的[设置和发运设置][10]。

## 其他配置

设置并激活您的Amazon帐户后，有几个[!DNL Commerce]建议可帮助简化Amazon销售渠道载入流程。

### 查看并记下要排除的任何产品

您可能不希望某些产品在Amazon上列出。 Amazon销售渠道具有一个列表规则引擎，用于确定哪些产品有资格发布到Amazon。 [列表](./listing-rules.md) 规则允许您选择要发布（或未发布）到您帐户的产品子集， [!DNL Amazon Seller Central] 例如按类别选择或通过定义一个或多个产品属性。与[!DNL Commerce] [catalog](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}或[购物车](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}价格规则类似，用于Amazon列表资格的产品属性必须将&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;设置为`Yes`。 请参阅[产品属性](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}中的&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**。

### 将[!DNL Amazon Seller Central]区域设置为不活动

为帮助在集成过程中实现无错误的数据过渡，建议在设置>帐户信息>休假设置中将Amazon区域设置为`Inactive`状态。 请参阅[Amazon:列出假期的状态][11]。 设置完成后，在Amazon中将状态更改回`Active`。

![下一](assets/btn-next.png) [**个图标继续创建属 [!DNL Commerce] 性**](./ob-creating-magento-attributes.md)
