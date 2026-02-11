---
title: Работа с комментариями
type: docs
weight: 220
url: /ru/net/working-with-comments/
description: На этой странице описывается, как добавлять или редактировать комментарии с помощью библиотеки Aspose.Diagram.
---
## **Добавьте комментарий на уровне страницы в Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API позволяет разработчикам размещать комментарии в любом месте страницы рисования Visio.
### **Добавить комментарий**
 Метод AddComment, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, позволяет разработчикам добавлять комментарии на страницу рисования. Он принимает координаты X и Y вместе со строкой комментария.
#### **Добавить комментарий Пример программирования**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.Save(dataDir + "AddComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Редактировать комментарий на уровне страницы в Visio Diagram**
 Microsoft Visio пользователи добавляют комментарии ко всей странице, которые представлены значком в верхнем левом углу страницы. Разработчики могут[добавить комментарии на уровне страницы в Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API дополнительно поддерживает изменение комментария на уровне страницы в файле Visio.
### **Редактировать комментарий**
 Свойство Comment, предоставляемое[Аннотация](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class позволяет разработчикам редактировать комментарии на странице рисования Visio.
#### **Пример программирования редактирования комментариев**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get collection of the annotations
AnnotationCollection annotations = diagram.Pages.GetPage("Page-1").PageSheet.Annotations;

// Iterate through the annotations
foreach (Annotation annotation in annotations)
{
    string comment = annotation.Comment.Value;
    comment += "Updation mark";
    annotation.Comment.Value = comment;
}
// Save Visio
diagram.Save(dataDir + "EditComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Добавление комментария на уровне формы в чертеже Visio**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API позволяет разработчикам добавлять комментарии к фигуре на чертеже Visio.
### **Добавить комментарий**
Перегруженный метод AddComment, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)class принимает экземпляр класса Shape и текстовую строку комментария.
#### **Добавить комментарий Пример программирования**
**C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
