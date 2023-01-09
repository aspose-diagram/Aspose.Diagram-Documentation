---
title: Öffentlich API Änderungen in Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.6.0 auf 6.8.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Fügen Sie ein ActiveX-Steuerelement ein**
Entwickler können ein ActiveX-Steuerelement in die Visio diagram einfügen. Wir haben die AddActiveXControl-Methode in die hinzugefügt[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse. Bitte überprüfen Sie dieses Codebeispiel:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
## **Setzen Sie das Farb-Kontrollkästchen der Ebene**
Entwickler können die Color CheckBox von Layer mit Aspose.Diagram API setzen oder abrufen. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
## **Fügt die InheritFill-Eigenschaft in der Shape-Klasse hinzu**
Entwickler können die inherit fill-Eigenschaft abrufen oder festlegen. Wir haben die InheritFill-Eigenschaft in der Shape-Klasse hinzugefügt. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
