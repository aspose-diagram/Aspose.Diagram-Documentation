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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddPageLevelCommentInVisio.class);
// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.save(dataDir + "AddPageLevelCommentInVisio_Out.vdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Редактировать комментарий на уровне страницы в Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API поддерживает изменение комментариев на уровне страницы на странице чертежа Visio, которые представлены значком в верхнем левом углу страницы.
### **Редактировать комментарий**
Свойство Comment, предоставляемое классом Annotation, позволяет разработчикам редактировать комментарии на странице рисования Visio.
#### **Пример программирования редактирования комментариев**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditPageLevelCommentInVisio.class);
// load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get collection of the annotations
AnnotationCollection annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations();

// iterate through the annotations
for (Annotation annotation : (Iterable<Annotation>) annotations) 
{
    String comment = annotation.getComment().getValue();
    comment += "Updation mark";
    annotation.getComment().setValue(comment);
}
// save Visio
diagram.save(dataDir + "EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
