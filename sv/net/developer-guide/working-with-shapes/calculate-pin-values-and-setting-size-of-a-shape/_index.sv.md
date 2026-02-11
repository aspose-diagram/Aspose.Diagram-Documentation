---
title: Beräkna stiftvärden och inställningsstorlek för en form
type: docs
weight: 60
url: /sv/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Det här avsnittet förklarar hur man beräknar PinX- och PinY-värden för underformen med Aspose.Diagram.
---
## **Beräkna PinX- och PinY-värden för underformen**
 Om formen är en undernod med gruppform, är dess xform en relativ koordinat av dess överordnade form men inte absolut koordinat i[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Om användaren behöver få den absoluta koordinaten hjälper den här exempelkoden.

En punkt specificerad i lokala koordinater kan omvandlas till överordnade koordinater genom att tillämpa följande transformationer i följande ordning:

1. Subtrahera värdet för egenskapen LocPinX för elementet Cell_Type från x-koordinaten.
1. Subtrahera värdet för egenskapen LocPinY för Cell_Type från y-koordinaten.
1. Spegla punkten kring y-axeln om värdet på egenskapen FlipX för Cell_Type är lika med ett.
1. Spegla punkten kring x-axeln om värdet på egenskapen FlipY för Cell_Type är lika med ett.
1. Rotera punkten moturs runt origo med värdet på egenskapen Angle för Cell_Type.
1. Lägg till värdet för PinX Cell_Type till x-koordinaten.
1. Lägg till värdet för PinY Cell_Type till y-koordinaten.
### **Beräkna PinX och PinY programmeringsexempel**
Använd följande kod i din .NET-applikation för att beräkna PinX- och PinY-värden för en underform med Aspose.Diagram for .NET API.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **Ställa in höjd och bredd på en form**
 De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klass låter dig styra formstorleken genom att ange höjd och bredd på formen med metoderna SetHeight och SetWidth.

 Metoderna SetHeight och SetWidth, exponerade av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)klass, stöder storleksändring av en form med mastern, utan mastern eller i form av en gruppform. Kodexemplen i den här artikeln ställer in höjd och bredd för att ändra storlek på formen på sidan.

Processen för att ställa in höjd och bredd är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in höjden på en form.
1. Ställ in bredden på en form.
1. Spara diagram.
### **Inställning av höjd och bredd Programmeringsexempel**
Kodavsnittet nedan visar hur du ställer in formens höjd och bredd. Koden letar efter en formnamnsrektangel, med form-ID 1, och ställer in dess höjd och bredd som dubbla.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

