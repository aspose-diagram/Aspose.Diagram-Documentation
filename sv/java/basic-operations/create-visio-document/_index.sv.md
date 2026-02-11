---
title: Skapa Visio dokument programmatiskt
linktitle: Skapa Visio dokument
type: docs
weight: 10
url: /sv/java/create-visio-document/
description: Den här sidan beskriver hur du skapar Visio-dokument från grunden med Aspose.Diagram-biblioteket.
---
## **Skapa en ny Visio-ritning**
Aspose.Diagram for Java låter dig läsa och skapa Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation. Det första steget när du skapar nya dokument är att skapa en diagram. Lägg sedan till former och kopplingar för att bygga upp diagram.
### **Skapa Visio Ritningsprogrammeringsexempel**
Koden nedan visar för att skapa en ny Microsoft Visio ritning. Observera att den tomma ritningen innehåller en enda tom sida.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Ritpappersstorleken är som standard Letter.

{{% /alert %}} 

