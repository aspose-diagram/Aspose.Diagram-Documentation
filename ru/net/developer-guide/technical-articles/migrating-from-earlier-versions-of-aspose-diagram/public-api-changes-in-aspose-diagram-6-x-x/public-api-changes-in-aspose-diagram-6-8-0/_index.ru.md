---
title: Общедоступный API Изменения в Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.6.0 до 6.8.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Вставьте элемент управления ActiveX**
Разработчики могут вставить элемент управления ActiveX в Visio diagram. Мы добавили метод AddActiveXControl в[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) учебный класс. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
## **Установите флажок цвета слоя**
Разработчики могут установить или получить флажок Color CheckBox слоя, используя Aspose.Diagram API. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
## **Добавляет свойство InheritFill в класс Shape**
Разработчики могут получить или установить наследуемое свойство заполнения. Мы добавили свойство InheritFill в класс Shape. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
