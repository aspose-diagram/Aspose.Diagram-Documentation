---
title: Définition des options d'impression
type: docs
weight: 10
url: /fr/net/setting-print-options/
description: Cette section explique comment définir les options d'impression avec Aspose.Diagram.
---
{{% alert color="primary" %}}

Parfois, il est nécessaire de configurer les paramètres de mise en page pour les pages afin de contrôler l'impression. Ces paramètres de configuration de page offrent diverses options.

{{% /alert %}}

## **Définition des options d'impression**

Les options de configuration de page sont entièrement prises en charge dans Aspose.Diagram. Cet article explique comment définir les options de page avec Aspose.Diagram et montre des exemples de code pour la configuration :

 Aspose.Diagram fournit une classe,[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , qui représente un fichier Microsoft Visio. La[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) classe contient un[**pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection qui permet d'accéder à chaque page du fichier Visio. Une page est représentée par le[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page)classer.

 La[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la classe fournit la[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propriété utilisée pour définir les options de mise en page de la page. En fait, cela[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) la propriété est un objet de la[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) classe utilisée pour définir différentes options de mise en page pour une page imprimée. La[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)La classe fournit diverses propriétés utilisées pour définir les options de mise en page. Certaines de ces propriétés sont décrites ci-dessous.

### **Orientation de la page d'impression**

 L'orientation de la page d'impression peut être réglée sur portrait ou paysage à l'aide de la[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) classer'[**ImprimerPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) propriété. La[**ImprimerPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) propriété accepte l'une des valeurs prédéfinies dans le[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)énumération ci-dessous.

|**Types d'orientation de la page d'impression**|**La description**|
|:- |:- |
|Identiqueàl'imprimante|Identique à l'orientation de l'imprimante|
|Paysage|Orientation paysage|
|Portrait|Orientation portrait|


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}


### **Facteur d'échelle**

 Il est possible de réduire ou d'agrandir la taille d'une page en ajustant le facteur d'échelle avec la[**ÉchelleX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)propriété.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}

