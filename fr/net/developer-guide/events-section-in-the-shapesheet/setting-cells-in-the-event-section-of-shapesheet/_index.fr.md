---
title: Définition de cellules dans la section Événement de ShapeSheet
type: docs
weight: 10
url: /fr/net/setting-cells-in-the-event-section-of-shapesheet/
description: Gérer les propriétés d'événement des fichiers visio.
---
{{% alert color="primary" %}} 

À l'aide de Aspose.Diagram API, les développeurs peuvent définir comment une forme répond à des actions utilisateur spécifiques en écrivant des formules Visio qui gèrent automatiquement les événements. Chaque fois que l'utilisateur effectue l'une des quatre actions décrites ci-dessous, la formule dans la cellule ShapeSheet correspondante est évaluée.

- **Le texte** - Un élément d'événement qui est évalué lorsque le texte ou la composition du texte d'une forme change.
- **EventXFMod** - La position, la taille ou l'orientation de la forme sur la page est modifiée.
- **ÉvénementDblClic** - La forme est double-cliquée.
- **EventDrop** Une nouvelle instance est créée en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **ÉvénementMultiDrop** - lorsque plusieurs nouvelles instances sont créées en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **Les données** - Réservé pour une utilisation future.

{{% /alert %}} 
## **Définition des cellules d'événement**
[Événement](https://reference.aspose.com/diagram/net/aspose.diagram/event) permet aux développeurs de définir des cellules d'événement dans la feuille ShapeSheet. Cette rubrique d'aide montre comment les développeurs peuvent définir des formules dans les cellules d'événement :


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}

