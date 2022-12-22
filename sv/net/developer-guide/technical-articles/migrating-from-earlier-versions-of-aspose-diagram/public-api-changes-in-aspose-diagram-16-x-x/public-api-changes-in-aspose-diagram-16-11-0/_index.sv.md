---
title: Offentlig API Ändringar i Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.8.0 till 16.11.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Ändra egenskaper för en ActiveX-kontroll**
 Utvecklare kan hämta en ActiveX-kontroll och sedan ändra dess egenskaper. Vi har lagt till ActiveXControl-egenskapen i[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass. Kontrollera detta kodexempel:

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

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
## **Infoga en textform i Visio Diagram**
Utvecklare kan infoga en textform i Visio diagram med Aspose.Diagram API. Kontrollera detta kodexempel:

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

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
