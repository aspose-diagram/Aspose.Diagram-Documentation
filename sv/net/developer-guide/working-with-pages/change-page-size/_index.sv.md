---
title: Ändra sidstorlek
type: docs
weight: 10
url: /sv/net/change-page-size/
description: Det här avsnittet förklarar hur du ändrar sidans storlek i en visio-fil med Aspose.Diagram.
---
## **Ändra sidstorlek**

 De[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt.
 De[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) objekt representerar sidattributen, såsom sidbredd, höjd och skala. Den här egenskapen kan användas för att ändra sidstorlek.

Använd egenskapen PageProps för att ändra sidstorlek.
### **Ställ in sidstorlek Programmeringsexempel**
Följande kodbit ändrar sidstorleken från en diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

