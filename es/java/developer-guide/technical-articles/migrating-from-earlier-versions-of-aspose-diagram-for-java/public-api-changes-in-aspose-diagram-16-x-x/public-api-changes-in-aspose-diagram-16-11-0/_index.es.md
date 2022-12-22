---
title: Público API Cambios en Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /es/java/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 6.8.0 a la 16.11.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **Modificar propiedades de un control ActiveX**
 Los desarrolladores pueden recuperar un control ActiveX y luego modificar sus propiedades. Hemos agregado la propiedad ActiveXControl en el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) clase. Por favor, compruebe este ejemplo de código:

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
### **Inserte una forma de texto en el Visio Diagram**
Los desarrolladores pueden insertar una forma de texto en Visio diagram usando Aspose.Diagram API. Consulte este ejemplo de código:

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
