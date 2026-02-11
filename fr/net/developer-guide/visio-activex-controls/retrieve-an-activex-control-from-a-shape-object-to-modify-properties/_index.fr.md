---
title: Récupérer un contrôle ActiveX à partir d'un objet de forme pour modifier les propriétés
type: docs
weight: 20
url: /fr/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Modifier les propriétés d'un contrôle ActiveX avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}} 

À l'aide de Aspose.Diagram API, les développeurs peuvent récupérer un contrôle ActiveX à partir d'un objet de forme Visio pour définir toutes ses propriétés disponibles.

{{% /alert %}} 
## **Récupérer un exemple de programmation de contrôle ActiveX**
[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe offre la propriété ActiveXControl qui permet aux développeurs de récupérer un contrôle ActiveX à partir d'un objet de forme Visio. Les développeurs peuvent caster un contrôle ActiveX dans la classe de contrôle ActiveX appropriée, puis définir toutes ses propriétés disponibles.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

