---
title: Converti una forma Visio in immagine
type: docs
weight: 10
url: /it/net/convert-a-visio-shape-to-image/
description: Questa sezione spiega come convertire una forma visio in un'immagine con Aspose.Diagram.
---
## **Converti una forma visio in immagine**
Questo argomento illustra come gli sviluppatori possono convertire una forma visio in un'immagine usando Aspose.Diagram.
 Il metodo ToImage esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzato per convertire in immagine.


Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in immagine.
#### **Esempio di programmazione da forma a immagine**
Utilizzare il codice seguente nell'applicazione .net per convertire una forma visio in un'immagine.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}
```
