---
title: ' [!DNL Amazon sales channel]的最佳实践和限制'
description: 在使用适用于Adobe Commerce和Magento Open Source的Amazon销售渠道时，请查看最佳实践和限制。
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# [!DNL Amazon sales channel]的最佳实践和限制

最佳实践包括：

- Amazon sales channel可以通过提高或降低价格、同步产品信息（包括可用库存）以及添加、更新和结束（删除）列表来影响您的Amazon列表。 在设置过程中按状态查看您的列表并调整设置（[列表设置](./listing-settings.md)、[列表规则](./listing-rules.md)、[定价规则](./pricing-products.md)、[覆盖](./overrides.md)等），然后再完成商店设置。 这些设置也可以在设置后根据需要进行修改。

- Amazon sales channel可以设置您的定价规则，以自动调整您的挂牌价格。 自动定价保护包括[智能重新定价规则](./intelligent-repricing-rules.md)的[最低价格](./floor-price.md)和[可选最高价格](./optional-ceiling-price.md)功能。 使用这些保护措施有助于确保您的上市价格不会低于成本或高于规定价格。

- Amazon sales channel与Amazon之间的数据同步由您的[[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)设置控制。 [!DNL Commerce]和Amazon之间的内置节流功能有助于确保流畅而高效的数据传输，但在电子商务流量高峰期（如“黑色星期五”），Amazon的系统可能需要比平常更长的时间才能更新。 将您的[!DNL Commerce] cron设置为每5分钟运行一次。

- Amazon sales channel可导入您的Amazon订单信息。 要在Amazon Sales Channel中管理Amazon订单，您必须确保已定义您的[订单设置](./order-settings.md)以导入并为每个Amazon订单创建相应的[!DNL Commerce]订单。 如果未定义，则只能查看Amazon订单信息。 通过Amazon缴纳的所有销售税仍通过您的[!DNL Amazon Seller Central]帐户进行管理和汇出。 在某些州，Amazon需要自动征收和汇出税款。 对于其他州，销售者可以选择手动或自动计算税款。 请参阅[Amazon：税务政策](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}。 您可能需要登录您的[!DNL Amazon Seller Central]帐户才能查看Amazon税务政策文档。

- 对于英国地区，最佳实践是在登录Amazon销售渠道之前注册[Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"}。

  >[!NOTE]
  >
  >Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

限制包括：

- Amazon Sales Channel不支持将捆绑包、礼品卡和分组产品类型列为Amazon的目录，因为这些产品类型是您的[!DNL Commerce]目录的一部分。

- Amazon sales channel无法为没有现有或以前的Amazon列表的产品创建列表。 如果[!DNL Amazon Seller Central]中不存在具有ASIN的产品，则必须在[!DNL Amazon Seller Central]中添加该产品，以便Amazon可以为产品分配ASIN。 在Amazon中添加产品并创建列表后，该列表便可与Amazon Sales Channel中的目录匹配并同步。
