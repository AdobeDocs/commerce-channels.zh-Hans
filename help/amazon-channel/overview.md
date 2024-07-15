---
title: “ [!DNL Amazon Sales Channel]简介”
description: “[!DNL Amazon Sales Channel]使商家能够在 [!DNL Amazon Marketplace]中无缝销售产品。”
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel]简介

作为Adobe Commerce或Magento Open Source商家，您可以使用[!DNL Amazon Sales Channel]扩展将您的商店与世界上最大的全球Internet购物目的地集成。 此扩展通过将[!DNL Commerce]与您的[!DNL Amazon Seller Central]帐户连接并提供目录和订单数据的自动化和同步，从而支持Amazon销售。 完全管理所有Amazon列表，实施简单或智能的定价规则，并通过单个[!DNL Commerce]仪表板维护您的订单和库存。

在[上线](./amazon-onboarding-home.md)后，[!DNL Commerce]将成为一个“中央指挥中心”，用于管理和控制您的Amazon清单、订单和库存以及Amazon商店的定价。 [存储集成](./store-integration.md)将您的[!DNL Commerce]实例连接到Amazon，以便在两个平台之间同步数据。 Amazon sales channel使您能够：

- [板载](./amazon-onboarding-home.md)并将一个或多个[!DNL Amazon Seller Central]帐户与Adobe Commerce或Magento Open Source集成。

- 导入并同步您现有的Amazon列表，并与[!DNL Commerce]目录中的产品匹配，从而创建一个集中的产品目录。

- 为您的[!DNL Commerce]目录中的产品创建和管理Amazon列表。

- 在[!DNL Commerce]和Amazon中查看和完成（发运）订单，同步订单状态、付款和退款信息。

- 查看[竞争性价格](./competitive-price-analysis.md)、[列表更改](./listing-changes-log.md)和[通信问题](./communication-errors-log.md)的分析和错误日志。

访问您的Amazon商店，以便在Amazon销售渠道[主页](./amazon-sales-channel-home.md)上查看和管理所有这些功能、帐户信息、清单、订单等。

## 促销和定价

使用[!DNL Amazon Sales Channel]扩展，您可以：

- 将Amazon列表定价同步到[!DNL Commerce]目录价格（或替代价格属性）。

- 在您的Amazon列表中启用MSRP [删除线定价](./listing-price.md#configure-listing-price-settings)以提高客户价值主张。

- 在Amazon列表中启用并管理[最低广告价格(MAP)](./listing-price.md#configure-listing-price-settings)。

- 在您的Amazon定价中配置额外的[增值税](./listing-price.md#configure-listing-price-settings)。

- 在您的[库存/数量设置](./stock-quantity.md#configure-stock--quantity-settings)中为“可用数量”设置自定义值，以便与您的Amazon清单一起显示，从而增加购买者的紧迫性。

## 定价规则

使用[!DNL Amazon Sales Channel]扩展，您可以：

- 创建可栈叠、灵活且复杂的[定价规则](./pricing-products.md)来管理您的Amazon定价以用于日常销售或季节性促销。

- 创建[下限](./floor-price.md)和[上限](./optional-ceiling-price.md)价格以保护您的最低和最高价格。

- 创建和管理[智能重新定价规则](./intelligent-repricing-rules.md)，该规则可自动调整您的产品定价使其相对于其他Amazon竞争对手([最低竞争对手](./lowest-competitor-pricing.md)和[Buy Box](./buy-box-competitor-pricing.md)价格)。

## 目录信息源管理

使用[!DNL Amazon Sales Channel]扩展，您可以：

- 导入现有Amazon列表（产品），并与您的[!DNL Commerce]目录中的现有或创建产品匹配。

- 将您的[!DNL Commerce]产品Publish到Amazon以创建Amazon列表。

- 创建[覆盖](./creating-editing-overrides.md)以设置单个价格、处理时间、条件和卖方备注消息。

- 从Amazon列表导入和映射产品[属性](./attributes-view.md)以自动与[!DNL Commerce]目录中的产品匹配。

- 设置多个搜索参数以将Amazon列表与您的[!DNL Commerce]目录相匹配。

- 定义[列表规则](./listing-rules.md)以确定您的[!DNL Commerce]产品中哪些产品有资格在Amazon上列表。

- 为新的Amazon列表设置默认[处理时间](./product-listing-actions.md)。

- 基于[!DNL Commerce]属性匹配列表条件。

- 为每种条件类型添加卖方备注（可选）。

- 将Amazon列表导入您的[!DNL Commerce]目录时，实施数量阈值。

- 查看推荐的[列表改进](./listing-improvements.md)。

## 订单管理和客户服务

使用[!DNL Amazon Sales Channel]扩展，您可以：

- 在Amazon和[!DNL Commerce]中支持和处理订单。

- [将您的Amazon订单](./order-settings.md#configure-order-settings)导入[!DNL Commerce]或保留在Amazon中。

- 定义要与Amazon订单关联的[!DNL Commerce]网站商店，以便导入和管理订单。

- 根据您的[履行设置](./fulfilled-by.md)，查看、取消和发运[!DNL Commerce]和/或Amazon中的订单。

- 将您的Amazon订单状态映射到[!DNL Commerce]中的自定义状态（可选）。

- 查看和管理订单错误以解决问题并与客户建立联系。

- 将订单跟踪数据发送到您的[!DNL Amazon Seller Central]帐户。

- [取消订单](./cancel-unshipped-order.md)并选择原因响应。

- 查看Amazon订单的[最新订单](./amazon-store-dashboard.md)信息。

## 报表

使用[!DNL Amazon Sales Channel]扩展，您可以查看有关以下各项的报告信息：

- 按活动、非活动、符合条件和未完成状态列出的列表。

- 等待装运的订单。

- 最近的订单。

- Amazon [列表更改日志](./listing-changes-log.md)以查看产品/列表信息源更改（如价格和数量）。

- 产品[Buy Box](./buy-box-competitor-pricing.md)竞争对手定价数据。

- 产品[最低竞争者定价](./lowest-competitor-pricing.md)数据。

## 支持全球销售

使用[!DNL Amazon Sales Channel]扩展，您可以：

- 管理多个[!DNL Amazon Marketplace]地区（国家/地区）。

- 使用[Commerce货币配置工具](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html)支持多种货币。

- 管理来自您的产品位置和Amazon履行中心的发运。

## 客户管理

通过[导入与您的Amazon订单关联的客户数据](./order-settings.md#configure-order-settings)来构建[!DNL Commerce]客户数据库。 通过您的[!DNL Amazon Marketplace]列表和[!DNL Commerce]店面，通过这一扩展的客户列表扩大您的营销潜力。


入门很简单。 一个简短的入门培训流程可指导您创建[!DNL Amazon Seller Central]帐户，并与Amazon销售渠道商店和[!DNL Commerce]目录集成，以管理Amazon清单、订单、库存和履行。 一个中央仪表板显示所有Amazon sales channel store集成和Amazon列表的状态更新。 通过简化和自动化的流程与全球[!DNL Amazon Marketplace]的新客户建立联系 — 只需很少或完全不需要安装新系统的成本和人力。

集成[!DNL Amazon Seller Central]帐户后，[!DNL Amazon Sales Channel]扩展允许您管理帐户并在[!DNL Commerce]和Amazon之间同步数据。 它允许您直接通过[!DNL Commerce]管理员创建清单、管理促销、设置价格以及管理库存和履行。 这些选项包括定价规则，用于监控Amazon对同一项目的定价，并自动调整您的价格以提高竞争力。

