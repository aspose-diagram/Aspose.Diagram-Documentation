---
title:  Konvertera Visio till andra format
linktitle:  Konvertera Visio till andra format
type: docs
weight: 40
url: /sv/python-net/convert-visio-to-other-files/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till SVG,XPS,XML,XAML format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,0761123411 till 3061123411 kod,3011123411 till 3011123411 till 301123411 kod
---
## **Exportera till XML**
### **Exportera Microsoft Visio Ritning till PDF**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till PDF med C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XML med[Aspose.Diagram för Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX definierar en XML diagram.
- VTX definierar en XML-mall.
- VSX definierar en XML-stencil.

 [Diagram]klassens konstruktörer läser ett diagram och Save-metoden används för att spara, eller exportera, en diagram i ett annat filformat. Kodavsnitten i den här artikeln visar hur du använder metoden Spara för att spara en Visio-fil till[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) och[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

Bilden nedan visar diagram som exporteras i kodavsnitten nedan. Den exporterade filen visas före varje kodavsnitt.

|**A Microsoft Visio diagram på väg att exporteras.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_3.png)|

### **Exportera VSD till VDX**
VDX är ett schemabaserat XML-filformat som låter dig spara diagram i ett format som andra produkter än Microsoft Visio kan läsa. Det är ett användbart format för att överföra diagram mellan program och behålla redigerbara data.

Så här exporterar du ett VSD diagram till VDX:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VDX.

|**Den exporterade VDX-filen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_4.png)|

### **Exportera från VSD till VSX**
VSX är ett XML-format för att definiera stenciler, de grundläggande objekten från vilka en diagram är uppbyggd. När en Visio-fil konverteras till VSX, exporteras endast schablonerna.

Så här exporterar du ett VSD diagram till VSX:

- Skapa en instans av klassen Diagram.
- Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VSX.
### **Exportera VSD till VTX**
TVX är en XML-representation av en mallfil och lagrar inställningarna för dokumentet.

Så här exporterar du ett VSD diagram till VTX:

1. Skapa en instans av klassen Diagram.
1. Ring diagram-klassens Spara-metod för att skriva Visio-ritningsfilen i formatet VTX.
### **Exportera Microsoft Visio Ritning till XML**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till XML med C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **Exportera till XPS**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XPS med[Aspose.Diagram för Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Använd [Diagram]class'-konstruktorn för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

Kodavsnitten i den här artikeln tar diagram nedan som indata. Du kan också använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, 0761803713) eller 4.

|**Källdokumentet.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_5.png)|


Så här exporterar du VSD diagram till XPS:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod och ställ in XPS som utdataformat.
### **Exportera Microsoft Visio Ritning till XPS**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till XPS med C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Exportera ett Diagram till SVG**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till SVG (Scalable Vector Graphics) med[Aspose.Diagram för Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Använd [Diagram]class'-konstruktorn för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

För att exportera VSD diagram till SVG, utför följande steg:

1. Skapa en instans av klassen Diagram.
1. Anropa klassens spara-metod och ange SVG som exportformat.
### **Exportera Microsoft Visio Ritning till SVG**
Kodexemplen visar hur man exporterar en diagram till SVG med C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Så här exporterar du en Visio-ritning med selektiva former:

1. Skapa en instans av klassen Diagram.
1. Skapa en instans av en SaveOption-klass för att ange inställningar som beskrivs här:[Ange Visio Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Anropa metoden Spara för klassobjektet Diagram och skicka spara alternativ klassobjekt som parameter.
### **Konvertera Visio Ritning med selektiva former Programmeringsexempel**
Kodexemplet visar hur man exporterar en ritning med selektiva Visio-former.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
