---
title: Работа с фигурами
type: docs
weight: 40
url: /ru/java/working-with-shapes-paragraph/
---
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Установите абзац формы.
#### **Образец программирования абзаца для фигуры**
Используйте следующий код в своем приложении Java, чтобы установить абзац формы, используя Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
