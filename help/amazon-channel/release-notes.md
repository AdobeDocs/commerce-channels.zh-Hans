---
title: ‘[!DNL Amazon Sales Channel] 发行说明
description: 查看发行说明，了解关于 [!DNL Amazon Sales Channel] 版本。
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: 3b2f60ad2796ee1fdc8808fc0941d76a603b2213
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# 发行说明

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] 可以安装在云基础架构版本2.3.x和2.4.x上具有Magento Open Source、Adobe Commerce和Adobe Commerce的实例上。Adobe Commerce 2.1、Magento Open Source2.2或Magento1上不再支持该扩展。
> <br>支持适用于 [!DNL Amazon sales channel]  版本4.0.0和4.1.0(仅适用于Adobe Commerce 2.3.x版本)。
> <br>[!DNL Amazon sales channel] 版本4.2.0+与Adobe Commerce 2.3.x版本兼容，但仅对Adobe Commerce 2.4.x版本提供支持。

以下发行说明介绍了 [!DNL Amazon sales channel] 并包括：

![新](../assets/new.svg) 新增功能
![已修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题

参见 [即将发行的版本](https://devdocs.magento.com/release/){target="_blank"} 版本控制、支持和兼容性。

## v4.4.4

*2023年3月7日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![已修复的问题](../assets/fix.svg) 添加了对Adobe Commerce 2.4.6和PHP 8.2的支持。

![已修复的问题](../assets/fix.svg) 减少日志中的噪音。

![已修复的问题](../assets/fix.svg) 提高了提取更新的稳定性。

![已修复的问题](../assets/fix.svg) 简化了运行单个操作（如拉取）或从CLI进行应用的流程。

![已修复的问题](../assets/fix.svg) 已升级以下项的依赖项： `magento/services-connector`.

![已修复的问题](../assets/fix.svg) 修复了使用无效国家/地区代码的英国帐户中的同步问题。

![已修复的问题](../assets/fix.svg) 对目录产品实体的entity_type_id进行硬编码会导致Magento价格来源出现问题。

![已修复的问题](../assets/fix.svg) 修复了导致从其他实例的后端删除的帐户无法从UI中删除的问题。

![已修复的问题](../assets/fix.svg) 修复了某些购物车规则中断订单导入的问题。

## v4.4.3

*2023年3月7日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg) 添加了对Adobe Commerce 2.4.4的支持。

## v4.4.2

*2021年11月11日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg) 更新了依赖关系以支持其他更新的扩展。
![修复](../assets/fix.svg) 添加了对PHP 8.1的支持。

## v4.4.1

*2021年11月11日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg) 更改了Adobe Commerce接收 _用户名_ Amazon中的字段。 以前，在订单创建过程中出错，因为 _用户名_ 字段包含特殊字符。 Adobe Commerce现在会收到 _用户名_ 并筛选掉特殊字符，以便成功创建订单。

## v4.4.0

*2021年4月9日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新](../assets/new.svg) 为配置添加了对只读模式的支持。 参见 [sales channel设置](sales-channel-settings.md).

![修复](../assets/fix.svg) 更改了数据流，以便同一实例的多个副本可以同时获取更新。

![修复](../assets/fix.svg) 已更改同步帐户信息的同步过程。 添加了一个cron作业以与远程帐户同步，并在CLI命令中添加了相同的功能。

![修复](../assets/fix.svg) 添加了CLI命令参数和标记，以便更精确地控制。

![修复](../assets/fix.svg) 已更正系统配置中的后台任务(cron)源。

![修复](../assets/fix.svg) 更正了当国家代码设置为波多黎各(PR)时阻止创建订单的问题。

## v4.3.0

*2021年3月3日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg) <!--CHAN-xxxx-->此 _订单详细信息_ 功能已重新设计，不再依赖 _导入订单_ 设置。 现在，所有订单的订单详细信息将显示在AmazonSales Channel界面中。

![修复](../assets/fix.svg) 在 _[!UICONTROL Marketing]_菜单中，名称已从_[!UICONTROL Amazon]_ 到 _[!UICONTROL Amazon Sales Channel]_.

![已知问题](../assets/bug.svg) **重要**：Adobe Commerce 2.4.1版本中解决了与Adobe Commerce 2.4.0兼容的已知问题。

- 中的Amazon cron流程 `error` state
- 在数据库中创建存储时，使用Commerce 2.4.0安装失败
- 安装MSI后，创建产品失败

## v4.2.0

*2021年3月3日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

如果您拥有以前的 [!DNL Amazon sales channel] 版本2.4.0。如果您已安装Adobe Commerce并尝试将其更新到版本2.4.0，则在完成Adobe Commerce更新之前，系统会提示您更新扩展。

![已知问题](../assets/bug.svg) 时间 [!DNL Amazon sales channel] 4.2.0与版本2.4.0和 [Inventory management](https://docs.magento.com/user-guide/catalog/inventory.html) 会有一个已知问题，该问题会阻止在您的商务目录中添加产品。 将在未来的Commerce版本中解决此问题。

![新](../assets/new.svg) [!DNL Amazon sales channel] 已增强以接受基于文本的地址数据，并将其与标准化地址格式（包括城市、州和邮政编码）匹配。 此更新使订单和装运数据能够与Amazon同步（同步），且不会出现地址错误。<br/>例如，购物者输入城市、州/省、邮政编码为 `Escondido, californiA 92025-1501`. AmazonSales Channel导入数据并将其与标准格式匹配，如下所示 `Escondido, CA 92025`，然后以这种标准化格式将其同步回Amazon。

![新](../assets/new.svg) 添加了对PHP 7.4的支持。

![新](../assets/new.svg) <!--CHAN-4334-->添加了对Adobe Commerce 2.4.x的支持。以前的版本可能与Commerce 2.4.x兼容，但不受支持。 参见 [即将发行的版本](https://devdocs.magento.com/release/){：target=&quot;_blank&quot;}以了解版本兼容性。 必须先将AmazonSales Channel更新到4.2.0，然后才能完成Adobe Commerce 2.4.0更新。

![修复](../assets/fix.svg) <!--CHAN-4431-->更正了导致出现错误的问题 _访问被拒绝_ 英国客户出错。

![修复](../assets/fix.svg) <!--CHAN-4394-->修复了阻止Amazon配送状态同步到相应的Commerce订单，从而将该订单的配送状态“锁定”为的问题 `Pending` 在Commerce和 `Unshipped` 在Amazon中。 通过新的标准化地址功能，这些运送状态错误已得到解决。

![修复](../assets/fix.svg) <!--ticket#-->更新了订单同步(sync)以忽略失败的订单导入，从而减少了多次同步尝试并允许后续导入进行处理，订单同步请求每5分钟提交一次。 同步错误仍记录在错误日志中，但标记为“已处理”以允许执行进一步的记录功能。 另外， [!DNL Amazon sales channel] 现在会自动删除为无法在Commerce中创建的订单收集的超额数据。

![修复](../assets/fix.svg) 更新了错误日志记录以收集有关未捕获异常和扩展更新错误的更多信息。

![修复](../assets/fix.svg) <!--ticket#-->更正了导致初始同步的问题 _最低价格_ 由于缺少数据而失败的数据 _价格_ 值。

![修复](../assets/fix.svg) <!--CHAN-4410-->已更正导致中过滤错误的问题 _Amazon订单_ 在日期范围字段留空时查看。

![修复](../assets/fix.svg) <!--CHAN-4439-->更正了导致与数量相关的库存和履行同步错误的问题。 现在，该扩展在与Amazon同步之前，对以小数形式输入的数量值进行四舍五入。<br/> 例如，当商家手动输入 `2.5`，扩展将该值向下舍入为 `2` 然后与Amazon同步更新的数量。

## v4.1.0

*2020年5月7日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新](../assets/new.svg) <!--4247, 4230-->更改了订单导入流程以符合Commerce订单要求。 这些更改纠正了阻止Commerce为导入的订单创建相应订单的问题。 参见 [管理订单](managing-orders.md) ，以了解有关订单拦截器和解决方案的信息。

![新](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->已更新 _最近的订单_ 部分，并添加了一个新的 _所有订单_ 该视图可显示您的所有Amazon订单，包括用于查看更多订单的筛选选项和分页。 参见 [Amazon Store功能板](amazon-store-dashboard.md) 和 [查看Amazon订单](amazon-orders-all.md).

![新](../assets/new.svg) 添加了 _[!UICONTROL Order Notes]_重新设计的列_[!UICONTROL Amazon Orders]_ 表格（两者） _[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_ 视图。 _[!UICONTROL Order Notes]_让商家知道该订单的导入存在问题。 参见 [查看Amazon订单](amazon-orders-all.md).

![新](../assets/new.svg) <!--CHAN-4013-->更新了产品条件参数以与 [已续订Amazon](https://sell.amazon.com/programs/renewed) 程序。 参见 [续订的产品](renewed-products.md).

![新](../assets/new.svg) <!--CHAN-3680-->已更新 [Amazon订单详细信息](amazon-order-details.md) 为Amazon履行的订单包含“通用数据”。 参见 [履行者](fulfilled-by.md).

![修复](../assets/fix.svg) <!--CHAN-4069-->更正了导致存储卡上图标失真的问题。

![修复](../assets/fix.svg) <!--CHAN-4165-->更正了错误，以防止出现 _登录_ 屏幕会在会话超时后显示。

![修复](../assets/fix.svg) <!--CHAN-4211-->修复了导致Amazon订单税额无法导入到新Commerce订单的问题。

![修复](../assets/fix.svg) <!--CHAN-4234-->更正了导致商店仪表板中显示的收入合计包含订单的问题 `Canceled` 或 `Error` 状态。

![修复](../assets/fix.svg) <!--CHAN-4326-->修复了导致订单导入错误的问题，该错误与使用的第三方扩展相关联 _Magento Shipping_ 创建订单的方法。

![修复](../assets/fix.svg) <!--CHAN-4357-->更正了运行cron同步时导致错误的问题。 在CLI命令中添加了锁，以防止两个cron作业同时同步。

![修复](../assets/fix.svg) 更新了内容安全策略，以支持Commerce版本2.3.5。

## v4.0.0

*2020年3月25日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

>[!IMPORTANT]
>
>Amazon 2.3.5不支持Adobe CommerceSales Channel4.0.0。要获得Adobe Commerce 2.3.5的支持，请升级到AmazonSales Channel4.1.0。

![新](../assets/new.svg) 引入了一个新的 [AmazonSales Channel](amazon-sales-channel-home.md) 主页，改进了“信息卡视图”。

![新](../assets/new.svg) 引入了一个新的 [存储仪表板](amazon-store-dashboard.md) 列表、最近订单和存储设置信息。

![新](../assets/new.svg) 引入了一个更简单、更精简的 [载入流程](amazon-onboarding-home.md) 和 [默认商店设置](default-store-settings.md) 以更快地集成您的商店。

![已知问题](../assets/bug.svg) <!--CHAN-4102--> 时间 [创建属性](managing-attributes.md) 用于从列表和导入图像 **商店查看次数** 设置为 `All Store Views (Global)`，存在一个已知问题，阻止将图像导入所有商店视图。 如果更改设置 **存储视图（将值导入）** 到特定商店，映像会为该商店导入。

## v3.0.1

*2019年11月11*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg) **数字字段设置**： <!--CHAN-3779-->需要基于数字的值的字段已更新为仅接受数字字符。 实例：定价规则设置>调整金额字段

![修复](../assets/fix.svg) **用户指南链接**： <!--CHAN-3778-->不正确 _用户指南_ 已更正链接。

![修复](../assets/fix.svg) **复制Amazon列表**： <!--CHAN-3593-->之前报告的问题现在已得到纠正，该问题会导致重复Amazon列表。 在此版本之前，扩展在导入列表时将Amazon区域的国家代码添加到SKU值。 该列表与目录项目匹配，但扩展创建了一个带有附加SKU的新重复列表。 在此版本中，扩展不会修改导入列表的SKU，并且不会对现有列表进行更改。 您可以使用 [!UICONTROL End Listing(s)] 用于删除重复列表的Amazon选项。

## v3.0.0

*2019年10月7日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新](../assets/new.svg) **Amazon UK Marketplace现已推出**：用户在创建和集成Commerce商店时可以选择英国市场。 此英国升级包括以下附加支持：

- [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} 信息。

![新](../assets/new.svg) **改进了日志记录**： <!--CHAN-3642, 3672-->已实施 **启用调试日志记录** 在需要故障排除时收集其他同步数据的功能。 请参阅 [Sales Channel设置](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html) 配置参考中的主题。

![修复](../assets/fix.svg) **产品目录**： <!--CHAN-3687-->修复了阻止将使用Amazon列表导入的图像应用于相应的Commerce目录产品的问题。

![修复](../assets/fix.svg) **订单创建**： <!--CHAN-3708-->修复了Commerce无法为与Commerce目录产品不匹配的Amazon订单创建订单的问题。

![已知问题](../assets/bug.svg) **复制Amazon列表**： <!--CHAN-3593-->此问题导致目录使用相同的SKU为导入列表创建项目，但末尾添加了区域代码。 然后，Amazon将修改后的SKU处理为新项目并创建一个列表。 此问题将在未来版本中解决。

## v2.0.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

>[!NOTE]
>
>版本1.0.0仅在有限版本中提供。

![新](../assets/new.svg)  **简化的载入和维护**：通过分步流程添加您的Amazon卖方帐户并与之集成，该流程包含通过管理员提供的详细说明。 通过一个仪表板维护您的商店、帐户和列出的产品。

![新](../assets/new.svg)  **多帐户支持**：通过管理员管理和监控多个Amazon品牌和市场区域。

![新](../assets/new.svg)  **智能定价**：设置自动重新定价规则，提高获得梦寐以求的Buy Box的机会。 设置价格以动态地调整到当前Buy Box价格或最低的竞争对手价格。 设置重新定价限制以保护您的利润。

![新](../assets/new.svg)  **列表管理**：自动化产品列表并使用列表规则将您的Commerce目录同步到Amazon Marketplace。 添加特定覆盖以精细地控制您的产品/服务。 直接从管理员监控和管理所有列表。

![新](../assets/new.svg)  **一致的Inventory management**：将Commerce和Amazon库存数量保持同步。

![新](../assets/new.svg)  **订单和订单履行管理**：通过功能板以及无缝的通信和库存更新跟踪Amazon订单。 完成并跟踪由Amazon履行的订单发运、已履行的商家发运或多种方法组合。

![已知问题](../assets/bug.svg)  更新产品数量可能会遇到更长的等待时间。 产品数量的更新可能需要约2小时才能同步。

![已知问题](../assets/bug.svg)  导入的订单可能具有 _Prime_ 或 _Premium_ 订单。 您应在Amazon卖方帐户中验证这些订单。

![已知问题](../assets/bug.svg)  不符合条件的捆绑产品可能会显示为符合在Amazon上列出的条件。 捆绑产品中的某个产品可能不符合条件。 如果您遇到问题，请检查捆绑产品项目的资格状态。

![已知问题](../assets/bug.svg)  使用Inventory management for Commerce 2.3.x时，在创建订单时不会触发部分股票重新索引。 可销售量会每小时重新计算一次，这可能会导致在此更新间隔内过度销售。
