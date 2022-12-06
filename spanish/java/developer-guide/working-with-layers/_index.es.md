---
title: Trabajar con capas
type: docs
weight: 160
url: /es/java/working-with-layers/
---
### **Configuración de objetos de forma con capas**
Aspose.Diagram for Java permite configurar objetos de forma con capas en Microsoft Office Visio diagram. Cada forma puede pertenecer a varias capas para que los desarrolladores puedan administrar las formas para satisfacer las necesidades del usuario final.

 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) El objeto de clase ofrece la propiedad LayerMember que permite agregar / eliminar objetos de forma a / desde las capas en el dibujo Visio. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:

**Agregue, elimine y mueva objetos de forma a / desde capas del diagram.** 

![todo:imagen_alternativa_texto](working-with-layers_1.png)

El siguiente fragmento de código ayuda a agregar, eliminar y mover propiedades de objetos de forma.
#### **Ejemplos de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-ConfigureShapeLayers-ConfigureShapeLayers.java" >}}
### **Agregar una capa en la hoja de página Visio**
Aspose.Diagram for Java permite a los desarrolladores agregar nuevas capas para organizar categorías personalizadas de formas y luego asignar formas a esas capas mediante programación.

 los[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class ofrece un método add que permite agregar un nuevo[Capa](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)objeto de clase en el dibujo Visio. Los desarrolladores pueden establecer las propiedades de la capa inicializando su objeto de clase.

El siguiente fragmento de código ayuda a agregar objetos de capa.
#### **Ejemplos de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-AddLayer-AddLayer.java" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Java brinda a los desarrolladores acceso a las capas existentes de Visio diagram.

{{% /alert %}} 
### **Obtener todas las capas disponibles**
 los[PáginaHoja](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propiedad de la[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permite recuperar la lista de capas disponibles del Visio diagram usando[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) clase.

El siguiente fragmento de código ayuda a obtener una lista de capas.
#### **Ejemplos de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-RetrieveAllLayers-RetrieveAllLayers.java" >}}
