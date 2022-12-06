---
title: Aspose.Diagram for Java 20.2 Notas de la versión
type: docs
weight: 60
url: /es/java/aspose-diagram-for-java-20-2-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for Java 20.2.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50361|El color de primer plano de la forma no se conserva al convertir un VST a PNG|Mejora|
|DIAGRAMJAVA-50504|VSD a PDF: se cambia el color de las líneas|Mejora|
## ` `**Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for Java. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Añadido ampliar página en ImageSaveOptions**
- Especifica si ampliar la página

{{< highlight "java" >}}

 com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);

opt.setEnlargePage(false);

{{< /highlight >}}
### **Se agregó hasHiddenInfo en Diagram**
- Indica si este diagram tiene información oculta

{{< highlight "java" >}}

 diagram.hasHiddenInfo();

{{< /highlight >}}




