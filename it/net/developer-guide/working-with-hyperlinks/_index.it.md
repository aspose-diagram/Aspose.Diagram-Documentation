---
title: Lavorare con i collegamenti ipertestuali
type: docs
weight: 160
url: /it/net/working-with-hyperlinks/
description: Questa sezione spiega come aggiungere o ottenere un collegamento ipertestuale in una forma Visio con Aspose.Diagram.
---
## **Aggiungi collegamento ipertestuale a una forma Visio**
Microsoft Office Visio supporta l'aggiunta di collegamenti ipertestuali a qualsiasi forma. I collegamenti ipertestuali possono collegarsi a un'altra pagina o forma nel disegno corrente, una pagina o forma in un altro disegno, un documento diverso da un disegno Visio, un sito Web, un sito FTP o un indirizzo di posta elettronica. Gli sviluppatori possono usare Aspose.Diagram API per aggiungere facilmente collegamenti ipertestuali a una forma Visio.

 Nel disegno a più pagine Visio, i collegamenti ipertestuali possono spostarti da una forma a molti altri tipi di collegamenti.[Collegamento ipertestuale](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) esposto dal[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offre il metodo Add che può essere utilizzato per aggiungere il collegamento ipertestuale di una forma.

Per identificare le proprietà in Microsoft Office Visio:

1. In un Visio diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Collegamento ipertestuale.**
1. Imposta le proprietà esistenti
1.  Premere**OK** pulsante

**I dati del collegamento ipertestuale di una forma, come mostrato in Microsoft Visio**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_1.png)
### **Aggiungi esempio di programmazione di collegamenti ipertestuali**
Il frammento di codice seguente aggiunge i dati del collegamento ipertestuale della forma.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ottieni i dati dei collegamenti ipertestuali delle forme Visio**
Gli sviluppatori possono recuperare tutti i collegamenti ipertestuali da una forma Visio allo stesso modo di loro[leggi i dati della forma Visio](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

Nel disegno a più pagine Visio, i collegamenti ipertestuali possono spostarti da una forma a molti altri tipi di collegamenti.[Collegamento ipertestuale](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) esposto dal[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class consente agli sviluppatori di recuperare i collegamenti ipertestuali.

Per identificare le proprietà in Microsoft Office Visio:

1. In un diagram, fare clic con il pulsante destro del mouse su una forma.
1.  Selezionare**Collegamento ipertestuale.**

Tutte le proprietà esistenti sono elencate nella finestra di dialogo.
**I dati del collegamento ipertestuale di una forma, come mostrato in Microsoft Visio**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_1.png)

**Una finestra della console che mostra l'output dei dati della forma**

![cose da fare:immagine_alt_testo](working-with-hyperlinks_3.png)
### **Ottieni un esempio di programmazione dei collegamenti ipertestuali**
Il frammento di codice seguente legge i dati del collegamento ipertestuale della forma.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
