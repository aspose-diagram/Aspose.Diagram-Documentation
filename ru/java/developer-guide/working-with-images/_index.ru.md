---
title: Работа с изображениями
type: docs
weight: 70
url: /ru/java/working-with-images/
---
## **Извлечь все изображения со страницы Visio**
В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Вы можете извлечь изображения с определенной страницы файла Visio.
### **Извлечь изображения**
Объект Page Class представляет область рисования страницы переднего плана или страницы фона. Свойство Shapes, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Shape. Это свойство можно использовать для извлечения всех изображений с определенной страницы.
#### **Пример программирования извлечения изображений**
Следующий фрагмент кода извлекает все изображения с определенной страницы Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
## **Получить иконки различных форм Visio**
Aspose.Diagram for Java API теперь позволяет разработчикам получать иконки различных Visio форм.
### **Получение значка формы**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram или шаблон.
1. Получить мастер по его индексу
1. Получить главный значок.
1. Сохранить значок в локальном пространстве.
#### **Получить пример программирования значков**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}
```
## **Замените форму изображения Visio Diagram**
Aspose.Diagram for Java API позволяет разработчикам получать доступ и заменять доступные формы изображений в файле Visio diagram.
### **Замена формы изображения**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram.
1. Повторите выборочные формы страниц.
1. Примените фильтр, чтобы получить формы изображения.
1. Сохраните результат Visio diagram в локальном пространстве.
#### **Замена примера программирования формы изображения**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Импортировать растровое изображение как форму Visio**
Aspose.Diagram for Java API теперь позволяет разработчикам импортировать растровое изображение в виде формы.
### **Вставьте изображение BMP в Visio**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Получить страницу Visio
1. Импорт растрового изображения в виде фигуры Visio
1. Сохраните номер diagram.
#### **Вставьте образец программирования изображения BMP**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
