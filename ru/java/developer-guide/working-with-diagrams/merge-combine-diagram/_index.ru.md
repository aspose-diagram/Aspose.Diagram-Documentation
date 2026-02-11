---
title: Слияние Комбинат Diagram
type: docs
weight: 30
url: /ru/java/merge-combine-diagram/
description: В этом разделе объясняется, как объединить файл visio
---
## **Возможные сценарии использования**

 Aspose.Diagram позволяет объединить два файла visio в один.
 Aspose.Diagram for Java API имеет[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) класс, представляющий чертеж Visio.
Использование метода[**Объединить**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) в[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) класс для объединения диаграмм.

## **Образец кода**
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
