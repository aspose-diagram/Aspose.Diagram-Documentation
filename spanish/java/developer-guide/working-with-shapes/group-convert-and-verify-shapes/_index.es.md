---
title: Agrupar, convertir y verificar formas
type: docs
weight: 50
url: /es/java/group-convert-and-verify-shapes/
---
## **Agrupe varias formas juntas en el dibujo Visio**
Aspose.Diagram API permite a los desarrolladores agrupar formas para moverlas todas a la vez. Cada forma en un grupo mantiene una identidad única y tiene su propio conjunto de propiedades. Cuando cambiamos el formato de un grupo de formas, asigna la nueva propiedad a cada forma.
### **Cómo agrupar formas**
El método Group expuesto por la clase ShapeCollection se puede usar para agrupar formas.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. inicializó una matriz de las formas
1. obtener una forma particular por id.
1. obtener otra forma particular particular por id.
1. asignar formas a la matriz.
1. formas de grupo llamando al método Group.
1. guardar diagram
#### **Ejemplo de programación de formas grupales**
Use el siguiente código en su aplicación Java para agrupar formas usando Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Convierta una forma Visio a otros formatos de archivo**
Aspose.Diagram for Java API permite a los desarrolladores convertir una sola forma Visio a cualquier otro formato de archivo compatible. En este artículo, eliminamos todas las demás formas Visio de la página y personalizamos la configuración de la página según el tamaño de la forma de origen.
### **Convertir una forma particular Visio**
 Los desarrolladores pueden convertir una forma Visio a PDF, HTML, imagen, SVG y SWF mediante[especificando las opciones de guardado Visio]().
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Convertir Visio Forma a PDF**
El método ToPdf de la clase Shape permite convertir una forma al formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convertir Visio Forma a HTML**
El método ToHTML de la clase Shape permite convertir una forma al formato HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}} 
## **Verifique si dos formas Visio están conectadas o pegadas**
 Aspose.Diagram for Java API permite a los desarrolladores verificar que las dos formas Visio estén pegadas o conectadas. Anteriormente, hemos visto cómo podemos conectar o pegar dos formas en estos temas de ayuda:[Agregar y conectar Visio Formas](/diagram/es/java/add-and-connect-visio-shapes/) y[Pegue las formas dentro del recipiente](/diagram/es/java/working-with-shapes-gluing/).
### **Verificación de las Formas Conectadas o Pegadas**
 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class ofrece las propiedades IsGlued e IsConnected para determinar si dos formas están pegadas o conectadas.
#### **Muestra de Programación de Verificación de Formas Conectadas o Pegadas**
El siguiente fragmento de código verifica si dos formas están conectadas o pegadas.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Verifique si la forma Visio está en un grupo de formas**
Aspose.Diagram for Java API permite a los desarrolladores verificar si la forma Visio está en un grupo de formas o no.
### **Verificación de Forma en el Grupo de Formas**
La clase Shape ofrece propiedades IsInGroup para determinar si la forma Visio está en una forma de grupo.
#### **Verificación de la forma en el ejemplo de programación del grupo de formas**
El siguiente fragmento de código verifica si la forma está en una forma de grupo.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
