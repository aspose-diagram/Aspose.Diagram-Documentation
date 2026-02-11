---
title: Crear, diseñar y autoajustar formas
type: docs
weight: 10
url: /es/java/create-layout-and-auto-fit-shapes/
---
## **Creando un Diagram**
 Aspose.Diagram for Java le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](/diagram/es/java/add-and-connect-visio-shapes/)para construir el diagram. Use el constructor predeterminado de[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Formas de diseño en estilo de diagrama de flujo**
 Con ciertos tipos de dibujos conectados, como diagramas de flujo y diagramas de red, puede utilizar el**Formas de diseño** característica para posicionar formas automáticamente. El posicionamiento automático es más rápido que arrastrar manualmente cada forma a una nueva ubicación.

Por ejemplo, si está actualizando un diagrama de flujo grande para incluir un nuevo proceso, puede agregar y conectar las formas que componen el proceso y luego usar la función de diseño para diseñar automáticamente el dibujo actualizado.

 El método Layout, expuesto por el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) la clase diseña las formas y/o redirige los conectores en todas las páginas de diagram. Este método acepta un objeto LayoutOptions como argumento. Use las diferentes propiedades expuestas por la clase LayoutOptions para diseñar formas automáticamente.

La siguiente imagen muestra el diagram cargado por los fragmentos de código en este artículo, antes de que se aplique el diseño automático. Los fragmentos de código muestran cómo aplicar[diseños de diagrama de flujo](/diagram/es/java/create-2c-layout-and-auto-fit-shapes/) y[diseños de árboles compactos](/diagram/es/java/create-2c-layout-and-auto-fit-shapes/).

**La fuente diagram.** 

![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_1.png)

Los fragmentos de código de este artículo toman la fuente diagram y le aplican varios tipos de diseño automático, guardando cada uno en un archivo separado.

|<p>**Formas de diseño de abajo hacia arriba** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Formas de diseño de arriba a abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Diseño de formas de izquierda a derecha** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Diseño de formas de derecha a izquierda** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_5.png)</p>|
Para diseñar formas en estilo de diagrama de flujo:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de la clase LayoutOptions y configure las propiedades relacionadas con el estilo del diagrama de flujo.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el dibujo Visio.
### **Ejemplo de programación de estilo de diagrama de flujo**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

### **Disposición de formas en el estilo de árbol compacto**
 El estilo de diseño de árbol compacto intenta construir una estructura de árbol. Utiliza el mismo archivo de entrada que el[ejemplo anterior](/diagram/es/java/create-2c-layout-and-auto-fit-shapes/) guarda en varios estilos diferentes de árboles compactos.

|<p>**Diseño de árbol compacto: abajo y a la derecha** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Diseño de árbol compacto: abajo e izquierda** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Diseño de árbol compacto: derecha y abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Diseño de árbol compacto: izquierda y abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Para diseñar formas en el estilo de árbol compacto:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) clase.
1. Cree una instancia de la clase LayoutOptions y establezca propiedades de estilo de árbol compacto.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el archivo Visio.
#### **Ejemplo de programación de estilo de árbol compacto**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Ajuste automático el Visio Diagram**
Aspose.Diagram API admite el ajuste automático del dibujo Visio. Esta función de operación ayuda a traer formas externas dentro del límite de la página Visio.

Aspose.Diagram for Java API tiene la clase Diagram que representa un dibujo Visio. La clase DiagramSaveOptions expone la propiedad AutoFitPageToDrawingContent para ajustar automáticamente el dibujo Visio.

Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Cree un objeto de la clase DiagramSaveOptions y pase el formato de archivo resultante.
1. Establezca la propiedad AutoFitPageToDrawingContent del objeto DiagramSaveOptions.
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Ejemplo de programación de ajuste automático**
El siguiente código de ejemplo muestra cómo ajustar formas automáticamente en Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}

## **Trabajando con Proyecto VBA**
### **Modifique el código del módulo VBA en Visio Diagram**
Este artículo muestra cómo modificar un código de módulo VBA automáticamente usando Aspose.Diagram for Java.

Hemos agregado las clases VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference y VbaProjectReferenceCollection. Estas clases ayudan a controlar el proyecto VBA. Los desarrolladores pueden extraer y modificar el código del módulo VBA.
### **Modificar ejemplo de programación de código de módulo VBA**
Por favor, compruebe este ejemplo de código:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Eliminar todas las macros del Visio Diagram**
Aspose.Diagram for Java permite a los desarrolladores eliminar todas las macros del Visio diagram.

La propiedad JavaProjectData, expuesta por el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, le permite eliminar todas las macros del dibujo Visio.
### **Eliminar todas las macros Ejemplo de programación**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

