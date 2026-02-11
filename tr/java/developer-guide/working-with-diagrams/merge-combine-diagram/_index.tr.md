---
title: Birleştir Birleştir Diagram
type: docs
weight: 30
url: /tr/java/merge-combine-diagram/
description: Bu bölümde visio dosyasının nasıl birleştirileceği açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

 Aspose.Diagram, iki visio dosyasını bir dosyada birleştirmenizi sağlar.
 Aspose.Diagram for Java API'de var[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) Visio çizimini temsil eden sınıf.
Yöntemi kullanma[**birleştir**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) içinde[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) diyagramları birleştirmek için sınıf.

## **Basit kod**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CombineDiagram.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(dataDir + Drawing2.vsdx");

diagram2.combine(diagram);

// save in the VSDX format
diagram.save(dataDir + "CombineDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
