---
title: Aspose.Diagram for .NET 19.11 Versionshinweise
type: docs
weight: 20
url: /de/net/aspose-diagram-for-net-19-11-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for .NET 19.11.

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50004| Unterstützung hinzufügen[Stylesheet anwenden](/diagram/de/net/format-visio-pages/) für ganze Seite|Erweiterung|
|DIAGRAMNET-50576|Unterstützung zum Verwerfen eines Diagram-Klassenobjekts hinzugefügt|Erweiterung|
|DIAGRAMNET-50098|Legen Sie die Hintergrundfarbe der Seite fest|Insekt|
|DIAGRAMNET-51722|Diagram zu SVG - Ausgabebild ist fehlerhaft|Insekt|
|DIAGRAMNET-51724|Fehler in der Chrome-Konsole beim Anzeigen von Ausgabe-SVG|Insekt|
|DIAGRAMNET-51725|Rufen Sie den Z-Index von Formen in Diagram ab|Insekt|
|DIAGRAMNET-51726|Hintergrundbild fehlt (PowerPoint wird in VISIO hinzugefügt), während unbenutzte Masterformen und -stile entfernt werden|Insekt|
|DIAGRAMNET-51727|CheckBox (CheckBox-Steuerelement) Fehlt beim Entfernen nicht verwendeter Masterformen und -stile|Insekt|
|DIAGRAMNET-51728|Linie fehlt beim Entfernen unbenutzter Masterformen und -stile|Insekt|

## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden das Aspose.Diagram Support-Forum.
### **ApplyStyle in Seite hinzugefügt**
Wendet den Stil auf die ganze Seite an.

{{< highlight "java" >}}

StyleSheet st = new StyleSheet();

st.ID = dia.StyleSheets.Count + 1;

Aspose.Diagram.Char ch = new Aspose.Diagram.Char();

ch.Color.Value = "#00ff00";

ch.IX = 0;

st.Chars.Add(ch);

st.Line.LineColor.Value = "#ff0000";

st.Line.LinePattern.Value = 1;

st.Line.LineWeight.Value = 0.01;

st.Fill.FillForegnd.Value = "#0000ff";

st.Fill.FillPattern.Value = 1;

st.Fill.ShdwPattern.Value = 0;

dia.StyleSheets.Add(st);

foreach (Shape shape in dia.Pages[0].Shapes)

{

     shape.Line.LinePattern.Value = 1;
    
     shape.Fill.FillPattern.Value = 1;

}

dia.Pages[0].ApplyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### **Entsorgung in Diagram hinzugefügt**
Führt anwendungsdefinierte Aufgaben im Zusammenhang mit dem Freigeben, Freigeben oder Zurücksetzen nicht verwalteter Ressourcen aus.

{{< highlight "java" >}}

 diagram.Dispose();

{{< /highlight >}}
