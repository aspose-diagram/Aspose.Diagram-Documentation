---
title: Raggruppa, converti e verifica le forme
type: docs
weight: 80
url: /it/net/group-convert-and-verify-shapes/
description: Questa sezione spiega come raggruppare le forme con Aspose.Diagram.
---
## **Raggruppa più forme insieme nel disegno Visio**
Aspose.Diagram API consente agli sviluppatori di raggruppare le forme insieme per spostarle tutte in una volta. Ogni forma in un gruppo mantiene un'identità univoca e ha il proprio insieme di proprietà. Quando cambiamo la formattazione di un gruppo di forme, assegna la nuova proprietà a ciascuna forma.
### **Come raggruppare le forme**
 Il metodo di gruppo esposto dal[Collezione Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class può essere utilizzato per raggruppare le forme insieme.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. inizializzato un array delle forme
1. ottenere una forma particolare per id.
1. ottieni un'altra particolare forma particolare per id.
1. assegnare forme all'array.
1. raggruppare le forme chiamando il metodo Group.
1. salvo diagram
#### **Esempio di programmazione delle forme di gruppo**
Utilizzare il seguente codice nell'applicazione .NET per raggruppare le forme utilizzando Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Converti una forma Visio in altri formati di file**
Aspose.Diagram for .NET API consente agli sviluppatori di convertire una singola forma Visio in qualsiasi altro formato di file supportato. In questo articolo rimuoviamo tutte le altre forme Visio dalla pagina e personalizziamo le impostazioni della pagina in base alla dimensione della forma di origine.
### **Conversione di una particolare forma Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **specificando le opzioni di salvataggio Visio**.
Questo codice di esempio funziona come segue:

1. Carica una fonte Visio.
1. Ottieni una pagina particolare.
1. Rimuovi la pagina di sfondo.
1. Costruisci una tabella hash di tutte le forme che contengono gli ID e i nomi.
1. Itera attraverso la tabella hash
1. Rimuovi tutte le forme dalla pagina Visio, tranne quella in particolare.
1. Imposta la dimensione della pagina.
1. Salva la pagina Visio in qualsiasi formato di file supportato.
#### **Esempio di programmazione di forme convertite**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}
```
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Verifica se due forme Visio sono collegate o incollate**
 Aspose.Diagram for .NET API consente agli sviluppatori di verificare che le due forme Visio siano incollate o collegate. In precedenza, abbiamo visto come collegare o incollare due forme in questi argomenti della guida:[Aggiungi e collega Visio Forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) e[Forme di colla all'interno del contenitore](/diagram/it/net/working-with-shapes-gluing/).
### **Verifica delle Forme Connesse o Incollate**
 Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) offre le proprietà IsGlued e IsConnected per determinare se due forme sono collegate o connesse.
#### **Esempio di programmazione per la verifica di forme connesse o incollate**
La parte di codice seguente verifica se due forme sono connesse o incollate.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Verificare se la forma Visio si trova in un gruppo di forme**
Aspose.Diagram for .NET API consente agli sviluppatori di verificare se la forma Visio si trova o meno in un gruppo di forme.
### **Verifica della forma nel gruppo delle forme**
Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)offre proprietà IsInGroup per determinare se la forma Visio è in una forma di gruppo.
#### **Verifica della forma nell'esempio di programmazione del gruppo di forme**
La parte di codice seguente verifica se la forma è in una forma di gruppo.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}
```
