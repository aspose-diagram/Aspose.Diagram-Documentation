---
title: Ändra sidstorlek
type: docs
weight: 10
url: /sv/java/change-page-size/
description: Det här avsnittet förklarar hur du ändrar sidans storlek i en visio-fil med Aspose.Diagram.
---
## **Ändra sidstorlek**

 De[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt.
 De[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) objekt representerar sidattributen, såsom sidbredd, höjd och skala. Den här egenskapen kan användas för att ändra sidstorlek.

Använd egenskapen PageProps för att ändra sidstorlek.
### **Ställ in sidstorlek Programmeringsexempel**
Följande kodbit ändrar sidstorleken från en diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

