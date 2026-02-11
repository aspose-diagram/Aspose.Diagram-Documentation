---
title: Agregar marca de agua a Visio
type: docs
weight: 10
url: /es/java/add-watermark-to-visio/
keywords: watermark, visi
description: Cómo agregar una marca de agua a visio usando Java Diagram API.
---
## **Creando un Diagram**
 Aspose.Diagram for Java le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)para construir el diagram. Use el constructor predeterminado de[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Agregar marca de agua a visio en la página
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Agregar marca de agua Ejemplo de programación**
El siguiente código de ejemplo muestra cómo agregar una marca de agua en Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

