---
title: Aspose.Diagram for Java 18.2 Notas de la versión
type: docs
weight: 110
url: /es/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Agregue soporte para recuperar el elemento Char relativo de la parte de texto|Mejora|
|DIAGRAMJAVA-50478|Las líneas del conector pasan a través de las otras formas al convertir un VDX a VSDM|Insecto|
|DIAGRAMJAVA-50581|VSDX a PDF - representación incorrecta de las formas|Insecto|
|DIAGRAMJAVA-50582|Salida VSDX - las líneas de conexión no son rectas|Insecto|
|DIAGRAMJAVA-50583|VSD importación: se produjo un error en el elemento VisioDocument|Insecto|
|DIAGRAMJAVA-50584|VDX importación: se produjo un error en el elemento VisioDocument|Insecto|
|DIAGRAMJAVA-50585|VSD importación: se produjo un error en el elemento VisioDocument|Insecto|
|DIAGRAMJAVA-50586|VSDX a SVG: color de borde incorrecto de la forma|Insecto|
### **Agrega el método getInheritChars en la clase Shape**
Contiene los valores de caracteres para la forma heredada por la forma maestra.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
