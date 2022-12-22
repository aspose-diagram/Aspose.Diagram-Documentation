---
title: Offentlig API Ändringar i Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /sv/java/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.8.0 till 16.11.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Ändra egenskaper för en ActiveX-kontroll**
 Utvecklare kan hämta en ActiveX-kontroll och sedan ändra dess egenskaper. Vi har lagt till ActiveXControl-egenskapen i[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass. Kontrollera detta kodexempel:

**Java**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("C:\\temp\\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get a shape by ID

Shape shape = page.getShapes().getShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();

// set width of the command button control

cbac.setWidth(4);

// set height of the command button control

cbac.setHeight(4);

// set caption of the command button control

cbac.setCaption("Test Button");

// save diagram

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Infoga en textform i Visio Diagram**
Utvecklare kan infoga en textform i Visio diagram med Aspose.Diagram API. Kontrollera detta kodexempel:

**Java**

{{< highlight "java" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

String text = "Test text";

// add text to a Visio page

diagram.getPages().get(0).addText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
