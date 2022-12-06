---
title: Öffentlich API Änderungen in Aspose.Diagram 16.11.0
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.8.0 bis 16.11.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Eigenschaften eines ActiveX-Steuerelements ändern**
 Entwickler können ein ActiveX-Steuerelement abrufen und dann seine Eigenschaften ändern. Wir haben die ActiveXControl-Eigenschaft in der hinzugefügt[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
## **Fügen Sie eine Textform in die Visio Diagram ein**
Entwickler können mit Aspose.Diagram API eine Textform in Visio diagram einfügen. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
