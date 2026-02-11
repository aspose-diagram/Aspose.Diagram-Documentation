---
title: Markera sidan Autoexpandera
type: docs
weight: 10
url: /sv/net/check-page-autoexpand/
description: Det här avsnittet förklarar hur du kontrollerar eller ändrar sidan automatiskt expanderas i en visio-fil med Aspose.Diagram.
---
## **Ändra sidstorlek**

 De[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt.
 De[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) objekt representerar sidattributen, såsom sidbredd, höjd och skala. Den här egenskapen kan användas för att kontrollera sidans autoexpandering.

Använd egenskapen PageProps för att kontrollera sidans autoexpandering.
### **Ställ in sidstorlek Programmeringsexempel**
Följande del av kodkontrollsidans autoexpanderar från en diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
