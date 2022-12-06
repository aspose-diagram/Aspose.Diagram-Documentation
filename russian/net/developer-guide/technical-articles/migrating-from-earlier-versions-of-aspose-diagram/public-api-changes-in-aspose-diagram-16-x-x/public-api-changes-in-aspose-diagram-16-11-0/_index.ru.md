---
title: Общедоступный API Изменения в Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.8.0 до 16.11.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Изменить свойства элемента управления ActiveX**
 Разработчики могут получить элемент управления ActiveX, а затем изменить его свойства. Мы добавили свойство ActiveXControl в[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) учебный класс. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"C:\temp\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get a shape by ID

Shape shape = page.Shapes.GetShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;

// set width of the command button control

cbac.Width = 4;

// set height of the command button control

cbac.Height = 4;

// set caption of the command button control

cbac.Caption = "Test Button";

// save diagram

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
## **Вставьте текстовую форму в Visio Diagram**
Разработчики могут вставить текстовую форму в Visio diagram, используя Aspose.Diagram API. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

string text = "Test text";

// add text to a Visio page

diagram.Pages[0].AddText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
