---
title: Público API Cambios en Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /es/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.6.0 a la 5.7.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **Establecer cadenas de patrón de fecha en la línea de tiempo**
Se agregaron los nuevos métodos setDateFormatStringForBE y setDateFormatStringForIntm en la clase TimelineHelper. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
