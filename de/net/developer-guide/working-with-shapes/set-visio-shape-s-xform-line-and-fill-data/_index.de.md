---
title: Legen Sie die XForm-, Linien- und Fülldaten von Visio Form fest
type: docs
weight: 20
url: /de/net/set-visio-shape-s-xform-line-and-fill-data/
description: In diesem Abschnitt wird erläutert, wie Sie den Stil der Form festlegen, einschließlich der Liniendaten und Fülldaten mit Aspose.Diagram.
---
## **Festlegen von XForm-Daten**
 Das XForm-Element ist Teil des XML-Schemas Microsoft Visio. XForm gibt die Position einer Form an, z. B. Breite, Höhe, Drehung und ob die Form gespiegelt wurde. Das[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) Eigentum, ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.XForm. Die XForm-Eigenschaft kann verwendet werden, um die XForm-Daten einer Form abzurufen oder zu aktualisieren. Die Codebeispiele in diesem Artikel ändern die XForm-Werte PinX (X-Koordinate) und PinY (Y-Koordinate), um die Shapes auf der Seite zu verschieben.

Der Prozess zum Aktualisieren von XForm-Daten ist:

1. Laden Sie ein diagram.# Finden Sie eine bestimmte Form.# Aktualisieren Sie die XForm-Daten der Form.
1. Speichern Sie die diagram.
### **Programmierbeispiel**
Das folgende Code-Snippet zeigt, wie die XForm-Daten einer Form aktualisiert werden. Der Code sucht nach einem Shape-Namensprozess mit der Shape-ID 1 und setzt seine X- und Y-Koordinaten auf 5.


{{< highlight csharp >}}
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

## **Legen Sie die Liniendaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. Dieser Artikel zeigt, wie Sie die Attribute einer Linie angeben.

Microsoft Visio lässt Benutzer Linien auf verschiedene Arten formatieren. Aspose.Diagram for .NET unterstützt:

- Gewicht: die Dicke einer Linie.
- Farbe: Legen Sie die Linienfarbe der Form fest.
- Transparenz der Linienfarbe: Legen Sie die Transparenz der Linienfarbe der Form in Prozent fest.
- Muster: legt fest, ob die Linie durchgezogen, gestrichelt oder mit einem anderen Muster ist.
- Rundung: der Radius der Ecken.
- Anfangs- und Endpfeile: Gibt an, ob die Linie Pfeile hat.
- Anfangs- und Endpfeilgröße: Legen Sie die Pfeilgröße fest.
- Kappe: die Rundung der Linienenden.
### **Ändern Sie die Linienfarbe, das Gewicht, den Strichtyp, die Transparenz, die Rundung, den Pfeiltyp und die Pfeilgröße des Rahmens einer Form**
 Das[Linie](http://www.aspose.com/api/net/diagram/aspose.diagram/line) Eigentum, ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)Klasse, unterstützt das Objekt Aspose.Diagram.Line. Diese Eigenschaft kann verwendet werden, um die Liniendaten einer Form abzurufen oder zu aktualisieren.
#### **Programmierbeispiel für Leitungsdaten**
Der folgende Codeabschnitt aktualisiert die Liniendaten von shape.


{{< highlight csharp >}}
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

## **Legen Sie die Fülldaten der Form Visio fest**
 Formen können auf verschiedene Arten formatiert werden. In diesem Thema wird beschrieben, wie Sie die Füllung einer Form angeben. Microsoft Office Visio lässt Benutzer Füllungen auf verschiedene Weise formatieren. Das[Füllen](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Klasse der Aspose.Diagram for .NET API unterstützt Einstellung:

- Hintergrund- und Vordergrundfarben.
- Transparenz.
- Muster füllen.
- Schatten.
### **Füllwerte einstellen**
 Die Fill-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt die[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Objekt. Die Fill-Eigenschaft kann verwendet werden, um die Fülldaten einer Form abzurufen oder zu aktualisieren.
#### **Füllen Sie das Programmierbeispiel für Daten aus**
Der folgende Codeausschnitt aktualisiert die Fülldaten einer Form. Der Code sucht nach einer Form namens Rechteck mit der Form-ID 1 und legt die Hintergrund- und Vordergrundfarben für die Füllung fest.


{{< highlight csharp >}}
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

### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die vererbten Fülldaten einer Visio-Form abrufen oder festlegen. Die InheritFill-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, enthält die Füllformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:


{{< highlight csharp >}}
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

