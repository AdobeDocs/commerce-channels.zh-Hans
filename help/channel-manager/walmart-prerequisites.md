---
title: 沃尔玛先决条件
description: 确认您拥有与渠道管理器集成所需的Walmart Marketplace信息和资源。
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 1f493dd40e23d459645704e5a52f9cc5edf4629f
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# 沃尔玛先决条件

渠道管理器需要以下资源和信息来为Walmart Marketplace配置商务销售渠道。

* 批准在沃尔玛销售，并凭证登录注册的Marketplace销售商帐户

* 用于将Adobe Commerce或Magento Open Source连接到Walmart Marketplace的API密钥

   Walmart Marketplace API密钥支持Adobe Commerce或Magento Open Source的渠道管理器与Walmart Marketplace之间的集成。 在启动Channel Manager载入过程之前，在Seller Central中设置API密钥。

## 设置Marketplace卖家帐户

1. [提交您的Walmart销售商申请](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
1. 在获得沃尔玛的批准后， [设置沃尔玛卖家账户](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## 生成Walmart Marketplace API密钥

1. 转到Walmart Marketplace以生成 [解决方案提供商生产API密钥，用于Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. 创建密钥并配置权限：

   * 选择Adobe作为解决方案提供商。

   * 如下表所示，设置权限。 有关详细信息，请参阅 [API凭据](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 在 _沃尔玛销售商帮助_.

   **AdobeWalmart的API密钥配置**

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
   | 返回结果 | 完全访问 |
   | 规则 | 完全访问 |
   | 装运 | 完全访问 |

## 沃尔玛商店状态

当您向Walmart Marketplace发布产品时，上市的可用性取决于您的Walmart Marketplace商店的状态：

* 对于实时商店，您的产品选件将列出并在匹配操作完成时可供销售。

* 对于不处于实时状态的商店，您的产品选件会进行暂存，且客户不可见。 当商店上线时，暂存列表会自动推送到实时商店。

![[!DNL Walmart Seller Central] 暂存产品](assets/walmart-seller-central-staged.png)
