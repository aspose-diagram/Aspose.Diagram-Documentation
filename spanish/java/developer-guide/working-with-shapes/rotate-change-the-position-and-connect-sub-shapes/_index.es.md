---
title: Rotar, cambiar la posición y conectar subformas
type: docs
weight: 60
url: /es/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Girar una forma con ángulo adecuado**
 Aspose.Diagram for Java le permite girar una forma en cualquier ángulo. El método SetAngle expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase se puede usar para rotar una forma a cualquier ángulo deseado. Toma un solo parámetro como un ángulo.
### **Rotar una muestra de programación de forma**
Use el siguiente código en su aplicación Java para rotar una forma usando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Cambiar la posición de una forma**
La clase de forma le permite cambiar la posición de una forma. La línea conectora se ajusta automáticamente cuando la forma se mueve a una posición diferente.

Los métodos Move y MoveTo, expuestos por la clase Shape, admiten cambiar la posición de una forma como parte de un grupo o no.
Los ejemplos de código de este artículo mueven una forma en la página.
**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/cThgWnB.png)


**El diagram después de mover la forma.** 

![todo:imagen_alternativa_texto](http://i.imgur.com/Q3QByqe.png)

El proceso para mover una forma es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Mover forma a una ubicación diferente
1. Guarda el diagram.
### **Ejemplo de programación de cambio de posición**
El fragmento de código siguiente muestra cómo mover la forma. El código recupera una página Visio por nombre y forma por ID 16 y mueve su posición.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Conectar subformas de los grupos**
Este tema explica cómo conectar dos subformas de dos formas de grupo diferentes en diagramas Microsoft Visio usando Aspose.Diagram for Java.

 El método ConnectShapesViaConnector expuesto por el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) La clase se puede usar para conectar las formas por sus ID. El método AddShape, expuesto por el[Diagram](https://reference.aspose.com/diagram/java)clase, se puede utilizar para agregar una forma.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/74rDby5.png)</p>|<p>**El diagram después de la conexión de subformas** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una página en particular.
1. Agregue forma de conector dinámico a la página seleccionada.
1. Conectar subformas
### **Ejemplo de programación de Connect Sub-shapes**
Use el siguiente código en su aplicación Java para conectar las subformas de dos formas de grupos diferentes usando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Obtener las formas conectadas a una forma particular**
[Agregar y conectar Visio Formas](/diagram/es/java/add-and-connect-visio-shapes/) explica cómo agregar una forma y conectarla a otras formas en diagramas Microsoft Visio usando Aspose.Diagram for Java. También es posible encontrar formas que están conectadas a una forma específica.

 El método ConnectedShapes expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase se puede usar para obtener los ID de las formas conectadas a una forma. El método GetShape, expuesto por el[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, se puede usar para encontrar una forma por su ID.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Obtenga los nombres de todas las formas conectadas a la forma seleccionada.
### **Obtener muestra de programación de formas**
Use el siguiente código en su aplicación Java para encontrar todas las formas conectadas a una forma específica usando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
