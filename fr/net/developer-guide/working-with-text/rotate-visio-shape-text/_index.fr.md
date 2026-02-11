---
title: Rotation Visio Texte de forme
type: docs
weight: 9
url: /fr/net/rotate-visio-shape-text/
keywords: Rotate, visio, Tex
description: Comment faire pivoter le texte de la forme dans visio en utilisant .NET Diagram API.
---
## **Création d'un Diagram**
 Aspose.Diagram for .NET vous permet de lire et de créer des diagrammes Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation. La première étape lors de la création de nouveaux documents consiste à créer un diagram. Ensuite[ajouter des formes et des connecteurs](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)pour construire le diagram. Utilisez le constructeur par défaut de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe pour créer un nouveau diagram.
### **Exemple de programmation**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}


Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Obtenir une page particulière
1. Obtenez une forme particulière
1. Obtenir le texte de la forme et faire pivoter le texte
1. Appelez la méthode Save de l'objet de classe Diagram et transmettez également le chemin d'accès complet au fichier et l'objet DiagramSaveOptions.
### **Faire pivoter le texte Exemple de programmation**
L'exemple de code suivant montre comment faire pivoter du texte dans le Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

