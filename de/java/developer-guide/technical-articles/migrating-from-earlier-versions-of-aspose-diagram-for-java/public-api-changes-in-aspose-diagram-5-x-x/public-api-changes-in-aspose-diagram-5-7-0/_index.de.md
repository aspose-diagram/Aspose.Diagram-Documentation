---
title: Öffentlich API Änderungen in Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /de/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 5.6.0 auf 5.7.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Legen Sie Datumsmusterzeichenfolgen auf der Zeitachse fest**
Die neuen Methoden setDateFormatStringForBE und setDateFormatStringForIntm wurden in der TimelineHelper-Klasse hinzugefügt. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
