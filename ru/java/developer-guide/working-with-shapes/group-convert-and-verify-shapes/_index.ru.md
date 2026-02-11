---
title: Группируйте, конвертируйте и проверяйте фигуры
type: docs
weight: 50
url: /ru/java/group-convert-and-verify-shapes/
---
## **Сгруппируйте несколько фигур вместе на чертеже Visio**
Aspose.Diagram API позволяет разработчикам группировать фигуры вместе, чтобы перемещать их все одновременно. Каждая фигура в группе имеет уникальный идентификатор и собственный набор свойств. Когда мы изменяем форматирование группы фигур, оно присваивает новое свойство каждой фигуре.
### **Как сгруппировать фигуры**
Метод Group, предоставляемый классом ShapeCollection, можно использовать для группировки фигур.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. инициализировал массив фигур
1. получить определенную форму по идентификатору.
1. получить другую конкретную форму по идентификатору.
1. назначать фигуры массиву.
1. сгруппируйте фигуры, вызвав метод Group.
1. сохранить diagram
#### **Образец программирования групповых форм**
Используйте следующий код в приложении Java для группировки фигур с помощью Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Преобразование формы Visio в другие форматы файлов**
Aspose.Diagram for Java API позволяет разработчикам преобразовывать одну форму Visio в любой другой поддерживаемый формат файла. В этой статье мы удалим все остальные фигуры Visio со страницы и настроим параметры страницы в соответствии с исходным размером фигуры.
### **Преобразование определенной формы Visio**
 Разработчики могут преобразовать форму Visio в PDF, HTML, изображение, SVG и SWF с помощью[указав параметры сохранения Visio]().
Этот пример кода работает следующим образом:

1. Загрузите источник Visio.
1. Получить конкретную страницу.
1. Удалите фоновую страницу.
1. Создайте хеш-таблицу всех форм, содержащих идентификаторы и имена.
1. Итерация по хеш-таблице
1. Удалите все фигуры со страницы Visio, кроме одной.
1. Установите размер страницы.
1. Сохраните страницу Visio в любом поддерживаемом формате файла.
#### **Образец программирования преобразования формы**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}
```
### **Преобразование формы Visio в форму PDF**
Метод ToPdf класса Shape позволяет преобразовать фигуру в формат PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Преобразование формы Visio в форму HTML**
Метод ToHTML класса Shape позволяет преобразовать фигуру в формат HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}} 
## **Проверьте, соединены или склеены две фигуры Visio**
 Aspose.Diagram for Java API позволяет разработчикам проверить, что две фигуры Visio склеены или соединены. Ранее мы видели, как мы можем соединить или склеить две фигуры в этих разделах справки:[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) а также[Приклейте фигуры внутри контейнера](/diagram/ru/java/working-with-shapes-gluing/).
### **Проверка соединенных или склеенных фигур**
[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class предлагает свойства IsGlued и IsConnected, чтобы определить, склеены ли две фигуры или соединены.
#### **Пример программирования проверки соединенных или склеенных фигур**
Следующий фрагмент кода проверяет, соединены ли две фигуры или склеены.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Проверьте, входит ли фигура Visio в группу фигур**
Aspose.Diagram for Java API позволяет разработчикам проверять, входит ли фигура Visio в группу фигур или нет.
### **Проверка формы в группе фигур**
Класс Shape предлагает свойства IsInGroup, чтобы определить, является ли фигура Visio фигурой группы.
#### **Проверка формы в примере программирования группы фигур**
Следующий фрагмент кода проверяет, является ли фигура групповой.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
