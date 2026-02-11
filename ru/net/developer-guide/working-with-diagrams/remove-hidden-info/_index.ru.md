---
title: Удалить скрытую информацию
type: docs
weight: 50
url: /ru/net/remove-hidden-info/
description: В этом разделе объясняется, как удалить неиспользуемую или скрытую информацию из diagram с помощью Aspose.Diagram.
---
## **Удалить скрытую информацию**
 Aspose.Diagram for .NET API позволяет разработчикам удалять скрытую информацию из diagram. Чтобы удалить скрытую информацию, вы можете использовать**RemoveHiddenInfoItem** свойства в**УдалитьСкрытуюИнформацию()**метод класса Diagram. В приведенном ниже примере кода показано, как удалить скрытую информацию из diagram.

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
