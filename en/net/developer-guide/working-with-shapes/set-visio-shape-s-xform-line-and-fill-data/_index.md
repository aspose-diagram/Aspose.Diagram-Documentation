---
title: Set Visio Shape's XForm, Line and Fill Data
type: docs
weight: 20
url: /net/set-visio-shape-s-xform-line-and-fill-data/
description: This section explains how to set shape's style including it's line data and fill data with Aspose.Diagram.
---

## **Setting XForm Data**
The XForm element is part of the Microsoft Visio XML schema. XForm specifies a shapes position, for example width, height, rotation and whether the shape has been flipped. The [XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supports the Aspose.Diagram.XForm object. The XForm property can be used to retrieve or update a shape's XForm data. The code examples in this article change the PinX (X-coordinate) and PinY (Y-coordinate) XForm values to move the shapes on the page.

The process for updating XForm data is:

1. Load a diagram.# Find a particular shape.# Update the shape's XForm data.
1. Save the diagram.
### **Programming Sample**
The code snippet below shows how to update a shape's XForm data. The code looks for a shape names process, with the shape ID 1, and sets its X and Y coordinates to 5.


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

## **Set Visio Shape's Line Data**
Shapes can be formatted in several ways. This article shows how to specify a line's attributes.

Microsoft Visio lets users format lines in various ways. Aspose.Diagram for .NET supports:

- Weight: a line's thickness.
- Color: set shape's line color.
- Line Color Transparency: set shape's line color transparency in percentage.
- Pattern: defines whether the line is solid, dashed or has another pattern.
- Rounding: the radius of corners.
- Beginning and ending arrows: specified whether the line has arrows.
- Beginning and ending arrow sizes: set the arrow sizes.
- Cap: the rounding of the line ends.
### **Change the line color, weight, dash type, transparency, rounding, arrow type and arrow size of a shape's border**
The [Line](http://www.aspose.com/api/net/diagram/aspose.diagram/line) property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supports the Aspose.Diagram.Line object. This property can be used to retrieve or update a shape's line data.
#### **Line Data Programming Sample**
The following piece of code updates the line data of shape.


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

## **Set Visio Shape's Fill Data**
Shapes can be formatted in several ways. This topic describes how to specify a shape's fill. Microsoft Office Visio lets users format fills in various ways. The [Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) class of the Aspose.Diagram for .NET API supports setting:

- Background and foreground colors.
- Transparency.
- Fill patterns.
- Shadows.
### **Setting Fill Values**
The Fill property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supports the [Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) object. The Fill property can be used to retrieve or update a shape's fill data.
#### **Fill Data Programming Sample**
The following code snippet updates a shape's fill data. The code looks for a shape named rectangle, with the shape ID 1, and sets the fill background and foreground colors.


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

### **Retrieve Inherited Fill Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit fill data of a Visio shape. The InheritFill property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contains the fill formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Fill Data Programming Sample**
The following code snippet retrieves the inherited fill data of the shape. Please check this sample code:


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

