---
title:  Konvertera Visio till PDF format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/python-net/convert-visio-to-pdf/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till PDF format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM.
---
## **Exportera till PDF**
{{% alert color="primary" %}}

 Aspose.Diagram för Python via .NET skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for .NET**Ansökan** fält med värdet 'Aspose.Diagram' och**PDF Producent** fält med värde, t.ex. 'Aspose.Diagram 17,9'.

Observera att du inte kan instruera Aspose.Diagram for .NET API att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med[Aspose.Diagram för Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Använd klasskonstruktorn [Diagram] för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Källfilen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)|


Så här exporterar du VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Anropa Diagram classs Save-metoden och ställ in utdataformatet till PDF.

Nedan finns en bild av utdatafilen PDF.

|**Utdatafilen PDF.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)|
### **Exportera Microsoft Visio Ritning till PDF**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till PDF med Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
