---
title: Calcola i valori dei pin e imposta le dimensioni di una forma
type: docs
weight: 60
url: /it/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Questa sezione spiega come calcolare i valori PinX e PinY della Sub Shape con Aspose.Diagram.
---
## **Calcola i valori PinX e PinY della forma secondaria**
 Se la forma è un nodo figlio di una forma di gruppo, la sua forma x è una coordinata relativa della sua forma padre ma non una coordinata assoluta nel[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Se l'utente richiede di ottenere la coordinata assoluta, allora questo codice di esempio aiuta.

Un punto specificato nelle coordinate locali può essere convertito in coordinate padre applicando le seguenti trasformazioni nel seguente ordine:

1. Sottrai il valore della proprietà LocPinX dell'elemento Cell_Type dalla coordinata x.
1. Sottrai il valore della proprietà LocPinY di Cell_Type dalla coordinata y.
1. Eseguire il mirroring del punto sull'asse y se il valore della proprietà FlipX di Cell_Type è uguale a uno.
1. Eseguire il mirroring del punto sull'asse x se il valore della proprietà FlipY di Cell_Type è uguale a uno.
1. Ruotare il punto in senso antiorario attorno all'origine in base al valore della proprietà Angle di Cell_Type.
1. Aggiungi il valore di PinX Cell_Type alla coordinata x.
1. Aggiungi il valore di PinY Cell_Type alla coordinata y.
### **Calcola il campione di programmazione PinX e PinY**
Utilizzare il seguente codice nell'applicazione .NET per calcolare i valori PinX e PinY di una forma secondaria utilizzando Aspose.Diagram for .NET API.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **Impostazione dell'altezza e della larghezza di una forma**
 Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe consente di controllare le dimensioni della forma specificando l'altezza e la larghezza della forma utilizzando i metodi SetHeight e SetWidth.

 I metodi SetHeight e SetWidth, esposti da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, supporta il ridimensionamento di una forma con il master, senza il master o sotto forma di una forma di gruppo. Gli esempi di codice in questo articolo impostano l'altezza e la larghezza per ridimensionare la forma nella pagina.

Il processo per impostare l'altezza e la larghezza è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta l'altezza di una forma.
1. Imposta la larghezza di una forma.
1. Salva lo diagram.
### **Impostazione dell'altezza e della larghezza Esempio di programmazione**
Il frammento di codice seguente mostra come impostare l'altezza e la larghezza della forma. Il codice cerca un rettangolo con il nome della forma, con l'ID forma 1, e ne imposta l'altezza e la larghezza su double.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

