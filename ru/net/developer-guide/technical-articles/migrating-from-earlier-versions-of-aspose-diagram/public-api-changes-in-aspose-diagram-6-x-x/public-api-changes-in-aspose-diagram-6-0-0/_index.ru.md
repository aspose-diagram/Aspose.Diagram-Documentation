---
title: Общедоступный API Изменения в Aspose.Diagram 6.0.0
type: docs
weight: 40
url: /ru/net/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.9.0 до 6.0.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Метод IsGlued добавлен в класс Shape**
Метод IsGlued принимает объект фигуры в качестве параметра, чтобы определить, склеены ли две фигуры или нет.
Пример кода:

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsGlued(ShapedTwo);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsGlued(ShapedTwo)

{{< /highlight >}}
## **Метод IsConnected добавлен в класс Shape**
Метод IsConnected принимает объект формы в качестве параметра, чтобы определить, соединены ли две фигуры.
Пример кода:

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsConnected(ShapedTwo);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsConnected(ShapedTwo)

{{< /highlight >}}
