---
title: 管理属性
description: 您可以管理商务产品属性到Amazon属性的映射，以确保系统之间有准确的产品信息。
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 管理属性

Amazon和[!DNL Commerce]都使用产品属性系统（称为属性）来定义产品。 属性可定义产品的描述、内容、图像、价格和各种数据。

商务与Amazon之间的成功通信要求将[!DNL Commerce]属性正确映射（或匹配）到相应的Amazon属性。 与Amazon集成时，您需要将这些属性映射到Amazon属性。 完成后，[!DNL Commerce]可以使用[!DNL Commerce]产品目录同步和维护Amazon列表。

例如，假设您的[!DNL Commerce]目录和Amazon列表中有相同的项目。 产品的一个属性可能是项目的列表价格。 [!DNL Commerce]中的上市价格名称可能名为`Price`，而Amazon的上市价格可能名为`ListingPrice`。 您必须指示[!DNL Commerce]在与Amazon通信时，名为`Price`的[!DNL Commerce]属性与名为`ListingPrice`的Amazon属性相同。 此过程称为&#x200B;_管理属性_，包括创建新属性和编辑现有属性。 确保属性正确匹配可确保[!DNL Commerce]和Amazon之间进行正确通信。

设置属性映射后，[!DNL Commerce]可以与Amazon来回传产品信息。 如果您有Amazon产品清单，[!DNL Commerce]可以将您的Amazon产品和详细信息导入[!DNL Commerce]目录中，从而允许您从单个中央产品目录管理Amazon清单。

Amazon销售渠道允许您根据需要在Amazon销售渠道主页的&#x200B;[_[!UICONTROL Attributes]_视图](./attributes-view.md)中访问、查看、创建和管理属性。 如果向[!DNL Commerce]目录添加属性，则可能需要更新所有产品中的这些值。

有关[!DNL Commerce]和Amazon属性集和值的详细信息，请参阅：

- [管理属性基础知识](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [创建属性](./creating-attributes.md#create-an-attribute)
- [编辑现有属性](./creating-attributes.md#edit-an-attribute)
- [查看属性映射](./amazon-matching-attributes-values.md)
- [编辑或创建属性映射](./amazon-manually-update-incomplete-listing.md)
