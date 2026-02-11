---
title: Spåra dokumentkonverteringsförlopp
type: docs
weight: 970
url: /sv/net/track-document-conversion-progress/
description: Det här avsnittet förklarar hur du spårar konverteringsförloppet för visio-filer med Aspose.Diagram.
---
## **Möjliga användningsscenarier**

 Ibland kan det ta lite tid att konvertera stora visio-filer. Under denna tid kanske du vill visa dokumentkonverteringsförloppet istället för bara en laddningsskärm för att förbättra användbarheten av din applikation. Aspose.Diagram stöder konverteringsprocess för spårning av dokument genom att tillhandahålla**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** gränssnitt. De**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**gränssnitt ger**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**och**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**metoder som du kan implementera i din anpassade klass. Du kan också styra vilka sidor som renderas som visas i T*estDiagramPageSavingCallback*anpassad klass.

## **Spåra dokumentkonverteringsförlopp**

 Följande kodexempel laddar[källfil visio](Drawing1.vsdx) och skriver ut dess konverteringsförlopp i konsolen med hjälp av*TestPageSavingCallback* anpassad klass som implementerar**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**gränssnitt.

## **Exempelkod**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

Följande är koden för*TestDiagramPageSavingCallback*anpassad klass.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}
```

## **Konsolutgång**

Börja spara sidindex 0 av sidorna 11</br>
Sluta spara sidindex 0 av sidorna 11</br>
Börja spara sidindex 1 av sidorna 11</br>
Avsluta att spara sidindex 1 av sidorna 11</br>
Börja spara sidindex 2 av sidorna 11</br>
Avsluta att spara sidindex 2 av sidorna 11</br>
Börja spara sidindex 3 av sidorna 11</br>
Avsluta att spara sidindex 3 av sidorna 11</br>
Börja spara sidindex 4 av sidorna 11</br>
Avsluta att spara sidindex 4 av sidorna 11</br>
Börja spara sidindex 5 av sidorna 11</br>
Avsluta att spara sidindex 5 av sidorna 11</br>
Börja spara sidindex 6 av sidorna 11</br>
Avsluta att spara sidindex 6 av sidorna 11</br>
Börja spara sidindex 7 av sidorna 11</br>
Avsluta att spara sidindex 7 av sidorna 11</br>
Börja spara sidindex 8 av sidorna 11</br>
Avsluta att spara sidindex 8 av sidorna 11
