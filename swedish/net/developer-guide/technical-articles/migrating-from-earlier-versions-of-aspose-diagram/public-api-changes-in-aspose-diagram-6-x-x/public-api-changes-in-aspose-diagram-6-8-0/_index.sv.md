---
title: Offentlig API Ändringar i Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.6.0 till 6.8.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Infoga en ActiveX-kontroll**
Utvecklare kan infoga en ActiveX-kontroll i Visio diagram. Vi har lagt till metoden AddActiveXControl i[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass. Kontrollera detta kodexempel:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
## **Ställ in färgkryssrutan för lager**
Utvecklare kan ställa in eller hämta Color CheckBox för Layer med Aspose.Diagram API. Kontrollera detta kodexempel:

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

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
## **Lägger till egenskapen InheritFill i Shape-klassen**
Utvecklare kan få eller ställa in arvsfyllningsegenskapen. Vi har lagt till egenskapen InheritFill i Shape-klassen. Kontrollera detta kodexempel:

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

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
