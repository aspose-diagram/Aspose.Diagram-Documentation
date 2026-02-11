---
title: Добавить водяной знак в Visio
type: docs
weight: 10
url: /ru/java/add-watermark-to-visio/
keywords: watermark, visi
description: Как добавить водяной знак в visio, используя Java Diagram API.
---
## **Создание Diagram**
 Aspose.Diagram for Java позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)для создания diagram. Используйте конструктор по умолчанию[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Добавить водяной знак на visio на странице
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования добавления водяного знака**
В следующем примере кода показано, как добавить водяной знак в файл Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
