---
title: Hello World Пример
type: docs
weight: 90
url: /ru/net/hello-world-example/
description: На этой странице описывается, как создать пример hello world с библиотекой Aspose.Diagram.
---
## **Hello World Пример**
Aspose.Diagram for .NET имеет широкие возможности для создания, открытия, редактирования и преобразования Microsoft Visio файлов с использованием C# и других .NET языков. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of форматы, такие как PDF, HTML, XML, SVG и XAML.

После[установка Aspose.Diagram for .NET](/diagram/ru/net/installation/)в вашей среде можно использовать следующие шаги, чтобы увидеть, как Aspose.Diagram API используется в приложениях .NET.

1. Создать экземпляр объекта Diagram
1. Используйте метод Save объекта класса Diagram, чтобы сохранить файл на диск.

Следующий фрагмент кода представляет собой программу Hello World, демонстрирующую работу Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```




