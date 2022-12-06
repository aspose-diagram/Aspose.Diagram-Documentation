---
title: Öffentlich API Änderungen in Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /de/java/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.8.0 bis 16.11.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Eigenschaften eines ActiveX-Steuerelements ändern**
 Entwickler können ein ActiveX-Steuerelement abrufen und dann seine Eigenschaften ändern. Wir haben die ActiveXControl-Eigenschaft in der hinzugefügt[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse. Bitte überprüfen Sie dieses Codebeispiel:

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
### **Fügen Sie eine Textform in die Visio Diagram ein**
Entwickler können mit Aspose.Diagram API eine Textform in Visio diagram einfügen. Bitte überprüfen Sie dieses Codebeispiel:

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
