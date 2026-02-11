---
title: 使用图像
type: docs
weight: 70
url: /zh/java/working-with-images/
---
## **从 Visio 页面中提取所有图像**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。您可以从 Visio 文件的特定页面中提取图像。
### **提取图像**
Page Class 对象表示前景页面或背景页面的绘图区域。 Diagram 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。此属性可用于从特定页面中提取所有图像。
#### **提取图像编程示例**
以下代码从特定的 Visio 页面中提取所有图像。

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
## **获取各种 Visio 形状的图标**
Aspose.Diagram for Java API 现在允许开发者获取各种 Visio 形状的图标。
### **获取形状图标**
下面示例中的代码显示了如何：

1. 加载现有的 diagram 或模板。
1. 通过索引掌握
1. 获取主图标。
1. 将图标保存到本地空间。
#### **获取图标编程示例**
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
## **替换Visio Diagram的图片形状**
Aspose.Diagram for Java API 允许开发人员访问和替换 Visio diagram 中可用的图片形状。
### **替换图片形状**
下面示例中的代码显示了如何：

1. 加载现有的 diagram。
1. 遍历选择性页面形状。
1. 应用过滤器以获得图片形状。
1. 将结果 Visio diagram 保存到本地空间。
#### **替换图片形状编程示例**
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
## **将位图图像导入为 Visio 形状**
Aspose.Diagram for Java API 现在允许开发人员将位图图像导入为 Microsoft Visio 形状。
### **Insert a BMP Image in Visio**
下面示例中的代码显示了如何：

1. 创建一个 diagram。
1. 获取 Visio 页
1. 将位图图像导入为 Visio 形状
1. 保存 diagram。
#### **Insert a BMP Image Programming Sample**
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
