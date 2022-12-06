---
title: Définition des marges
type: docs
weight: 20
url: /fr/net/setting-margins/
description: Cette section explique comment définir les options de page de visio avec Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram prend entièrement en charge les options de configuration de page de Microsoft Visio. Les développeurs peuvent avoir besoin de configurer les paramètres de mise en page pour les pages afin de contrôler le processus d'impression. Cette rubrique explique comment utiliser Aspose.Diagram pour configurer les marges de page.

{{% /alert %}}

## **Définition des marges**

 Aspose.Diagram fournit une classe,[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , qui représente un fichier Microsoft Visio. La[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) classe contient un[**pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection qui permet d'accéder à chaque page du fichier Visio. Une page est représentée par le[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page)classer.

 La[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la classe fournit la[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propriété utilisée pour définir les options de mise en page de la page. En fait, cela[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) la propriété est un objet de la[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) classe utilisée pour définir différentes options de mise en page pour une page imprimée. La[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)La classe fournit diverses propriétés utilisées pour définir les options de mise en page. Certaines de ces propriétés sont décrites ci-dessous.

### **Marges de page**

 Définissez les marges de page (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) à l'aide de[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)membres de la classe. Quelques-unes des méthodes sont répertoriées ci-dessous qui sont utilisées pour spécifier les marges de page :

- [**Marge du haut de la page**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageMargin-SetPageMargin.cs" >}}