---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändra en Visio sidlayout till stående eller liggande**
Aspose.Diagram för Python via Java API låter utvecklare ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

Aspose.Diagram för Python via Java API har klassen `Page` som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet `PrintPageOrientation` för utskriftsegenskaper gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram för Python via Java API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.

### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize the new visio diagram
diagram = Diagram("DrawingFlowCharts.vsdx")

# get Visio page
page = diagram.getPages().getPage("Flow 1")
# page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE)
# save Visio
diagram.save("SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Kontrollera exporten av dolda Visio-sidor när du sparar**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Till och med de kan dölja Visio sidor med Aspose.Diagram för Python via Java API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility i sidan ShapeSheet.

### **Göm en sida i Visio Diagram och ange exportalternativ**
Aspose.Diagram för Python via Java API har klassen `Page` som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. Fältet `UIVisibility` i sidegenskaper gör det möjligt att dölja sidan. Utvecklare kan sedan använda egendomen `exportHiddenPage` som läggs till i klasserna `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` och `PdfSaveOptions`.

#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till PDF.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = PdfSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToPDF_Out.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till HTML.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = HTMLSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)
# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToHTML_Out.html", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)
# initialize PDF save options
options = ImageSaveOptions(SaveFileFormat.JPEG)
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToImage_Out.jpeg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```

#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till SVG.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = SVGSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# Set SVG fit to view port
options.setSVGFitToViewPort(True)
# Set export element as Rectangle
options.setExportElementAsRectTag(True)

# save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToSVG_Out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
