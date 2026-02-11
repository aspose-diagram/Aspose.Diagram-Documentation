---
title: Calculate Pin Values and Setting Size of a Shape
type: docs
weight: 60
url: /net/calculate-pin-values-and-setting-size-of-a-shape/
description: This section explains how to calculate PinX and PinY Values of the Sub Shape with Aspose.Diagram.
---

## **Calculate PinX and PinY Values of the Sub Shape**
If the shape is a child node of group shape, its xform is a relative coordinate of its parent shape but not absolute coordinate in the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page). If the user require to get the absolute coordinate, then this sample code helps.

A point specified in local coordinates can be converted into parent coordinates by applying the following transformations in the following order:

1. Subtract the value of the LocPinX property of the Cell_Type element from the x-coordinate.
1. Subtract the value of the LocPinY property of the Cell_Type from the y-coordinate.
1. Mirror the point about the y-axis if the value of the FlipX property of the Cell_Type is equal to one.
1. Mirror the point about the x-axis if the value of the FlipY property of the Cell_Type is equal to one.
1. Rotate the point counterclockwise around the origin by the value of the Angle property of the Cell_Type.
1. Add the value of the PinX Cell_Type to the x-coordinate.
1. Add the value of the PinY Cell_Type to the y-coordinate.
### **Calculate PinX and PinY Programming Sample**
Use the following code in your .NET application to calculate PinX and PinY values of a sub-shape using Aspose.Diagram for .NET API.








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

## **Setting Height and Width of a Shape**
The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class allows you to control the shape size by specifying height and width of the shape using SetHeight and SetWidth methods.

The SetHeight and SetWidth methods, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, support resizing a shape with the master, without the master or in the form of a group shape. The code examples in this article set the Height and Width to resize the shape on the page.

The process for setting Height and Width is:

1. Load a diagram.
1. Find a particular shape.
1. Set the height of a shape.
1. Set the Width of a shape.
1. Save the diagram.
### **Setting Height and Width Programming Sample**
The code snippet below shows how to set the shape's height and width. The code looks for a shape name rectangle, with the shape ID 1, and sets its Height and Width as double.


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

