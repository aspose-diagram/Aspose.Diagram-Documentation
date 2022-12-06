---
title: Din första Aspose.Diagram-applikation - Hello World
type: docs
weight: 30
url: /sv/python-java/your-first-aspose-diagram-application-hello-world/
description: Den här sidan beskriver hur du skapar den första applikationen med biblioteket Aspose.Diagram.
---
{{% alert color="primary" %}}

Denna handledning visar hur man skapar en allra första applikation (Hello World) med Aspose.Diagram' enkel API. Denna enkla applikation skapar en Microsoft Visio-fil med texten 'Hello World' på en angiven sida.

{{% /alert %}}

## **Skapa Hello World-applikationen**

Stegen nedan skapar Hello World-applikationen med hjälp av Aspose.Diagram API:

1. Skapa en instans av klassen Diagram.
1. Använd licensen:
 1. Om du har köpt en licens, använd sedan licensen i din applikation för att få tillgång till Aspose.Diagram' full funktionalitet
 1. Om du använder utvärderingsversionen av komponenten (om du använder Aspose.Diagram utan licens), hoppa över det här steget.
1. Skapa en ny Visio-fil eller öppna en befintlig Visio-fil.
1. Skapa en ny textruta.
1.  Sätt in orden**Hej världen!** i en textruta.
1. Generera den modifierade filen Microsoft Visio.

Implementeringen av stegen ovan visas i exemplen nedan.

### **Kodprov: Skapa en ny Diagram och skriva Hej världen!**

Följande exempel öppnar en befintlig Microsoft Visio mallfil med namnet "[Basic_Shapes.vss](Basic_Shapes.vss)", matar in texten "Hello World!" på första sidan och sparar diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-CreatingHelloWorldVisioFile.py" >}}
