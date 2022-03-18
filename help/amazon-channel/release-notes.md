---
title: '''[!DNL Amazon Sales Channel] 发行说明'''
description: 查看发行说明，了解有关 [!DNL Amazon Sales Channel] 版本。
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: 19424bf0deebf2b5464f973edad48f63d6042463
workflow-type: tm+mt
source-wordcount: '2090'
ht-degree: 0%

---

# 发行说明

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] 可以在云基础架构版本2.3.x和2.4.x上具有Magento Open Source、Adobe Commerce和Adobe Commerce的实例上安装。Adobe Commerce 2.1、Magento Open Source2.2或Magento1不再支持该扩展。
> <br>支持 [!DNL Amazon sales channel]  版本4.0.0和4.1.0(仅适用于Adobe Commerce 2.3.x版本)。
> <br>[!DNL Amazon sales channel] 版本4.2.0及更高版本与Adobe Commerce 2.3.x版本兼容，但仅支持Adobe Commerce 2.4.x版本。

以下发行说明介绍了 [!DNL Amazon sales channel] 包括：

![新建](../assets/new.svg) 新增功能
![修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题

请参阅 [即将发行的版本](https://devdocs.magento.com/release/)用于版本控制、支持和兼容性的{target=&quot;_blank&quot;}。

## v4.4.2

[!DNL Amazon sales channel]  4.4.2与Adobe Commerce版本2.3.x和2.4.0兼容，但仅受云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce版本2.4.1及更高版本支持

此版本的 [!DNL Amazon sales channel] 包括以下修复。

![修复](../assets/fix.svg) 更新了依赖关系以支持其他更新的扩展。
![修复](../assets/fix.svg) 添加了对PHP 8.1的支持。

## v4.4.1

[!DNL Amazon sales channel] 4.4.1与Adobe Commerce版本2.3.x和2.4.0兼容，但仅适用于云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce版本2.4.1及更高版本。

此版本的 [!DNL Amazon sales channel]  包括以下修复。

![修复](../assets/fix.svg) 更改了Adobe Commerce接收 _用户名_ 字段。 以前，在创建订单时，如果 _用户名_ 字段中包含特殊字符。 Adobe Commerce现在收到 _用户名_ 数据，并过滤掉特殊字符，以便成功创建顺序。

## v4.4.0

[!DNL Amazon sales channel] 4.4.0与Adobe Commerce版本2.3.x和2.4.0兼容，但仅适用于云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce版本2.4.1及更高版本。

此版本的 [!DNL Amazon sales channel] 包括以下改进和修复。

![新建](../assets/new.svg) 为配置添加了对只读模式的支持。 请参阅 [销售渠道设置](sales-channel-settings.md).

![修复](../assets/fix.svg) 更改了数据流，以便同一实例的多个副本可以同时获取更新。

![修复](../assets/fix.svg) 更改了同步帐户信息的同步过程。 添加了一个要与远程帐户同步的cron作业，并在CLI命令中添加了相同的功能。

![修复](../assets/fix.svg) 添加了CLI命令参数和标记，以实现更精确的控制。

![修复](../assets/fix.svg) 更正了系统配置中的“Background Tasks(cron)Source(后台任务(cron)Source（源）)”。

![修复](../assets/fix.svg) 更正了将国家/地区代码设置为波多黎各(PR)时无法创建订单的问题。

## v4.3.0

[!DNL Amazon sales channel] 4.3.0与Adobe Commerce版本2.3.x和2.4.0兼容。仅对云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce版本2.4.1及更高版本提供支持。

此版本的 [!DNL Amazon sales channel] 包括以下改进和修复。

![修复](../assets/fix.svg) <!--CHAN-xxxx-->的 _订单详细信息_ 功能已重新设计，不再依赖 _导入订单_ 设置。 现在，所有订单的订单详细信息都显示在AmazonSales Channel界面中。

![修复](../assets/fix.svg) 在 _[!UICONTROL Marketing]_菜单中，名称已从_[!UICONTROL Amazon]_ to _[!UICONTROL Amazon Sales Channel]_.

![已知问题](../assets/bug.svg) **重要信息**:在Adobe Commerce 2.4.1版本中，解决了与Adobe Commerce 2.4.0兼容的已知问题。

- Amazon cron流程 `error` state
- 在数据库中创建存储时，使用Commerce 2.4.0进行安装失败
- 安装MSI后，创建产品失败

## v4.2.0

[!DNL Amazon sales channel] 4.2.0与Adobe Commerce版本2.3.x兼容，但仅受云基础架构上版本2.4.x的Magento Open Source、Adobe Commerce和Adobe Commerce支持。 如果您之前 [!DNL Amazon sales channel] 安装的版本并尝试将Adobe Commerce更新到版本2.4.0时，系统会提示您更新扩展，然后才能完成Adobe Commerce更新。

此版本的 [!DNL Amazon sales channel] 包含新功能以及改进和修复。

![已知问题](../assets/bug.svg) When [!DNL Amazon sales channel] 4.2.0已与版本2.4.0和 [Inventory management](https://docs.magento.com/user-guide/catalog/inventory.html) 启用时，存在一个已知问题，该问题会阻止在您的商务目录中添加产品。 此问题将在未来的Commerce版本中解决。

![新建](../assets/new.svg) [!DNL Amazon sales channel] 已得到增强，可接受基于文本的地址数据并将其与标准化地址格式（包括城市、州和邮政编码）进行匹配。 此更新使订单和发运数据能够与Amazon同步（同步），而不会出现地址错误。<br/>例如，购物者将城市、州/省、邮政编码输入为 `Escondido, californiA 92025-1501`. AmazonSales Channel会导入数据，并将数据与标准格式匹配，如 `Escondido, CA 92025`，然后以此标准化格式将其同步回Amazon。

![新建](../assets/new.svg) 添加了对PHP 7.4的支持。

![新建](../assets/new.svg) <!--CHAN-4334-->添加了对Adobe Commerce 2.4.x的支持。以前的版本可能与Commerce 2.4.x兼容，但不支持。 请参阅 [即将发行的版本](https://devdocs.magento.com/release/){:target=&quot;_blank&quot;}以实现版本兼容性。 AmazonSales Channel必须更新到4.2.0，然后才能完成Adobe Commerce 2.4.0更新。

![修复](../assets/fix.svg) <!--CHAN-4431-->更正了导致 _拒绝访问_ 英国客户的错误。

![修复](../assets/fix.svg) <!--CHAN-4394-->更正了导致Amazon发运状态无法同步到相应商务订单的问题，从而将订单的发运状态“锁定”为 `Pending` 商务和 `Unshipped` 在Amazon。 使用新的标准化地址功能，已解决这些发运状态错误。

![修复](../assets/fix.svg) <!--ticket#-->更新了订单同步（同步）以忽略失败的订单导入，从而减少了多次同步尝试并允许后续导入处理，每五分钟提交一次订单同步请求。 同步错误仍会记录在错误日志中，但标记为“已处理”，以允许进一步记录功能。 此外， [!DNL Amazon sales channel] 现在，会自动删除为未能在Commerce中创建的订单收集的多余数据。

![修复](../assets/fix.svg) 更新了错误日志记录以收集有关未捕获异常和扩展更新错误的更多信息。

![修复](../assets/fix.svg) <!--ticket#-->更正了导致 _最低价格_ 数据因缺失而失败 _价格_ 值。

![修复](../assets/fix.svg) <!--CHAN-4410-->更正了导致 _Amazon订单_ 查看日期范围字段何时留空。

![修复](../assets/fix.svg) <!--CHAN-4439-->更正了导致与数量相关的库存和履行同步错误的问题。 现在，该扩展会在与Amazon同步之前，将输入的数量值以小数形式进行四舍五入。<br/> 例如，当商户手动输入 `2.5`，扩展会将值四舍五入为 `2` ，然后将更新数量与Amazon同步。

## v4.1.0

AmazonSales Channel4.1.0与云基础架构上的Adobe Commerce 2.3.x的Commerce Open Source、Adobe Commerce和Adobe Commerce兼容。 此版本的AmazonSales Channel包含用户界面增强功能，以及一些小错误修复。

![新建](../assets/new.svg) <!--4247, 4230-->更改了订单导入流程以符合商务订单要求。 这些更改更正了商务无法为导入订单创建相应订单的问题。 请参阅 [管理订单](managing-orders.md) 有关订单阻止程序和解决方案的信息。

![新建](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->更新了 _最近订购_ 区域，并在 _所有订单_ 显示所有Amazon订单的视图，包括过滤器选项和分页以查看更多订单。 请参阅 [Amazon商店功能板](amazon-store-dashboard.md) 和 [查看Amazon订单](amazon-orders-all.md).

![新建](../assets/new.svg) 添加了 _[!UICONTROL Order Notes]_重新设计的列_[!UICONTROL Amazon Orders]_ 两者的表 _[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_ 视图。 _[!UICONTROL Order Notes]_让商户知道订单的进口有问题。 请参阅 [查看Amazon订单](amazon-orders-all.md).

![新建](../assets/new.svg) <!--CHAN-4013-->更新了产品条件参数，以与 [Amazon续订](https://sell.amazon.com/programs/renewed) 项目。 请参阅 [续订的产品](renewed-products.md).

![新建](../assets/new.svg) <!--CHAN-3680-->已更新 [Amazon订单详细信息](amazon-order-details.md) ，以包含由Amazon履行的订单的“通用数据”。 请参阅 [履行者](fulfilled-by.md).

![修复](../assets/fix.svg) <!--CHAN-4069-->更正了导致存储卡上图标失真的问题。

![修复](../assets/fix.svg) <!--CHAN-4165-->更正了阻止 _登录_ 会话超时后显示屏幕。

![修复](../assets/fix.svg) <!--CHAN-4211-->更正了Amazon订单税额无法导入新商务订单的问题。

![修复](../assets/fix.svg) <!--CHAN-4234-->更正了导致商店仪表板上显示的总收入在 `Canceled` 或 `Error` 状态。

![修复](../assets/fix.svg) <!--CHAN-4326-->更正了导致与使用 _Magento Shipping_ 创建订单的方法。

![修复](../assets/fix.svg) <!--CHAN-4357-->更正了在运行cron同步时导致错误的问题。 在CLI命令中添加了锁，以阻止两个cron作业同时同步。

![修复](../assets/fix.svg) 更新了内容安全策略，以便在Commerce版本2.3.5中提供支持。

## v4.0.0

AmazonSales Channel4.0.0与云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce 2.3.0、2.3.1、2.3.2、2.3.3和2.3.4版兼容。 此版本的AmazonSales Channel包含许多用户界面升级，以及一些小错误修复。

>[!IMPORTANT]
>
>Adobe Commerce 2.3.5不支持AmazonSales Channel4.0.0。要获得Adobe Commerce 2.3.5的支持，请升级到AmazonSales Channel4.1.0。

![新建](../assets/new.svg) 引入了 [AmazonSales Channel](amazon-sales-channel-home.md) 主页中“卡片视图”对您的商店信息进行了改进。

![新建](../assets/new.svg) 引入了 [存储仪表板](amazon-store-dashboard.md) 和存储设置信息。

![新建](../assets/new.svg) 引入了更简单、更简单的 [载入过程](amazon-onboarding-home.md) 和 [默认存储设置](default-store-settings.md) 以便更快地集成您的商店。

![已知问题](../assets/bug.svg) <!--CHAN-4102--> When [创建属性](managing-attributes.md) 用于从列表和 **存储查看次数** 设置为 `All Store Views (Global)`，则存在一个已知问题，该问题会阻止图像导入到所有商店视图。 如果更改 **存储视图（将值导入）** 到特定存储区时，该存储区的图像会导入。

## v3.0.1

AmazonSales Channel3.0.1与云基础架构上的Adobe Commerce版本2.2.4+和2.3.xMagento Open Source、Adobe Commerce和Adobe Commerce兼容。

![修复](../assets/fix.svg) **数字字段设置**: <!--CHAN-3779-->需要基于数字的值的字段已更新为仅接受数字字符。 示例：定价规则设置>调整金额字段

![修复](../assets/fix.svg) **用户指南链接**: <!--CHAN-3778-->错误 _用户指南_ 链接已更正。

![修复](../assets/fix.svg) **复制Amazon列表**: <!--CHAN-3593-->现在已更正以前报告的导致Amazon列表重复的问题。 在此版本之前，扩展在导入列表时，会将Amazon地区的国家/地区代码添加到SKU值。 该列表与目录项目匹配，但扩展创建了一个新的重复列表，其中包含附加的SKU。 在此版本中，扩展不会修改导入列表的SKU，并且不会对现有列表进行更改。 您可以使用 [!UICONTROL End Listing(s)] “在Amazon上”选项来删除重复的列表。

## v3.0.0

AmazonSales Channel3.0.0与云基础架构上的Adobe Commerce版本2.2.4及更高版本、Magento Open Source、Adobe Commerce和Adobe Commerce 2.3.x兼容。

![新建](../assets/new.svg) **Amazon英国市场现已推出**:用户在创建和集成商店时，可以选择英国市场。 此英国升级包括对以下项的其他支持：

- [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources){target=&quot;_blank&quot;}

- [产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}信息。

![新建](../assets/new.svg) **改进了日志记录**: <!--CHAN-3642, 3672-->实施了 **启用调试日志记录** 功能，在需要进行故障诊断时收集其他同步数据。 请参阅 [Sales Channel设置](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html) 配置参考中的主题。

![修复](../assets/fix.svg) **产品目录**: <!--CHAN-3687-->更正了导致通过Amazon列表导入的图像无法应用于相应商务目录产品的问题。

![修复](../assets/fix.svg) **订单创建**: <!--CHAN-3708-->更正了商务无法为与商务目录产品不匹配的Amazon订单创建订单的问题。

![已知问题](../assets/bug.svg) **复制Amazon列表**: <!--CHAN-3593-->此问题会导致目录使用相同的SKU为导入的列表创建项目，但最终会添加区域代码。 然后，Amazon会将修改后的SKU作为新项目进行处理并创建一个列表。 此问题将在以后的版本中解决。

## v2.0.0

AmazonSales Channel2.0.0与云基础架构上的Magento Open Source、Adobe Commerce和Adobe Commerce版本2.2.4及更高版本和2.3.x兼容。

>[!NOTE]
>
>版本1.0.0仅在有限版本中可用。

![新建](../assets/new.svg)  **简化的入门和维护**:通过分步流程添加Amazon销售商帐户并与其集成，并通过管理员提供详细说明。 通过一个功能板维护您的商店、帐户和列出的产品。

![新建](../assets/new.svg)  **多帐户支持**:通过管理员管理和监控多个Amazon品牌和市场区域。

![新建](../assets/new.svg)  **智能定价**:设置自动重新定价规则，以增加您获得梦寐以求的Buy Box的机会。 设置价格以根据当前Buy Box价格或最低竞争者定价进行动态调整。 设置限制以重新定价，以保护利润。

![新建](../assets/new.svg)  **列表管理**:使用上市规则自动列出产品，并将您的商务目录同步到Amazon Marketplace。 添加特定覆盖以精细控制您的产品。 直接从管理员监控和管理所有列表。

![新建](../assets/new.svg)  **一致的Inventory management**:保持商务和Amazon库存数量保持同步。

![新建](../assets/new.svg)  **订单和履行管理**:通过功能板跟踪Amazon订单，实现无缝通信和库存更新。 完成并跟踪由Amazon、商户履行或多种方法组合履行的订单发运。

![已知问题](../assets/bug.svg)  您可能会遇到更新产品数量的等待时间较长的问题。 产品数量的更新可能需要大约两个小时才能同步。

![已知问题](../assets/bug.svg)  导入的订单可能具有 _Prime_ 或 _Premium_ 订单数。 您应在Amazon卖家帐户中验证这些订单。

![已知问题](../assets/bug.svg)  不合格的捆绑产品可能显示为符合在Amazon上列出的条件。 捆绑产品中的某个产品可能不符合条件。 如果遇到问题，请检查捆绑产品项目的资格状态。

![已知问题](../assets/bug.svg)  使用Inventory management for Commerce 2.3.x时，在创建订单时可能不会触发部分股票重新指数。 可出售数量会每小时重新计算一次，这可能会在此更新间隔期间导致超销。
