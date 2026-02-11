---
title: Créer, mettre à jour, mettre en page et ajuster automatiquement les formes
type: docs
weight: 10
url: /fr/net/create-update-layout-and-auto-fit-shapes/
description: Utilisez C# Diagram API pour créer, mettre à jour et mettre en page automatiquement des formes dans des fichiers Visio en utilisant C# dans vos applications. Guide complet avec des exemples de code C#.
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

## **Formes de mise en page dans le style d'organigramme**
 Avec certains types de dessins connectés, tels que les organigrammes et les schémas de réseau, vous pouvez utiliser le**Formes de mise en page** fonctionnalité pour positionner automatiquement les formes. Le positionnement automatique est plus rapide que le déplacement manuel de chaque forme vers un nouvel emplacement.

Par exemple, si vous mettez à jour un organigramme volumineux pour inclure un nouveau processus, vous pouvez ajouter et connecter les formes qui composent le processus, puis utiliser la fonctionnalité de mise en page pour mettre automatiquement en page le dessin mis à jour.

 La méthode Layout, exposée par la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe met en page les formes et/ou redirige les connecteurs sur toutes les pages du diagram. Cette méthode accepte une[Options de mise en page](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)objet comme argument. Utilisez les différentes propriétés exposées par la classe LayoutOptions pour disposer automatiquement les formes.

L'image ci-dessous montre le diagram chargé par les extraits de code de cet article, avant l'application de la mise en page automatique. Les extraits de code montrent comment postuler[mises en page d'organigramme](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) et[arborescences compactes](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**La source diagram.**

![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_1.png)

Les extraits de code de cet article prennent la source diagram et lui appliquent plusieurs types de mise en page automatique, en enregistrant chacun dans un fichier séparé.

|<p>**Disposition des formes de bas en haut** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Disposition des formes de haut en bas** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Formes de mise en page de gauche à droite** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Formes de mise en page de droite à gauche** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Pour mettre en forme des formes dans un style d'organigramme :

1. Créez une instance de la classe Diagram.
1. Créez une instance de la classe LayoutOptions et définissez les propriétés liées au style Flowchart.
1. Appelez la méthode Layout de la classe Diagram en passant LayoutOptions.
1. Appelez la méthode Save de la classe Diagram pour écrire le dessin Visio.
### **Exemple de programmation de style organigramme**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

### **Disposition des formes dans le style d'arbre compact**
 Le style d'arborescence compacte essaie de construire une structure arborescente. Il utilise le même fichier d'entrée que le[exemple ci-dessus](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)et enregistre plusieurs styles d'arbres compacts différents.

|<p>**Arborescence compacte - vers le bas et vers la droite** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Arborescence compacte - vers le bas et vers la gauche** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Arborescence compacte - droite et bas** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Arborescence compacte - gauche et bas** </p><p>![tâche : image_autre_texte](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Pour disposer des formes dans le style d'arborescence compacte :

1.  Créer une instance de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classer.
1. Créez une instance de la classe LayoutOptions et définissez les propriétés de style d'arborescence compacte.
1. Appelez la méthode Layout de la classe Diagram en passant LayoutOptions.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier Visio.
#### **Exemple de programmation de style d'arborescence compacte**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Ajustement automatique du Visio Diagram**
 Aspose.Diagram API prend en charge l'ajustement automatique du dessin Visio. Cette opération de fonctionnalité permet d'amener des formes extérieures à l'intérieur de la limite de page Visio. Aspose.Diagram for .NET API a le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio. La[Options d'enregistrement du diagramme](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) La classe expose la propriété AutoFitPageToDrawingContent pour ajuster automatiquement le dessin Visio.

Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Créez un objet de la classe DiagramSaveOptions et transmettez le format de fichier résultant.
1. Définissez la propriété AutoFitPageToDrawingContent de l'objet DiagramSaveOptions.
1. Appelez la méthode Save de l'objet de classe Diagram et transmettez également le chemin d'accès complet au fichier et l'objet DiagramSaveOptions.
### **Exemple de programmation d'ajustement automatique**
L'exemple de code suivant montre comment ajuster automatiquement les formes dans le Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}

## **Travailler avec le projet VBA**
### **Modifier le code du module VBA dans Visio Diagram**
 Cet article montre comment modifier automatiquement un code de module VBA à l'aide de Aspose.Diagram for .NET. Nous avons ajouté[Module Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollectionVbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Projet Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReferenceVbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) et[VbaProjectReferenceCollectionVbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) Des classes. Ces classes aident à prendre le contrôle du projet VBA. Les développeurs peuvent extraire et modifier le code du module VBA.
### **Modifier l'exemple de programmation de code de module VBA**
Veuillez vérifier cet exemple de code :


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Supprimer toutes les macros du Visio Diagram**
 Aspose.Diagram for .NET permet aux développeurs de supprimer toutes les macros du Visio diagram. La propriété VbProjectData, exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe, vous permet de supprimer toutes les macros du dessin Visio.
### **Exemple de programmation de suppression de toutes les macros**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Création d'un nouveau Diagram avec VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)permet aux développeurs de créer et de travailler avec des diagrammes Microsoft Office Visio et d'incorporer des fonctionnalités dans leurs applications logicielles. Il existe d'autres façons de travailler avec les fichiers Visio, le plus souvent, Microsoft Automation. Malheureusement, cela a quelques limites. Aspose.Diagram est puissant et rapide et fonctionne indépendamment sans installation Microsoft Office.

 Cet article sur la migration montre comment utiliser en premier[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) et alors[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) pour créer un nouveau diagram et y ajouter des formes. Vous remarquerez que le code Aspose.Diagram est plus court que le code VSTO. N'hésitez pas à utiliser le code comme base pour votre propre développement et à l'améliorer pour répondre à vos besoins. VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour créer un nouveau diagram :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Créez un diagram vide.
1. Ajoutez des formes à partir des maîtres Visio (pochoirs).
1. Enregistrez le fichier sous VDX.
### **Créer un nouveau Diagram avec un exemple de programmation VSTO**
{{% alert color="primary" %}}

en utilisant Visio = Microsoft.Office.Interop.Visio ;
Importations Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Exemple:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}

## **Création d'un nouveau Diagram avec Aspose.Diagram for .NET**
En utilisant Aspose.Diagram API, les développeurs n'ont pas besoin d'installer Microsoft Office Visio sur la machine, et ils peuvent travailler indépendamment de Microsoft Office Automation.

Pour créer un nouveau diagram :

1. Créez un diagram vide.
1. Ajoutez des formes à partir des maîtres Visio (pochoirs).
1. Enregistrez le fichier sous VDX.
### **Nouveau Diagram avec Aspose.Diagram for .NET Exemple de programmation**
{{% alert color="primary" %}}

en utilisant Aspose.Diagram ;
Importations Aspose.Diagram

{{% /alert %}}

Exemple:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Mettre à jour les propriétés de la forme**
 Lorsque vous travaillez avec des diagrammes Microsoft Visio, les utilisateurs peuvent mettre à jour les attributs de forme, y compris le texte, le style, la position, la hauteur et la largeur. En tant que développeur de logiciels travaillant avec des fichiers Visio, il vous sera demandé de le faire par programmation. La bonne nouvelle est que c'est possible, soit en utilisant les mécanismes de programmation avec les fichiers Visio que fournit Microsoft, VSTO, soit en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Le sujet ci-dessous montre comment utiliser[VSTO](https://products.aspose.com/diagram/net/) et[Aspose.Diagram](https://products.aspose.com/diagram/net/) pour mettre à jour les propriétés de la forme. Les extraits de code ci-dessous montrent comment mettre à jour les propriétés de forme pour VSTO et Aspose.Diagram for .NET. N'hésitez pas à utiliser le code et à l'appliquer à votre situation particulière.
### **Mise à jour des propriétés de forme avec VSTO**
VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour mettre à jour les propriétés de la forme :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Ouvrez un fichier Visio VSD existant.
1. Trouvez la forme requise.
1. Mettez à jour les propriétés de la forme (texte, style de texte, position et taille).
1. Enregistrez le fichier sous VDX.
#### **Mise à jour des propriétés de forme avec l'exemple de programmation VSTO**
{{% alert color="primary" %}}

en utilisant Visio = Microsoft.Office.Interop.Visio ;
Importations Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Exemple:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}

### **Mise à jour des propriétés de forme avec Aspose.Diagram for .NET**
En utilisant Aspose.Diagram API, les développeurs n'ont pas besoin de Microsoft Office Visio sur la machine, et ils peuvent travailler indépendamment de Microsoft Office Automation.

Pour mettre à jour les propriétés de la forme avec Aspose.Diagram for .NET :

1. Ouvrez un fichier Visio VSD existant.
1. Trouvez la forme requise.
1. Mettez à jour les propriétés de la forme (texte, style de texte, position et taille).
1. Enregistrez le fichier sous VDX.
#### **Mise à jour des propriétés de forme avec l'exemple de programmation Aspose.Diagram for .NET**
{{% alert color="primary" %}}

en utilisant Aspose.Diagram ;
Importations Aspose.Diagram

{{% /alert %}}

**Exemple:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}

