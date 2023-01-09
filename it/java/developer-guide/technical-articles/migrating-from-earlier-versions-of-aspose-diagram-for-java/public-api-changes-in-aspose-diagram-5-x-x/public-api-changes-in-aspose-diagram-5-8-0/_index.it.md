---
title: Pubblico API Modifiche Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /it/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 5.7.0 alla 5.8.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **L'opzione SaveToolBar viene aggiunta in HTMLSaveOptions**
La nuova opzione SaveToolBar è stata aggiunta nella classe HTMLSaveOptions. Specifica se salvare o meno la barra degli strumenti. Il valore predefinito è vero. Esempi di codici:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX L'opzione di salvataggio viene aggiunta in SaveFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura del formato VSDX, ma ora abbiamo aggiunto il supporto per la scrittura di diagrammi nel formato VSDX. Esempi di codici:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Il metodo Group è stato aggiunto nella classe ShapeCollection**
Gli sviluppatori possono ora raggruppare più forme insieme in Visio diagram utilizzando Aspose.Diagram API. Codici di esempio:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
