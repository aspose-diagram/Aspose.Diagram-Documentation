---
title: Agrupar, convertir y verificar formas
type: docs
weight: 80
url: /es/net/group-convert-and-verify-shapes/
description: Esta sección explica cómo agrupar formas con Aspose.Diagram.
---
## **Agrupe varias formas juntas en el dibujo Visio**
Aspose.Diagram API permite a los desarrolladores agrupar formas para moverlas todas a la vez. Cada forma en un grupo mantiene una identidad única y tiene su propio conjunto de propiedades. Cuando cambiamos el formato de un grupo de formas, asigna la nueva propiedad a cada forma.
### **Cómo agrupar formas**
 El método de grupo expuesto por el[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) La clase se puede utilizar para agrupar formas.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. inicializó una matriz de las formas
1. obtener una forma particular por id.
1. obtener otra forma particular particular por id.
1. asignar formas a la matriz.
1. formas de grupo llamando al método Group.
1. guardar diagram
#### **Ejemplo de programación de formas grupales**
Use el siguiente código en su aplicación .NET para agrupar formas usando Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **Convierta una forma Visio a otros formatos de archivo**
Aspose.Diagram for .NET API permite a los desarrolladores convertir una sola forma Visio a cualquier otro formato de archivo compatible. En este artículo, eliminamos todas las demás formas Visio de la página y personalizamos la configuración de la página según el tamaño de la forma de origen.
### **Convertir una forma particular Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **especificando las opciones de guardado Visio**.
Este código de ejemplo funciona de la siguiente manera:

1. Cargue una fuente Visio.
1. Obtener una página en particular.
1. Eliminar la página de fondo.
1. Cree una tabla hash de todas las formas que contenga las identificaciones y los nombres.
1. Iterar a través de la tabla hash
1. Elimina todas las formas de la página Visio, excepto la particular.
1. Establezca el tamaño de la página.
1. Guarde la página Visio en cualquier formato de archivo compatible.
#### **Ejemplo de programación de conversión de formas**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Verifique si dos formas Visio están conectadas o pegadas**
 Aspose.Diagram for .NET API permite a los desarrolladores verificar que las dos formas Visio estén pegadas o conectadas. Anteriormente, hemos visto cómo podemos conectar o pegar dos formas en estos temas de ayuda:[Agregar y conectar Visio Formas](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) y[Pegue las formas dentro del recipiente](/diagram/es/net/working-with-shapes-gluing/).
### **Verificación de las Formas Conectadas o Pegadas**
 los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ofrece las propiedades IsGlued e IsConnected para determinar si dos formas están pegadas o conectadas.
#### **Muestra de Programación de Verificación de Formas Conectadas o Pegadas**
El siguiente fragmento de código verifica si dos formas están conectadas o pegadas.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Verifique si la forma Visio está en un grupo de formas**
Aspose.Diagram for .NET API permite a los desarrolladores verificar si la forma Visio está en un grupo de formas o no.
### **Verificación de Forma en el Grupo de Formas**
los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class ofrece propiedades IsInGroup para determinar si la forma Visio está en una forma de grupo.
#### **Verificación de la forma en el ejemplo de programación del grupo de formas**
El siguiente fragmento de código verifica si la forma está en una forma de grupo.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
