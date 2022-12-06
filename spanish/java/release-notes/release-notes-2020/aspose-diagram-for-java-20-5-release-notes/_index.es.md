---
title: Aspose.Diagram for Java 20.5 Notas de la versión
type: docs
weight: 30
url: /es/java/aspose-diagram-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for Java 20.5.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50487|Elementos de texto desplazados al convertir un VSD a SVG|Mejora|
|DIAGRAMJAVA-50692|Texto en negrita colocado incorrectamente al guardar VSDX como SVG|Mejora|
|DIAGRAMJAVA-50693|Las imágenes no están presentes en la salida SVG|Insecto|
|DIAGRAMJAVA-50695|No se puede guardar el archivo VSDX como una imagen: arroja NullPointerException|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados en el API público, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram para JAVA. Si tiene inquietudes sobre algún cambio en la lista, plantéelo en el foro de soporte Aspose.Diagram.
### **Agrega isIntersect en Shape**
Indica si esta forma se cruza con otra forma.

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
