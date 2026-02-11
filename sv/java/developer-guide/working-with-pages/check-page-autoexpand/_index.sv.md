---
title: Markera sidan Autoexpandera
type: docs
weight: 10
url: /sv/java/check-page-autoexpand/
description: Det här avsnittet förklarar hur du kontrollerar eller ändrar sidan automatiskt expanderas i en visio-fil med Aspose.Diagram.
---
## **Kontrollera sidan AutoExpand**

 De[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt.
 De[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) objekt representerar sidattributen, såsom sidbredd, höjd och skala. Den här egenskapen kan användas för att kontrollera sidans autoexpandering.

Använd egenskapen PageProps för att kontrollera sidans autoexpandering.
### **Kontrollera sidan AutoExpand Programmeringsexempel**
Följande del av kodkontrollsidans autoexpanderar från en diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
