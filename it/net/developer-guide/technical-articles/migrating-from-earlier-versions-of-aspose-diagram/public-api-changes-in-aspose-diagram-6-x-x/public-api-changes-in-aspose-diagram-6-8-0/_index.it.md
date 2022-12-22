---
title: Pubblico API Modifiche Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.6.0 alla 6.8.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Inserisci un controllo ActiveX**
Gli sviluppatori possono inserire un controllo ActiveX nel Visio diagram. Abbiamo aggiunto il metodo AddActiveXControl nel[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe. Si prega di controllare questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
## **Imposta la casella di controllo del colore del livello**
Gli sviluppatori possono impostare o ottenere il Color CheckBox di Layer utilizzando Aspose.Diagram API. Controlla questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
## **Aggiunge la proprietà InheritFill nella classe Shape**
Gli sviluppatori possono ottenere o impostare la proprietà inherit fill. Abbiamo aggiunto la proprietà InheritFill nella classe Shape. Si prega di controllare questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
