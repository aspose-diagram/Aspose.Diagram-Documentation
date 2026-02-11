---
title: Öffnen Sie das Dokument Visio programmgesteuert
linktitle: Öffnen Sie das Dokument Visio
type: docs
weight: 20
url: /de/java/open-visio-document/
description: Auf dieser Seite wird beschrieben, wie Sie das Dokument Visio mit der Bibliothek Aspose.Diagram von Grund auf öffnen.
---
## **Lesen Sie eine vorhandene Visio-Zeichnung**
Aspose.Diagram API unterstützt das Erstellen der neuen Visio-Diagramme von Grund auf und das anschließende Speichern in einem beliebigen unterstützten Dateiformat. Entwickler können auch eine vorhandene Visio diagram zum Ändern, Hinzufügen oder Verarbeiten laden.
### **Lesen einer Diagram**
Mit Aspose.Diagram API können Entwickler alle unterstützten Visio-Dateiformate laden. Die verfügbaren Konstruktoren der Klasse Diagram erlauben dies und sie akzeptieren eine gültige Dateipfadzeichenfolge oder einen Dateistream der Quelldatei Visio.

Die unterstützten lesbaren Dateiformate sind wie folgt:
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM and VSX**

Konstruktoren der Klasse diagram bieten auch einen optionalen Parameter, der LoadFileFormat oder LoadOptions definiert. Es sind die Vorladeinformationen, die Entwickler an die Aspose.Diagram API weitergeben können. Wir empfehlen, die realistischen Informationen weiterzugeben, um eine ideale Leistung zu erzielen.
#### **Lesen von Diagram Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}

