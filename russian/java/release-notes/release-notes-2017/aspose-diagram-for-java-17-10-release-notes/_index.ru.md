---
title: Aspose.Diagram for Java 17.10 Примечания к выпуску
type: docs
weight: 30
url: /ru/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Эта страница содержит примечания к выпуску для[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality не влияет на выходной документ|Улучшение|
|DIAGRAMJAVA-50548|Выход VSDX - соединительная линия, проходящая через границу фигуры|Ошибка|
|DIAGRAMJAVA-50550|Раздел «Преобразование формы» не сохраняет формулы|Ошибка|
|DIAGRAMJAVA-50551|VSDX в PNG - неправильная отрисовка углов формы|Ошибка|
|DIAGRAMJAVA-50552|Цвета заливки не сохраняются при сохранении рисунка Visio в SVG.|Ошибка|
|DIAGRAMJAVA-50553|Неверная отрисовка линий при сохранении рисунка Visio в SVG.|Ошибка|
|DIAGRAMJAVA-50554|Цвета заливки не сохраняются при сохранении рисунка Visio в SVG.|Ошибка|
|DIAGRAMJAVA-50555|Неверная отрисовка линий при сохранении рисунка Visio в SVG.|Ошибка|
|DIAGRAMJAVA-50559|с VSDM по VDX - соединительные линии не связаны с фигурами|Ошибка|
|DIAGRAMJAVA-50561|Рисунок VSDX поврежден после добавления элемента SolutionXML|Ошибка|
### **Добавляет SameAsPdfConversionArea в ImageSaveOptions**
Он указывает, следует ли сохранять область так же, как PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
