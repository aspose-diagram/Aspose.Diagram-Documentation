---
title: Aspose.Diagram for Java 19.3 Notas de la versión
type: docs
weight: 100
url: /es/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene notas de la versión para Aspose.Diagram for Java 19.3

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|Agregue soporte para recuperar directorios de fuentes comunes en sistemas operativos|Mejora|
|DIAGRAMJAVA-50097|VSD a conversión de PDF - Las líneas curvas se convierten en una línea recta|Insecto|
|DIAGRAMJAVA-50161|Conversión de VTX a HTML: falta la imagen de fondo de todo diagram|Insecto|
|DIAGRAMJAVA-50301|VSD a exportación de PDF: las formas de metatipo se convierten en símbolos desordenados|Insecto|
|DIAGRAMJAVA-50464|La forma se ha renderizado incorrectamente al convertir VSDX a PNG|Insecto|
|DIAGRAMJAVA-50652|VISIO a PDF: el PDF de salida muestra un error en Adobe Reader|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for Java. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega GetDefaultFontDir en Diagram**
Obtener la ruta de la carpeta Fuentes predeterminadas

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
