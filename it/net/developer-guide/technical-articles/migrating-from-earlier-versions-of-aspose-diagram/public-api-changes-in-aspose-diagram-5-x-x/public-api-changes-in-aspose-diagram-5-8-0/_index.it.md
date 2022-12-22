---
title: Pubblico API Modifiche Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 5.7.0 alla 5.8.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **L'opzione SaveToolBar viene aggiunta in HTMLSaveOptions**
La nuova opzione SaveToolBar è stata aggiunta nella classe HTMLSaveOptions. Specifica se salvare o meno la barra degli strumenti. Il valore predefinito è vero. Esempi di codici:

**C#**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.SaveToolBar = false;

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' initialize HTMLSaveOptions class object

Dim opts As New HTMLSaveOptions()

' set save toolbar option

opts.SaveToolBar = False

{{< /highlight >}}
## **VSDX L'opzione di salvataggio viene aggiunta in SaveFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura del formato VSDX, ma ora abbiamo aggiunto il supporto per la scrittura di diagrammi nel formato VSDX. Esempi di codici:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' save diagram in the VSDX format

diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
## **Il metodo Group è stato aggiunto nella classe ShapeCollection**
Gli sviluppatori possono ora raggruppare più forme insieme in Visio diagram utilizzando Aspose.Diagram API. Codici di esempio:

**C#**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes

Aspose.Diagram.Shape[]ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array

ss[0]= diagram.Pages[0].Shapes.GetShape(1);

ss[1]= diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group

diagram.Pages[0].Shapes.Group(ss);

// save visio diagram

diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' load a Visio diagram

Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes

Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array

ss(0) = diagram.Pages(0).Shapes.GetShape(1)

ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group

diagram.Pages(0).Shapes.Group(ss)

' save visio diagram

diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
