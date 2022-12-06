---
title: Общедоступный API Изменения в Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /ru/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.7.0 до 6.8.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Вставьте элемент управления ActiveX**
 Разработчики могут вставить элемент управления ActiveX в Visio diagram. Мы добавили метод addActiveXControl в[Страница](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) учебный класс. Пожалуйста, проверьте этот пример кода:

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Установите флажок цвета слоя**
Разработчики могут установить или получить флажок Color CheckBox слоя, используя Aspose.Diagram API. Пожалуйста, проверьте этот пример кода:

**Java**

{{< highlight "java" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Добавляет свойство InheritFill в класс Shape**
Разработчики могут получить или установить наследуемое свойство заполнения. Мы добавили свойство InheritFill в класс Shape. Пожалуйста, проверьте этот пример кода:

**Java**

{{< highlight "java" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
