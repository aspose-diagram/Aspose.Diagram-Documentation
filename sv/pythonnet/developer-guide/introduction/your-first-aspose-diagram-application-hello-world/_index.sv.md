---
title: Din första Aspose.Diagram-ansökan - Hello World
type: docs
weight: 30
url: /sv/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

Det här nybörjarämnet visar hur utvecklare kan skapa en enkel första applikation (Hello World) med Aspose.Diagram' enkel API. Applikationen skapar en Microsoft Visio fil med orden Hello World på sidan.

{{% /alert %}}

### **Skapar Hello World-applikationen**

Så här skapar du Hello World-applikationen med Aspose.Diagram API:

1. Skapa en instans av klassen Workbook.
1. Använd licensen:
 1. Om du har köpt en licens, använd sedan licensen i din applikation för att få tillgång till Aspose.Diagram' full funktionalitet
 1. Om du använder utvärderingsversionen av komponenten (om du använder Aspose.Diagram utan licens), hoppa över det här steget.
1. Skapa en ny Microsoft Visio fil, eller öppna en befintlig fil där du vill lägga till/uppdatera lite text.
1.  Sätt in orden**Hello World!** på sidan som du kommer åt.
1. Generera den modifierade filen Microsoft Visio.

Exemplen nedan visar stegen ovan.

#### **Skapar ett Diagram**

Följande exempel skapar en ny diagram från början, skriver orden "Hello World!" på första sidan och sparar filen.

**Skapa ny visio-fil** 

![todo:image_alt_text](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Öppna en befintlig fil**

Följande exempel öppnar en befintlig Microsoft Visio mallfil, skriver orden "Hello World!" på första sidan och sparar diagram som en ny fil.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

