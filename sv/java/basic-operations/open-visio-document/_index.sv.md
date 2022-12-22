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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
