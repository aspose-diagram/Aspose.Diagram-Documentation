---
title:  Конвертировать Visio в форматы изображений
linktitle: Преобразовать Visio в изображения
type: docs
weight: 20
url: /ru/net/convert-visio-to-image/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в различные форматы изображений. Конвертируйте Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в изображения PNG, JPEG, BMP с помощью нескольких строк кода.
---
## **Экспорт диаграмм в форматы файлов изображений**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в изображение с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Используйте[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) конструктор класса для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

Чтобы экспортировать diagram в изображение:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram и установите формат изображения, в который вы хотите экспортировать. Выходной файл изображения выглядит как исходный файл.
### **Экспорт Microsoft Visio чертежа в файл изображения**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Также можно сохранить в изображение определенную страницу, а не весь документ:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

// Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.PageIndex = 0;

// Save resultant Image file
diagram.Save(dataDir + "ExportPageToImage_out.png", options);

{{< /highlight >}}
