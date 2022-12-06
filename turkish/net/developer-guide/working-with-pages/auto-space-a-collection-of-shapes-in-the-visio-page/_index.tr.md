---
title: Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala
type: docs
weight: 30
url: /tr/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: Bu bölüm, visio sayfasındaki bir şekil koleksiyonunun Aspose.Diagram ile nasıl otomatik boşluk bırakılacağını açıklar.
---
## **Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala**
Aspose.Diagram for .NET API ile geliştiriciler, Visio çiziminde bir şekil koleksiyonunu otomatik olarak aralayabilir. Bunu gerçekleştirmek için Page sınıfı, ShapeCollection ve AutoSpaceOptions parametrelerini alan AutoSpaceShapes üyesini sunar. AutoSpaceOptions sınıfı, yatay ve dikey mesafelerin ayarlanmasına izin verir.
### **Sayfadaki Şekilleri Otomatik Arala**
.NET çiziminin herhangi bir sayfasında bir şekiller koleksiyonunu otomatik boşluk bırakmak için .NET uygulamanızda aşağıdaki kodu kullanın.

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
