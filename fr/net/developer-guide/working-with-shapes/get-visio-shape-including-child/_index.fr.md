---
title: Obtenir la forme Visio, y compris l'enfant
type: docs
weight: 110
url: /fr/net/get-visio-shape-including-child/
description: Cette section explique comment obtenir la forme visio, y compris l'enfant avec l'identifiant ou le nom de la forme avec Aspose.Diagram.
---
### **Récupérer une forme Visio avec enfant**
Chaque forme dans un diagram a un ID et un nom. L'ID est important lors de la programmation avec Visio : c'est la principale méthode d'accès à une forme. Chaque forme conserve également des informations sur le maître (pochoir) à partir duquel elle est fabriquée.

 UN[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) est un objet dans un dessin Visio qui a peut-être un père ou des fils. La propriété Shapes, exposée par la classe Page, prend en charge une collection d'objets Aspose.Diagram.Shape. La propriété Shapes peut être utilisée pour récupérer des informations sur une forme.
#### **Récupérer l'exemple de programmation de forme Visio**
L'extrait de code suivant récupère la forme, y compris l'enfant. Veuillez vérifier cet exemple de code :


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


