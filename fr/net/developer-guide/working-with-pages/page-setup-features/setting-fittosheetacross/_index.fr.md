---
title: Définition de FitToSheetAcross
type: docs
weight: 10
url: /fr/net/setting-fittosheetacross/
description: Cette section explique comment définir fittosheetacross avec Aspose.Diagram.
---
{{% alert color="primary" %}}

Parfois, il est nécessaire de configurer les paramètres de mise en page pour les pages afin de contrôler l'impression. Ces paramètres de configuration de page offrent diverses options.

{{% /alert %}}

## **Définition de FitToSheetAcross**

Les options de configuration de page sont entièrement prises en charge dans Aspose.Diagram. Cet article explique comment définir les options de page avec Aspose.Diagram et montre des exemples de code pour la configuration :

 Aspose.Diagram fournit une classe,[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , qui représente un fichier Microsoft Visio. La[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) classe contient un[**pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection qui permet d'accéder à chaque page du fichier Visio. Une page est représentée par le[**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page)classer.

 La[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la classe fournit la[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propriété utilisée pour définir les options de mise en page de la page. En fait, cela[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) la propriété est un objet de la[**Feuille de page**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) classe utilisée pour définir différentes options de mise en page pour une page imprimée. La[**Accessoires d'impression**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)La classe fournit diverses propriétés utilisées pour définir les options de mise en page. Certaines de ces propriétés sont décrites ci-dessous.

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


