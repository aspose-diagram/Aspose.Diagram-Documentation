---
title: Recuperar Visio Conectores e información de fuentes
type: docs
weight: 20
url: /es/java/retrieve-visio-connectors-and-font-information/
---
## **Recuperación de información del conector**
 Aspose.Diagram for Java proporciona mecanismos para la recuperación de información - DNI y nombre - sobre[paginas](/diagram/es/java/retrieve-get-copy-and-insert-a-page/) y[Maestro](). También te permite obtener información sobre los conectores, los elementos que unen las formas.

 los[Conectar](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) El objeto representa un conector que une dos formas en una página de dibujo Visio. La propiedad Conecta, expuesta por el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) La clase admite una colección de objetos Aspose.Diagram.Connect. Esta propiedad se puede utilizar para recuperar información de ID y nombre sobre un conector.

**Una ventana de la consola que muestra el resultado del siguiente código.** 

![todo:imagen_alternativa_texto](retrieve-visio-connectors-and-font-information_1.png)
### **Ejemplo de programación**
El siguiente fragmento de código recupera la información de los conectores en un diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.java" >}}
## **Recuperación de información de fuentes**
 Aspose.Diagram dispone de mecanismos de recuperación de información sobre los elementos que componen un diagram, de[paginas](/diagram/es/java/retrieve-get-copy-and-insert-a-page/), [plantillas](), [conectores](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) también fuentes. Este artículo muestra cómo averiguar qué fuentes se utilizan en un diagram.

 los[Fuente](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) objeto representa un tipo de letra que se aplica al texto de un documento o que está disponible para su uso en el sistema.

Un objeto Fuente asigna un nombre (por ejemplo, "Arial") al ID de fuente (por ejemplo, 3) que Microsoft Visio almacena en una celda Fuente en una sección Carácter de una forma que contiene texto formateado con esa fuente. Los ID de fuente pueden cambiar cuando se abre un documento en diferentes sistemas o cuando se instalan o eliminan fuentes.
### **Ejemplo de recuperación de programación de fuentes**
El siguiente fragmento de código recupera información de fuente del Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveFontInfo-RetrieveFontInfo.java" >}}

![todo:imagen_alternativa_texto](retrieve-visio-connectors-and-font-information_2.png)
### **Obtener el directorio de fuentes predeterminado**
Aspose.Diagram for Java API también permite obtener la ruta del directorio de fuentes predeterminada utilizando el método getDefaultFontDir() de la clase Diagram. El siguiente fragmento de código recupera el directorio de fuentes predeterminado del Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.java" >}}
