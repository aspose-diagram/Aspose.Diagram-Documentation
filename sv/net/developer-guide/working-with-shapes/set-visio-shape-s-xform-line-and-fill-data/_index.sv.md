---
title: Ställ in Visio Shapes XForm, Line och Fill Data
type: docs
weight: 20
url: /sv/net/set-visio-shape-s-xform-line-and-fill-data/
description: Det här avsnittet förklarar hur du ställer in formens stil inklusive dess linjedata och fyllningsdata med Aspose.Diagram.
---
## **Ställa in XForm-data**
 XForm-elementet är en del av XML-schemat Microsoft Visio. XForm anger en forms position, till exempel bredd, höjd, rotation och om formen har vänts. De[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) egendom, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.XForm. XForm-egenskapen kan användas för att hämta eller uppdatera en forms XForm-data. Kodexemplen i den här artikeln ändrar PinX (X-koordinat) och PinY (Y-koordinat) XForm-värden för att flytta formerna på sidan.

Processen för att uppdatera XForm-data är:

1. Ladda en diagram.# Hitta en viss form.# Uppdatera formens XForm-data.
1. Spara diagram.
### **Programmeringsexempel**
Kodavsnittet nedan visar hur du uppdaterar en forms XForm-data. Koden letar efter en process för formnamn, med form-ID 1, och ställer in dess X- och Y-koordinater till 5.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.XForm.PinX.Value = 5;
        shape.XForm.PinY.Value = 5;
    }
}
// Save diagram
diagram.Save(dataDir + "SetXFormdata_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ställ in Visio Shape's Line Data**
Former kan formateras på flera sätt. Den här artikeln visar hur du anger en linjes attribut.

Microsoft Visio låter användare formatera linjer på olika sätt. Aspose.Diagram for .NET stöder:

- Vikt: en linjes tjocklek.
- Färg: ställ in formens linjefärg.
- Linjefärgstransparens: ställ in formens linjefärgtransparens i procent.
- Mönster: definierar om linjen är heldragen, streckad eller har ett annat mönster.
- Avrundning: radien på hörnen.
- Start- och slutpilar: ange om linjen har pilar.
- Början och slutet pilstorlekar: ställ in pilstorlekarna.
- Cap: avrundningen av linjen slutar.
### **Ändra linjefärg, vikt, strecktyp, transparens, avrundning, piltyp och pilstorlek för en forms kant**
 De[Linje](http://www.aspose.com/api/net/diagram/aspose.diagram/line) egendom, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)klass, stöder objektet Aspose.Diagram.Line. Den här egenskapen kan användas för att hämta eller uppdatera en forms linjedata.
#### **Linjedataprogrammeringsexempel**
Följande kodbit uppdaterar formens linjedata.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set line dash type by index
shape.Line.LinePattern.Value = 4;
// Set line weight, defualt in inch
shape.Line.LineWeight.Value = 2;
// Set color of the shape's line
shape.Line.LineColor.Ufe.F = "RGB(95,108,53)";
// Set line rounding, default in inch
shape.Line.Rounding.Value = 0.3125;
// Set line caps
shape.Line.LineCap.Value = BOOL.True;
// Set line color transparency in percent
shape.Line.LineColorTrans.Value = 50;

/* add arrows to the connector or curve shapes */
// Select arrow type by index
shape.Line.BeginArrow.Value = 4;
shape.Line.EndArrow.Value = 4;
// Set arrow size 
shape.Line.BeginArrowSize.Value = ArrowSizeValue.Large;
shape.Line.EndArrowSize.Value = ArrowSizeValue.Large;

// Save the Visio
diagram.Save(dataDir + "SetLineData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Ställ in Visio Shape's Fill Data**
 Former kan formateras på flera sätt. Det här avsnittet beskriver hur du anger en forms fyllning. Microsoft Office Visio låter användare formatera fyllningar på olika sätt. De[Fylla](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) klass av Aspose.Diagram for .NET API stöder inställning:

- Bakgrunds- och förgrundsfärger.
- Genomskinlighet.
- Fyllningsmönster.
- Skuggor.
### **Ställa in fyllningsvärden**
 Fill-egenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stödjer[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) objekt. Fill-egenskapen kan användas för att hämta eller uppdatera en forms fyllningsdata.
#### **Fyll i dataprogrammeringsexempel**
Följande kodavsnitt uppdaterar en forms fyllningsdata. Koden letar efter en form som heter rektangel, med form-ID 1, och ställer in fyllningsbakgrunds- och förgrundsfärgerna.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetFillData.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "rectangle" && shape.ID == 1)
    {
        shape.Fill.FillBkgnd.Value = diagram.Pages[1].Shapes[0].Fill.FillBkgnd.Value;
        shape.Fill.FillForegnd.Value = "#ebf8df";
    }
}
// Save diagram
diagram.Save(dataDir + "SetFillData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Hämta ärvd fyllningsdata för en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvd fyllningsdata för en Visio-form. Egenskapen InheritFill, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, innehåller fyllningsformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwObliqueAngle.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetX.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetY.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwScaleFactor.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwType.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgnd.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwForegnd.Value);
Console.WriteLine(shape.InheritFill.ShdwForegndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwPattern.Value);

{{< /highlight >}}
```
