---
title: Gizli Bilgileri Kaldır
type: docs
weight: 50
url: /tr/net/remove-hidden-info/
description: Bu bölüm, kullanılmayan veya gizli bilgilerin diagram ile Aspose.Diagram'den nasıl kaldırılacağını açıklar.
---
## **Gizli Bilgileri Kaldır**
 Aspose.Diagram for .NET API, geliştiricilerin bir diagram'den gizli bilgileri kaldırmasına olanak tanır. Gizli bilgileri kaldırmak için şunu kullanabilirsiniz:**Gizli Bilgi Öğesini Kaldır** özellikleri**Gizli Bilgileri Kaldır()**Diagram sınıfının yöntemi. Aşağıdaki kod örneği, diagram'den gizli bilgilerin nasıl kaldırılacağını gösterir.

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
