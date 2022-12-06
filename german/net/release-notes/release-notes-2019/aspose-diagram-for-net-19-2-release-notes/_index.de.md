---
title: Aspose.Diagram for .NET 19.2 Versionshinweise
type: docs
weight: 110
url: /de/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50009|Die Herzform wird beim Exportieren der Zeichnung VSD im PDF-Dateiformat verwechselt|Erweiterung|
|DIAGRAMNET-50010|VSD in PDF exportiert mehrere Zickzacklinien mit einem gleichzeitigen Punkt anstelle einer einzelnen Kurvenlinie|Erweiterung|
|DIAGRAMNET-51257|Unterstützung der NUBRS-Linie beim Exportieren einer Zeichnung hinzufügen|Erweiterung|
|DIAGRAMNET-51611|Prop.Prompt.Value kann nicht korrekt abgerufen werden|Erweiterung|
|DIAGRAMNET-50355|Gebogene Linien werden als gerade Linien exportiert|Insekt|
|DIAGRAMNET-50702|VSDX zum PDF-Export - die gebogenen Verbinder werden gerade|Insekt|
|DIAGRAMNET-51348|VSDX zu PDF - Falsche Wiedergabe von Buchstaben|Insekt|
|DIAGRAMNET-51399|VSD in PNG - die gekrümmte Linie wird in eine gerade Linie umgewandelt|Insekt|
|DIAGRAMNET-51448|VSD zu PNG - die Ellipse fehlt um das Wort Netzwerk|Insekt|
|DIAGRAMNET-51472|VSD in PDF - die gekrümmten Linien werden als gerade Linien exportiert|Insekt|
|DIAGRAMNET-51507|VSDX zu PNG - gefüllte ovale Formen fehlen in der Ausgabe|Insekt|
|DIAGRAMNET-51508|VSDX zu SVG - gefüllte ovale Formen fehlen in der Ausgabe|Insekt|
|DIAGRAMNET-51537|VSDX in SVG – gebogene Verbinder werden zu geraden Verbindern, wenn VSDX in PDF gerendert wird|Insekt|
|DIAGRAMNET-51540|Formkanten wurden nach der Konvertierung in quadratisch geändert|Insekt|
|DIAGRAMNET-51577|VISIO zu SVG - Ausgabe ist nicht korrekt|Insekt|
|DIAGRAMNET-51592|Gebogene Linien werden während der Konvertierung in gerade Linien umgewandelt|Insekt|
|DIAGRAMNET-51600|Gerade Linien werden zu Spitzen, wenn eine diagram als anderes Format gespeichert wird|Insekt|
|DIAGRAMNET-51604|VSDX zu PDF-Konvertierungsfehler - schwarze Ellipsen|Insekt|
|DIAGRAMNET-51605|Aktualisieren Sie API-Referenzen und fügen Sie Details zur Shape.SetAngle()-Methode hinzu|Insekt|
|DIAGRAMNET-51610|VSDX zu SVG - Text wird nicht in der richtigen Schriftart wiedergegeben|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügen Sie InheritProps in Form hinzu**
Enthält die Requisiten für die Form, die von der Masterform geerbt wird.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
