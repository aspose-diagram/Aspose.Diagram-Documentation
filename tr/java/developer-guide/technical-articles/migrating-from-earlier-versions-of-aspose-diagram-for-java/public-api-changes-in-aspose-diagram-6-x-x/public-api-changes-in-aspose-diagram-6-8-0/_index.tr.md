---
title: Genel API Aspose.Diagram 6.8.0'daki değişiklikler
type: docs
weight: 10
url: /tr/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 6.7.0'dan 6.8.0'a modül/uygulama geliştiricilerin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Bir ActiveX Denetimi Ekleme**
 Geliştiriciler, Visio diagram'e bir ActiveX denetimi ekleyebilir. AddActiveXControl yöntemini ekledik.[Sayfa](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) sınıf. Lütfen bu kod örneğini kontrol edin:

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Katmanın Renk Onay Kutusunu Ayarlayın**
Geliştiriciler, Aspose.Diagram API'i kullanarak Katmanın Renk Onay Kutusunu ayarlayabilir veya alabilir. Lütfen bu kod örneğini kontrol edin:

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
### **Shape Sınıfına InheritFill Özelliği ekler**
Geliştiriciler, fill özelliğini devralabilir veya ayarlayabilir. Shape sınıfına InheritFill özelliğini ekledik. Lütfen bu kod örneğini kontrol edin:

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
