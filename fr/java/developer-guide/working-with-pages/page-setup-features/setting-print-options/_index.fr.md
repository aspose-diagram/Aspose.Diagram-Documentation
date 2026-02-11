---
title: Définition des options d'impression
type: docs
weight: 10
url: /fr/java/setting-print-options/
description: Cette section explique comment définir les options d'impression avec Aspose.Diagram.
---
{{% alert color="primary" %}}

Parfois, il est nécessaire de configurer les paramètres de mise en page pour les pages afin de contrôler l'impression. Ces paramètres de configuration de page offrent diverses options.

{{% /alert %}}

## **Définition des options d'impression**

Les options de configuration de page sont entièrement prises en charge dans Aspose.Diagram. Cet article explique comment définir les options de page avec Aspose.Diagram et montre des exemples de code pour la configuration :

 Aspose.Diagram fournit une classe,[**Page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , qui représente un fichier Microsoft Visio. La[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe contient un[**pages**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) collection qui permet d'accéder à chaque page du fichier Visio. Une page est représentée par le[**Page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)classer.

 La[**Feuille de page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) la classe fournit la[**Accessoires d'impression**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) propriété utilisée pour définir les options de mise en page de la page. En fait, cela[**Accessoires d'impression**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) la propriété est un objet de la[**Feuille de page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) classe utilisée pour définir différentes options de mise en page pour une page imprimée. La[**Accessoires d'impression**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)La classe fournit diverses propriétés utilisées pour définir les options de mise en page. Certaines de ces propriétés sont décrites ci-dessous.

### **Orientation de la page d'impression**

 L'orientation de la page d'impression peut être réglée sur portrait ou paysage à l'aide de la[**Accessoires d'impression**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) classer'[**ImprimerPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) propriété. La[**ImprimerPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) propriété accepte l'une des valeurs prédéfinies dans le[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)énumération ci-dessous.

|**Types d'orientation de la page d'impression**|**La description**|
|:- |:- |
|Identiqueàl'imprimante|Identique à l'orientation de l'imprimante|
|Paysage|Orientation paysage|
|Portrait|Orientation portrait|


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);


// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Page page = diagram.getPages().getPage(0);

//Set PrintPageOrientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);

{{< /highlight >}}


### **Facteur d'échelle**

 Il est possible de réduire ou d'agrandir la taille d'une page en ajustant le facteur d'échelle avec la[**ÉchelleX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)propriété.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Page page = diagram.getPages().getPage(0);
//Set ScaleX and ScaleY
page.getPageSheet().getPrintProps().getScaleX().setValue( 1);
page.getPageSheet().getPrintProps().getScaleY().setValue ( 1);
{{< /highlight >}}

