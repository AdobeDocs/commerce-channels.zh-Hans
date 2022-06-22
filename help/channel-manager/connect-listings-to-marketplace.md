---
title: 将上市信息与沃尔玛连接
description: '''连接列表 [!DNL Commerce] 产品 [!DNL Walmart Marketplace]开始卖。'
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: bc2e14714e9b532263c480395da28b31b4c3797c
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# 将上市信息与沃尔玛连接

和其他市场一样， [!DNL Walmart] 允许第三方销售者列出他人销售的项目。

- [!DNL Walmart Marketplace] 使用产品标识符（如UPC和GTIN）将产品与现有产品进行匹配 [!DNL Walmart Marketplace] 列表。

- 对于匹配的产品， Walmart Marketplace会列出更新，以包括 [!DNL Commerce] 产品选件 [!DNL Channel Manager].

- 通常，价格最低的产品选件会首先显示在 [!DNL Walmart Marketplace] 列表，但其他因素（如评论）也会影响投放。

## 匹配产品

当您匹配产品时，渠道管理器会将产品数据发送到 [!DNL Walmart Marketplace] 搜索具有与映射的 [!DNL Commerce] 产品属性。 匹配条件由 [属性映射配置](map-catalog-attributes.md) 的渠道。

如果找到匹配项，则会更新现有产品列表以添加您的选件。

### 先决条件

在匹配产品之前，请确认您的产品目录属性值是否满足Walmart要求，并配置产品属性设置。 请参阅 [映射目录属性](map-catalog-attributes.md).

#### 选择并匹配产品

1. 打开连接的销售渠道。

1. 从 **[!UICONTROL Listings]**，选择要与 *[!UICONTROL Draft]* 状态。

   ![从列表中选择产品并发送以进行匹配](assets/products-in-marketplace-sales-channel.png)

1. 选择 **[!UICONTROL Match Products]**.

   消息指示为匹配而发送的产品数量。

   ![将产品发送到连接的销售渠道](assets/products-submitted-for-matching.png)

   选定产品的状态将更改为 [!UICONTROL *处理*] 直到匹配操作完成。 沃尔玛商城可能需要30分钟才能完成比赛操作。

### 检查匹配状态

匹配完成后，选择 **[!UICONTROL Refresh products]** 查看当前产品状态。 *匹配* 或 *错误*.

- **[!UICONTROL Match]** 表示产品已成功匹配。 您的产品选件与沃尔玛Marketplace的现有列表相关。 如果 [市场商店不活动](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* 显示在 *[!UICONTROL Status detail]* 列。 在 [!DNL Walmart Marketplace] 存储区已激活。

- **[!UICONTROL Error]** 表示由于以下问题之一，匹配操作失败：

   - [!DNL Channel Manager] 由于连接问题，无法发送以进行匹配。

   - 未找到匹配项。

   - 找到匹配项，但无法连接列表，因为 [!DNL Walmart Marketplace] 返回了错误代码。 请参阅 **[!UICONTROL Error Description]** 以了解有关该问题的信息。

### 在沃尔玛上市

匹配产品后，复查更新的产品列表，并验证 [[!UICONTROL Walmart Marketplace Seller Account Items] 仪表板](https://seller.walmart.com/items-and-inventory/manage-items) 查看更新的产品。

### 产品匹配错误疑难解答

如果产品匹配操作失败并出现错误，则会在 *[!UICONTROL Status detail]* 列 [!UICONTROL Channel Manager] 产品列表。

返回的常见错误格式不正确，产品ID值或缺少必需的属性。

#### 修复产品ID值

| 类型 | 描述 | 示例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12,12位数，包括校验位。 </br></br>如果UPC的位数少于12位（如8位的UPC-E），则添加结束零以满足要求。 | 更改自 `45678912345` to `045678912345` |
| GTIN | GTIN-14,14位数，包括校验位。 </br></br>如果GTIN的位数少于14位，则添加前导零 </br>以满足要求。 | 更改 `456789123456` to `0045678912345` |
| EAN | GTIN-13,13位数，包括校验位。 </br></br>如果EAN的位数少于13位，则添加前导 </br>零以满足要求。 | 更改自 `4567891234` to `0004567891234` |

有关Walmart Marketplace错误代码的详细信息，请参阅 [沃尔玛卖家帮助](https://sellerhelp.walmart.com/s/guide?article=000005844).

## 上传新产品列表

对于在Walmart Marketplace上没有匹配项的产品，请使用Walmart产品类别Excel模板批量上传产品列表。 使用从 [!DNL Commerce] 实例。

对于新产品清单，请检查您的产品目录，以确保您计划在沃尔玛市场销售的产品具有沃尔玛市场产品清单所需的属性。

**Walmart Marketplace列表 — 属性要求**

| **属性** | **需求级别** |
|--------------------------|-----------------------|
| SKU | 必需 |
| 产品名称 | 必需 |
| 产品ID类型 | 必需 |
| 产品ID | 必需 |
| 品牌 | 必需 |
| 简短描述 | 必需 |
| 售价 | 必需 |
| 网站描述 | 必需 |
| 主图像URL | 必需 |
| 装运重量 | 必需 |
| 主要功能 | 建议 |
| 型号 | 建议 |
| 制造商名称 | 建议 |
| 制造商部件号 | 建议 |
| 大小 | 建议 |
| 颜色 | 建议 |
| 主图像URL | 可选 |
| 其他图像URL | 可选 |
| 制造商 | 可选 |

### 先决条件

- 确认您满足 [沃尔玛要求](walmart-requirements.md).

- 在 [!DNL Commerce] 产品目录，验证要在Walmart Marketplace上列出的产品的目录配置是否具有所有必需属性并符合Walmart Marketplace内容准则。

- 验证cron作业是否正在运行以完成导出操作。

   - 有关本地实例，请参阅 [配置并运行cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   - 有关Adobe云基础架构，请参阅 [设置创建作业](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### 创建要上传的产品数据文件

1. 从 [沃尔玛卖家账户](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)，请从沃尔玛销售中心下载产品列表模板。

   - 从产品目录项目页面中，选择 **[!UICONTROL Add Items]**. 然后，选择 **[!UICONTROL Add items in bulk]**.

      ![在Walmart Marketplace项目配置中以批量方式添加项目](assets/walmart-seller-account-add-items-bulk.png)

   - 在下载页面上，选择 **[!UICONTROL Full Setup]**. 然后，选择项目类别并下载类别模板。

      ![在Walmart Marketplace项目配置中下载类别模板选项](assets/walmart-seller-account-full-setup-download.png)

   - 验证模板是否包含产品清单的必需属性和推荐属性。

1. 从 [!DNL Commerce] 管理员，选择要从您的Adobe导出的产品数据 [!DNL Commerce] 网站。

   - 在管理员中，选择 [!UICONTROL **系统** >数据传输> **导出**].

   - 在 [!UICONTROL Export] 页面 [!UICONTROL Entity Type] 字段，选择 [!UICONTROL **产品**].

   - 在 [!UICONTROL Entity Attributes] 表中，为产品数据导出配置选择条件。
   ![导出 [!UICONTROL [!DNL Commerce] Admin]](assets/walmart-seller-account-full-setup-download.png)

   使用过滤器选择并配置适用于您所销售产品类别的属性值。 确保包括沃尔玛的必需属性和推荐属性(请参阅 [导出数据](https://docs.magento.com/user-guide/system/data-export.html) Adobe [!DNL Commerce] 用户指南以了解详细说明。)

   要在导出中忽略属性，请选择 [!UICONTROL **排除**] 复选框。

1. 滚动到属性表的结尾，然后选择 [!UICONTROL **继续**] 以开始导出数据。

   CSV导出文件通过使用cron作业的消息队列进行处理，并保存在 `var/export/folder`. (请参阅 [管理消息队列](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) 在 *Commerce Developer指南*.)

1. 打开Walmart Marketplace产品类别的Excel模板，然后使用Excel宏功能将导出的产品数据合并到Excel模板中。

1. 使用导出的产品数据上载Excel文件。

   - 返回至 [沃尔玛卖家中心](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - 选择 [!UICONTROL **添加项目** > **批量添加项目**].
   - 将填写好的电子表格拖至“上传”部分。
   - 选择 [!UICONTROL **提交**].
   - 选择&#x200B;[!UICONTROL  **活动馈送**] 查看进度。

有关完整说明，请参阅 [使用完整的项目规范批量添加项目](https://sellerhelp.walmart.com/s/guide?article=000007680) 在 [!DNL *沃尔玛卖家帮助*].
