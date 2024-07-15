---
title: 将列表连接到沃尔玛
description: '将 [!DNL Commerce] 产品的清单连接到 [!DNL Walmart Marketplace]以开始销售。'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# 将列表连接到沃尔玛

与其他市场一样，[!DNL Walmart]允许第三方销售者列出他人销售的项目。

- [!DNL Walmart Marketplace]使用产品标识符（如UPC和GTIN）将产品与现有[!DNL Walmart Marketplace]列表进行匹配。

- 对于匹配的产品，Walmart Marketplace将列出更新，以便在您连接来自[!DNL Channel Manager]的产品时包含[!DNL Commerce]产品选件。

- 通常，价格最低的产品选件首先出现在[!DNL Walmart Marketplace]列表中，但其他因素（如审核）也会影响置入。

## 匹配产品

当您匹配产品时，Channel Manager将产品数据发送到[!DNL Walmart Marketplace]以搜索其属性值匹配映射的[!DNL Commerce]产品属性的现有清单。 匹配条件由商店渠道的[属性映射配置](map-catalog-attributes.md)确定。

如果找到匹配项，则会更新现有产品列表以添加您的选件。

### 先决条件

在匹配产品之前，请验证产品目录属性值是否符合Walmart要求，并配置产品属性设置。 查看[映射目录属性](map-catalog-attributes.md)。

#### 选择和匹配产品

1. 打开连接的销售渠道。

1. 从&#x200B;**[!UICONTROL Listings]**&#x200B;中，选择要匹配的处于&#x200B;*[!UICONTROL Draft]*&#x200B;状态的产品。

   ![从列表中选择产品并发送以进行匹配](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL Match Products]**。

   一条消息指示已发送进行匹配的产品数量。

   在匹配操作完成之前，选定产品的状态将更改为&#x200B;[!UICONTROL *正在处理*]。 沃尔玛商场最多需要30分钟才能完成配对。

### 检查匹配状态

匹配完成后，选择&#x200B;**[!UICONTROL Refresh products]**&#x200B;以查看当前产品状态。 *匹配*&#x200B;或&#x200B;*错误*。

- **[!UICONTROL Match]**&#x200B;指示产品已成功匹配。 你的产品选件与沃尔玛商城的现有列表相关联。 如果[Marketplace存储区不是活动的](walmart-requirements.md#walmart-marketplace-store-status)，则&#x200B;*[!UICONTROL Status detail]*&#x200B;列中会显示&#x200B;*[!UICONTROL Staged for Match]*。 在激活[!DNL Walmart Marketplace]存储时自动连接暂存产品。

- **[!UICONTROL Error]**&#x200B;指示匹配操作由于以下问题之一而失败：

   - 由于连接问题，[!DNL Channel Manager]无法发送匹配请求。

   - 未找到匹配项。

   - 找到了匹配项，但无法连接列表，因为[!DNL Walmart Marketplace]返回了错误代码。 有关该问题的信息，请参阅&#x200B;**[!UICONTROL Error Description]**。

### 查看沃尔玛的列表

匹配产品后，从[[!UICONTROL Walmart Marketplace Seller Account Items]仪表板](https://seller.walmart.com/items-and-inventory/manage-items)中查看更新的产品列表并验证产品详细信息、价格和库存数量，以查看更新的产品。

### 产品匹配错误疑难解答

如果产品匹配操作失败并出现错误，则错误消息会显示在[!UICONTROL Channel Manager]产品列表的&#x200B;*[!UICONTROL Status detail]*&#x200B;列中。

返回的常见错误是产品ID值的格式不正确或缺少所需的属性。

#### 修复产品ID值

| 类型 | 描述 | 示例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12，包含校验位的12位数字。 </br></br>如果UPC少于12位，例如UPC-E为8位，请添加结尾的零以满足要求。 | 从`45678912345`更改为`045678912345` |
| GTIN | GTIN-14，包含校验位的14位数字。 </br></br>如果您的GTIN少于14位，请添加前导零</br>以满足要求。 | 将`456789123456`更改为`0045678912345` |
| EAN | GTIN-13，包含校验位的13位数字。 </br></br>如果您的EAN少于13位，请添加前置</br>零以满足要求。 | 从`4567891234`更改为`0004567891234` |

有关沃尔玛商城错误代码的详细信息，请参阅[沃尔玛卖家帮助](https://sellerhelp.walmart.com/s/guide?article=000005844)。

## 上传新产品列表

对于沃尔玛商城中没有匹配项的产品，请使用沃尔玛产品类别Excel模板批量上传产品清单。 您使用从[!DNL Commerce]实例导出的产品目录数据填充Walmart模板。

对于新产品清单，请检查您的产品目录，以确保您计划在沃尔玛商店销售的产品具有沃尔玛商店产品清单所需的属性。

**Walmart Marketplace列表属性要求**

| **属性** | **要求级别** |
|--------------------------|-----------------------|
| SKU | 必填 |
| 产品名称 | 必填 |
| 产品ID类型 | 必填 |
| 产品ID | 必填 |
| 品牌 | 必填 |
| 简短描述 | 必填 |
| 售价 | 必填 |
| 站点描述 | 必填 |
| 主图像URL | 必填 |
| 装运重量 | 必填 |
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

- 验证您是否符合[沃尔玛要求](walmart-requirements.md)。

- 在您的[!DNL Commerce]产品目录中，验证要在沃尔玛商城中列出的产品的目录配置是否具有所有必需属性，并符合沃尔玛商城内容准则。

- 验证cron作业是否正在运行，以完成导出操作。

   - 对于内部部署实例，请参阅[配置和运行cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)。

   - 有关Adobe云基础架构，请参阅[设置cron作业](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html)。

### 创建要上传的产品数据文件

1. 从您的[沃尔玛销售商帐户](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)下载沃尔玛销售中心的产品列表模板。

   - 从产品目录项页面中，选择&#x200B;**[!UICONTROL Add Items]**。 然后选择&#x200B;**[!UICONTROL Add items in bulk]**。

     ![在Walmart Marketplace项目配置中批量添加项目选项](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - 在下载页面上，选择&#x200B;**[!UICONTROL Full Setup]**。 然后，选择项目类别并下载类别模板。

     在Walmart Marketplace项目配置中![下载类别模板选项](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - 验证模板是否包含产品清单所需的属性和建议的属性。

1. 从[!DNL Commerce]管理员中，选择要从Adobe[!DNL Commerce]网站导出的产品数据。

   - 从管理员中，选择&#x200B;[!UICONTROL **系统** >数据传输> **导出**]。

   - 在[!UICONTROL Entity Type]字段的[!UICONTROL Export]页面上，选择&#x200B;[!UICONTROL **产品**]。

   - 在[!UICONTROL Entity Attributes]表中，配置产品数据导出的选择标准。

     使用过滤器选择和配置适用于您销售的产品类别的属性值。 确保包括沃尔玛的必需属性和建议属性。 (有关详细说明，请参阅Adobe[!DNL Commerce]用户指南中的[导出数据](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html)。)

     要从导出中忽略某个属性，请选中行开头的&#x200B;[!UICONTROL **排除**]&#x200B;复选框。

1. 滚动到属性表的末尾，然后选择&#x200B;[!UICONTROL **继续**]&#x200B;以开始数据导出。

   CSV导出文件通过使用cron作业的消息队列进行处理，并保存在`var/export/folder`中。 （请参阅&#x200B;*配置指南*&#x200B;中的[管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html)。）

1. 打开Walmart Marketplace产品类别的Excel模板，然后使用Excel宏功能将导出的产品数据合并到Excel模板中。

1. 上载包含导出的产品数据的Excel文件。

   - 返回到[沃尔玛销售中心](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)的产品目录项目页面。

   - 选择&#x200B;[!UICONTROL **添加项** > **批量添加项**]。
   - 将已完成的电子表格拖到“上传”部分。
   - 选择&#x200B;[!UICONTROL **提交**]。
   - 选择&#x200B;[!UICONTROL  **活动信息源**]&#x200B;以查看进度。

有关完整说明，请参阅&#x200B;[!DNL *Walmart卖家帮助*]&#x200B;中的[使用完整项目规范](https://sellerhelp.walmart.com/s/guide?article=000007680)批量添加项目。
