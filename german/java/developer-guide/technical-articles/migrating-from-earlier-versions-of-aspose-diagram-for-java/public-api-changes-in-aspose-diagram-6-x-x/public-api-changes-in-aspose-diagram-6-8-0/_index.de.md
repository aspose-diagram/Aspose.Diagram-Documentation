---
title: Öffentlich API Änderungen in Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /de/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.7.0 auf 6.8.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Fügen Sie ein ActiveX-Steuerelement ein**
 Entwickler können ein ActiveX-Steuerelement in die Visio diagram einfügen. Wir haben die addActiveXControl-Methode in die hinzugefügt[Buchseite](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) Klasse. Bitte überprüfen Sie dieses Codebeispiel:

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Setzen Sie das Farb-Kontrollkästchen der Ebene**
Entwickler können die Color CheckBox von Layer mit Aspose.Diagram API setzen oder abrufen. Bitte überprüfen Sie dieses Codebeispiel:

**Java**

{{< highlight "java" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Fügt die InheritFill-Eigenschaft in der Shape-Klasse hinzu**
Entwickler können die inherit fill-Eigenschaft abrufen oder festlegen. Wir haben die InheritFill-Eigenschaft in der Shape-Klasse hinzugefügt. Bitte überprüfen Sie dieses Codebeispiel:

**Java**

{{< highlight "java" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
