---
title:  Konvertera Visio till PDF-format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Exporterar till PDF**
{{% alert color="primary" %}}

Aspose.Diagram för Python via Java skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for Java**Ansökan**fält med värdet 'Aspose.Diagram' och**PDF-producent**fält med ett värde, t.ex. 'Aspose.Diagram 17.9'.

Observera att du inte kan instruera Aspose.Diagram för Python via Java att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

[VSD diagram](ExportToPDF.vsd) är exempel på ritningsfilen för att exportera PDF. Du kan även använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 071617781 eller 38161 eller 38161).

För att exportera VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram klasser Spara metoden och ställ in utdataformatet till PDF.

### **Exportera till PDF Programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Dela flera sidor**
Aspose.Diagram for Java tillåter att dela flera sidor samtidigt som Microsoft Visio Diagram konverteras till PDF. Följande kodavsnitt visar funktionaliteten.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
