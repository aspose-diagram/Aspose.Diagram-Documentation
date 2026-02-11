---
title: 删除隐藏信息
type: docs
weight: 50
url: /zh/net/remove-hidden-info/
description: 本节介绍如何使用 Aspose.Diagram 从 diagram 中删除未使用或隐藏的信息。
---
## **删除隐藏信息**
 Aspose.Diagram for .NET API 允许开发人员从 diagram 中删除隐藏信息。为了删除隐藏信息，您可以使用**删除隐藏信息项**中的属性**移除隐藏信息()**Diagram 类的方法。下面的代码示例显示了如何从 diagram 中提取隐藏信息。


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

