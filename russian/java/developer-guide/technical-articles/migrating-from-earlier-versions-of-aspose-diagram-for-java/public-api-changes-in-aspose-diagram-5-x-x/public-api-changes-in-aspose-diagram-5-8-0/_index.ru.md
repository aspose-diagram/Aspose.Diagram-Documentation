---
title: Общедоступный API Изменения в Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /ru/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.7.0 до 5.8.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Параметр SaveToolBar добавлен в HTMLSaveOptions.**
В класс HTMLSaveOptions добавлен новый параметр SaveToolBar. Указывает, сохранять панель инструментов или нет. Значение по умолчанию верно. Примеры кодов:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX Опция сохранения добавлена в SaveFileFormat**
Раньше Aspose.Diagram API поддерживал чтение формата VSDX, но теперь мы добавили поддержку записи диаграмм в формате VSDX. Примеры кодов:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **В класс ShapeCollection добавлен групповой метод.**
Теперь разработчики могут группировать несколько фигур вместе в Visio diagram, используя Aspose.Diagram API. Примеры кодов:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
