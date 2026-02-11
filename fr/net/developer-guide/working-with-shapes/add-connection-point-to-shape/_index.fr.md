---
title: Ajouter un point de connexion à la forme
type: docs
weight: 70
url: /fr/net/add-connection-point-to-shape/
description: Cette section explique comment ajouter un point de connexion à une forme visio avec Aspose.Diagram.
---
## **Ajouter un point de connexion à une forme dans Visio**
Cette rubrique explique comment les développeurs peuvent ajouter un point de connexion à une forme visio à l'aide de Aspose.Diagram for .NET.
### **Ajouter un point de connexion**
 La[Connexions](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) l'objet représente la collection de connexions dans le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classer.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. nouvelle connexion
1.  définir la propriété de connexion
1. ajouter une connexion à la forme
1. enregistrer diagram
#### **Ajouter un point de connexion à la forme Exemple de programmation**
Utilisez le code suivant dans votre application .NET pour ajouter une connexion à une forme à l'aide de Aspose.Diagram for .NET.


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

