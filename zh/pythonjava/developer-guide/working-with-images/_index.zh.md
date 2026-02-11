---
title: 使用图像
type: docs
weight: 70
url: /zh/python-java/working-with-images/
description: 本页介绍如何使用 Aspose.Diagram 库从 Visio 绘图的页面中提取、替换或插入图像。
---
## **从 Visio 页面中提取所有图像**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。您可以从特定页面中提取图像[一个 Visio 文件](ExtractAllImagesFromPage.vsd).
### **提取图像**
Page Class 对象表示前景页面或背景页面的绘图区域。 Diagram 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。此属性可用于从特定页面中提取所有图像。
#### **提取图像编程示例**
以下代码从特定的 Visio 页面中提取所有图像。


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load a VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        fos = java.io.FileOutputStream("ExtractAllImages" + str(shape.getID()) + "_Out.bmp")
        fos.write(shape.getForeignData().getValue())
        fos.close()

jpype.shutdownJVM()

{{< /highlight >}}

## **获取各种 Visio 形状的图标**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio 形状](Timeline.vss). 
### **获取形状图标**
下面示例中的代码显示了如何：

1. 加载现有的 diagram 或模板。
1. 通过索引掌握
1. 获取主图标。
1. 将图标保存到本地空间。
#### **获取图标编程示例**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load stencil file to a diagram object
stencil = Diagram("Timeline.vss")
# get master
master = stencil.getMasters().getMasterByName("Triangle milestone")
# get byte array
icon_bytes = master.getIcon()
# create an image file
fos = java.io.FileOutputStream("MasterIcon_Out.png")
# write byte array of the image
fos.write(icon_bytes)
# close array
fos.close()
jpype.shutdownJVM()

{{< /highlight >}}

## **替换Visio Diagram的图片形状**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [Visio diagram](ExtractAllImagesFromPage.vsd).
### **替换图片形状**
下面示例中的代码显示了如何：

1. 加载现有的 diagram。
1. 遍历选择性页面形状。
1. 应用过滤器以获得图片形状。
1. 将结果 Visio diagram 保存到本地空间。
#### **替换图片形状编程示例**

{{< highlight python >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load the VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# convert image into bytes array       
fi = java.io.File("image.png")
fileContent = java.nio.file.Files.readAllBytes(fi.toPath())

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        # replace picture shape
        shape.getForeignData().setValue(fileContent)

# save diagram
diagram.save("ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}

## **将图像导入为 Visio 形状**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **在 Visio 中插入图像**
下面示例中的代码显示了如何：

1. 创建一个 diagram。
1. 获取 Visio 页
1. 将图像导入为 Visio 形状
1. 保存 diagram。
#### **插入图像编程示例**

{{< highlight python >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Create a new diagram
diagram = Diagram()

# Get page object by index
page0 = diagram.getPages().getPage(0)
# Set pinX, pinY, width and height
pinX = 2
pinY = 2
width = 4
height = 3

# Import Bitmap image as Visio shape
page0.addShape(pinX, pinY, width, height, java.io.FileInputStream("image.png"))

# Save Visio diagram
diagram.save("InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

