---
title: Автоматическое размещение коллекции фигур на странице Visio
type: docs
weight: 30
url: /ru/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: В этом разделе объясняется, как авторазместить коллекцию фигур на странице visio с помощью Aspose.Diagram.
---
## **Автоматическое размещение коллекции фигур на странице Visio**
С помощью Aspose.Diagram for .NET API разработчики могут автоматически размещать набор фигур на чертеже Visio. Для этого класс Page предлагает член AutoSpaceShapes, который принимает параметры ShapeCollection и AutoSpaceOptions. Класс AutoSpaceOptions позволяет задавать горизонтальные и вертикальные расстояния.
### **Авто-пространство фигур на странице**
Используйте следующий код в своем приложении .NET для автоматического размещения набора фигур на любой странице чертежа Visio.

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
