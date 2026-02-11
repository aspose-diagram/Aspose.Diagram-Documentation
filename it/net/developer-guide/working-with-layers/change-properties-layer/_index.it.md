---
title: Modifica le proprietà del livello
type: docs
weight: 130
url: /it/net/change-properties-layer/
description: Questa sezione spiega come modificare le proprietà del layer con Aspose.Diagram.
---
## **Modifica le proprietà del livello in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) consente di modificare le proprietà del livello in Microsoft Office Visio diagram.Ogni forma può appartenere a più livelli in modo che gli sviluppatori possano modificare le proprietà del livello per soddisfare le esigenze dell'utente finale. Il[PaginaFoglio](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)class object offre Layers che permette di aggiungere e rimuovere oggetti layer nel disegno Visio. Gli utenti possono gestire[Strato](https://reference.aspose.com/diagram/net/aspose.diagram/layer) properties a livello di codice utilizzando Aspose.Diagram API come segue:
### **Esempio di programmazione delle proprietà del livello di modifica**
Il seguente pezzo di codice aiuta a modificare le proprietà del layer.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
