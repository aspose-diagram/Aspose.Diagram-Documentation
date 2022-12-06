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

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Öppna en befintlig fil**

Följande exempel öppnar en befintlig Microsoft Visio mallfil, skriver orden "Hello World!" på första sidan och sparar diagram som en ny fil.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
