---
title: Общественный API Изменения в Aspose.Diagram 17.01
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 16.12.0 до 17.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Преобразовать Visio Рисунок с выбранными фигурами**
Разработчики могут выбрать определенные формы для преобразования чертежа Visio в любой другой поддерживаемый формат. Мы добавили[Формы](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)член в[RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)класс для этой цели. Каждый класс параметров сохранения является расширенной формой класса RenderingSaveOptions. Пожалуйста, проверьте пример кода:

**C#**

{{< highlight "csharp" >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
