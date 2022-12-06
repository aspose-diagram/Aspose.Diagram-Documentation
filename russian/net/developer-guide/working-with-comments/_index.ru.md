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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **Редактировать комментарий на уровне страницы в Visio Diagram**
 Microsoft Visio пользователи добавляют комментарии ко всей странице, которые представлены значком в верхнем левом углу страницы. Разработчики могут[добавить комментарии на уровне страницы в Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API дополнительно поддерживает изменение комментария на уровне страницы в файле Visio.
### **Редактировать комментарий**
 Свойство Comment, предоставляемое[Аннотация](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class позволяет разработчикам редактировать комментарии на странице рисования Visio.
#### **Пример программирования редактирования комментариев**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
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
