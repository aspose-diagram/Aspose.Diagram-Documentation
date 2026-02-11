---
title: Извлечение элемента управления ActiveX из объекта Shape для изменения свойств
type: docs
weight: 20
url: /ru/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут получить элемент управления ActiveX из объекта формы Visio, чтобы установить все его доступные свойства.

{{% /alert %}} 
## **Получение примера программирования элемента управления ActiveX**
[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Класс предлагает метод getActiveXControl, который позволяет разработчикам извлекать элемент управления ActiveX из объекта формы Visio. Разработчики могут преобразовать элемент управления ActiveX в соответствующий класс элемента управления ActiveX, а затем установить все его доступные свойства.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
