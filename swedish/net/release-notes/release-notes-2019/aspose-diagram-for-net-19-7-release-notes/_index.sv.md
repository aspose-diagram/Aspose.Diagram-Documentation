---
title: Aspose.Diagram for .NET 19.7 Release Notes
type: docs
weight: 60
url: /sv/net/aspose-diagram-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.7](https://www.nuget.org/packages/Aspose.Diagram/19.7.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51219|Få bilder från förhandsgranskningen av en Visio-sida|Förbättring|
|DIAGRAMNET-51615|Dela Diagram till flera sidor samtidigt som PDF-dokument genereras|Förbättring|
|DIAGRAMNET-51656|Lägg till stöd för att övervaka dokumentkonverteringens framsteg|Förbättring|
|DIAGRAMNET-50045|Felaktiga radbrytningar vid konvertering av VSD till PDF-format|Insekt|
|DIAGRAMNET-50075|VSD till PDF-konvertering, felaktig texttypsnitt|Insekt|
|DIAGRAMNET-50201|VSD till PDF-konvertering, former är felplacerade|Insekt|
|DIAGRAMNET-50274|VSDX till SVG-konvertering, anslutningslayouterna är felaktiga|Insekt|
|DIAGRAMNET-51172|Ändrar inte formen ordentligt när den sparas i ett bildformat|Insekt|
|DIAGRAMNET-51613|Egenskapen AutoFitPageToDrawingContent fungerar inte som förväntat|Insekt|
|DIAGRAMNET-51657|VISIO till JPG - utdatabilden är inte i rätt format|Insekt|
|DIAGRAMNET-51658|VSDX blir skadad efter att det oanvända temat tagits bort|Insekt|
|DIAGRAMNET-51659|Bakgrunden försvinner när oanvända teman tas bort|Insekt|
|DIAGRAMNET-51660|Former saknas efter att du har tagit bort det oanvända temat|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till SplitMultiPages i PdfSaveOptions**
{{< highlight "java" >}}

 Aspose.Diagram.Saving.PdfSaveOptions o = new Aspose.Diagram.Saving.PdfSaveOptions();

o.SplitMultiPages = true;

diagram.Save("c:\\out.pdf", o);

{{< /highlight >}}
### **Lägger till PageSavingCallback i PdfSaveOptions**
{{< highlight "java" >}}

 Aspose.Diagram.Saving.PdfSaveOptions od = new Aspose.Diagram.Saving.PdfSaveOptions();

od.PageSavingCallback = new TestDiagramPageSavingCallback();

d.Save("c:\\test.pdf", od);

{{< /highlight >}}

{{< highlight "java" >}}

 public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{

    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)

    {

        Console.WriteLine("Start saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);

    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)

    {

        Console.WriteLine("End saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);

        //don't output pages after page index 8.

        if (args.PageIndex >= 8)

        {

            args.HasMorePages = false;

        }

    }

}

{{< /highlight >}}




