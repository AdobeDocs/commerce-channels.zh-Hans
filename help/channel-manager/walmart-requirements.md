---
title: “[!DNL Walmart]要求”
description: '确认您拥有与渠道管理器集成所需的 [!DNL Walmart Marketplace]信息和资源。'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!DNL Walmart]要求

[!DNL Channel Manager]需要以下资源和信息才能为[!DNL Walmart Marketplace.]配置[!DNL Commerce]销售渠道

* [!DNL Walmart]卖方帐户

* 用于将Adobe Commerce或Magento Open Source连接到[!DNL Walmart Marketplace]的API密钥

  [!DNL Walmart Marketplace] API密钥启用Adobe[!DNL Commerce]或Magento Open Source的[!DNL Channel Manager]与Walmart Marketplace之间的集成。 在销售人员入门培训流程开始之前，在销售人员中心中设置API密钥。

## 设置[!DNL Walmart Seller]帐户

转到[!DNL Walmart Seller Center]以设置你的[沃尔玛卖家帐户](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp)。

## 生成[!DNL Walmart Marketplace]生产API密钥

1. 转到[!DNL Walmart Marketplace]为Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey)生成[解决方案提供程序生产API密钥。

1. 创建密钥并配置权限：

   * 选择Adobe作为解决方案提供商。

   * 设置权限，如下表所示。 有关详细信息，请参阅&#x200B;_Walmart Marketplace卖家帮助_&#x200B;中的[API凭据](https://sellerhelp.walmart.com/seller/s/guide?article=000006422)。

   沃尔玛的&#x200B;**API密钥配置Adobe**

   | **权限** | **设置** |
   |----------------|-------------|
   | 内容 | 完全访问 |
   | 获取信息源 | 仅查看 |
   | 库存 | 完全访问 |
   | 项目 | 完全访问 |
   | 滞后时间 | 完全访问 |
   | 订购 | 完全访问 |
   | 价格 | 完全访问 |
   | 报告 | 仅查看 |
   | 返回 | 完全访问 |
   | 规则 | 完全访问 |
   | 配送 | 完全访问 |

## [!DNL Walmart Marketplace]存储状态

将产品连接到市场时，列表可用性取决于[!DNL Walmart Marketplace]商店的状态：

* 对于实时商店，您的产品选件将列出并在匹配操作完成后出售。

* 对于未上线的商店，您的产品选件处于暂存状态，因此客户无法看到。 当[!DNL Walmart Marketplace]存储区上线时，暂存列表会自动推送到实时存储区。

![[!DNL Walmart Seller Central]暂存产品](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>安装和配置[!DNL Channel Manager]后，所有库存、价格和订单更新将自动同步。 在禁用任何更新产品和订单数据的其他集成之前，请勿将[!DNL Channel Manager]连接到沃尔玛商城的实时商店。 如果您配置了其他集成，请在连接到实时商店之前验证[!DNL Commerce]中的项目数量和价格是否与[!DNL Walmart Marketplace]中的数量匹配。

