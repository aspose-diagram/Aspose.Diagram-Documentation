---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /it/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Applicazione**campo con valore 'Aspose.Diagram' e**PDF Producer**campo con un valore, ad esempio 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for Python via Java to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using Aspose.Diagram for Python via Java.

Usare il costruttore Diagram class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

[Il VSD diagram](ExportToPDF.vsd) is the example drawing file to export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

To export VSD diagram to PDF:

1. Creare un'istanza della classe Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

### **Exporting to PDF Programming Sample**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToPDF.vsd")

# Save as PDF file format
diagram.save("ExportToPDF_Out.pdf", SaveFileFormat.PDF)

jpype.shutdownJVM()

{{< /highlight >}}


### **Dividi più pagine**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("Network Diagram_start.vsdx")
# Options when saving a diagram into the PDF format
options = PdfSaveOptions()
# set SplitMultiPages option
options.setSplitMultiPages(True)
# save in PDF format
diagram.save("SplitMultiPages.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}

