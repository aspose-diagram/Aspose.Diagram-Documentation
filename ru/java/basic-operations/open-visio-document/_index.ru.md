---
title: Открыть документ Visio программно
linktitle: Открыть документ Visio
type: docs
weight: 20
url: /ru/java/open-visio-document/
description: На этой странице описывается, как открыть документ Visio с нуля с помощью библиотеки Aspose.Diagram.
---
## **Чтение существующего чертежа Visio**
Aspose.Diagram API поддерживает создание новых диаграмм Visio с нуля и последующее сохранение в любом поддерживаемом формате файла. Разработчики также могут загрузить существующий Visio diagram для модификации, добавления или обработки.
### **Чтение Diagram**
Используя Aspose.Diagram API, разработчики могут загружать все поддерживаемые форматы файлов Visio. Доступные конструкторы класса Diagram позволяют это сделать, и они принимают допустимую строку пути к файлу или файловый поток исходного файла Visio.

Поддерживаются следующие читаемые форматы файлов:
**VSDX, VSD, VSDM, ВСС, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM и VSX**

Конструкторы класса diagram также предлагают необязательный параметр, определяющий LoadFileFormat или LoadOptions. Это информация о предварительной загрузке, которую разработчики могут передавать по телефону Aspose.Diagram API. Мы рекомендуем передавать реалистичную информацию для достижения идеальной производительности.
#### **Чтение Diagram Пример программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
