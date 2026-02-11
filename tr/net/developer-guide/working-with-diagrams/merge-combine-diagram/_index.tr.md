---
title: Birleştir Birleştir Diagram
type: docs
weight: 30
url: /tr/net/merge-combine-diagram/
description: Bu bölümde visio dosyasının nasıl birleştirileceği açıklanmaktadır.
---
## **Olası Kullanım Senaryoları**

 Aspose.Diagram, iki visio dosyasını bir dosyada birleştirmenizi sağlar.
 Aspose.Diagram for .NET API'de var[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf.
Yöntemi kullanma[**birleştir**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) içinde[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) diyagramları birleştirmek için sınıf.

## **Basit kod**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(Drawing2.vsdx");
diagram2.Combine(diagram);

// Save the new Visio
newDiagram.Save(dataDir + "out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
