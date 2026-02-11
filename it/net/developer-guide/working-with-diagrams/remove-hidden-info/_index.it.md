---
title: Rimuovi informazioni nascoste
type: docs
weight: 50
url: /it/net/remove-hidden-info/
description: Questa sezione spiega come rimuovere le informazioni inutilizzate o nascoste da uno diagram con Aspose.Diagram.
---
## **Rimuovi informazioni nascoste**
 Aspose.Diagram for .NET API consente agli sviluppatori di rimuovere le informazioni nascoste da un diagram. Per rimuovere le informazioni nascoste, puoi utilizzare**RimuoviHiddenInfoItem** proprietà in**RimuoviInformazioni Nascoste()**metodo della classe Diagram. L'esempio di codice seguente mostra come rimuovere le informazioni nascoste da diagram.


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

