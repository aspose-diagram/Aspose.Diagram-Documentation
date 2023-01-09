---
title: Trabajar con el pegado de formas
type: docs
weight: 10
url: /es/java/working-with-shapes-gluing/
---
## **Obtenga los conectores pegados a una forma particular**
[Agregar y conectar Visio Formas](/diagram/es/java/add-and-connect-visio-shapes/) explica cómo agregar una forma y conectarla a otras formas en diagramas Microsoft Visio usando Aspose.Diagram for Java. También es posible encontrar conectores que están pegados a esta forma.
### **Conseguir formas pegadas**
 El método GluedShapes expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)La clase se puede usar para obtener una lista de los ID de todos los conectores pegados a una forma o, si la forma en cuestión es un conector, los ID de las formas a las que está conectado. El método GetShape, expuesto por el[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, se puede usar para encontrar una forma por su ID.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Obtenga una lista de ID de todos los conectores pegados a esta forma.
#### **Obtenga una muestra de programación pegada de conectores**
Use el siguiente código en su aplicación Java para encontrar todos los conectores pegados a una forma usando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Pegue las formas Visio junto con el punto de conexión**
Aspose.Diagram for Java permite a los desarrolladores unir formas a través de los puntos de conexión.
### **Formas de pegamento**
 El método GlueShapes expuesto por el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Se puede usar la clase.

|<p>**Entrada diagram** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/Z69f4hg.png)</p>|<p>**El diagram después de pegar las formas.** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Pega formas.
1. Guardar diagram.
#### **Pegamento Visio Muestra de programación de formas**
Use el siguiente código en su aplicación Java para pegar formas a través de los puntos de conexión:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Pegue las formas dentro del recipiente**
Aspose.Diagram for Java permite a los desarrolladores pegar formas grupales dentro de un contenedor.
### **Forma de grupo de pegamento**
Se puede usar el método GlueShapesInContainer expuesto por la clase Page.

|<p>**Entrada diagram** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/HRRzIEh.png)</p>|<p>**El diagram después de pegar las formas del grupo.** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Pegue las formas del grupo.
1. Guardar diagram.
#### **Muestra de programación de formas de pegamento en el interior**
Use el siguiente código en su aplicación Java para pegar la forma del grupo dentro de un contenedor:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
