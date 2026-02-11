---
title: Работа с изображениями
type: docs
weight: 70
url: /ru/python-java/working-with-images/
description: На этой странице описывается, как извлечь, заменить или вставить изображение со страницы чертежа Visio с библиотекой Aspose.Diagram.
---
## **Извлечь все изображения со страницы Visio**
 В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Вы можете извлекать изображения с определенной страницы[файл Visio](ExtractAllImagesFromPage.vsd).
### **Извлечь изображения**
Объект Page Class представляет область рисования страницы переднего плана или страницы фона. Свойство Shapes, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Shape. Это свойство можно использовать для извлечения всех изображений с определенной страницы.
#### **Пример программирования извлечения изображений**
Следующий фрагмент кода извлекает все изображения с определенной страницы Visio.

```
{{< highlight "python" >}}
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
```
## **Получить иконки различных форм Visio**
 Aspose.Diagram for Python via Java API теперь позволяет разработчикам получать иконки различных[Visio формы](Timeline.vss). 
### **Получение значка формы**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram или шаблон.
1. Получить мастер по его индексу
1. Получить главный значок.
1. Сохранить значок в локальном пространстве.
#### **Получить пример программирования значков**
```
{{< highlight "python" >}}
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
```
## **Замените форму изображения Visio Diagram**
 Aspose.Diagram для Python via Java API позволяет разработчикам получать доступ и заменять доступные формы изображений в[Visio diagram](ExtractAllImagesFromPage.vsd).
### **Замена формы изображения**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram.
1. Повторите выборочные формы страниц.
1. Примените фильтр, чтобы получить формы изображения.
1. Сохраните результат Visio diagram в локальном пространстве.
#### **Замена примера программирования формы изображения**
```
{{< highlight "python" >}}
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
```
## **Импорт изображения как формы Visio**
Aspose.Diagram для Python via Java API теперь позволяет разработчикам импортировать изображение в виде формы Microsoft Visio.
### **Вставьте изображение в Visio**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Получить страницу Visio
1. Импорт изображения в виде фигуры Visio
1. Сохраните номер diagram.
#### **Вставьте пример программирования изображения**
```
{{< highlight "python" >}}
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
```
