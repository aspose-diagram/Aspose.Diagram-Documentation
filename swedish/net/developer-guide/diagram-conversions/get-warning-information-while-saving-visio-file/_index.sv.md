---
title: Få varningsinformation när du sparar Visio-fil
type: docs
weight: 110
url: /sv/net/get-warning-information-while-saving-visio-file/
---
## **Möjliga användningsscenarier**

 Ibland försöker användaren spara diagram som innehåller text som inte har ett lokalt teckensnitt. I sådana fall skickar Aspose.Diagram varningar samtidigt som diagram sparas. Du kan fånga dessa varningar genom att implementera**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** gränssnitt och inställning**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**fast egendom.

## **Få varningar medan du sparar Visio-fil**

 Följande exempelkod förklarar hur du får varningar när du sparar visio-filen. Koden konverterar[exempel visio fil](sampleFontSubstitution.vsdx) som kastar**[FontSubstitution](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** varning om att spara. Denna varning fångas sedan av**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**metod som skriver ut varningsmeddelanden på konsolen. Vänligen kontrollera också konsolutgången för koden nedan för mer förståelse.

## **Exempelkod**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Konsolutgång**

Här är konsolutgången för ovanstående kod när den körs med den medföljande[exempel visio fil](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
