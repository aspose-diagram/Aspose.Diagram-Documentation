---
title: Aspose.Diagram for Java 19.11 Versionshinweise
type: docs
weight: 20
url: /de/java/aspose-diagram-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.Diagram for Java 19.11.

{{% /alert %}} 
## **Verbesserungen und Änderungen**
Die Version dieses Monats ermöglicht die Formatierung von Visio Seiten durch[Stylesheets anwenden](/diagram/de/java/format-visio-pages/).

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50671|Die Einstellung für das neue Fenster des Formblatts wird beim Konvertieren in SVG nicht berücksichtigt|Erweiterung|
### **Öffentliche API und rückwärts inkompatible Änderungen**
Das Folgende ist eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram für JAVA vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte im Aspose.Diagram-Supportforum.
### **applyStyle in Seite hinzugefügt**
{{< highlight "java" >}}

 StyleSheet st = new StyleSheet();

dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### ` `**Entsorgung in Klasse Diagram hinzugefügt**
Führt anwendungsdefinierte Aufgaben im Zusammenhang mit dem Freigeben, Freigeben oder Zurücksetzen nicht verwalteter Ressourcen aus.

{{< highlight "java" >}}

 diagram.dispose();

{{< /highlight >}}
