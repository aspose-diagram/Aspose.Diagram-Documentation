---
title: Recuperar Visio Conectores e información de fuentes
type: docs
weight: 20
url: /es/net/retrieve-visio-connectors-and-font-information/
description: Esta sección explica cómo obtener conectores visio e información de fuentes.
---
## **Recuperación de información del conector**
 Aspose.Diagram for .NET proporciona mecanismos para la recuperación de información - DNI y nombre - sobre[paginas](/diagram/es/net/retrieve-2c-get-2c-copy-and-insert-a-page/) y[Maestro](https://docs.aspose.com/diagram/net/working-with-masters/). También te permite obtener información sobre los conectores, los elementos que unen las formas.

 los[Conectar](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) El objeto representa un conector que une dos formas en una página de dibujo Visio. La propiedad Conecta, expuesta por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La clase admite una colección de objetos Aspose.Diagram.Connect. Esta propiedad se puede utilizar para recuperar información de ID y nombre sobre un conector.
### **Ejemplo de programación**
El siguiente fragmento de código recupera la información de los conectores en un diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.cs" >}}
## **Recuperación de información de fuentes**
 Aspose.Diagram dispone de mecanismos de recuperación de información sobre los elementos que componen un diagram, de[paginas](/diagram/es/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [plantillas](https://docs.aspose.com/diagram/net/working-with-masters/), [conectores](/diagram/es/net/retrieving-connector-information/) también fuentes. Este artículo muestra cómo averiguar qué fuentes se utilizan en un diagram.

 los[Fuente](http://www.aspose.com/api/net/diagram/aspose.diagram/font) objeto representa un tipo de letra que se aplica al texto de un documento o que está disponible para su uso en el sistema. Un objeto Fuente asigna un nombre (por ejemplo, "Arial") al ID de fuente (por ejemplo, 3) que Microsoft Visio almacena en una celda Fuente en una sección Carácter de una forma que contiene texto formateado con esa fuente. Los ID de fuente pueden cambiar cuando se abre un documento en diferentes sistemas o cuando se instalan o eliminan fuentes.
### **Ejemplo de recuperación de programación de fuentes**
El siguiente fragmento de código recupera información de fuente del Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveFontInfo-RetrieveFontInfo.cs" >}}
### **Obtener el directorio de fuentes predeterminado**
Aspose.Diagram for .NET API también permite obtener la ruta del directorio de fuentes predeterminada utilizando el método GetDefaultFontDir() de la clase Diagram. El siguiente fragmento de código recupera el directorio de fuentes predeterminado del Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.cs" >}}
### **Obtener fuentes no utilizadas**
{{% alert color="primary" %}}

Este método es compatible con la versión 19.6 o superior.

{{% /alert %}}

Aspose.Diagram for .NET API también permite obtener fuentes no utilizadas utilizando el método GetUnusedStyles() de la clase Diagram. El siguiente fragmento de código recupera las fuentes no utilizadas del Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetUnusedFonts-1.cs" >}}
