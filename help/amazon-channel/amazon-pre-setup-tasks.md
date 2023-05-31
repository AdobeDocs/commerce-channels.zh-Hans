---
title: 的预设置任务 [!DNL Amazon sales channel]
description: 查看在AmazonSales Channel中集成Adobe Commerce或Magento Open Source存储区之前需要完成的任务。
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# 的预设置任务 [!DNL Amazon sales channel]

早于 [存储集成](./store-integration.md)，您必须确保 [!DNL Amazon Seller Central] 帐户和您的 [!DNL Commerce] 帐户已准备好进行集成。 要成功集成，有一些必需的预设置任务。

当您在Amazon sales channel中设置第一个Amazon商店时，会显示一个设置任务列表。 建议您先查看这些任务，然后再查看 [添加Amazon商店](./store-integration.md). 添加您的第一个商店后，您可以在Amazon销售渠道的“学习和准备”视图中查看这些任务 [主页](./amazon-sales-channel-home.md).

## 1.在中启用后台任务 [!DNL Commerce]

所有产品和数据都在以下日期之间同步： [!DNL Commerce] 并且Amazon由 [cron作业](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). 当您完成添加或更新列表和接收订单等任务时，cron任务会在您与客户之间 [!DNL Commerce] 后端和您的 [!DNL Amazon Seller Central] 帐户。

- [启用 [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- 为获得最佳性能， [设置 [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) 每五分钟运行一次。

## 2.创建您的 [!DNL Amazon Seller Central] 帐户

在开始设置Amazon销售渠道之前，您必须拥有有效的 [!DNL Amazon Seller Central] 帐户。 如果您在中没有现有的Amazon卖方帐户 [北美（美国、CA、MX）](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} ，即可完成Amazon卖方账户设置流程。

Amazon销售渠道需要 [!DNL Professional Seller] 帐户于 [!DNL Amazon Seller Central]. Amazon按月收取订购费和销售费。 参见 [Amazon：选择您的销售计划](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3.确保您是经认可的Amazon销售商

要集成，您必须拥有一个 [!DNL Amazon Seller Central] 帐户。 您的帐户对产品或类别不得有任何限制。 某些产品和类别在创建列表之前需要审批。 查看Amazon的类别和产品批准策略，确保您的产品获得批准。 参见 [Amazon：需要批准的类别和产品](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （需要以Seller Central登录）。

此外，确保已在以下位置配置以下也很重要： [!DNL Amazon Seller Central] 帐户：

- 确保您的退货政策与Amazon退货政策相同或更好。 参见 [Amazon：退货政策](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- 确保已配置税务设置。 参见 [Amazon：税收政策](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} （需要以Seller Central登录）。

- 确保正确配置配送方式。 要设置符合以下条件的配送方式： [!DNL Commerce] 提供给客户以完成Amazon订单，更新 [Amazon：配送设置](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} 在您的 [!DNL Amazon Seller Central] 帐户。

## 4.确保为商店配置增值税

（主要由英国卖家使用。） Amazon建议注册 [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. 如果选择其他方法，则由您负责符合VAT规定。

>[!NOTE]
>
>Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

## 5.增加自动目录匹配的数量

在新用户引导期间，Amazon销售渠道使用产品属性将您现有的Amazon列表（如果适用）与您现有的产品进行匹配 [!DNL Commerce] 目录。 新用户引导后，这些产品属性将用于发布您的 [!DNL Commerce] 将项目编录到Amazon列表，并在其中同步产品数据 [!DNL Commerce] 和Amazon。

拥有数量最多的 [!DNL Commerce] 产品会自动与Amazon列表匹配，您应该为创建一组产品属性， [!DNL Commerce] 目录。 在设置Amazon sales channel store之前，您应该添加 [!DNL Commerce] 产品属性以匹配这些Amazon属性，例如：ASIN、EAN、ISBN、UPC或GCID。 参见 [在中创建产品属性 [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6.配置货币和兑换（根据需要）

如果您的Amazon商店使用的货币与为配置的货币不同 [!DNL Commerce] 商店， [启用货币](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) 并设置 [货币兑换率](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7.创建产品条件属性（根据需要）

如果您的Amazon清单包含多个产品条件(例如 _新_， _已使用_，或 _喜欢新内容_)，创建 [!DNL Commerce] 属性和分配条件值。 在新用户引导期间，您必须将此属性映射到Amazon Condition产品属性。 参见 [为Amazon创建属性](./ob-creating-magento-attributes.md).

## 8.配置您的 [!DNL Amazon Seller Central] 配送方式

要设置要提供的发运方法以满足Amazon订单，请参阅 _设置和送货设置_ 在您的 [!DNL Amazon Seller Central] 帐户。

## 其他配置

设置并激活您的Amazon帐户后，会执行以下多项操作 [!DNL Commerce] 有助于简化Amazon销售渠道入门流程的建议。

### 查看并记下要排除的任何产品

您可能不希望某些产品在Amazon中列出。 Amazon sales channel有一个列表规则引擎，用于确定哪些产品有资格发布到Amazon。 [上市规则](./listing-rules.md) 允许您选择要发布（或未发布）到您的产品的子集 [!DNL Amazon Seller Central] 帐户，例如通过类别选择或通过定义一个或多个产品属性来实现。 点赞 [!DNL Commerce] [目录](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) 或 [购物车](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) 价格规则，用于Amazon列表资格的产品属性必须具有 **[!UICONTROL Use for Promo Rule Conditions]** 设置为 `Yes`. 请参阅 **[!UICONTROL Use for Promo Rule Conditions]** 在 [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### 设置您的 [!DNL Amazon Seller Central] 区域到非活动

为了帮助在集成期间实现无错误数据转换，建议将Amazon区域设置为 `Inactive` “设置”>“帐户信息”>“假期设置”中的状态。 设置完成后，将状态更改为 `Active` 在Amazon中。

![“下一步”图标](assets/btn-next.png) [**继续创建 [!DNL Commerce] 属性**](./ob-creating-magento-attributes.md)
