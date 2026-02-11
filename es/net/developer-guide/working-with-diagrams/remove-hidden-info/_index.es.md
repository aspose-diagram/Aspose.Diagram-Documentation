---
title: Eliminar información oculta
type: docs
weight: 50
url: /es/net/remove-hidden-info/
description: Esta sección explica cómo eliminar información no utilizada u oculta de un diagram con Aspose.Diagram.
---
## **Eliminar información oculta**
 Aspose.Diagram for .NET API permite a los desarrolladores eliminar información oculta de un diagram. Para eliminar información oculta, puede usar**Quitar elemento de información oculta** propiedades en**Eliminar información oculta ()**método de la clase Diagram. El siguiente código de ejemplo muestra cómo dibujar eliminar información oculta de diagram.

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
