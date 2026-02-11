---
title: Hello World Пример
type: docs
weight: 100
url: /ru/java/hello-world-example/
---
## **Hello World Пример**
Пример «Hello World» традиционно используется для ознакомления с функциями языка программирования или программного обеспечения с простым вариантом использования.

Aspose.Diagram for Java — это многофункциональная Visio обработка файлов, которая позволяет разработчикам приложений встраивать Visio функции создания, чтения и преобразования документов в свои Java приложения. It supports working with many popular Visio file-formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. The API has strong conversion features to convert Visio Diagrams to a number of форматы, такие как PDF, HTML, XML, SVG и XAML.

После[установка Aspose.Diagram for Java](/diagram/ru/java/installation/)в вашей среде вы можете выполнить приведенный ниже пример кода, чтобы увидеть, как работает Aspose.Diagram API.

В приведенном ниже фрагменте кода выполняются следующие шаги:

1. Создать экземпляр объекта Diagram
1. Используйте метод Save объекта класса Diagram, чтобы сохранить файл на диск.

Следующий фрагмент кода представляет собой программу Hello World, демонстрирующую работу Aspose.Diagram for Java API.

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




