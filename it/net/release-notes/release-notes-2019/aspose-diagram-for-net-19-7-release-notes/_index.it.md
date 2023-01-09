---
title: Aspose.Diagram for .NET 19.7 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-diagram-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 19.7](https://www.nuget.org/packages/Aspose.Diagram/19.7.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51219|Ottieni immagini dall'anteprima di stampa di una pagina Visio|Aumento|
|DIAGRAMNET-51615|Split Diagram to Multiple Pages while generating PDF Document|Aumento|
|DIAGRAMNET-51656|Aggiunto il supporto per il monitoraggio dell'avanzamento della conversione del documento|Aumento|
|DIAGRAMNET-50045|Incorrect line breaks when converting VSD to PDF format|Insetto|
|DIAGRAMNET-50075|VSD to PDF conversion, incorrect text font|Insetto|
|DIAGRAMNET-50201|VSD to PDF conversion, shapes are misplaced|Insetto|
|DIAGRAMNET-50274|VSDX to SVG conversion, the connection layouts are incorrect|Insetto|
|DIAGRAMNET-51172|Non ridimensiona correttamente la forma durante il salvataggio in un formato immagine|Insetto|
|DIAGRAMNET-51613|La proprietà AutoFitPageToDrawingContent non funziona come previsto|Insetto|
|DIAGRAMNET-51657|Da VISIO a JPG - l'immagine di output non è nel formato corretto|Insetto|
|DIAGRAMNET-51658|VSDX viene danneggiato dopo aver rimosso il tema inutilizzato|Insetto|
|DIAGRAMNET-51659|Lo sfondo scompare durante la rimozione dei temi inutilizzati|Insetto|
|DIAGRAMNET-51660|Le forme vengono perse dopo aver rimosso il tema inutilizzato|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge SplitMultiPages in PdfSaveOptions**
{{< highlight "java" >}}

 Aspose.Diagram.Saving.PdfSaveOptions o = new Aspose.Diagram.Saving.PdfSaveOptions();

o.SplitMultiPages = true;

diagram.Save("c:\\out.pdf", o);

{{< /highlight >}}
### **Aggiunge PageSavingCallback in PdfSaveOptions**
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




