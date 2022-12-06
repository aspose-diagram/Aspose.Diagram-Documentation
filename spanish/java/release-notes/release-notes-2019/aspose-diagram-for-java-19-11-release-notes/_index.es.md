---
title: Aspose.Diagram for Java 19.11 Notas de la versión
type: docs
weight: 20
url: /es/java/aspose-diagram-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for Java 19.11.

{{% /alert %}} 
## **Mejoras y Cambios**
El lanzamiento de este mes permite formatear Visio páginas por[aplicar hojas de estilo](/diagram/es/java/format-visio-pages/).

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50671|La configuración de la nueva ventana de la hoja de forma no se respeta al convertir a SVG|Mejora|
### **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados en el API público, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram para JAVA. Si tiene inquietudes sobre algún cambio en la lista, plantéelo en el foro de soporte Aspose.Diagram.
### **Se agregó applyStyle en la página**
{{< highlight "java" >}}

 StyleSheet st = new StyleSheet();

dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### ` `**Eliminación agregada en la clase Diagram**
Realiza tareas definidas por la aplicación asociadas con la liberación, la liberación o el restablecimiento de recursos no administrados.

{{< highlight "java" >}}

 diagram.dispose();

{{< /highlight >}}
