---
title: Rufen Sie ein ActiveX-Steuerelement von einem Shape-Objekt ab, um Eigenschaften zu ändern
type: docs
weight: 20
url: /de/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram API können Entwickler ein ActiveX-Steuerelement aus einem Visio-Shape-Objekt abrufen, um alle verfügbaren Eigenschaften festzulegen.

{{% /alert %}} 
## **Rufen Sie ein Programmierbeispiel für ActiveX-Steuerelemente ab**
[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) -Klasse bietet die getActiveXControl-Methode, mit der Entwickler ein ActiveX-Steuerelement aus einem Visio-Shape-Objekt abrufen können. Entwickler können ein ActiveX-Steuerelement in die entsprechende ActiveX-Steuerelementklasse umwandeln und dann alle verfügbaren Eigenschaften festlegen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
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
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

