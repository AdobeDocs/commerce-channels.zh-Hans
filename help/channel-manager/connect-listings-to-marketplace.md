---
title: 将列表连接到沃尔玛
description: '''连接以下项的列表 [!DNL Commerce] 产品目标 [!DNL Walmart Marketplace]开始销售。”'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 0%

---

# 将列表连接到沃尔玛

和其他市场一样， [!DNL Walmart] 允许第三方销售者列出由他人销售的商品。

- [!DNL Walmart Marketplace] 使用产品标识符（如UPC和GTIN）将产品与现有产品进行匹配 [!DNL Walmart Marketplace] 列表。

- 对于匹配的产品，沃尔玛市场将列出更新内容，包括 [!DNL Commerce] 产品选件（当您从连接产品时） [!DNL Channel Manager].

- 通常，价格最低的产品选件首先出现在 [!DNL Walmart Marketplace] 列表，但其他因素（如审核）也会影响投放位置。

## 匹配产品

当您匹配产品时， Channel Manager会将产品数据发送至 [!DNL Walmart Marketplace] 搜索其属性值匹配映射的现有列表 [!DNL Commerce] 产品属性。 匹配标准由以下因素确定 [属性映射配置](map-catalog-attributes.md) 商店渠道的ID。

如果找到匹配项，则会更新现有产品列表以添加您的选件。

### 先决条件

在匹配产品之前，请验证产品目录属性值是否符合Walmart要求，并配置产品属性设置。 参见 [映射目录属性](map-catalog-attributes.md).

#### 选择并匹配产品

1. 打开连接的销售渠道。

1. 起始日期 **[!UICONTROL Listings]**，选择要匹配的产品，这些产品 *[!UICONTROL Draft]* 状态。

   ![从列表中选择产品并发送以进行匹配](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. 选择 **[!UICONTROL Match Products]**.

   一条消息指示已发送进行匹配的产品数量。

   所选产品的状态将更改为 [!UICONTROL *正在处理*] 直到匹配操作完成。 沃尔玛商场最多需要30分钟才能完成赛事。

### 检查匹配状态

匹配完成后，选择 **[!UICONTROL Refresh products]** 以查看当前产品状态。 *匹配* 或 *错误*.

- **[!UICONTROL Match]** 表示产品已成功匹配。 你的产品选件与沃尔玛商城的一个现有名单有关。 如果 [商城商店未处于活动状态](walmart-requirements.md#walmart-marketplace-store-status)， *[!UICONTROL Staged for Match]* 在中显示 *[!UICONTROL Status detail]* 列。 分段产品在以下情况下自动连接： [!DNL Walmart Marketplace] 存储区已激活。

- **[!UICONTROL Error]** 表示匹配操作因以下问题之一而失败：

   - [!DNL Channel Manager] 由于连接问题，无法发送以进行匹配。

   - 未找到匹配项。

   - 找到匹配项，但列表无法连接，因为 [!DNL Walmart Marketplace] 返回了错误代码。 请参阅 **[!UICONTROL Error Description]** 以获取有关该问题的信息。

### 查看沃尔玛的列表

匹配产品后，查看更新的产品列表，并从验证产品详细信息、价格和库存数量 [[!UICONTROL Walmart Marketplace Seller Account Items] 仪表板](https://seller.walmart.com/items-and-inventory/manage-items) 以查看更新的产品。

### 产品匹配错误故障诊断

如果产品匹配操作失败并出现错误，则错误消息会显示在 *[!UICONTROL Status detail]* 中的列 [!UICONTROL Channel Manager] 产品列表。

返回的常见错误是产品ID值的格式不正确或缺少所需的属性。

#### 修复产品ID值

| 类型 | 描述 | 示例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12，包括校验位在内的12位数字。 </br></br>如果UPC的位数少于12位，例如UPC-E为8位，请添加结尾零以满足要求。 | 更改自 `45678912345` 到 `045678912345` |
| GTIN | GTIN-14，包含校验位的14位数字。 </br></br>如果GTIN少于14位数，请添加前导零 </br>以满足要求。 | 更改 `456789123456` 到 `0045678912345` |
| EAN | GTIN-13,13位数字，包括校验位数。 </br></br>如果EAN少于13位数，请添加行距 </br>零以满足要求。 | 更改自 `4567891234` 到 `0004567891234` |

有关沃尔玛商城错误代码的详细信息，请参见 [沃尔玛卖家帮助](https://sellerhelp.walmart.com/s/guide?article=000005844).

## 上传新产品列表

对于沃尔玛商城中没有匹配项的产品，使用沃尔玛产品类别Excel模板批量上传产品清单。 您使用从以下位置导出的产品目录数据填充Walmart模板： [!DNL Commerce] 实例。

对于新产品列表，请检查您的产品目录，以确保您计划在沃尔玛商城销售的产品具有沃尔玛商城产品列表所需的属性。

**沃尔玛商城列表 — 属性要求**

| **属性** | **需求级别** |
|--------------------------|-----------------------|
| SKU | 必需 |
| 产品名称 | 必需 |
| 产品ID类型 | 必需 |
| 产品ID | 必需 |
| 品牌 | 必需 |
| 简短描述 | 必需 |
| 售价 | 必需 |
| 站点描述 | 必需 |
| 主图像URL | 必需 |
| 装运重量 | 必需 |
| 主要功能 | 推荐 |
| 型号 | 推荐 |
| 制造商名称 | 推荐 |
| 制造商部件号 | 推荐 |
| 大小 | 推荐 |
| 颜色 | 推荐 |
| 主图像URL | 可选 |
| 其他图像URL | 可选 |
| 制造商 | 可选 |

### 先决条件

- 确认您符合 [沃尔玛要求](walmart-requirements.md).

- 在您的 [!DNL Commerce] 产品目录，验证要在沃尔玛商城中列出的产品的目录配置是否具有所有必需属性，并符合《沃尔玛商城内容指南》。

- 验证cron作业是否正在运行以完成导出操作。

   - 有关内部部署实例，请参阅 [配置和运行cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html).

   - 有关Adobe云基础架构的信息，请参阅 [设置cron作业](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html).

### 创建要上传的产品数据文件

1. 来自您的 [沃尔玛卖家账户](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)，从沃尔玛卖家中心下载产品列表模板。

   - 从产品目录项页面中，选择 **[!UICONTROL Add Items]**. 然后，选择 **[!UICONTROL Add items in bulk]**.

     ![在Walmart Marketplace项目配置中的批量选项中添加项目](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - 在下载页面上，选择 **[!UICONTROL Full Setup]**. 然后，选择物料类别并下载类别模板。

     ![Walmart Marketplace项目配置中的下载类别模板选项](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - 验证模板是否包含产品列表所需的和建议的属性。

1. 从 [!DNL Commerce] 管理员，选择要从Adobe导出的产品数据 [!DNL Commerce] 站点。

   - 在管理员中，选择 [!UICONTROL **系统** >数据传输> **导出**].

   - 在 [!UICONTROL Export] 中的页面 [!UICONTROL Entity Type] 字段，选择 [!UICONTROL **产品**].

   - 在 [!UICONTROL Entity Attributes] 表格中，配置用于产品数据导出的选择标准。

     使用过滤器选择和配置适用于您销售的产品类别的属性值。 确保包括沃尔玛的必需属性和建议属性。 (请参阅 [导出数据](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) 在Adobe中 [!DNL Commerce] 用户指南，以了解详细说明。)

     要从导出中省略属性，请选择 [!UICONTROL **排除**] 复选框。

1. 滚动到属性表的末尾，然后选择 [!UICONTROL **继续**] 以开始数据导出。

   CSV导出文件通过使用cron作业的消息队列进行处理，并保存在中 `var/export/folder`. (请参阅 [管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 *配置指南*.)

1. 打开Walmart Marketplace产品类别的Excel模板，并使用Excel宏功能将导出的产品数据合并到Excel模板中。

1. 上载包含导出的产品数据的Excel文件。

   - 返回页中的“产品目录项目”页。 [沃尔玛销售中心](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - 选择 [!UICONTROL **添加项目** > **批量添加项目**].
   - 将已完成的电子表格拖到“上传”部分。
   - 选择 [!UICONTROL **提交**].
   - 选择&#x200B;[!UICONTROL  **活动信息源**] 查看进度。

有关完整说明，请参阅 [使用完整项目规格批量添加项目](https://sellerhelp.walmart.com/s/guide?article=000007680) 在 [!DNL *沃尔玛卖家帮助*].
