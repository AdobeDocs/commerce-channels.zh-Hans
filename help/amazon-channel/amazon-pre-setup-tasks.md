---
title: ' [!DNL Amazon sales channel]的预设置任务'
description: 查看在AmazonSales Channel中集成Adobe Commerce或Magento Open Source存储区之前需要完成的任务。
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# [!DNL Amazon sales channel]的预设置任务

在[存储集成](./store-integration.md)之前，必须确保您的[!DNL Amazon Seller Central]帐户和[!DNL Commerce]帐户已准备好进行集成。 要成功集成，有一些必需的预设置任务。

在Amazon Sales Channel中设置您的第一个Amazon商店时，会显示一个设置任务列表。 建议在[添加Amazon应用商店](./store-integration.md)之前查看这些任务。 添加第一个商店后，您可以在Amazon销售渠道[主页](./amazon-sales-channel-home.md)的“学习和准备”视图中查看这些任务。

## 1.在[!DNL Commerce]中启用后台任务

所有在[!DNL Commerce]和Amazon之间同步的产品和数据都由[cron作业](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)管理。 当您完成添加或更新列表和接收订单等任务时，cron作业会在[!DNL Commerce]后端和[!DNL Amazon Seller Central]帐户之间发送和接收数据。

- [启用 [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)。

- 为获得最佳性能，[设置 [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html)每五分钟运行一次。

## 2.创建您的[!DNL Amazon Seller Central]帐户

在开始设置Amazon销售渠道之前，您必须拥有有效的[!DNL Amazon Seller Central]帐户。 如果您在[北美（美国、CA、MX）](https://sell.amazon.com/){target="_blank"}或[欧洲（英国）](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"}区域中没有现有的Amazon卖方帐户，则可以完成Amazon的卖方帐户设置过程。

Amazon sales channel需要[!DNL Amazon Seller Central]上的[!DNL Professional Seller]帐户。 Amazon按月收取订购费和销售费。 查看[Amazon：选择您的销售计划](https://sell.amazon.com/pricing.html){target="_blank"}。

## 3.确保您是获得批准的Amazon销售商

要集成，您必须拥有已批准的[!DNL Amazon Seller Central]帐户。 您的帐户对产品或类别不得有任何限制。 某些产品和类别在创建列表之前需要审批。 查看Amazon的类别和产品批准策略，确保您的产品获得批准。 请参阅[Amazon：需要批准的类别和产品](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （需要卖方中心登录）。

此外，确保已在[!DNL Amazon Seller Central]帐户中配置以下内容也很重要：

- 确保您的退货政策与Amazon退货政策相同或更好。 请参阅[Amazon：退货政策](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}。

- 确保已配置您的税务设置。 请参阅[Amazon：税务政策](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"}（需要以卖方中心身份登录）。

- 确保正确配置配送方式。 要设置向客户提供[!DNL Commerce]的配送方式以履行Amazon订单，请在[!DNL Amazon Seller Central]帐户中更新[Amazon：配送设置](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"}。

## 4.确保为您的商店配置增值税

（主要由英国销售商使用。） Amazon建议注册[Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}。 如果选择其他方法，则由您负责符合VAT标准。

>[!NOTE]
>
>Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

## 5.增加自动目录匹配数

在新用户引导期间，Amazon Sales Channel使用产品属性将您现有的Amazon列表（如果适用）与[!DNL Commerce]目录中的现有产品相匹配。 新用户引导后，这些产品属性用于将您的[!DNL Commerce]目录项目发布到Amazon列表，并在[!DNL Commerce]和Amazon之间同步您的产品数据。

若要让[!DNL Commerce]个产品的最大数量自动与Amazon列表匹配，您应该为[!DNL Commerce]目录创建一组产品属性。 在设置Amazon销售渠道商店之前，您应该添加[!DNL Commerce]产品属性以匹配这些Amazon属性，例如：ASIN、EAN、ISBN、UPC或GCID。 请参阅[在 [!DNL Commerce]](./ob-creating-magento-attributes.md)中创建产品属性。

## 6.配置货币和兑换（根据需要）

如果您的Amazon商店使用的货币与为您的[!DNL Commerce]商店配置的货币不同，请[启用该货币](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html)并设置[货币兑换率](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html)。

## 7.创建产品条件属性（根据需要）

如果您的Amazon清单包含多个产品条件（如&#x200B;_new_、_used_&#x200B;或&#x200B;_like new_），请创建[!DNL Commerce]属性并分配条件值。 您必须在载入期间将此属性映射到Amazon条件产品属性。 请参阅[创建Amazon的属性](./ob-creating-magento-attributes.md)。

## 8.配置您的[!DNL Amazon Seller Central]配送方式

要设置要提供的配送方式以满足Amazon订单，请参阅[!DNL Amazon Seller Central]帐户中的&#x200B;_设置和配送设置_。

## 其他配置

当您的Amazon帐户设置并处于活动状态时，有几个[!DNL Commerce]建议可帮助简化Amazon销售渠道新用户引导流程。

### 查看并记下要排除的任何产品

您可能不希望某些产品在Amazon中列出。 Amazon sales channel有一个列表规则引擎，用于确定哪些产品有资格发布到Amazon。 [列表规则](./listing-rules.md)允许您选择要发布（或未发布）到[!DNL Amazon Seller Central]帐户的产品子集，例如通过类别选择或通过定义一个或多个产品属性。 与[!DNL Commerce] [目录](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)或[购物车](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html)价格规则一样，用于Amazon列表资格的产品属性必须将&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;设置为`Yes`。 查看[产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)中的&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**。

### 将您的[!DNL Amazon Seller Central]区域设置为非活动状态

为了帮助在集成期间实现无错误数据转换，建议您在设置>帐户信息>假期设置中将您的Amazon区域设置为`Inactive`状态。 完成设置后，在Amazon中将状态更改为`Active`。

![下一个图标](assets/btn-next.png) [**继续创建[!DNL Commerce]属性**](./ob-creating-magento-attributes.md)
