---
title: Public API Changements dans Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.6.0 à 6.8.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Insérer un contrôle ActiveX**
Les développeurs peuvent insérer un contrôle ActiveX dans le Visio diagram. Nous avons ajouté la méthode AddActiveXControl dans le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classer. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
## **Définir la case à cocher de couleur du calque**
Les développeurs peuvent définir ou obtenir la case à cocher Couleur du calque à l'aide de Aspose.Diagram API. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
## **Ajoute la propriété InheritFill dans la classe Shape**
Les développeurs peuvent obtenir ou définir la propriété inherit fill. Nous avons ajouté la propriété InheritFill dans la classe Shape. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
