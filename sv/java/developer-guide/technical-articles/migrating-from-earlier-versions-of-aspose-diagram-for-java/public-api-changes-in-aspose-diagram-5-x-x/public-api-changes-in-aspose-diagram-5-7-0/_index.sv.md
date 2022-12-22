---
title: Offentlig API Ändringar i Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /sv/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.6.0 till 5.7.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Ställ in datummönstersträngar på tidslinjen**
De nya metoderna setDateFormatStringForBE och setDateFormatStringForIntm har lagts till i klassen TimelineHelper. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
