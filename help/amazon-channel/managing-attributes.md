---
title: 管理Amazon列表的属性
description: 您可以管理Commerce产品属性到Amazon属性的映射，以确保系统之间的产品信息准确无误。
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 管理Amazon列表的属性

Amazon和[!DNL Commerce]都使用用于定义产品的产品属性系统（称为属性）。 属性定义了产品的描述、内容、图像、价格以及各种数据。

Commerce与Amazon之间的成功通信要求[!DNL Commerce]属性正确映射（或匹配）到相应的Amazon属性。 与Amazon集成时，您可以将这些属性映射到Amazon属性。 完成后，[!DNL Commerce]可以将您的Amazon列表与您的[!DNL Commerce]产品目录同步并进行维护。

例如，假设您的[!DNL Commerce]目录和Amazon列表中具有相同的项目。 产品的一个属性可能是物料的列表价格。 [!DNL Commerce]中挂牌价的名称可能名为`Price`，而Amazon的挂牌价可能名为`ListingPrice`。 您必须指示[!DNL Commerce]在与Amazon通信时，名为`Price`的[!DNL Commerce]属性与名为`ListingPrice`的Amazon属性相同。 此过程称为&#x200B;_管理属性_，包括创建新属性和编辑现有属性。 确保属性正确匹配可确保[!DNL Commerce]与Amazon之间的通信正确。

设置属性映射后，[!DNL Commerce]可以与Amazon来回传递产品信息。 如果您有Amazon产品清单，则[!DNL Commerce]可以将您的Amazon产品和详细信息导入您的[!DNL Commerce]目录，从而允许您从单一集中式产品目录管理Amazon清单。

Amazon sales channel允许您根据需要在Amazon sales channel主页上的&#x200B;[_[!UICONTROL Attributes]_视图](./attributes-view.md)中访问、查看、创建和管理属性。 如果向[!DNL Commerce]目录添加属性，则可能需要更新所有产品中的这些值。

有关[!DNL Commerce]和Amazon属性集及值的详细信息，请参阅：

- [管理属性基础知识](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [创建属性](./creating-attributes.md#create-an-attribute)
- [编辑现有属性](./creating-attributes.md#edit-an-attribute)
- [查看属性映射](./amazon-matching-attributes-values.md)
- [编辑或创建属性映射](./amazon-manually-update-incomplete-listing.md)
