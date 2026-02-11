---
title: 使用图层
type: docs
weight: 160
url: /zh/java/working-with-layers/
---
### **使用图层配置形状对象**
Aspose.Diagram for Java 允许在 Microsoft Office Visio diagram 中配置具有图层的形状对象。每个形状可以属于多个图层，因此开发人员可以管理形状以满足最终用户的需求。

这[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类对象提供 LayerMember 属性，允许在 Visio 绘图的图层中添加/删除形状对象。用户可以使用 Aspose.Diagram API 以编程方式管理这些属性，如下所示：

**在 diagram 的图层中添加、删除和移动形状对象。** 

![待办事项：图片_替代_文本](working-with-layers_1.png)

以下代码有助于添加、删除和移动形状对象属性。
#### **编程示例**
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
### **在 Visio PageSheet 中添加图层**
Aspose.Diagram for Java 允许开发人员添加新层来组织形状的自定义类别，然后以编程方式将形状分配给这些层。

这[图层集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection)类提供了添加方法，允许添加一个新的[层](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)Visio 绘图中的类对象。开发者可以通过初始化它的类对象来设置 Layer 的属性。

下面的一段代码有助于添加 Layer 对象。
#### **编程示例**
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

Aspose.Diagram for Java 允许开发人员访问 Visio diagram 的现有层。

{{% /alert %}} 
### **获取所有可用图层**
这[页表](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet)的财产[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)类允许使用 Visio diagram 检索可用层的列表[图层集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection)班级。

以下代码有助于获取图层列表。
#### **编程示例**
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
