---
title: Добавить водяной знак в Visio
type: docs
weight: 10
url: /ru/net/add-watermark-to-visio/
keywords: watermark, visi
description: Как добавить водяной знак в visio, используя .NET Diagram API.
---
## **Создание Diagram**
 Aspose.Diagram for .NET позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)для создания diagram. Используйте конструктор по умолчанию[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Добавить водяной знак на visio на странице
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования добавления водяного знака**
В следующем примере кода показано, как добавить водяной знак в файл Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
    double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
    double width = page.PageSheet.PageProps.PageWidth.Value;
    double height = page.PageSheet.PageProps.PageHeight.Value;
    
    //Add watermark
    Shape shape = page.AddText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);
    diagram.Save(dataDir + "Watermark.vsdx", SaveFileFormat.VSDX);
}


{{< /highlight >}}
```
