---
title: Работа с комментариями
type: docs
weight: 210
url: /ru/java/working-with-comments/
---
## **Добавьте комментарий на уровне страницы в Visio**
Aspose.Diagram for Java API позволяет разработчикам добавлять комментарии в любом месте страницы чертежа Visio.
### **Добавить комментарий**
Метод addComment, предоставляемый классом Page, позволяет добавлять комментарии на страницу рисования. Он принимает координаты X и Y вместе со строкой комментария.

 Microsoft Visio пользователи добавляют комментарии ко всей странице, которые представлены значком в верхнем левом углу страницы. Разработчики могут[добавить комментарии на уровне страницы в Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API дополнительно поддерживает изменение комментария на уровне страницы в файле Visio.
#### **Добавить комментарий Пример программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Редактировать комментарий на уровне страницы в Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API поддерживает изменение комментариев на уровне страницы на странице чертежа Visio, которые представлены значком в верхнем левом углу страницы.
### **Редактировать комментарий**
Свойство Comment, предоставляемое классом Annotation, позволяет разработчикам редактировать комментарии на странице рисования Visio.
#### **Пример программирования редактирования комментариев**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Добавление комментария на уровне формы в чертеже Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API позволяет разработчикам добавлять комментарии к фигуре на чертеже Visio.
### **Добавить комментарий**
Перегруженный метод addComment, предоставляемый классом Page, принимает экземпляр класса Shape и текстовую строку комментария.
#### **Добавить комментарий Пример программирования**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
