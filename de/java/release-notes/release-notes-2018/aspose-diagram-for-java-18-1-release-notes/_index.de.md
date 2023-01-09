---
title: Aspose.Diagram for Java 18.1 Versionshinweise
type: docs
weight: 120
url: /de/java/aspose-diagram-for-java-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Diagram for Java 18.1](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-1-release-notes/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50200|Unterstützung zum Duplizieren / Klonen einer diagram-Seite hinzufügen|Erweiterung|
|DIAGRAMJAVA-50408|Nach dem Entfernen einer Seite aus VSDM ist ein Fehler aufgetreten|Insekt|
|DIAGRAMJAVA-50577|VDX bis VSDM - die Verbindungsleitungen sind nicht richtig angeschlossen|Insekt|
|DIAGRAMJAVA-50578|VDX bis VSDM - die Verbindungsleitungen sind nicht richtig angeschlossen|Insekt|
|DIAGRAMJAVA-50579|Ausgabe VDX - Platzierung aller Visio-Formen auf dem gleichzeitigen Punkt|Insekt|
|DIAGRAMJAVA-50580|Ausgabe VDX - falsches Layout der Shapes|Insekt|
### **Fügt Copy-Member in der Page-Klasse hinzu**
Das Kopieelement verwendet eine Zielseiteninstanz als Parameter zum Klonen dieser Seite.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy page

newPage.copy(diagram.getPages().get(0));

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Seite Visio in eine andere Seiteninstanz kopieren]
