---
title: Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala
type: docs
weight: 30
url: /tr/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala**
Aspose.Diagram for Java API ile geliştiriciler, Visio çiziminde bir şekil koleksiyonunu otomatik olarak aralayabilir. Bunu gerçekleştirmek için Page sınıfı, ShapeCollection ve AutoSpaceOptions parametrelerini alan autoSpaceShapes üyesini sunar. AutoSpaceOptions sınıfı, yatay ve dikey mesafelerin ayarlanmasına izin verir.
### **Sayfadaki Şekilleri Otomatik Arala**
Java çiziminin herhangi bir sayfasında bir şekiller koleksiyonunu otomatik boşluk bırakmak için Java uygulamanızda aşağıdaki kodu kullanın.

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
