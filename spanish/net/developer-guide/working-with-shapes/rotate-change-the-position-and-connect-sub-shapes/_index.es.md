---
title: Rotar, cambiar la posición y conectar subformas
type: docs
weight: 30
url: /es/net/rotate-change-the-position-and-connect-sub-shapes/
description: Esta sección explica cómo rotar una forma visio con Aspose.Diagram.
---
## **Girar una forma con ángulo adecuado**
 Aspose.Diagram for .NET le permite girar una forma en cualquier ángulo. El método SetAngle expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede usar para rotar una forma a cualquier ángulo deseado. Toma un solo parámetro como un ángulo.
### **Rotar una muestra de programación de forma**
Use el siguiente código en su aplicación .NET para rotar una forma usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **Cambiar la posición de una forma**
 los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase le permite cambiar la posición de una forma. La línea conectora se ajusta automáticamente cuando la forma se mueve a una posición diferente. Los métodos Move y MoveTo, expuestos por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, admite cambiar la posición de una forma como parte de un grupo o no. Los ejemplos de código de este artículo mueven una forma en la página.

El proceso para mover una forma es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Mover forma a una ubicación diferente
1. Guarda el diagram.
### **Ejemplo de programación de cambio de posición**
El fragmento de código siguiente muestra cómo mover la forma. El código recupera una página Visio por nombre y forma por ID 16 y mueve su posición.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **Conectar subformas de los grupos**
 Este tema explica cómo conectar dos subformas de dos formas de grupo diferentes en diagramas Microsoft Visio usando Aspose.Diagram for .NET. El método ConnectShapesViaConnector expuesto por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La clase se puede usar para conectar las formas por sus ID. El método AddShape, expuesto por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)clase, se puede utilizar para agregar una forma.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una página en particular.
1. Agregue forma de conector dinámico a la página seleccionada.
1. Conectar subformas
### **Ejemplo de programación de Connect Sub-shapes**
Use el siguiente código en su aplicación .NET para conectar las subformas de dos formas de grupos diferentes usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **Obtener las formas conectadas a una forma particular**
[Agregar y conectar Visio Formas](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) explica cómo agregar una forma y conectarla a otras formas en diagramas Microsoft Visio usando Aspose.Diagram for .NET. También es posible encontrar formas que están conectadas a una forma específica.

 El método ConnectedShapes expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede usar para obtener los ID de las formas conectadas a una forma. El método GetShape, expuesto por el[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, se puede usar para encontrar una forma por su ID.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Obtenga los nombres de todas las formas conectadas a la forma seleccionada.
### **Obtener muestra de programación de formas**
Use el siguiente código en su aplicación .NET para encontrar todas las formas conectadas a una forma específica usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
