---
title: Få varningsinformation när du sparar Visio-fil
type: docs
weight: 110
url: /sv/java/get-warning-information-while-saving-visio-file/
---
## **Möjliga användningsscenarier**

 Ibland försöker användaren spara diagram som innehåller text som inte har ett lokalt teckensnitt. I sådana fall skickar Aspose.Diagram varningar samtidigt som diagram sparas. Du kan fånga dessa varningar genom att implementera**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** gränssnitt och inställning**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**fast egendom.

## **Få varningar medan du sparar Visio-fil**

 Följande exempelkod förklarar hur du får varningar när du sparar visio-filen. Koden konverterar[exempel visio fil](sampleFontSubstitution.vsdx) som kastar**[FontSubstitution](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** varning om att spara. Denna varning fångas sedan av**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**metod som skriver ut varningsmeddelanden på konsolen. Vänligen kontrollera också konsolutgången för koden nedan för mer förståelse.

## **Exempelkod**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "sampleFontSubstitution.vsdx");

// create an instance SVG save options class
Aspose.Diagram.Saving.SVGSaveOptions so = new Aspose.Diagram.Saving.SVGSaveOptions();

so.WarningCallback = new TestDiagramWarningCallback();
// save Visio drawing
diagram.Save(dataDir + "WarningCallback_out.svg", options);


public class TestDiagramWarningCallback : Aspose.Diagram.IWarningCallback
{
    public void Warning(Aspose.Diagram.WarningInfo info)
    {
        if (info.WarningType == Aspose.Diagram.WarningType.FontSubstitution)
        {
            Console.WriteLine("Diagram WARNING INFO: " + info.Description);
        }

    }
}

{{< /highlight >}}
```

## **Konsolutgång**

Här är konsolutgången för ovanstående kod när den körs med den medföljande[exempel visio fil](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
