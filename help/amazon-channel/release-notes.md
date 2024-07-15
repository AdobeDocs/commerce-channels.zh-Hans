---
title: '[!DNL Amazon Sales Channel]发行说明'
description: 查看发行说明，了解所有 [!DNL Amazon Sales Channel] 发行版本的信息。
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel]发行说明

>[!IMPORTANT]
>
> [!DNL Amazon sales channel]可以安装在云基础架构版本2.3.x和2.4.x上具有Magento Open Source、Adobe Commerce和Adobe Commerce的实例上。Adobe Commerce 2.1、Magento Open Source2.2或Magento1上不再支持该扩展。
> <br>仅在Adobe Commerce 2.3.x版本上为[!DNL Amazon sales channel]版本4.0.0和4.1.0提供支持。
> <br>[!DNL Amazon sales channel] 版本4.2.0及更高版本与Adobe Commerce 2.3.x版本兼容，但仅对Adobe Commerce 2.4.x版本提供支持。
>

这些发行说明描述了[!DNL Amazon sales channel]的初始版本，其中包括：

![新](../assets/new.svg)新功能
![已修复问题](../assets/fix.svg)修复和改进
![已知问题](../assets/bug.svg)已知问题

有关版本控制、支持和兼容性，请参阅[即将发布的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html)。

请参阅[产品可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)，了解哪些Adobe Commerce版本支持此扩展。

## v4.5.0

*2023年8月30日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)已添加Adobe.IO API网关（从MAGI更改），以提高身份验证安全性。 `ServicesId`提供了一个新的UI来管理您的Adobe.IO凭据，类似于其他[Adobe Commerce服务](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html)。

>[!NOTE]
>
>商家必须确保为生产更新[私有和公共API密钥](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html)。


![已修复问题](../assets/fix.svg)识别了配置设置问题并修复了订单创建流程。

## v4.4.4

*2023年3月7日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![修复了问题](../assets/fix.svg)添加了对Adobe Commerce 2.4.6和PHP 8.2的支持。

![修复了问题](../assets/fix.svg)减少了日志中的噪音。

![修复了问题](../assets/fix.svg)提高了获取更新的稳定性。

![修复了问题](../assets/fix.svg)简化了运行单个操作（如拉取）或从CLI应用的流程。

![修复了问题](../assets/fix.svg)已升级`magento/services-connector`的依赖关系。

![修复了问题](../assets/fix.svg)修复了使用无效国家/地区代码的英国帐户中的同步问题。

![修复了问题](../assets/fix.svg)对目录产品实体的entity_type_id进行硬编码会导致Magento价格Source出现问题。

![修复了问题](../assets/fix.svg)修复了导致从其他实例的后端删除的帐户也无法从UI中删除的问题。

![修复了问题](../assets/fix.svg)修复了一些购物车规则中断订单导入的问题。

## v4.4.3

*2023年3月7日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![Fix](../assets/fix.svg)添加了对Adobe Commerce 2.4.4的支持。

## v4.4.2

*2021年11月11日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![修复](../assets/fix.svg)更新的依赖项以支持其他更新的扩展。
![修复](../assets/fix.svg)添加了对PHP 8.1的支持。

## v4.4.1

*2021年11月11日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![修复](../assets/fix.svg)更改了Adobe Commerce从Amazon接收&#x200B;_用户名_&#x200B;字段的方式。 以前，当&#x200B;_用户名_&#x200B;字段包含特殊字符时，订单创建过程中出错。 Adobe Commerce现在接收&#x200B;_用户名_&#x200B;数据并过滤掉特殊字符，以便成功创建订单。

## v4.4.0

*2021年4月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)已添加对配置的只读模式的支持。 查看[销售渠道设置](sales-channel-settings.md)。

![修复](../assets/fix.svg)更改了数据流，以便同一实例的多个副本可以同时获取更新。

![修复](../assets/fix.svg)更改了同步帐户信息的同步过程。 添加了cron作业以与远程帐户同步，并在CLI命令中添加了相同的功能。

![Fix](../assets/fix.svg)添加了CLI命令参数和标志，以便更精确地控制。

![修复](../assets/fix.svg)更正了系统配置中的后台任务(cron) Source。

![修复](../assets/fix.svg)修复了将国家/地区代码设置为波多黎各(PR)时阻止创建订单的问题。

## v4.3.0

*2021年3月3日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![修复](../assets/fix.svg) <!--CHAN-xxxx--> _订单详细信息_&#x200B;功能已重新设计，不再依赖于&#x200B;_导入订单_&#x200B;设置。 现在，所有订单的订单详细信息均显示在AmazonSales Channel界面中。

![修复](../assets/fix.svg)在管理员的&#x200B;_[!UICONTROL Marketing]_菜单中，名称已从_[!UICONTROL Amazon]_&#x200B;更改为&#x200B;_[!UICONTROL Amazon Sales Channel]_。

![已知问题](../assets/bug.svg) **重要信息**：在Adobe Commerce 2.4.1版本中解决了与Adobe Commerce 2.4.0兼容的已知问题。

- Amazon cron进程处于`error`状态
- 在数据库中创建存储时，使用Commerce 2.4.0安装失败
- 安装MSI后，创建产品失败

## v4.2.0

*2021年3月3日*

[!BADGE 支持]{type=Informative tooltip="支持"}

如果您安装了以前的[!DNL Amazon sales channel]版本，并尝试将Adobe Commerce更新到2.4.0版本，则在完成Adobe Commerce更新之前，系统会提示您更新扩展。

![已知问题](../assets/bug.svg)当[!DNL Amazon sales channel] 4.2.0与版本2.4.0集成并且启用了[Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en)时，有一个已知问题阻止在您的Commerce目录中添加产品。 此问题将在未来的Commerce版本中解决。

![New](../assets/new.svg) [!DNL Amazon sales channel]已得到增强，可以接受基于文本的地址数据，并将其与标准化地址格式匹配，包括城市、州和邮政编码。 此更新使订单和装运数据能够与Amazon同步（同步），且不会出现地址错误。<br/>例如，购物者输入城市、省/市/自治区、邮政编码为`Escondido, californiA 92025-1501`。 AmazonSales Channel以`Escondido, CA 92025`的形式导入数据并将其与标准格式匹配，然后以这种标准化格式将数据同步回Amazon。

![新](../assets/new.svg)添加了对PHP 7.4的支持。

![新](../assets/new.svg) <!--CHAN-4334-->已添加对Adobe Commerce 2.4.x的支持。以前的版本可能与Commerce 2.4.x兼容，但不受支持。 有关版本兼容性，请参阅[即将发布的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html)。 必须先将AmazonSales Channel更新到4.2.0，然后才能完成Adobe Commerce 2.4.0更新。

![修复](../assets/fix.svg) <!--CHAN-4431-->更正了导致UK客户出现&#x200B;_访问被拒绝_&#x200B;错误的问题。

![修复](../assets/fix.svg) <!--CHAN-4394-->修复了阻止Amazon配送状态同步到相应Commerce订单的问题，从而在Commerce中将订单的配送状态“锁定”为`Pending`，在Amazon中锁定为`Unshipped`。 通过新的标准化地址功能，这些运送状态错误已得到解决。

![修复](../assets/fix.svg) <!--ticket#-->更新了订单同步（同步）以忽略失败的订单导入，从而减少了多次同步尝试并允许后续导入，每五分钟提交一次订单同步请求。 同步错误仍记录在错误日志中，但会标记为“已处理”以允许执行进一步的记录功能。 此外，[!DNL Amazon sales channel]现在会自动删除为无法在Commerce中创建的订单收集的超额数据。

![修复](../assets/fix.svg)更新了错误日志记录以收集有关未捕获的异常和扩展更新错误的更多信息。

![修复](../assets/fix.svg) <!--ticket#-->更正了由于缺少&#x200B;_price_&#x200B;值而导致&#x200B;_最低价格_&#x200B;数据的初始同步失败的问题。

![修复](../assets/fix.svg) <!--CHAN-4410-->修复了日期范围字段留空时导致&#x200B;_Amazon订单_&#x200B;视图出现过滤错误的问题。

![修复](../assets/fix.svg) <!--CHAN-4439-->更正了导致与数量相关的库存和履行同步错误的问题。 现在，该扩展在与Amazon同步之前，对以小数形式输入的数量值进行四舍五入。<br/>例如，当商家手动输入数量`2.5`时，扩展程序会将该值舍入为`2`，然后将更新的数量与Amazon同步。

## v4.1.0

*2020年5月7日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新建](../assets/new.svg) <!--4247, 4230-->已更改订单导入流程以符合Commerce订单要求。 这些更改纠正了阻止Commerce为导入的订单创建相应订单的问题。 有关订单阻止程序和解决方案的信息，请参阅[管理订单](managing-orders.md)。

![新](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->更新了商店仪表板的&#x200B;_最近订单_&#x200B;部分，并添加了一个新的&#x200B;_所有订单_&#x200B;视图，该视图显示了您的所有Amazon订单，包括筛选选项和用于查看更多订单的分页。 查看[Amazon商店信息板](amazon-store-dashboard.md)和[查看Amazon订单](amazon-orders-all.md)。

![New](../assets/new.svg)已在&#x200B;_[!UICONTROL Recent Orders]_和_[!UICONTROL All Orders]_&#x200B;视图中添加重新设计的&#x200B;_[!UICONTROL Amazon Orders]_表的_[!UICONTROL Order Notes]_&#x200B;列。 _[!UICONTROL Order Notes]_告知商家订单导入存在问题。 请参阅[查看Amazon订单](amazon-orders-all.md)。

![新建](../assets/new.svg) <!--CHAN-4013-->已更新产品条件参数以符合[Amazon已续订](https://sell.amazon.com/programs/renewed)计划。 查看[续订的产品](renewed-products.md)。

![新](../assets/new.svg) <!--CHAN-3680-->已更新[Amazon订单详细信息](amazon-order-details.md)以包含Amazon所履行的订单的“通用数据”。 查看[履行者](fulfilled-by.md)。

![修复](../assets/fix.svg) <!--CHAN-4069-->更正了导致商店信息卡上的图标失真的问题。

![修复](../assets/fix.svg) <!--CHAN-4165-->更正了一个错误，该错误导致会话超时后无法显示&#x200B;_登录_&#x200B;屏幕。

![修复](../assets/fix.svg) <!--CHAN-4211-->修复了导致Amazon订单税额无法导入到新的Commerce订单中的问题。

![修复](../assets/fix.svg) <!--CHAN-4234-->更正了导致商店仪表板中显示的收入总数包含`Canceled`或`Error`状态的订单的问题。

![修复](../assets/fix.svg) <!--CHAN-4326-->修复了导致订单导入错误的问题，该错误与使用&#x200B;_Magento Shipping_&#x200B;方法创建订单的第三方扩展相关联。

![修复](../assets/fix.svg) <!--CHAN-4357-->更正了在运行cron同步时导致错误的问题。 在CLI命令中添加了锁，以防止两个cron作业同时同步。

![修复](../assets/fix.svg)更新了内容安全策略，以支持Commerce版本2.3.5。

## v4.0.0

*2020年3月25日*

[!BADGE 支持]{type=Informative tooltip="支持"}

>[!IMPORTANT]
>
>Amazon 2.3.5不支持Adobe CommerceSales Channel4.0.0。要获取有关Adobe Commerce 2.3.5的支持，请升级到AmazonSales Channel4.1.0。

![新](../assets/new.svg)引入了新的[AmazonSales Channel](amazon-sales-channel-home.md)主页，该主页改进了您商店信息的“卡片视图”。

![新](../assets/new.svg)推出了新的[商店仪表板](amazon-store-dashboard.md)，其中包含列表、最新订单和商店设置信息。

![新](../assets/new.svg)引入了更简单、简化的[登录流程](amazon-onboarding-home.md)和[默认商店设置](default-store-settings.md)，以更快地集成您的商店。

![已知问题](../assets/bug.svg) <!--CHAN-4102-->当[创建属性](managing-attributes.md)以便从列表导入图像且&#x200B;**商店视图**&#x200B;设置为`All Store Views (Global)`时，存在一个已知问题，导致无法将图像导入到所有商店视图。 如果将&#x200B;**存储视图（用于将值导入）**&#x200B;的设置更改为特定存储，则图像将为该存储导入。

## v3.0.1

*2019年11月11日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![修复](../assets/fix.svg) **数字字段设置**： <!--CHAN-3779-->需要基于数字的值的字段已更新为仅接受数字字符。 实例：定价规则设置>调整金额字段

![修复](../assets/fix.svg) **用户指南链接**： <!--CHAN-3778-->不正确的&#x200B;_用户指南_&#x200B;链接已更正。

![修复](../assets/fix.svg) **重复的Amazon列表**： <!--CHAN-3593-->现在已更正以前报告的问题，该问题会导致重复的Amazon列表。 在此版本之前，扩展在导入列表时向SKU值中添加了Amazon区域的国家代码。 该列表与目录项目匹配，但扩展创建了一个带有附加SKU的新重复列表。 在此版本中，扩展不会修改导入列表的SKU，并且不会对现有列表进行更改。 您可以使用Amazon上的[!UICONTROL End Listing(s)]选项删除重复列表。

## v3.0.0

*2019年10月7日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg) **Amazon UK Marketplace现已推出**：用户在创建和集成Commerce商店时，可以选择英国Marketplace。 此英国升级包括对以下各项的额外支持：

- [Amazon VAT计算服务](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}信息。

![新](../assets/new.svg) **改进的日志记录**： <!--CHAN-3642, 3672-->实现了&#x200B;**启用调试日志记录**&#x200B;功能，以便在需要故障排除时收集额外的同步数据。 请参阅配置参考中的[Sales Channel设置](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html)主题。

![修复](../assets/fix.svg) **产品目录**： <!--CHAN-3687-->修复了导致使用Amazon列表导入的图像无法应用于相应Commerce目录产品的问题。

![修复](../assets/fix.svg) **订单创建**： <!--CHAN-3708-->修复了Commerce无法为与Commerce目录产品不匹配的Amazon订单创建订单的问题。

![已知问题](../assets/bug.svg) **重复的Amazon列表**： <!--CHAN-3593-->此问题导致目录使用相同的SKU为导入列表创建项目，但末尾添加了区域代码。 然后，Amazon将修改的SKU处理为新项目并创建列表。 此问题将在未来版本中解决。

## v2.0.0

[!BADGE 支持]{type=Informative tooltip="支持"}

>[!NOTE]
>
>版本1.0.0仅在限量发行版中提供。

![新](../assets/new.svg) **简化的入门和维护**：通过包含管理员提供的详细说明的分步过程添加并与您的Amazon销售方帐户集成。 通过一个仪表板维护您的商店、帐户和列出的产品。

![新建](../assets/new.svg) **多个帐户支持**：通过管理员管理和监控多个Amazon品牌和市场区域。

![新](../assets/new.svg) **智能定价**：设置自动重新定价规则以提高您获得所渴望Buy Box的机会。 设置价格以动态调整为当前Buy Box价格或最低竞争者定价。 设置重新定价的限制以保护您的利润。

![新](../assets/new.svg) **列表管理**：使用列表规则自动列出产品并将您的Commerce目录同步到Amazon Marketplace。 添加特定覆盖以精细地控制您的产品/服务。 直接从管理员监视和管理所有列表。

![新](../assets/new.svg) **一致的Inventory management**：保持您的Commerce和Amazon库存数量恒常同步。

![新](../assets/new.svg) **订单和履行管理**：通过信息板跟踪Amazon订单，以及无缝通信和库存更新。 完成并跟踪由Amazon履行的订单发运、已履行的商家发运或方法的组合。

![已知问题](../assets/bug.svg)您可能会遇到更新产品数量的等待时间较长的问题。 产品数量的更新可能需要约2小时才能同步。

![已知问题](../assets/bug.svg)导入的订单可能具有&#x200B;_Prime_&#x200B;或&#x200B;_Premium_&#x200B;订单类型。 您应在Amazon卖方帐户中验证这些订单。

![已知问题](../assets/bug.svg)不符合条件的捆绑产品可能会显示为符合在Amazon上列出的条件。 捆绑产品中的某个产品可能不符合条件。 如果您遇到问题，请检查捆绑产品项目的资格状态。

![已知问题](../assets/bug.svg)在使用Inventory management for Commerce 2.3.x时，创建订单时不会触发部分股票重新索引。 可销售数量每小时重新计算一次，这可能会导致在此更新间隔内过度销售。
