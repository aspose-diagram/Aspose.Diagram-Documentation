---
title: Public API Changements dans Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.8.0 à 16.11.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Modifier les propriétés d'un contrôle ActiveX**
 Les développeurs peuvent récupérer un contrôle ActiveX puis modifier ses propriétés. Nous avons ajouté la propriété ActiveXControl dans le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classer. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"C:\temp\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get a shape by ID

Shape shape = page.Shapes.GetShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;

// set width of the command button control

cbac.Width = 4;

// set height of the command button control

cbac.Height = 4;

// set caption of the command button control

cbac.Caption = "Test Button";

// save diagram

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
## **Insérez une forme de texte dans le Visio Diagram**
Les développeurs peuvent insérer une forme de texte dans le Visio diagram en utilisant Aspose.Diagram API. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

string text = "Test text";

// add text to a Visio page

diagram.Pages[0].AddText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
