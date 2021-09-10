---
title: Amazon销售渠道的最佳实践和限制
description: 查看使用Amazon销售渠道进行Adobe商务和Magento Open Source时的最佳实践和限制。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Amazon销售渠道的最佳实践和限制

最佳实践包括：

- Amazon销售渠道可通过提高或降低价格、同步产品信息（包括可用库存）以及添加、更新和结束（删除）列表来影响您的Amazon列表。 在完成存储设置之前，按设置期间的状态查看列表并调整设置（[列表设置](./listing-settings.md)、[列表规则](./listing-rules.md)、[定价规则](./pricing-products.md)、[覆盖](./overrides.md)等）。 还可以根据需要在设置后修改这些设置。

- Amazon销售渠道可设置您的定价规则以自动调整您的上市价格。 自动定价保障包括[智能重定价规则](./intelligent-repricing-rules.md)的[底价](./floor-price.md)和[可选最高价格](./optional-ceiling-price.md)功能。 使用这些保障措施有助于确保贵机构的上市价格不会低于或高于既定价格。

- Amazon销售渠道与Amazon之间的数据同步由您的[[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}设置控制。 [!DNL Commerce]和Amazon之间的内置限制有助于确保数据传输的顺畅和高效，但在高电子商务流量时间（如“黑色星期五”），Amazon系统可能需要比往常更长的更新时间。 将[!DNL Commerce] cron设置为每五分钟运行一次。

- Amazon销售渠道导入您的Amazon订单信息。 要在Amazon销售渠道中管理Amazon订单，必须确保将[订单设置](./order-settings.md)定义为导入并为每个Amazon订单创建相应的[!DNL Commerce]订单。 如果未定义，则您只能查看Amazon订单信息。 通过Amazon销售的所有税仍通过您的[!DNL Amazon Seller Central]帐户管理和汇付。 在有些州，Amazon必须自动征收和缴税。 对于其他州，卖方可以选择手动或自动计算税。 请参阅[Amazon:税策](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}。 您可能需要登录[!DNL Amazon Seller Central]帐户才能查看Amazon税收政策文档。

- 对于英国地区，最好在登记Amazon销售渠道之前，先注册[Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;}。


   >[!NOTE]
   >
   >Amazon可能需要10-14天才能验证和激活您的增值税计算服务帐户。

限制包括：

- Amazon销售渠道不支持将包、礼品卡和分组的产品类型列入[!DNL Commerce]目录，因此不支持将这些类型列入Amazon。

- Amazon销售渠道无法为没有现有或以前Amazon列表的产品创建列表。 如果某个产品在[!DNL Amazon Seller Central]中不存在，且该产品不具有ASIN，则必须将其添加到[!DNL Amazon Seller Central]中，以便Amazon可以为该产品分配一个ASIN。 在Amazon中添加产品并创建列表后，该列表可以与Amazon销售渠道中的目录匹配并同步。
