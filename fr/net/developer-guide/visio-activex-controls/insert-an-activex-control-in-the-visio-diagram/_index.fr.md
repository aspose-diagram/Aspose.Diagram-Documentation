---
title: Insérez un contrôle ActiveX dans le Visio Diagram
type: docs
weight: 10
url: /fr/net/insert-an-activex-control-in-the-visio-diagram/
description: Cette page décrit comment insérer un contrôle ActiveX avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

 Les développeurs peuvent ajouter des contrôles ActiveX directement aux dessins Microsoft Visio pour rendre le Visio diagram interactif en utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Insérer un exemple de programmation de contrôle ActiveX**
[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La classe offre la méthode AddActiveXControl et permet aux développeurs d'insérer n'importe quel type de contrôle ActiveX comme le bouton de commande, la liste déroulante, la case à cocher, la liste, la zone de texte, le bouton rotatif, le bouton radio, l'étiquette, l'image, le bouton bascule et la barre de défilement.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
