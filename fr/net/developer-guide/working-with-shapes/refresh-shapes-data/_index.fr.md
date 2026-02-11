---
title: Actualiser les données des formes
type: docs
weight: 40
url: /fr/net/refresh-shapes-data/
description: Cette section explique comment actualiser les données de la forme pour une forme visio avec Aspose.Diagram.
---
## **Actualise la position de la forme, y compris xform, connection et geom lors de la modification du texte de la forme ou d'un autre**
 La méthode RefreshData exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) la classe peut être utilisée pour actualiser les données de la forme

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Actualiser les données de la forme.
### **Actualiser les données de Shape**
Utilisez le code suivant dans votre application .NET pour actualiser une forme à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


