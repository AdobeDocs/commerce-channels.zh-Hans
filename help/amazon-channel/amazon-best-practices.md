---
title: 的最佳实践和限制 [!DNL Amazon sales channel]
description: 在使用适用于Adobe Commerce和Magento Open Source的Amazon销售渠道时，请查看最佳实践和限制。
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# 的最佳实践和限制 [!DNL Amazon sales channel]

最佳实践包括：

- Amazon sales channel可以通过提高或降低价格、同步产品信息（包括可用库存）以及添加、更新和结束（删除）列表来影响您的Amazon列表。 在设置过程中按状态查看您的列表并调整设置([列表设置](./listing-settings.md)， [上市规则](./listing-rules.md)， [定价规则](./pricing-products.md)， [覆盖](./overrides.md)、等等)之前完成商店设置。 这些设置也可以在设置后根据需要进行修改。

- Amazon sales channel可以设置您的定价规则，以自动调整您的挂牌价格。 自动化定价保护包括 [底价](./floor-price.md) 和 [可选最高价](./optional-ceiling-price.md) 的功能 [智能重新定价规则](./intelligent-repricing-rules.md). 使用这些保护措施有助于确保您的上市价格不会低于成本或高于规定价格。

- Amazon Sales Channel与Amazon之间的数据同步受您的控制。 [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 设置。 在此之间内置调节 [!DNL Commerce] Amazon有助于确保流畅高效的数据传输，但在电子商务流量高峰期（如黑色星期五），Amazon的系统更新时间可能会比平时更长。 设置您的 [!DNL Commerce] 每五分钟就跑一次。

- Amazon sales channel可导入您的Amazon订单信息。 要在Amazon sales channel中管理Amazon订单，您必须确保 [订单设置](./order-settings.md) 定义来导入和创建相应的 [!DNL Commerce] 每个Amazon订单对应的订单。 如果未定义，则只能查看Amazon订单信息。 通过Amazon缴纳的所有销售税仍通过贵机构的 [!DNL Amazon Seller Central] 帐户。 在某些州，Amazon需要自动征收和汇出税款。 对于其他州，销售者可以选择手动或自动计算税款。 请参阅 [Amazon：税收政策](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. 您可能需要登录 [!DNL Amazon Seller Central] 用于查看Amazon税务政策文档的帐户。

- 对于英国地区，最佳做法是注册 [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} 载入Amazon sales channel之前。

  >[!NOTE]
  >
  >Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

限制包括：

- 捆绑包、礼品卡和属于您的组合产品类型 [!DNL Commerce] Amazon sales channel不支持将目录列为Amazon。

- Amazon sales channel无法为没有现有或以前的Amazon列表的产品创建列表。 如果中不存在产品 [!DNL Amazon Seller Central] 对于ASIN，必须将它添加到 [!DNL Amazon Seller Central] 以便Amazon可以为产品分配ASIN。 在Amazon中添加产品并创建列表后，该列表便可与Amazon Sales Channel中的目录匹配并同步。
