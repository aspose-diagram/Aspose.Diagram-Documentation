---
title: Öppna Visio dokument programmatiskt
linktitle: Öppna dokumentet Visio
type: docs
weight: 20
url: /sv/java/open-visio-document/
description: Den här sidan beskriver hur du öppnar Visio-dokument från början med Aspose.Diagram-biblioteket.
---
## **Läs en befintlig Visio-ritning**
Aspose.Diagram API stöder att skapa de nya Visio-diagrammen från början och sedan spara i valfritt filformat som stöds. Utvecklare kan också ladda ett befintligt Visio diagram för ändring, tillägg eller bearbetningsändamål.
### **Läser en Diagram**
Med hjälp av Aspose.Diagram API kan utvecklare ladda alla Visio filformat som stöds. De tillgängliga konstruktörerna i klassen Diagram tillåter detta och de accepterar en giltig sökvägssträng eller en filström av källfilen Visio.

De läsbara filformaten som stöds är följande:
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX.**

Konstruktörer av klassen diagram erbjuder också en valfri parameter som definierar LoadFileFormat eller LoadOptions. Det är förladdningsinformationen som utvecklare kan skicka till Aspose.Diagram API. Vi rekommenderar att du skickar realistisk information för att få en idealisk prestanda.
#### **Läsning Diagram Programmeringsexempel**
```
{{< highlight "java" >}}
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
```
