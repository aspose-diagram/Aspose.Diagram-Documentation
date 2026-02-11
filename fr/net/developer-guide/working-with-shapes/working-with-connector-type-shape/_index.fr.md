---
title: Travailler avec la forme du type de connecteur
type: docs
weight: 70
url: /fr/net/working-with-connector-type-shape/
description: Cette section explique comment définir l'apparence du connecteur avec Aspose.Diagram.
---
## **Définir l'apparence de la forme du type de connecteur dans Visio**
Cette rubrique explique comment les développeurs peuvent modifier l'apparence de la forme du type de connecteur dynamique à l'aide de Aspose.Diagram for .NET.
### **Définir l'apparence du connecteur**
 La méthode SetConnectorsType exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe peut être utilisée pour définir l'apparence de la forme du type de connecteur.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme de connecteur particulière.
1. définir l'apparence de la forme.
1. enregistrer diagram
#### **Définir l'apparence du connecteur Exemple de programmation**
Utilisez le code suivant dans votre application .NET pour définir l'apparence de la forme du type de connecteur à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Sélectionnez l'option de réacheminement de la forme du connecteur**
 La propriété ConFixedCode exposée par le[Disposition](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) class peut être utilisé pour sélectionner l'option de réacheminement. La propriété Layout, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, sera utilisé.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. obtenir une page particulière.
1. obtenir une forme de connecteur particulière.
1. définir les options de réacheminement.
1. enregistrer diagram.
### **Sélectionner l'exemple de programmation de l'option de réacheminement**
Utilisez le code suivant dans votre application .NET pour sélectionner l'option de réacheminement de la forme du connecteur à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

