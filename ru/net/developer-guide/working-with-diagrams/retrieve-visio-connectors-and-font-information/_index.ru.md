---
title: Получить Visio соединители и информацию о шрифтах
type: docs
weight: 20
url: /ru/net/retrieve-visio-connectors-and-font-information/
description: В этом разделе объясняется, как получить информацию о разъемах visio и шрифтах.
---
## **Получение информации о соединителе**
 Aspose.Diagram for .NET предоставляет механизмы для получения информации - ID и имя - о[страницы](/diagram/ru/net/retrieve-2c-get-2c-copy-and-insert-a-page/) а также[мастер](https://docs.aspose.com/diagram/net/working-with-masters/). Он также позволяет получить информацию о соединителях, элементах, которые связывают фигуры.

[Соединять](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) Объект представляет соединитель, который соединяет две фигуры на странице рисования Visio. Свойство Connects, предоставляемое[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class поддерживает набор объектов Aspose.Diagram.Connect. Это свойство можно использовать для получения сведений об идентификаторе и имени соединителя.
### **Образец программирования**
Следующий фрагмент кода извлекает информацию о соединителях в файле diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}

## **Получение информации о шрифте**
 Aspose.Diagram имеет механизмы для получения информации об элементах, составляющих diagram, из[страницы](/diagram/ru/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [трафареты](https://docs.aspose.com/diagram/net/working-with-masters/), [соединители](/diagram/ru/net/retrieving-connector-information/)а также шрифты. В этой статье показано, как узнать, какие шрифты используются в файле diagram.

[Шрифт](http://www.aspose.com/api/net/diagram/aspose.diagram/font) объект представляет собой шрифт, который либо применяется к тексту в документе, либо доступен для использования в системе. Объект Font сопоставляет имя (например, «Arial») с идентификатором шрифта (например, 3), который Microsoft Visio хранится в ячейке «Шрифт» в разделе «Символ» фигуры, содержащей текст, отформатированный с помощью этого шрифта. Идентификаторы шрифтов могут меняться при открытии документа в разных системах или при установке или удалении шрифтов.
### **Получение примера программирования шрифтов**
Следующий фрагмент кода извлекает информацию о шрифте из файла Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}

### **Получение каталога шрифтов по умолчанию**
Aspose.Diagram for .NET API также позволяет получить путь к каталогу шрифтов по умолчанию с помощью метода GetDefaultFontDir() класса Diagram. Следующий фрагмент кода извлекает каталог шрифтов по умолчанию из файла Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}

### **Получение неиспользуемых шрифтов**
{{% alert color="primary" %}}

Этот метод поддерживается версией 19.6 или более поздней.

{{% /alert %}}

Aspose.Diagram for .NET API также позволяет получить неиспользуемые шрифты с помощью метода GetUnusedStyles() класса Diagram. Следующий фрагмент кода извлекает неиспользуемые шрифты из каталога Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}

