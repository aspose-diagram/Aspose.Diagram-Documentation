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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}
