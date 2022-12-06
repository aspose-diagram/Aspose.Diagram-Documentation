---
title: Aspose.Diagram for .NET 17.8 Примечания к выпуску
type: docs
weight: 50
url: /ru/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Эта страница содержит примечания к выпуску для[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX to SVG - низкое качество вывода SVG.|Улучшение|
|DIAGRAMNET-51298|SVGSaveOptions — добавлена поддержка управления уровнем сжатия растрового изображения.|Улучшение|
|DIAGRAMNET-51300|Добавить поддержку соединения фигур с индексом соединения.|Улучшение|
|DIAGRAMNET-50577|Преобразование VSDX в PDF, текст круглой формы неуместен - I.|Ошибка|
|DIAGRAMNET-50582|VSDX в HTML, текст круглой формы неуместен - I.|Ошибка|
|DIAGRAMNET-50601|Преобразование VSDX в PDF, текст круглой формы неуместен - II.|Ошибка|
|DIAGRAMNET-50606|Преобразование VSDX в HTML, текст круглой формы неуместен - II.|Ошибка|
|DIAGRAMNET-51197|Формы предупреждающего треугольника отображаются неправильно при сохранении VSDM в SVG.|Ошибка|
|DIAGRAMNET-51245|Смещенные текстовые элементы при преобразовании VSD в PDF.|Ошибка|
|DIAGRAMNET-51246|Неверные шрифты применялись к тексту при преобразовании VSD в PDF.|Ошибка|
|DIAGRAMNET-51296|VSDM в SVG — изображение обрезается.|Ошибка|
|DIAGRAMNET-51301|VSDX в PDF - изменен цвет текста на соединительных линиях.|Ошибка|
|DIAGRAMNET-51302|VSDX в PDF - отсутствуют графические элементы.|Ошибка|
|DIAGRAMNET-51304|VSDX в PDF - неполная визуализация блок-схемы.|Ошибка|
|DIAGRAMNET-51305|VSDX в PDF - отсутствуют графические элементы.|Ошибка|
|DIAGRAMNET-51306|VSDX в PDF - изменен цвет текста на соединительных линиях.|Ошибка|
|DIAGRAMNET-51307|VSDX в PDF - отсутствуют графические элементы.|Ошибка|
|DIAGRAMNET-51313|Процедура открытия и сохранения чертежа VSDX создает поврежденный выходной файл.|Ошибка|
|DIAGRAMNET-51314|VSDX в SVG - неправильное позиционирование текста.|Ошибка|
|DIAGRAMNET-51317|VSDX в PDF - текст соединительных строк отсутствует.|Ошибка|
|DIAGRAMNET-51318|VSDX в PDF - жирный форматированный текст прямоугольных фигур отсутствует.|Ошибка|
|DIAGRAMNET-51319|VSDM в SVG — арифметическая операция привела к ошибке переполнения.|Ошибка|
|DIAGRAMNET-51320|Ошибка в элементе формы при загрузке VSDM.|Ошибка|
|DIAGRAMNET-51323|VSDM в SVG - отсутствуют все соединительные линии.|Ошибка|
|DIAGRAMNET-51324|VSDM в SVG - неправильный стиль границы и цвет границы различных форм.|Ошибка|
|DIAGRAMNET-51326|Проблема после добавления двух комментариев к форме.|Ошибка|
|DIAGRAMNET-51327|Проблема после использования метода «AddComment» при добавлении комментариев к различным фигурам.|Ошибка|
|DIAGRAMNET-51328|Aspose Diagram неправильно импортирует форму в документ.|Ошибка|
|DIAGRAMNET-51330|VSDM в SVG - добавлен дополнительный текст водяного знака.|Ошибка|
|DIAGRAMNET-51332|VSDM в SVG - некорректная отрисовка иконки.|Ошибка|
|DIAGRAMNET-51334|VSDM в SVG — смещенный текст в правом верхнем углу.|Ошибка|
|DIAGRAMNET-51335|VSDM в SVG - некорректная отрисовка фонового изображения.|Ошибка|
|DIAGRAMNET-51337|VSD в HTML - ошибка неверного формата входной строки.|Ошибка|
## **Public API и обратно несовместимые изменения**
Ниже приведен список любых изменений, внесенных в общедоступный номер API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в номер Aspose.Diagram for .NET. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите о них в в[Aspose.Diagram форум поддержки](https://forum.aspose.com/c/diagram/17).
### **Добавляет член качества в класс SVGSaveOptions**
Он получает или устанавливает значение, определяющее качество сгенерированных изображений.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Добавляет метод ConnectShapesViaConnectorIndex в класс Page.**
Это позволяет соединять фигуры, используя индексы соединения.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Примеры использования**
Пожалуйста, проверьте список разделов справки, добавленных в Aspose.Diagram вики-документы:

1. [Используйте индексы соединения для соединения фигур](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Использование параметров сохранения SVG](https://docs.aspose.com/diagram/net/save-visio-document/)
