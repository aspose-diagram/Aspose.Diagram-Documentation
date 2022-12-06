---
title: Trabajar con texto
type: docs
weight: 120
url: /es/java/working-with-text/
---
## **Insertar una forma de texto en la página Visio**
 Aspose.Diagram API permite a los desarrolladores insertar una forma de texto en cualquier lugar de la página Visio. Para lograr esto, el método addText del[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) La clase toma los parámetros PinX, PinY, ancho, alto y texto.
### **Insertar una muestra de programación de forma de texto**
El siguiente fragmento de código agrega una forma de texto en el Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-InsertTextShape-InsertTextShape.java" >}}
## **Actualizar Visio Texto de forma**
 Tanto como[creando diagramas](/diagram/es/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java le permite trabajar con formas de diferentes maneras. Este artículo analiza cómo acceder y actualizar el texto en las formas.

 La propiedad Text, expuesta por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) clase, admite el objeto Aspose.Diagram.Text. La propiedad se puede utilizar para recuperar o actualizar el texto de una forma.

**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/6aEp7h0.png)

**Diagram después de que el texto en la forma central se haya cambiado de Proceso a Texto nuevo** 

![todo:imagen_alternativa_texto](http://i.imgur.com/o977cxw.png)

El proceso para actualizar el texto de una forma es sencillo:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Establecer el nuevo texto.
1. Guarda el diagram.
### **Actualizar muestra de programación de texto de forma**
El siguiente fragmento de código actualiza el texto de una forma. Las formas se identifican por sus ID. Los segmentos de código a continuación buscan una forma llamada proceso y con el ID 1 y cambia su texto.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-UpdateShapeText-UpdateShapeText.java" >}}
## **Aplicar una hoja de estilo integrada o personalizada a una forma Visio**
Microsoft Visio Las hojas de estilo almacenan información de formato que se puede aplicar a las formas para lograr una apariencia uniforme. Aspose.Diagram for Java le permite aplicar hojas de estilo desde dentro de una aplicación.

 Las propiedades TextStyle, FillStyle y LineStyle expuestas por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) apoyo de la clase[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) objeto. La propiedad se puede utilizar para recuperar información de estilo y aplicar estilos personalizados de texto, línea y relleno a un diagram.

**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/feV1x2N.png)

**El diagram después de aplicar una hoja de estilo personalizada que define estilos de texto, línea y relleno** 

![todo:imagen_alternativa_texto](http://i.imgur.com/Xk9W0wN.png)
### **Estilos personalizados en Microsoft Visio**
Para aplicar estilos personalizados a formas en Microsoft Visio:

1. Abra un diagram en Microsoft Visio.
1.  Seleccione**Definir estilos** desde el**Formato** menú (Visio 2007), o haga clic con el botón derecho**Estilos** en el**Explorador de dibujo** ventana y seleccione**Definir estilos** (Visio 2010).
1.  En el**Definir estilos** cuadro de diálogo, escriba un nuevo nombre para su hoja de estilo personalizada. Por ejemplo, CustomStyle1.
1.  Haga clic en el**Texto**, **Línea** y**Llenar** botones para establecer estilos de texto, línea y relleno respectivamente.
1.  Hacer clic**OK**.

Después de definir hojas de estilo personalizadas en Microsoft Visio, use el siguiente código en una aplicación Java para aplicar estilos personalizados a sus formas. Tenga en cuenta que los ejemplos de código a continuación llaman a la hoja de estilo personalizada definida anteriormente: necesita saber el nombre y la ubicación de la hoja que aplica.

Para aplicar estilos personalizados mediante programación:

1. Cargue un diagram.
1. Encuentre la forma a la que desea aplicar un estilo.
1. Cargue la hoja de estilo.
1. Aplicar estilos.
1. Guarda el diagram.
#### **Aplicar muestra de programación de estilos personalizados**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.java" >}}
## **Aplicar un estilo diferente en cada valor de texto de una forma**
 Tanto como[creando diagramas](/diagram/es/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java le permite trabajar con formas de diferentes maneras. Este artículo ayuda a agregar múltiples valores de texto a una forma y aplicar un estilo diferente en cada valor de texto.

{{% alert color="primary" %}} 

El elemento Forma contiene un elemento denominado Texto, que contiene los caracteres del texto y elementos especiales (cp, pp, tp y fld) que marcan el final de una ejecución y el comienzo de la siguiente. Char Element contiene los atributos de formato para el texto de la forma, como fuente, color, estilo de texto, mayúsculas y minúsculas, posición relativa a la línea de base y tamaño de punto.

{{% /alert %}} 
### **Adición de texto y estilos de formas**
**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/ZqgQPQC.png)

**Diagram después de agregar varios valores de texto a una forma con un estilo diferente en cada valor de texto** 

![todo:imagen_alternativa_texto](http://i.imgur.com/7UWhFbU.png)
#### **Ejemplo de programación de adición de texto y estilos**
El siguiente fragmento de código agrega el texto de una forma y diferentes estilos.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyFontOnText-ApplyFontOnText.java" >}}
## **Buscar y reemplazar el texto de una forma**
 los[TXT](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) La clase le permite editar el texto de la forma. El método Reemplazar, expuesto por el[TXT](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) class, admite cambiar el texto de una forma.
Los ejemplos de código de este artículo buscan y reemplazan el texto de la forma en la página.

**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/lW5xaP0.png)


**El diagram después de editar la forma.** 

![todo:imagen_alternativa_texto](http://i.imgur.com/m33W1Tk.png)

El proceso para cambiar el texto de la forma:

1. Cargue un diagram.
1. Encuentra un texto particular de una forma.
1. Reemplazar el texto de esta forma
1. Guarda el diagram.
### **Ejemplo de programación de buscar y reemplazar texto**
Los fragmentos de código a continuación muestran cómo modificar el texto de la forma. El código itera a través de las formas de una página.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.java" >}}
## **Extraer texto sin formato de la página Visio Diagram**
Aspose.Diagram API permite a los desarrolladores extraer texto sin formato de la página Visio diagram. También pueden iterar a través de las páginas Visio diagram para cubrir todo el texto Visio diagram.

 Microsoft Office Visio agrega el texto a las formas. los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class contiene un elemento llamado Texto, que contiene los caracteres del texto y elementos especiales (cp, pp, tp y fld) que marcan el final de una ejecución y el comienzo de la siguiente.
### **Extraer muestra de programación de texto sin formato**
El siguiente fragmento de código itera a través de las formas de la página Visio y filtra el texto sin formato sin información de formato.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.java" >}}
