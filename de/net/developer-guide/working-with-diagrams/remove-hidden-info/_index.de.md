---
title: Versteckte Informationen entfernen
type: docs
weight: 50
url: /de/net/remove-hidden-info/
description: In diesem Abschnitt wird erläutert, wie Sie unbenutzte oder versteckte Informationen aus einer diagram mit Aspose.Diagram entfernen.
---
## **Versteckte Informationen entfernen**
 Aspose.Diagram for .NET API ermöglicht es Entwicklern, versteckte Informationen aus einer diagram zu entfernen. Um versteckte Informationen zu entfernen, können Sie verwenden**RemoveHiddenInfoItem** Eigenschaften hinein**RemoveHiddenInformation()**Methode der Klasse Diagram. Das folgende Codebeispiel zeigt, wie man versteckte Informationen aus diagram entfernt.


{{< highlight csharp >}}
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

