---
title: Aspose.Diagram for .NET 21.12 Versionshinweise
type: docs
weight: 1
url: /de/net/aspose-diagram-for-net-21-12-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 21.12.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-52408|Probleme, wenn wir das EmfRederSetting EmfPlusPrefer verwenden|Erweiterung|
|DIAGRAMNET-52438|SaveForegroundPagesOnly zum Drucken|Erweiterung|
|DIAGRAMNET-52450|Visio zu SVG - Rasterbild separat speichern|Erweiterung|
|DIAGRAMNET-51171|Teildarstellung der Formen beim Speichern der Zeichnung im PDF-Format|Insekt|
|DIAGRAMNET-51390|Eingebettetes Objekt wird nicht richtig ersetzt|Insekt|
|DIAGRAMNET-51800|Visio zu SVG - Hintergrundbild fehlt (PowerPoint wird in VISIO hinzugefügt)|Insekt|
|DIAGRAMNET-52423|Page.Copy() kopiert kein Excel-Objekt in diagram|Insekt|
|DIAGRAMNET-52443|Fehlende Formen beim Öffnen und Speichern von MS Visio Diagram|Insekt|
|DIAGRAMNET-52444|Visio zu JPG - Unterschiedliche Ergebnisse, die von API generiert werden|Insekt|
|DIAGRAMNET-52445|Das Konvertieren des Beispiels in der Linux- und Windows-Umgebung führt zu unterschiedlichen Ergebnissen|Insekt|

## **Öffentliche API und rückwärtsinkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.


### **Fügt IsSavingImageSeparately in SVGSaveOptions hinzu**
- Legt fest, ob das Bild separat gespeichert wird.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.IsSavingImageSeparately = true;

{{< /highlight >}}


### **Fügt CustomImagePath in SVGSaveOptions hinzu**
- Der benutzerdefinierte Pfad (URL) des Benutzers, der in der generierten SVG-Datei für das Bild gespeichert ist. Wenn nicht vom Benutzer definiert, wird das aktuelle Verzeichnis verwendet.

{{< highlight "java" >}}

  o.CustomImagePath = "d:/output/";

{{< /highlight >}}

### **Fügt SaveForegroundPagesOnly in PrintSaveOptions hinzu**
- Gibt an, ob alle Seiten gedruckt werden oder nur der Vordergrund.

{{< highlight "java" >}}

 PrintSaveOptions options = new PrintSaveOptions();
 options.SaveForegroundPagesOnly = true;

{{< /highlight >}}
