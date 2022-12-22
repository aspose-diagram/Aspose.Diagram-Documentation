---
title: Pubblico API Modifiche Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.8.0 alla 16.11.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Modificare le proprietà di un controllo ActiveX**
 Gli sviluppatori possono recuperare un controllo ActiveX e quindi modificarne le proprietà. Abbiamo aggiunto la proprietà ActiveXControl nel file[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe. Si prega di controllare questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"C:\temp\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get a shape by ID

Shape shape = page.Shapes.GetShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;

// set width of the command button control

cbac.Width = 4;

// set height of the command button control

cbac.Height = 4;

// set caption of the command button control

cbac.Caption = "Test Button";

// save diagram

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
## **Inserisci una forma di testo nel Visio Diagram**
Gli sviluppatori possono inserire una forma di testo in Visio diagram utilizzando Aspose.Diagram API. Controllare questo esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

string text = "Test text";

// add text to a Visio page

diagram.Pages[0].AddText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Errore durante il rendering della macro 'codice': valore non valido specificato per il parametro lang
