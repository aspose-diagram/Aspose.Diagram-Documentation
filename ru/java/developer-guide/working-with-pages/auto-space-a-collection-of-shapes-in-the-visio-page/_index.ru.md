---
title: Автоматическое размещение коллекции фигур на странице Visio
type: docs
weight: 30
url: /ru/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Автоматическое размещение коллекции фигур на странице Visio**
С помощью Aspose.Diagram for Java API разработчики могут автоматически размещать набор фигур на чертеже Visio. Для этого класс Page предлагает член autoSpaceShapes, который принимает параметры ShapeCollection и AutoSpaceOptions. Класс AutoSpaceOptions позволяет задавать горизонтальные и вертикальные расстояния.
### **Авто-пространство фигур на странице**
Используйте следующий код в своем приложении Java для автоматического размещения набора фигур на любой странице чертежа Visio.

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
