---
title: Trabajo con forma de tipo de conector
type: docs
weight: 80
url: /es/java/working-with-connector-type-shape/
---
## **Establecer apariencia de la forma del tipo de conector en Visio**
Este tema explica cómo los desarrolladores pueden cambiar la apariencia de la forma del tipo de conector dinámico usando Aspose.Diagram for Java.
### **Establecer la apariencia del conector**
 El método SetConnectorsType expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase se puede utilizar para establecer la apariencia de la forma del tipo de conector.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma de conector particular.
1. establecer la apariencia de la forma.
1. guardar diagram
#### **Ejemplo de programación de la apariencia del conector establecido**
Use el siguiente código en su aplicación Java para establecer la apariencia de la forma del tipo de conector usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Seleccione la opción de redirección de la forma del conector**
 La propiedad ConFixedCode expuesta por el[Diseño](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) La clase se puede utilizar para seleccionar la opción de redirección. La propiedad Layout, expuesta por el[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) clase, se utilizará.

|<p>**Cómo seleccionar las opciones de redirección** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. obtener una página en particular.
1. obtener una forma de conector particular.
1. establecer opciones de redirección.
1. guardar diagram.
### **Seleccionar ejemplo de programación de opción de redirección**
Use el siguiente código en su aplicación Java para seleccionar la opción de cambio de ruta de la forma del conector usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
