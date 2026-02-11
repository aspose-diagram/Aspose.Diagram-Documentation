---
title: Lavorare con le immagini
type: docs
weight: 60
url: /it/net/working-with-images/
description: Questa sezione spiega come inserire o ottenere un'immagine da una pagina visio con Aspose.Diagram.
---
## **Estrai tutte le immagini da una pagina Visio**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. È possibile estrarre immagini da una particolare pagina di un file Visio.
### **Estrai immagini**
L'oggetto Page Class rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Shapes esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Shape. Questa proprietà può essere utilizzata per estrarre tutte le immagini da una determinata pagina.
#### **Estrarre le immagini di esempio di programmazione**
Il seguente pezzo di codice estrae tutte le immagini da una particolare pagina Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}
```
## **Ottieni icone di varie forme Visio**
Aspose.Diagram for .NET API ora consente agli sviluppatori di ottenere icone di varie Visio forme.
### **Ottenere l'icona della forma**
Il codice negli esempi seguenti mostra come:

1. Carica uno diagram o uno stencil esistente.
1. Ottieni master dal suo indice
1. Ottieni l'icona principale.
1. Salva l'icona nello spazio locale.
#### **Ottieni un esempio di programmazione delle icone**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}
```
## **Sostituire una forma immagine del Visio Diagram**
Aspose.Diagram for .NET API consente agli sviluppatori di accedere e sostituire le forme immagine disponibili nel Visio diagram.
### **Sostituzione di una forma immagine**
Il codice negli esempi seguenti mostra come:

1. Carica un diagram esistente.
1. Scorri le forme di pagina selettive.
1. Applica il filtro per ottenere le forme dell'immagine.
1. Salva il risultante Visio diagram nello spazio locale.
#### **Sostituire un esempio di programmazione di Picture Shape**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Importa immagine bitmap come forma Visio**
Aspose.Diagram for .NET API consente ora agli sviluppatori di importare un'immagine bitmap come forma Microsoft Visio.
### **Insert a BMP Image in Visio**
Il codice negli esempi seguenti mostra come:

1. Crea uno diagram.
1. Ottenere Visio pagina
1. Importa un'immagine bitmap come forma Visio
1. Salva lo diagram.
#### **Insert a BMP Image Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Converti l'area specificata della pagina Visio in un'immagine**
Con Aspose.Diagram for .NET API, gli sviluppatori possono definire un'area con coordinate XY, larghezza e altezza e quindi convertire quest'area in un formato immagine supportato.
### **Converti l'area di disegno Visio in un'immagine**
Il codice negli esempi seguenti mostra come:

1. Carica un disegno Visio esistente
1. Definisci l'area del rettangolo
1. Converti l'area specificata in un'immagine

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
