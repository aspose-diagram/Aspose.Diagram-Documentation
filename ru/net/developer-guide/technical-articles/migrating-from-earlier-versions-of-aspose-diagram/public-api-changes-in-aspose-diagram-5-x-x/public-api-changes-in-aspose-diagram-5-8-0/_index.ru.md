---
title: Общедоступный API Изменения в Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.7.0 до 5.8.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Параметр SaveToolBar добавлен в HTMLSaveOptions.**
В класс HTMLSaveOptions добавлен новый параметр SaveToolBar. Указывает, сохранять панель инструментов или нет. Значение по умолчанию верно. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.SaveToolBar = false;

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' initialize HTMLSaveOptions class object

Dim opts As New HTMLSaveOptions()

' set save toolbar option

opts.SaveToolBar = False

{{< /highlight >}}
## **VSDX Опция сохранения добавлена в SaveFileFormat**
Раньше Aspose.Diagram API поддерживал чтение формата VSDX, но теперь мы добавили поддержку записи диаграмм в формате VSDX. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' save diagram in the VSDX format

diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
## **В класс ShapeCollection добавлен групповой метод.**
Теперь разработчики могут группировать несколько фигур вместе в Visio diagram, используя Aspose.Diagram API. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes

Aspose.Diagram.Shape[]ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array

ss[0]= diagram.Pages[0].Shapes.GetShape(1);

ss[1]= diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group

diagram.Pages[0].Shapes.Group(ss);

// save visio diagram

diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' load a Visio diagram

Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes

Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array

ss(0) = diagram.Pages(0).Shapes.GetShape(1)

ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group

diagram.Pages(0).Shapes.Group(ss)

' save visio diagram

diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
