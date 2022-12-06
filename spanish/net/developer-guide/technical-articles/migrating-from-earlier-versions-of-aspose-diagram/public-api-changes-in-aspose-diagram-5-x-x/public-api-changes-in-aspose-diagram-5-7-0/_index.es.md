---
title: Público API Cambios en Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /es/net/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.6.0 a la 5.7.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Establecer cadenas de patrón de fecha en la línea de tiempo**
Las nuevas propiedades DateFormatStringForBE y DateFormatStringForIntm se han agregado en la clase TimelineHelper. Códigos de ejemplo:

**C#**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";

// set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd"

' set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd"

{{< /highlight >}}
