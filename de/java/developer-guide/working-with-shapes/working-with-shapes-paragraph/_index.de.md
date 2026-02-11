---
title: Arbeiten mit dem Shapes-Absatz
type: docs
weight: 40
url: /de/java/working-with-shapes-paragraph/
---
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Stellen Sie den Absatz der Form ein.
#### **Beispiel für die Absatzprogrammierung von Form festlegen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um den Absatz der Form mit Aspose.Diagram for Java festzulegen.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```