---
title: Supprimer les informations masquées
type: docs
weight: 50
url: /fr/net/remove-hidden-info/
description: Cette section explique comment supprimer les informations inutilisées ou masquées d'un diagram avec Aspose.Diagram.
---
## **Supprimer les informations masquées**
 Aspose.Diagram for .NET API permet aux développeurs de supprimer les informations cachées d'un diagram. Afin de supprimer les informations cachées, vous pouvez utiliser**Supprimer l'élément d'information caché** propriétés dans**Supprimer les informations cachées ()**méthode de la classe Diagram. L'exemple de code ci-dessous montre comment dessiner supprimer les informations masquées de diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();
// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Remove hidden information from diagram
diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));
// Initialize HTML save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Save the Visio diagram
diagram.Save(dataDir + "RemoveHiddenInfo_out.html", options);

{{< /highlight >}}
```
