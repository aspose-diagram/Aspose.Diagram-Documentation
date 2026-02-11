---
title: Configurar formas de línea de tiempo Visio
type: docs
weight: 50
url: /es/net/configure-visio-timeline-shapes/
description: Esta sección explica cómo configurar la propiedad de una forma de hito con Aspose.Diagram.
---
## **Establecer propiedades de forma de hito**
Aspose.Diagram permite a los desarrolladores establecer propiedades de hitos. Este artículo muestra cómo configurar la fecha del hito, el formato de fecha, el indicador de actualización automática y el tipo.
### **Configuración de fecha de hito, formato de fecha, indicador de actualización automática y tipo**
 los[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)la clase toma un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objeto mientras se inicializa el[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) objeto. El ejemplo de código de este artículo establece la fecha del hito, el formato de fecha, el indicador de actualización automática y las propiedades del tipo de hito.

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 22;
// Get timeline shape
Shape milestone = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize MilestoneHelper object
Aspose.Diagram.MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set milestone date
milestoneHelper.MilestoneDate = new DateTime(2014, 10, 21);
// Set date format
milestoneHelper.DateFormat = 21;
// Set auto update flag
milestoneHelper.IsAutoUpdate = true;
// Set milestone type
milestoneHelper.Type = 6;

// Save to VDX format
diagram.Save(dataDir + "SetMilestoneProps_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



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
 los[Ayudante de línea de tiempo](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)la clase toma un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objeto al inicializar el[Ayudante de línea de tiempo](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) objeto. El ejemplo de código de este artículo establece los valores de formato de fecha, finalización e inicio del período de tiempo.

El proceso para actualizar el formato de inicio, fin y fecha del período de tiempo es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Inicialice el objeto TimeLineHelper.
1. Establezca el inicio del período de tiempo.
1. Establezca el final del período de tiempo.
1. Establecer un formato de fecha.
1. Guarde el dibujo Visio en cualquier formato compatible.
#### **Establecer período de tiempo y muestra de programación de fecha**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize TimeLineHlper object
Aspose.Diagram.TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.TimePeriodStart = new DateTime(2014, 12, 21);
// Set end time
timelineHelper.TimePeriodFinish = new DateTime(2015, 2, 19);

// Set date format
// TimelineHelper.DateFormatForBE = 21;
// Set date format for intm of timeline shape   
// TimelineHelper.DateFormatForIntm = 21;

// Or

// Set date format string for start and finish of timeline shape
timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";
// Set date format string for intm of timeline shape
timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

// Save to VDX format
diagram.Save(dataDir + "ConfigureTimeLine_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



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
 El método RefreshTimeLine expuesto por el[Ayudante de línea de tiempo](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) La clase se puede utilizar para revivir hitos en la línea de tiempo.

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
Use el siguiente código en su aplicación .NET para revivir hitos en la línea de tiempo usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.TimePeriodStart = new DateTime(2014, 12, 21);
// Set end time
timelineHelper.TimePeriodFinish = new DateTime(2015, 2, 19);

// Set date format
timelineHelper.DateFormatForBE = 21;

// Revive milestones on the timeline
timelineHelper.RefreshTimeLine();

// Save to VDX format
diagram.Save(dataDir + "RefreshTimeLine_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Actualizar hitos en la línea de tiempo usando la clase MilestoneHelper**
 El método RefreshMilestone expuesto por el[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)La clase se puede usar para actualizar hitos en la línea de tiempo.

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
Use el siguiente código en su aplicación .NET para actualizar hitos en la línea de tiempo usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

string pageName = "Page-1";

////////////// Modify time line /////////// 
DateTime startDate = new DateTime(2015, 8, 1);
DateTime endDate = new DateTime(2016, 6, 1);
DateTime fisYear = startDate;

// Load a diagram 
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(pageName);

long timelineId = 1;
Shape timeline = diagram.Pages.GetPage(pageName).Shapes.GetShape(timelineId);
double xpos = timeline.XForm.PinX.Value;
double ypos = timeline.XForm.PinY.Value;

// Add milestone 
string milestoneMasterName = "2 triangle milestone";

// Add Master
diagram.AddMaster(dataDir + "Timeline.vss", milestoneMasterName);

// Add Shape in Visio diagram using AddShape method
long milestoneShapeId = diagram.AddShape(xpos, ypos, milestoneMasterName, 0);

// Get the shape based on ID
Shape milestone = page.Shapes.GetShape(milestoneShapeId);

// Instantiate MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set Milestone Date
milestoneHelper.MilestoneDate = new DateTime(2015, 8, 1);

// Set IsAutoUpdate to true
milestoneHelper.IsAutoUpdate = true;

// RefreshMilesone of timeline shape
milestoneHelper.RefreshMilestone(timeline);

// Save Visio file
diagram.Save(dataDir + "RefreshMilestone_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

