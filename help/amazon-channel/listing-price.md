---
title: 上市价格
description: 使用“列表价格”设置可确定您的Amazon列表的价格来源和基本（默认）价格值。
redirect_from: /sales-channels/asc/ob-listing-price.html: 
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 0%

---

# 上市价格

[!UICONTROL Listing Price] 设置是商店列表设置的一部分。可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

这些设置定义要用作价格源的[!DNL Commerce]定价属性，该价格源是您的Amazon列表的基本（默认）价格值。 这些设置由[定价规则](./pricing-rule-general-settings.md)用来根据为&#x200B;_[!UICONTROL Magento Price Source]_设置的值自动调整Amazon上市价格。

您可以将[定价范围](./price-scope.md)配置为全局或网站。 如果您的定价范围设置为`Global`，则所有商店/网站都有一个单一的价格来源。 如果您的定价范围设置为`Website`，则价格来源使用网站价格（如果可用）的回退逻辑，后跟默认（全球）价格。

如果将列表规则设置为应用于多个网站，则使用网站价格的顺序由[列表规则](./listing-rules.md)中定义的网站优先级设置决定。 利用这些规则，可定义整个目录的产品定价。 要查看您是否在使用网站价格范围，请参阅[目录价格范围](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}。

_[!UICONTROL Magento Price Source]_、_[!UICONTROL Minimum Advertised Price (Map)]_&#x200B;和&#x200B;_[!UICONTROL Strike Through Price (MSRP)]_中列出的选项包括您配置的定价属性。 定价属性是[!DNL Commerce]产品属性，其“商店所有者”的“目录输入类型”值设置为`Price`。 请参阅[属性输入类型](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}。

## 配置列表价格设置 {#configure-listing-price-settings}

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Listing Price]_部分。

1. 对于&#x200B;**[!UICONTROL Magento Price Source]**（必需），选择一个选项。

   默认值为`Price`。 此设置可确定用于Amazon列表的价格源。 如果创建[定价规则](./pricing-products.md)，则规则将应用于为此处选择的属性定义的值。 您可以选择任何已配置的定价属性。 但是，如果未为产品填写选定属性，则当应用定价规则确定已发布的Amazon上市价格时，产品的价格来源将默认回`Price`。

1. 对于**[!UICONTROL Minimum Advertised Price (MAP)**]，选择一个选项。

   默认为无选择。 此设置为产品启用最低广告价格(MAP)。 当您定义定价属性，并且产品的上市价格低于您确定的最低价格（基于您的定价来源和规则）时，此值将成为上市的MAP。 此设置允许您实施[定价规则](./pricing-products.md)，同时仍控制产品的最低价格。 要防止上市价格过低，请选择要用作MAP的定价属性。 但是，如果未为产品定义选定的定价字段，则不会使用MAP。

1. 对于&#x200B;**[!UICONTROL Strike Through Price (MSRP)]**，选择一个选项。

   默认为无选择。 此设置确定哪个定价属性用作制造商建议的产品零售价(MSRP)。 如果您的上市价格低于定义的MSRP，则您的Amazon上市将显示MSRP价格的点进，并且上市价格较低，以及计算的“您节省”金额和百分比。 但是，如果未为产品定义所选定价字段，则不计算MSRP。

   >[!NOTE]
   >
   >此设置仅适用于已获得[Buy Box](./buy-box-competitor-pricing.md)位置的列表。 该Buy Box由Amazon授予产品以最佳价格上市的销售者，以及FBA/Prime送货、供货情况和销售者业绩等其他因素。

1. 对于&#x200B;**应用增值税(VAT)**，选择一个选项：

   - `Disabled`  — （默认）选择您不希望将增值税应用于列表价格的时间。

   - `Enabled`  — 选择何时要将增值税应用到清单价格。增值税通常用作欧洲国家/地区的销售税，并添加到您在Amazon的最终上市价格中。 增值税不适用于智能定价规则内使用的列表的最终价格，除非点击[底价](./floor-price.md)。
   >[!NOTE]
   >
   >欧盟(EU)的企业需要向企业购买者发送发票，以便客户可以汇税。 您可以自行生成这些发票并计算税金，也可以使用税务计算服务，如Amazon的增值税计算服务。 Amazon建议注册[Amazon VAT计算服务](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}。 如果您选择其他方法，则需负责增值税合规性。>
   >
   >Amazon可能需要10-14天才能验证和激活您的增值税计算服务帐户。

1. 对于&#x200B;**[!UICONTROL VAT Percentage]**，输入增值税税率的值。

   默认值为`0.00`。 此值用于计算要添加到上市价格的增值税额。 如果输入了`10.2`，则对您的上市价格应用10.20%的增值税。 将“应用增值税(VAT)”字段设置为`Disabled`时，会禁用此字段。

1. **（仅限英国商店）** 对于 **[!UICONTROL Amazon Product Tax Code (PTC)]**，选择一个选项：

   - `Do Not Manage PTC`  — （默认）选择您是使用第三方计税服务，还是已在帐户中设置所有计 [!DNL Amazon Seller Central] 税。选择后，Amazon销售渠道不会向您的[!DNL Amazon Seller Central]帐户发送产品税码信息。

   - `Set Default PTC`  — 选择是否具有要用于所有产品的通用产品税码(PTC)。选择后，必须完成&#x200B;_[!UICONTROL Default PTC]_。

      - 对于&#x200B;**[!UICONTROL Default PTC]**，输入要用于所有符合条件的Amazon列表的默认PTC。 如果在[!DNL Amazon Seller Central]帐户中设置了默认PTC，请将此字段留空。 对此字段所做的更改不会影响现有的Amazon列表。 要更改现有列表的“默认PTC”，该列表必须是[ended](./end-listings-manually.md)，并且已创建新列表。
   >[!NOTE]
   >
   >如果您使用Amazon的增值税计算服务，则必须知道产品的税种。 PTC是Amazon在欧盟为B2B购买的税类ID代码。 请参阅[Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}。

1. 对于&#x200B;**[!UICONTROL Currency Conversion]**，选择一个选项。

   默认值为`Disabled`。 这些选项取决于您的[!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}设置。 如果没有可用的选项，请设置您的货币设置。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![上市价格](assets/amazon-listing-price.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Magento Price Source] | 确定创建Amazon列表时使用的价格源。 默认值为`Price`。 如果选择其他属性，如`Amazon Price`或`Special Price`，则该属性的定义值将用于Amazon列表。 但是，如果未定义选定的属性，则使用`Price`。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | MAP定价的[!DNL Commerce]属性。 选择MAP选项会在上市价格低于MAP价格时，将您的Amazon列表自动设置为MAP价格。 |
| [!UICONTROL Strike Through Price (MSRP)] | 表示MSRP定价的[!DNL Commerce]属性。 如果您的Amazon上市价格低于MSRP，则会显示MSRP价格和上市价格的一次执行。 此设置还用于计算“您保存”数量和百分比，但此功能仅适用于已获得[Buy Box](./buy-box-competitor-pricing.md)位置的列表。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | 增值税由欧盟的销售者使用。<br><br>选 `Disabled` 择是否不想在列价中添加增值税。<br><br>选择 `Enabled` ，然后输入增值税百分比，以将增值税应用于列表价格。 |
| [!UICONTROL VAT Percentage] | 定义用于计算要添加到Amazon列表的列价中的增值税金额的百分比。 <br><br>如果输入 `5`，则在应用所有定价规则后，最终上市价格将应用5%的增值税。增值税不适用于智能定价规则内使用的清单的最终价格，除非点击了[floor](./floor-price.md)或[ceiling](./optional-ceiling-price.md)。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （仅对英国商店显示）确定Amazon销售渠道是否将产品税码信息发送到您的[!DNL Amazon Seller Central]帐户。 <br><br>如果 **您使用第三** 方计税服务或已在帐户中设置所有计税，请选择“不管理PTC” [!DNL Amazon Seller Central] 。设置为此选项后，Amazon销售渠道不会向您的[!DNL Amazon Seller Central]帐户发送产品税码信息。<br><br>如果 **您有要用** 于所有产品的通用产品税代码，请选择“设置默认PTC”。<br><br>请参 [阅Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}。 |
| [!UICONTROL Default PTC] | 仅当&#x200B;**Amazon产品税码(PTC)**&#x200B;设置为`Set Default PTC`时才显示。 输入将用于所有符合条件的Amazon列表的默认PTC。 如果在[!DNL Amazon Seller Central]帐户中设置了默认PTC，请将此字段留空。 <br><br>对此字段所做的更改不会影响现有的列表。该列表必须为[ended](./end-listings-manually.md)，并且为使更改生效而创建的新列表。 |
| [!UICONTROL Currency Conversion] | 允许[!DNL Commerce]店面默认货币准确换算为默认的Amazon货币，以正确的货币发布列表价格。 货币换算始终基于您的[!DNL Commerce]默认货币。<br><br>当其他货币可用时，您仍 [!DNL Commerce] 可以查看默认货币和Amazon货币。如果默认的[!DNL Commerce]货币与默认的Amazon货币匹配，请将“货币兑换”保留为禁用状态。<br><br>例如，如果您的默 [!DNL Commerce] 认货币为CAD（加元），而Amazon的默认货币为USD，则必须启用“货币换算”并选择“CAD至USD的换算率”。提供的选项基于内置的[!DNL Commerce]货币换算。 如果您没有看到要查找的选项，请[在 [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}中设置货币。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
