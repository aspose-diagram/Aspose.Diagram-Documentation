---
title: Configurar formas de línea de tiempo Visio
type: docs
weight: 20
url: /es/java/configure-visio-timeline-shapes/
---
## **Establecer propiedades de forma de hito**
Aspose.Diagram permite a los desarrolladores establecer propiedades de hitos. Este artículo muestra cómo configurar la fecha del hito, el formato de fecha, el indicador de actualización automática y el tipo.
### **Configuración de fecha de hito, formato de fecha, indicador de actualización automática y tipo**
 los[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)la clase toma un[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) objeto mientras se inicializa el[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) objeto. El ejemplo de código de este artículo establece la fecha del hito, el formato de fecha, el indicador de actualización automática y las propiedades del tipo de hito.

|<p>**El hito antes de la actualización** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**El hito después de la actualización. Tenga en cuenta el formato de fecha modificado.** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
El proceso para actualizar la fecha del hito, el formato de fecha, el indicador de actualización automática y el tipo de hito:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Inicialice el objeto MilestoneHelper.
1. Establezca una fecha de hito.
1. Establezca el formato de fecha del hito.
1. Establezca un indicador de actualización automática.
1. Establecer el tipo de hito
1. Guarde el dibujo Visio en cualquier formato compatible.
#### **Establecer ejemplo de programación de hitos**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetMilestoneProps.class);  
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 22;
// Get timeline shape
Shape milestone = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set milestone date
milestoneHelper.setMilestoneDate(new DateTime(2014, 10, 21));
// Set date format
milestoneHelper.setDateFormat(21);
// Set auto update flag
milestoneHelper.setAutoUpdate(true);
// Set milestone type
milestoneHelper.setType(6);

// Save to VDX format
diagram.save(dataDir + "SetMilestoneProps_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```


Tabla de valores de formato de fecha:

|**Valor**|**cadena de formato**|
|:- |:- |
|0|dddd, aaaa-Md|
|1|aaaa-MM-dd|
|2|aa-MMM-d|
|3|aaaa/M/d|
|4|aa-MMM.-d|
|5|d MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM d, aaaa|
|9|MMM d, aaaa|
|10|Md-aa|
|11|Maryland|
|12|d MMMM, aaaa|
|13|d MMM, aaaa|
|14|dM-aa|
|15|DM|
|16|aa-md|
|17|aaaa-md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|yy|
|25|aaaa|
|26|d|
|27|MMMMM|
|28|MMM|
|29|METRO|
## **Establecer el período de tiempo y el formato de fecha de la forma de la línea de tiempo**
Aspose.Diagram permite a los desarrolladores configurar la línea de tiempo mediante programación. Aquí se explica cómo ajustar el período de tiempo y el formato de fecha de las formas de la línea de tiempo (bloque, línea, regla, dividida o cilíndrica).
### **Configuración del período de tiempo y el formato de fecha**
 los[Ayudante de línea de tiempo](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)la clase toma un[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) objeto al inicializar el[Ayudante de línea de tiempo](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) objeto. El ejemplo de código de este artículo establece los valores de formato de fecha, finalización e inicio del período de tiempo.

|<p>**La pestaña de período de tiempo del cuadro de diálogo Configurar línea de tiempo Visio** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/nHth3W8.png)</p>|<p>**La pestaña de formato de hora del cuadro de diálogo Configurar línea de tiempo Visio** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Entrada diagram** </p><p>![todo:imagen_alternativa_texto](configure-visio-timeline-shapes_1.png)</p>|<p>**El diagram después de que se hayan cambiado los valores.** </p><p>![todo:imagen_alternativa_texto](configure-visio-timeline-shapes_2.png)</p>|
El proceso para actualizar el formato de inicio, fin y fecha del período de tiempo es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Inicialice el objeto TimeLineHelper.
1. Establezca el inicio del período de tiempo.
1. Establezca el final del período de tiempo.
1. Establecer un formato de fecha.
1. Guarde el dibujo Visio en cualquier formato compatible.
#### **Establecer período de tiempo y muestra de programación de fecha**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureTimeLine.class); 
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
//timelineHelper.setDateFormatForBE(21);
// Set date format for intm of timeline shape   
//timelineHelper.setDateFormatForIntm(21);

// Or

// Set date format string for start and finish of timeline shape
timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");
// Set date format string for intm of timeline shape
timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

// Save to VDX format
diagram.save(dataDir + "ConfigureTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```


Tabla de valores de formato de fecha:

|**Valor**|**cadena de formato**|
|:- |:- |
|0|dddd, aaaa-Md|
|1|aaaa-MM-dd|
|2|aa-MMM-d|
|3|aaaa/M/d|
|4|aa-MMM.-d|
|5|d MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM d, aaaa|
|9|MMM d, aaaa|
|10|Md-aa|
|11|Maryland|
|12|d MMMM, aaaa|
|13|d MMM, aaaa|
|14|dM-aa|
|15|DM|
|16|aa-md|
|17|aaaa-md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|yy|
|25|aaaa|
|26|d|
|27|MMMMM|
|28|MMM|
|29|METRO|
## **Actualizar hitos en la línea de tiempo en Visio**
Aspose.Diagram permite a los desarrolladores ajustar hitos en las formas de la línea de tiempo (bloque, línea, regla, dividido o cilíndrico) según el cambio de período de tiempo.
### **Actualizar hitos en la línea de tiempo usando la clase TimeLineHelper**
 El método RefreshTimeLine expuesto por el[Ayudante de línea de tiempo](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) La clase se puede utilizar para revivir hitos en la línea de tiempo.

El siguiente código muestra cómo:

1. cargar una muestra diagram.
1. obtener una forma de línea de tiempo.
1. inicialice el objeto TimeLineHelper.
1. establecer el inicio del período de tiempo.
1. establecer el final del período de tiempo.
1. establecer formato de fecha (opcional).
1. llame al método RefreshTimeLine del objeto TimeLineHelper.
1. guardar diagram
#### **Actualizar hitos con el ejemplo de programación de TimeLineHelper**
Use el siguiente código en su aplicación Java para revivir hitos en la línea de tiempo usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshTimeLine.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
timelineHelper.setDateFormatForBE(21);

//revive milestones on the timeline
timelineHelper.refreshTimeLine();

// Save to VDX format
diagram.save(dataDir + "RefreshTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Actualizar hitos en la línea de tiempo usando la clase MilestoneHelper**
 El método RefreshMilestone expuesto por el[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)La clase se puede usar para actualizar hitos en la línea de tiempo.

El siguiente código muestra cómo:

1. cargar una muestra diagram.
1. obtener una forma de línea de tiempo.
1. agregue Shape en Visio diagram usando el método AddShape.
1. inicialice el objeto MilestoneHelper.
1. establecer la fecha del hito.
1. establezca la propiedad IsAutoUpdate de Milstone en verdadero.
1. llame al método RefreshMilestone del objeto MilestoneHelper.
1. guardar diagram
#### **Actualizar hitos con el ejemplo de programación de MilestoneHelper**
Use el siguiente código en su aplicación Java para actualizar hitos en la línea de tiempo usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshMilestoneWithMilestoneHelper.class);
        
String pageName = "Page-1";

////////////// Modify time line /////////// 
DateTime startDate = new DateTime(2015, 8, 1);
DateTime endDate = new DateTime(2016, 6, 1);
DateTime fisYear = startDate;

//Load a diagram 
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

//Get page
Page page = diagram.getPages().getPage(pageName);

long timelineId = 1;
Shape timeline = diagram.getPages().getPage(pageName).getShapes().getShape(timelineId);
double xpos = timeline.getXForm().getPinX().getValue();
double ypos = timeline.getXForm().getPinY().getValue();

// Add milestone 
String milestoneMasterName = "2 triangle milestone";

//Add Master
diagram.addMaster(dataDir + "Timeline.vss", milestoneMasterName);

//Add Shape in Visio diagram using AddShape method
long milestoneShapeId = diagram.addShape(xpos, ypos, milestoneMasterName, 0);

//Get the shape based on ID
Shape milestone = page.getShapes().getShape(milestoneShapeId);

//Instantiate MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

//Set Milestone Date
milestoneHelper.setMilestoneDate(new DateTime(2015, 8, 1));

//Set IsAutoUpdate to true
milestoneHelper.setAutoUpdate(true);

//RefreshMilesone of timeline shape
milestoneHelper.refreshMilestone(timeline);

//Save Visio file
diagram.save(dataDir + "RefreshMilestone_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
