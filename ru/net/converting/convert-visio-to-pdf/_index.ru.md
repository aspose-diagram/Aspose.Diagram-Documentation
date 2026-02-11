---
title:  Преобразование Visio в формат PDF
linktitle: Преобразование Visio в PDF
type: docs
weight: 10
url: /ru/net/convert-visio-to-pdf/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать форматы Visio в PDF. Преобразуйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в PDF с помощью нескольких строк кода.
---
## **Экспорт в PDF**
{{% alert color="primary" %}}

 Aspose.Diagram for .NET непосредственно записывает информацию о API и номере версии в выходных документах. Например, при отображении чертежа на PDF, Aspose.Diagram for .NET заполняет**Заявление** поле со значением «Aspose.Diagram» и**PDF Продюсер** поле со значением, например 'Aspose.Diagram 17.9'.

Обратите внимание, что вы не можете поручить Aspose.Diagram for .NET API изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

 В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Использовать[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) конструктор класса для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

На изображении ниже показан VSD diagram, который фрагменты кода ниже экспортируют PDF. Вы можете использовать другие форматы diagram (VSS, VSSM, VDX, VST, VSTX, VDX, 08161081, 08161081 или 34.64 или 34.

|**Исходный файл.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_1.png)|


Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод Save классов Diagram и установите выходной формат PDF.

Ниже приведено изображение выходного файла PDF.

|**Выходной файл PDF.**|
|:- |
|![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_2.png)|
### **Экспорт Microsoft Visio Чертеж в PDF**
В примерах кода показано, как экспортировать чертеж Microsoft Visio в PDF с помощью C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}

### **Разделить несколько страниц**
Aspose.Diagram for .NET позволяет разделить несколько страниц при преобразовании Microsoft Visio Diagram в PDF. В следующем фрагменте кода показана функциональность.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Initialize PdfSaveOptions
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
// set SplitMultiPages option
options.SplitMultiPages = true;
// save in PDF format
diagram.Save(dataDir + "SplitMultiPages.pdf", options);

{{< /highlight >}}

### **Использовать обратный вызов для сохранения страницы**
Если у вас есть несколько страниц, Aspose.Diagram for .NET позволяет использовать обратный вызов сохранения страницы при преобразовании Microsoft Visio Diagram в PDF. Следующий фрагмент кода показывает функциональность.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Initialize PdfSaveOptions
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
// set PageSavingCallback option
options.PageSavingCallback = new TestDiagramPageSavingCallback();
// save in PDF format
diagram.Save(dataDir + "PageSavingCallback.pdf", options);

{{< /highlight >}}

#### **Класс TestDiagramPageSavingCallback**
{{< highlight "java" >}}

 открытый класс TestDiagramPageSavingCallback: Aspose.Diagram.Saving.IPageSavingCallback

{
 
 public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
 
 {
 
 Console.WriteLine("Начать сохранение diagram страницы {0} из страниц {1}", args.PageIndex_x.0Page); 
 }
 
 public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
 
 {
 
 Console.WriteLine("Завершить сохранение diagram страницы {0} из страниц {1}", args.1,Countarddex.PageIndex. 
 
 // не выводит страницы после индекса страницы 8.
 
 if (args.pageindex> = 8) 
 
 {
 
 args.hasmorepages = false; 
 
 
 
 
 
 
 
0.
