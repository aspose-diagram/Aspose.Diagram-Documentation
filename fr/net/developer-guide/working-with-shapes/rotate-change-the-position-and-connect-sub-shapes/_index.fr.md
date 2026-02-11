---
title: Faire pivoter, modifier la position et connecter les sous-formes
type: docs
weight: 30
url: /fr/net/rotate-change-the-position-and-connect-sub-shapes/
description: Cette section explique comment faire pivoter une forme visio avec Aspose.Diagram.
---
## **Faire pivoter une forme avec un angle approprié**
 Aspose.Diagram for .NET vous permet de faire pivoter une forme à n'importe quel angle. La méthode SetAngle exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe peut être utilisée pour faire pivoter une forme à n'importe quel angle souhaité. Il prend un seul paramètre comme angle.
### **Faire pivoter un échantillon de programmation de forme**
Utilisez le code suivant dans votre application .NET pour faire pivoter une forme à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Modifier la position d'une forme**
 La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe vous permet de changer la position d'une forme. La ligne de connexion s'ajuste automatiquement lorsque la forme est déplacée vers une position différente. Les méthodes Move et MoveTo, exposées par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge la modification de la position d'une forme en tant que partie d'un groupe ou non. Les exemples de code de cet article déplacent une forme sur la page.

Le processus de déplacement d'une forme est le suivant :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Déplacer la forme vers un autre emplacement
1. Enregistrez le diagram.
### **Exemple de programmation de changement de position**
L'extrait de code ci-dessous montre comment déplacer la forme. Le code récupère une page Visio par nom et forme par ID 16, et déplace sa position.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Connecter les sous-formes des groupes**
 Cette rubrique explique comment connecter deux sous-formes de deux formes de groupe différentes dans des diagrammes Microsoft Visio à l'aide de Aspose.Diagram for .NET. La méthode ConnectShapesViaConnector exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class peut être utilisé pour connecter les formes par leurs identifiants. La méthode AddShape, exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class, peut être utilisé pour ajouter une forme.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une page particulière.
1. Ajouter une forme de connecteur dynamique à la page sélectionnée.
1. Connecter les sous-formes
### **Connecter les sous-formes Exemple de programmation**
Utilisez le code suivant dans votre application .NET pour connecter les sous-formes de deux formes de groupe différentes à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Obtenir les formes connectées à une forme particulière**
[Ajouter et connecter des formes Visio](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explique comment ajouter une forme et la connecter à d'autres formes dans les diagrammes Microsoft Visio en utilisant Aspose.Diagram for .NET. Il est également possible de trouver des formes qui sont connectées à une forme spécifique.

 La méthode ConnectedShapes exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class peut être utilisé pour obtenir les identifiants des formes connectées à une forme. La méthode GetShape, exposée par le[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, peut ensuite être utilisé pour trouver une forme par son ID.

Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Obtenez les noms de toutes les formes connectées à la forme sélectionnée.
### **Obtenir un exemple de programmation de formes**
Utilisez le code suivant dans votre application .NET pour trouver toutes les formes connectées à une forme spécifique en utilisant Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}

