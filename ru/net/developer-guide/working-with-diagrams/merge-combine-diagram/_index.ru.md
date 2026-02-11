---
title: Слияние Комбинат Diagram
type: docs
weight: 30
url: /ru/net/merge-combine-diagram/
description: В этом разделе объясняется, как объединить файл visio
---
## **Возможные сценарии использования**

 Aspose.Diagram позволяет объединить два файла visio в один.
 Aspose.Diagram for .NET API имеет[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio.
Использование метода[**Объединить**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) в[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс для объединения диаграмм.

## **Образец кода**
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
