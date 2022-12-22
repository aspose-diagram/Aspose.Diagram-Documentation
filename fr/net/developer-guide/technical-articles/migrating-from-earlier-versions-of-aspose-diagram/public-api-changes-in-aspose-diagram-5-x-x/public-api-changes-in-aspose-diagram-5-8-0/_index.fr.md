---
title: Public API Changements dans Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 5.7.0 à 5.8.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **L'option SaveToolBar est ajoutée dans HTMLSaveOptions**
La nouvelle option SaveToolBar a été ajoutée dans la classe HTMLSaveOptions. Il spécifie s'il faut enregistrer la barre d'outils ou non. La valeur par défaut est true. Exemples de codes :

**C#**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.SaveToolBar = false;

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' initialize HTMLSaveOptions class object

Dim opts As New HTMLSaveOptions()

' set save toolbar option

opts.SaveToolBar = False

{{< /highlight >}}
## **VSDX L'option d'enregistrement est ajoutée dans le SaveFileFormat**
Auparavant, Aspose.Diagram API prenait en charge la lecture du format VSDX, mais nous avons maintenant ajouté la prise en charge de l'écriture de diagrammes au format VSDX. Exemples de codes :

**C#**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSDX format

diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
## **La méthode de groupe a été ajoutée dans la classe ShapeCollection**
Les développeurs peuvent désormais regrouper plusieurs formes dans le Visio diagram en utilisant Aspose.Diagram API. Exemples de codes :

**C#**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes

Aspose.Diagram.Shape[]ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array

ss[0]= diagram.Pages[0].Shapes.GetShape(1);

ss[1]= diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group

diagram.Pages[0].Shapes.Group(ss);

// save visio diagram

diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load a Visio diagram

Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes

Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array

ss(0) = diagram.Pages(0).Shapes.GetShape(1)

ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group

diagram.Pages(0).Shapes.Group(ss)

' save visio diagram

diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
