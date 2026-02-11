---
title: Работа со слоями
type: docs
weight: 160
url: /ru/java/working-with-layers/
---
### **Настройка объектов Shape со слоями**
Aspose.Diagram for Java позволяет настраивать объекты формы со слоями в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут управлять формами в соответствии с потребностями конечных пользователей.

[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Объект класса предлагает свойство LayerMember, которое позволяет добавлять/удалять объекты формы в/из слоев в чертеже Visio. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:

**Добавляйте, удаляйте и перемещайте объекты формы в/из слоев diagram.** 

![дело:изображение_альтернативный_текст](working-with-layers_1.png)

Следующий фрагмент кода помогает добавлять, удалять и перемещать свойства объектов формы.
#### **Примеры программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureShapeLayers.class);
        
//call the diagram constructor to load visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// iterate through the shapes
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    if (shape.getName().toLowerCase() == "shape1")
    {
        //Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0;1");
    }
    else if (shape.getName().toLowerCase() == "shape2")
    {
        //Remove shape2 from all the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("");
    }
    else if (shape.getName().toLowerCase() == "shape3")
    {
        //Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0");
    }
}
// save diagram
diagram.save(dataDir + "ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Добавьте слой на странице Visio.**
Aspose.Diagram for Java позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.

[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) класс предлагает метод add, который позволяет добавить новый[Слой](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)объект класса на чертеже Visio. Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.

Следующий фрагмент кода помогает добавить объекты слоя.
#### **Примеры программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddLayer.class) + "Layers/";

// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// initialize a new Layer class object
Layer layer = new Layer();
// set Layer name
layer.getName().setValue("Layer1");
// set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE);
// set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE);
// add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer);

// get shape by ID
Shape shape = page.getShapes().getShape(3);
// assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));
// save diagram
diagram.save(dataDir + "AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

{{% alert color="primary" %}} 

Aspose.Diagram for Java предоставляет разработчикам доступ к существующим уровням Visio diagram.

{{% /alert %}} 
### **Получить все доступные слои**
[СтраницаЛист](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) собственность[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс позволяет получить список доступных слоев из Visio diagram с помощью[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) учебный класс.

Следующий фрагмент кода помогает получить список слоев.
#### **Примеры программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveAllLayers.class);  
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// iterate through the layers
for (Layer layer : (Iterable<Layer>) page.getPageSheet().getLayers())
{
    System.out.println("Name: " + layer.getName().getValue());
    System.out.println("Visibility: " + layer.getVisible().getValue());
    System.out.println("Status: " + layer.getStatus().getValue());
}

{{< /highlight >}}
```
