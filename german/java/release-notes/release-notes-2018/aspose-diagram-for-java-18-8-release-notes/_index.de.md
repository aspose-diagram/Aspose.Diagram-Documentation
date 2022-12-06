---
title: Aspose.Diagram for Java 18.8 Versionshinweise
type: docs
weight: 50
url: /de/java/aspose-diagram-for-java-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for Java 18.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-8-release-notes/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50611|Unterstützung für das Festlegen des Gebietsschemas mit API|Erweiterung|
|DIAGRAMJAVA-50606|VSDX zu SVG - falsche Darstellung der Pfeile|Insekt|
|DIAGRAMJAVA-50610|Die Position von Text auf Konnektoren ist in der Ausgabedatei VSDX falsch|Insekt|
|DIAGRAMJAVA-50612|Die Ausgabedatei VDX kann mit Visio Viewer 2010 Professional nicht geöffnet werden|Insekt|
## **Öffentliche API und rückwärts inkompatible Änderungen**
Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for Java vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
#### **setLocale in LoadOption hinzugefügt**
{{< highlight "java" >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

legt das Gebietsschema fest, das zum Zeitpunkt des Ladens der Datei für diagram verwendet wurde.
