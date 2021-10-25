---
title: Amazon销售渠道的最佳实践和限制
description: 查看使用AmazonAdobe Commerce和Magento Open Source销售渠道时的最佳实践和限制。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Amazon销售渠道的最佳实践和限制

最佳实践包括：

- Amazon销售渠道可通过提高或降低价格、同步产品信息（包括可用库存）以及添加、更新和结束（删除）列表来影响您的Amazon列表。 在设置过程中按状态查看列表并调整设置([列表设置](./listing-settings.md), [列表规则](./listing-rules.md), [定价规则](./pricing-products.md), [覆盖](./overrides.md)等)。 还可以根据需要在设置后修改这些设置。

- Amazon销售渠道可设置您的定价规则以自动调整您的上市价格。 自动定价保障包括 [底价](./floor-price.md) 和 [可选上限价格](./optional-ceiling-price.md) 功能 [智能重定价规则](./intelligent-repricing-rules.md). 使用这些保障措施有助于确保贵机构的上市价格不会低于或高于既定价格。

- Amazon销售渠道与Amazon之间的数据同步由您的 [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}设置。 在 [!DNL Commerce] 而Amazon有助于确保数据传输的顺畅和高效，但在高电子商务流量（如“黑色星期五”）期间，Amazon的系统更新可能比往常花费的时间长。 设置 [!DNL Commerce] 克隆每五分钟运行一次。

- Amazon销售渠道导入您的Amazon订单信息。 要在Amazon销售渠道中管理Amazon订单，您必须确保 [订购设置](./order-settings.md) 定义为导入并创建相应的 [!DNL Commerce] 订购每份Amazon订单。 如果未定义，则您只能查看Amazon订单信息。 通过Amazon销售的所有税仍通过 [!DNL Amazon Seller Central] 帐户。 在有些州，Amazon必须自动征收和缴税。 对于其他州，卖方可以选择手动或自动计算税。 请参阅 [Amazon:税收政策](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}。 您可能需要登录 [!DNL Amazon Seller Central] 帐户以查看Amazon税务政策文档。

- 对于英国地区，最好注册 [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;}，然后再载入Amazon销售渠道。


   >[!NOTE]
   >
   >Amazon可能需要10-14天才能验证和激活您的增值税计算服务帐户。

限制包括：

- 捆绑、礼品卡和分组的产品类型(属于您的 [!DNL Commerce] Amazon销售渠道不支持将目录列入Amazon。

- Amazon销售渠道无法为没有现有或以前Amazon列表的产品创建列表。 如果中不存在产品 [!DNL Amazon Seller Central] 使用ASIN时，必须将其添加到 [!DNL Amazon Seller Central] 以便Amazon可以将产品分配为ASIN。 在Amazon中添加产品并创建列表后，该列表可以与Amazon销售渠道中的目录匹配并同步。
