---
title: Özellikleri Değiştirmek için Şekil Nesnesinden ActiveX Denetimi Alın
type: docs
weight: 20
url: /tr/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Geliştiriciler, Aspose.Diagram API'i kullanarak, mevcut tüm özelliklerini ayarlamak için bir Visio şekil nesnesinden bir ActiveX denetimi alabilir.

{{% /alert %}} 
## **Bir ActiveX Kontrol Programlama Örneği Alın**
[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, geliştiricilerin bir Visio şekil nesnesinden bir ActiveX denetimi almasına izin veren getActiveXControl yöntemini sunar. Geliştiriciler, bir ActiveX denetimini uygun ActiveX denetim sınıfında yayınlayabilir ve ardından tüm kullanılabilir özelliklerini ayarlayabilir.


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

