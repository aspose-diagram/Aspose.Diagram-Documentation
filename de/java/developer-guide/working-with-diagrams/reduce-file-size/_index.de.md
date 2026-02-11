---
title: Dateigröße reduzieren
type: docs
weight: 50
url: /de/java/reduce-file-size/
description: In diesem Abschnitt wird erläutert, wie Sie die Dateigröße von diagram auf Aspose.Diagram reduzieren.
---
## **Dateigröße reduzieren**
 Aspose.Diagram for Java API ermöglicht es Entwicklern, versteckte Informationen aus einer diagram zu entfernen, um die Dateigröße zu reduzieren.
 Das[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Um die Dateigröße zu reduzieren, können Sie verwenden[RemoveHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) Eigenschaften hinein**RemoveHiddenInformation()** Methode von[Diagram](https://reference.aspose.com/diagram/java)Klasse. Das folgende Codebeispiel zeigt, wie versteckte Informationen aus diagram entfernt werden.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}
```
