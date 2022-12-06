---
title: Общественный API Изменения в Aspose.Diagram 17.01
type: docs
weight: 10
url: /ru/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 16.12.0 до 17.01, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Преобразовать Visio Рисунок с выбранными фигурами**
Разработчики могут выбрать определенные формы для преобразования чертежа Visio в любой другой поддерживаемый формат. Для этой цели мы добавили элемент Shapes в класс RenderingSaveOptions. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions. Пожалуйста, проверьте пример кода:

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
