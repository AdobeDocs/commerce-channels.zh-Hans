---
title: Amazon销售渠道 — [!UICONTROL Listing Price]
description: 使用“列表价格”设置可确定Amazon列表的价格来源和基本（默认）价格值。
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price]设置是商店列表设置的一部分。 列表设置可从[存储仪表板](./amazon-store-dashboard.md)访问。

这些设置定义将哪个[!DNL Commerce]定价属性用作您的价格来源，它是您的Amazon列表的基底（默认）价格值。 您的[定价规则](./pricing-rule-general-settings.md)使用这些设置自动调整相对于&#x200B;_[!UICONTROL Magento Price Source]_的值集的Amazon列表价格。

您可以将[定价范围](./price-scope.md)配置为全局或网站。 如果您的定价范围设置为`Global`，则您的所有商店/网站都只有一个价格来源。 如果您的定价范围设置为`Website`，则价格来源使用网站价格的回退逻辑（如果有），后跟默认（全局）价格。

如果列表规则设置为应用于多个网站，则使用网站价格的顺序由[列表规则](./listing-rules.md)中定义的网站优先级设置确定。 利用这些规则，可在目录间定义产品定价。 要查看您是否正在使用网站价格范围，请参阅[目录价格范围](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)。

_[!UICONTROL Magento Price Source]_、_[!UICONTROL Minimum Advertised Price (Map)]_&#x200B;和&#x200B;_[!UICONTROL Strike Through Price (MSRP)]_中列出的选项包括您配置的定价属性。 定价属性是[!DNL Commerce]个产品属性，其“商店所有者的目录输入类型”值设置为`Price`。 请参阅[属性输入类型](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html)。

## 配置列表价格设置 {#configure-listing-price-settings}

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Listing Price]_部分。

1. 对于&#x200B;**[!UICONTROL Magento Price Source]** （必需），请选择一个选项。

   默认值为`Price`。 此设置确定用于Amazon清单的价格来源。 如果您创建[定价规则](./pricing-products.md)，则这些规则将应用于为此处所选属性定义的值。 您可以选择任何已配置的定价属性。 但是，如果没有为产品填写所选属性，则在应用定价规则以确定发布的Amazon上市价格时，产品的价格来源默认为`Price`。

1. 对于**[!UICONTROL Minimum Advertised Price (MAP)**]，请选择一个选项。

   缺省为无选项。 此设置允许产品的最低广告价格(MAP)。 当您定义定价属性并且产品的上市价格低于您确定的最低价格（基于您的定价来源和规则）时，此值将成为上市的MAP。 此设置允许您实施[定价规则](./pricing-products.md)，同时仍控制产品的最低价格。 要防止挂牌价格过低，请选择一个要用作MAP的定价属性。 但是，如果没有为产品定义所选定价字段，则不会使用MAP。

1. 为&#x200B;**[!UICONTROL Strike Through Price (MSRP)]**&#x200B;选择一个选项。

   缺省为无选项。 此设置确定将哪个定价属性用作产品的制造商建议零售价(MSRP)。 如果您的挂牌价格低于定义的MSRP，则显示您的Amazon列表时将使用MSRP价格的删除线（较低的挂牌价格），以及计算的“您保存”金额和百分比。 但是，如果没有为产品定义所选定价字段，则不会计算MSRP。

   >[!NOTE]
   >
   >此设置仅适用于已获得[Buy Box](./buy-box-competitor-pricing.md)职位的列表。 Buy Box由Amazon授予销售者，销售者通常以最佳价格列出产品，同时考虑其他因素，如提供的FBA/Prime运费、可用性和销售者的表现。

1. 对于&#x200B;**申请增值税**，请选择一个选项：

   - `Disabled` — （默认）选择您不希望向上市价格中应用VAT的情况。

   - `Enabled` — 选择您何时要将增值税应用于您的标价。 在欧洲国家/地区，增值税通常用作销售税，并添加到Amazon的最终上市价格中。 VAT不适用于智能定价规则中使用的列表的最终价格，除非点击[最低价格](./floor-price.md)。

   >[!NOTE]
   >
   >欧盟(EU)企业必须将发票发送给商业购买者，以便客户可以汇款。 您可以自行生成这些发票并计算税款，也可以使用计税服务(如Amazon的增值税计算服务)。 Amazon建议注册[Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;)。 如果选择其他方法，您应负责符合增值税。>
   >
   >Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

1. 对于&#x200B;**[!UICONTROL VAT Percentage]**，输入增值税率的值。

   默认值为`0.00`。 此值用于计算要添加到列表价格的增值税金额。 如果输入`10.2`，则对您的标价征收10.20%的增值税。 当“应用增值税(VAT)”字段设置为`Disabled`时，此字段被禁用。

1. **（仅限英国商店）**&#x200B;对于&#x200B;**[!UICONTROL Amazon Product Tax Code (PTC)]**，请选择一个选项：

   - `Do Not Manage PTC` — （默认）选择是使用第三方计税服务还是已在[!DNL Amazon Seller Central]帐户中设置所有计税。 选择后，Amazon销售渠道不会向您的[!DNL Amazon Seller Central]帐户发送产品税码信息。

   - `Set Default PTC` — 选择您是否具有要用于所有产品的通用产品税码(PTC)。 选择后，您必须完成&#x200B;_[!UICONTROL Default PTC]_。

      - 对于&#x200B;**[!UICONTROL Default PTC]**，输入用于所有符合条件的Amazon列表的默认PTC。 如果在您的[!DNL Amazon Seller Central]帐户中设置默认PTC，请将此字段留空。 对此字段所做的更改不会影响现有Amazon列表。 要更改现有列表的默认PTC，该列表必须为[已结束](./end-listings-manually.md)并创建一个新列表。

   >[!NOTE]
   >
   >如果您使用Amazon的增值税计算服务，则必须了解产品的税种。 PTC是Amazon在欧盟购买B2B的税类ID代码。 查看[Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}。

1. 为&#x200B;**[!UICONTROL Currency Conversion]**&#x200B;选择一个选项。

   默认值为`Disabled`。 这些选项取决于您的[!DNL Commerce] [货币](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html)设置。 如果没有可用选项，请设置您的货币设置。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![列表价格](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | 确定创建Amazon列表时使用的价格来源。 默认值为`Price`。 如果您选择其他属性，如`Amazon Price`或`Special Price`，则该属性的定义值将用于您的Amazon列表。 但是，如果未定义所选属性，则使用`Price`。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | MAP定价的[!DNL Commerce]属性。 如果选择MAP选项，则在上市价格低于MAP价格时，您的Amazon上市价格将自动设置为MAP价格。 |
| [!UICONTROL Strike Through Price (MSRP)] | 表示MSRP定价的[!DNL Commerce]属性。 如果您的Amazon上市价格低于MSRP，则会显示MSRP价格和上市价格的删除线。 此设置还用于计算“您保存”的金额和百分比，但此功能仅适用于已获得[Buy Box](./buy-box-competitor-pricing.md)职位的列表。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | 增值税由欧盟内的销售方使用。<br><br>如果不希望向标价中添加增值税，请选择`Disabled`。<br><br>选择`Enabled`，然后输入根据您的列表价格应用增值税的增值税百分比。 |
| [!UICONTROL VAT Percentage] | 定义用于计算要添加到Amazon列表价中的增值税税额的百分比。 <br><br>如果您输入`5`，则在应用所有定价规则后，最终上市价格将收取5%的增值税。 增值税不适用于智能定价规则中使用的列表的最终价格，除非点击[下限](./floor-price.md)或[上限](./optional-ceiling-price.md)。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （仅针对英国商店显示）确定Amazon销售渠道是否将产品税码信息发送到您的[!DNL Amazon Seller Central]帐户。 <br><br>如果您使用第三方计税服务或已在[!DNL Amazon Seller Central]帐户中设置所有计税服务，请选择&#x200B;**不管理PTC**。 当设置为此选项时，Amazon销售渠道不会向您的[!DNL Amazon Seller Central]帐户发送产品税码信息。如果要对所有产品使用通用产品税码，请选择<br><br>选择&#x200B;**设置默认PTC**。<br><br>查看[Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}。 |
| [!UICONTROL Default PTC] | 仅在&#x200B;**Amazon产品税码(PTC)**&#x200B;设置为`Set Default PTC`时显示。 输入要用于所有符合条件的Amazon列表的默认PTC。 如果在您的[!DNL Amazon Seller Central]帐户中设置默认PTC，请将此字段留空。 <br><br>对此字段所做的更改不会影响现有列表。 列表必须为[已结束](./end-listings-manually.md)且已创建新列表以使更改生效。 |
| [!UICONTROL Currency Conversion] | 允许您的[!DNL Commerce]店面默认货币准确地转换为默认Amazon货币，以使用正确的货币发布您的挂牌价。 货币兑换始终基于您的[!DNL Commerce]默认货币。<br><br>当其他货币可用时，您仍可以查看默认[!DNL Commerce]和Amazon货币。 如果默认[!DNL Commerce]货币与默认Amazon货币匹配，请禁用“货币换算”。<br><br>例如，如果[!DNL Commerce]的默认货币为CAD（加元），而Amazon的默认货币为USD，则必须启用“货币换算”并选择“兑换率”（CAD至USD）。 提供的选项基于内置[!DNL Commerce]货币换算。 如果没有看到您要查找的选项，请[在 [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html)中设置货币。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
