---
title: Din första Aspose.Diagram-ansökan - Hello World
type: docs
weight: 30
url: /sv/net/your-first-aspose-diagram-application-hello-world/
description: Den här sidan beskriver hur du skapar den första applikationen med biblioteket Aspose.Diagram.
---
{{% alert color="primary" %}}

Denna handledning visar hur man skapar en allra första applikation (Hello World) med Aspose.Diagram' simple API. Denna enkla applikation skapar en Microsoft Visio-fil med texten 'Hello World' på en specificerad sida.

{{% /alert %}}

## **Skapar Hello World-applikationen**

Stegen nedan skapar Hello World-applikationen med hjälp av Aspose.Diagram API:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) klass.
1.  Om du har en licens, då[tillämpa den](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Om du använder utvärderingsversionen, hoppa över de licensrelaterade kodraderna.
1. Skapa en ny Visio-fil eller öppna en befintlig Visio-fil.
1. Skapa en ny textruta.
1.  Sätt in orden**Hello World!** i en textruta.
1. Generera den modifierade filen Microsoft Visio.

Implementeringen av stegen ovan visas i exemplen nedan.

### **Kodexempel: Skapa en ny Diagram**

Följande exempel skapar en ny diagram från början, skriver Hello World! på första sidan och sparar filen Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateNewVisio-CreateNewVisio.cs" >}}

### **Kodexempel: Öppna en befintlig fil**

Följande exempel öppnar en befintlig Microsoft Visio mallfil med namnet "Sample.vsdx", matar in "Hello World!" text på första sidan och sparar diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ReadVisioDiagram-ReadVisioDiagram.cs" >}}
