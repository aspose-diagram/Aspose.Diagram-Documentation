---
title: Establecer Visio Forma XForm, Línea y Datos de relleno
type: docs
weight: 20
url: /es/net/set-visio-shape-s-xform-line-and-fill-data/
description: Esta sección explica cómo configurar el estilo de la forma, incluidos sus datos de línea y datos de relleno con Aspose.Diagram.
---
## **Configuración de datos de XForm**
 El elemento XForm es parte del esquema XML Microsoft Visio. XForm especifica la posición de una forma, por ejemplo, ancho, alto, rotación y si la forma ha sido volteada. los[Formulario X](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) propiedad expuesta por la[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, admite el objeto Aspose.Diagram.XForm. La propiedad XForm se puede usar para recuperar o actualizar los datos XForm de una forma. Los ejemplos de código de este artículo cambian los valores de XForm PinX (coordenada X) y PinY (coordenada Y) para mover las formas en la página.

El proceso para actualizar los datos de XForm es:

1. Cargue un diagram.# Encuentre una forma particular.# Actualice los datos XForm de la forma.
1. Guarda el diagram.
### **Ejemplo de programación**
El fragmento de código a continuación muestra cómo actualizar los datos XForm de una forma. El código busca un proceso de nombres de forma, con el ID de forma 1, y establece sus coordenadas X e Y en 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Establecer Visio datos de línea de forma**
Las formas se pueden formatear de varias maneras. Este artículo muestra cómo especificar los atributos de una línea.

Microsoft Visio permite a los usuarios dar formato a las líneas de varias formas. Aspose.Diagram for .NET admite:

- Peso: el grosor de una línea.
- Color: establezca el color de línea de la forma.
- Transparencia de color de línea: establezca la transparencia de color de línea de la forma en porcentaje.
- Patrón: define si la línea es sólida, discontinua o tiene otro patrón.
- Redondeo: el radio de las esquinas.
- Flechas de inicio y fin: especifica si la línea tiene flechas.
- Tamaños de flecha inicial y final: establezca los tamaños de flecha.
- Cap: el redondeo de los extremos de la línea.
### **Cambie el color de línea, el grosor, el tipo de guión, la transparencia, el redondeo, el tipo de flecha y el tamaño de flecha del borde de una forma**
 los[Línea](http://www.aspose.com/api/net/diagram/aspose.diagram/line) propiedad expuesta por la[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)clase, admite el objeto Aspose.Diagram.Line. Esta propiedad se puede usar para recuperar o actualizar los datos de línea de una forma.
#### **Ejemplo de programación de datos de línea**
El siguiente fragmento de código actualiza los datos de línea de forma.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Establecer los datos de relleno de la forma Visio**
 Las formas se pueden formatear de varias maneras. Este tema describe cómo especificar el relleno de una forma. Microsoft Office Visio permite a los usuarios dar formato a los rellenos de varias formas. los[Llenar](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) La clase de Aspose.Diagram for .NET API admite la configuración:

- Colores de fondo y de primer plano.
- Transparencia.
- Patrones de relleno.
- Oscuridad.
### **Configuración de valores de relleno**
 La propiedad Relleno, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, apoya la[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) objeto. La propiedad Relleno se puede utilizar para recuperar o actualizar los datos de relleno de una forma.
#### **Ejemplo de programación de datos de relleno**
El siguiente fragmento de código actualiza los datos de relleno de una forma. El código busca una forma denominada rectángulo, con el Id. de forma 1, y establece los colores de fondo y de primer plano del relleno.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Recuperar datos de relleno heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de relleno heredados de una forma Visio. La propiedad InheritFill, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene los valores de formato de relleno para la forma heredada por el estilo principal y la forma maestra.
#### **Recuperar muestra de programación de datos de llenado heredados**
El siguiente fragmento de código recupera los datos de relleno heredados de la forma. Por favor revise este código de muestra:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
