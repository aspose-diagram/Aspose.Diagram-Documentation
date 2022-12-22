---
title: Genel API Aspose.Diagram 6.0.0'daki değişiklikler
type: docs
weight: 50
url: /tr/java/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 5.9.0'dan 6.0.0'a modül/uygulama geliştiricilerin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **Shape sınıfına isGlued Yöntemi eklendi**
isGlued yöntemi, iki şeklin yapıştırılıp yapıştırılmadığını belirlemek için bir şekil nesnesini parametre olarak alır.
Örnek kod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **isConnected Yöntemi, Shape sınıfına eklenir**
isConnected yöntemi, iki şeklin bağlantılı olup olmadığını belirlemek için bir şekil nesnesini parametre olarak alır.
Örnek kod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
