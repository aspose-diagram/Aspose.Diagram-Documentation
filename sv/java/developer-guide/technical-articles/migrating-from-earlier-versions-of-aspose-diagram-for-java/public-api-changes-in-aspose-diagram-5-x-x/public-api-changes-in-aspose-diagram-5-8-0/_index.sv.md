---
title: Offentlig API Ändringar i Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /sv/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.7.0 till 5.8.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **SaveToolBar Option läggs till i HTMLSaveOptions**
Det nya alternativet SaveToolBar har lagts till i klassen HTMLSaveOptions. Den anger om verktygsfältet ska sparas eller inte. Standardvärdet är sant. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX Sparningsalternativ läggs till i SaveFileFormat**
Tidigare stödde Aspose.Diagram API läsning av formatet VSDX, men nu har vi lagt till stöd för att skriva diagram i formatet VSDX. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Gruppmetoden har lagts till i ShapeCollection-klassen**
Utvecklare kan nu gruppera flera former tillsammans i Visio diagram med Aspose.Diagram API. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
