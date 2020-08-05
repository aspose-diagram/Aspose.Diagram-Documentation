---
title : "Set Visio Shapes XForm Line and Fill Data" 
description : "" 
weight : 12037 
toc : false
type: docs
url: /java/developerguide/workingwithshapes/set+visio+shapes+xform+line+and+fill+data/
---

# Aspose.Diagram for Java : Set Visio Shape's XForm, Line and Fill Data


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Setting XForm Data](#setting-xform-data)
    *   1.1 [Programming Sample](#programming-sample)
*   2 [Set Visio Shape's Line Data](#set-visio-shape's-line-data)
    *   2.1 [Change the line color, weight, dash type, transparency, rounding, arrow type and arrow size of a shape's border](#change-the-line-color,-weight,-dash-type,-transparency,-rounding,-arrow-type-and-arrow-size-of-a-shape's-border)
        *   2.1.1 [Line Data Programming Sample](#line-data-programming-sample)
*   3 [Set Visio Shape's Fill Data](#set-visio-shape's-fill-data)
    *   3.1 [Setting Fill Values](#setting-fill-values)
        *   3.1.1 [Fill Data Programming Sample](#fill-data-programming-sample)
    *   3.2 [Retrieve Inherited Fill Data of a Visio Shape](#retrieve-inherited-fill-data-of-a-visio-shape)
        *   3.2.1 [Retrieve Inherited Fill Data Programming Sample](#retrieve-inherited-fill-data-programming-sample)
{{< /panel >}}
 

 

## Setting XForm Data

The XForm element is part of the Microsoft Visio XML schema. XForm specifies a shapes position, for example width, height, rotation and whether the shape has been flipped. The [XForm](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/xform) property, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, supports the `Aspose.Diagram.XForm` object. The `XForm` property can be used to retrieve or update a shape's XForm data. The code examples in this article change the `PinX` (X-coordinate) and `PinY` (Y-coordinate) `XForm` values to move the shapes on the page.

**Input diagram**  
![image](https://docs2.aspose.com/diagram/java/attachments/18612231/18809112.png)

**The diagram after the** `**PinX**` **and** `**PinY**` **values have been changed**  
![image](https://docs2.aspose.com/diagram/java/attachments/18612231/18809113.png)

The process for updating XForm data is:

1.  Load a diagram.# Find a particular shape.# Update the shape's `XForm` data.
2.  Save the diagram.

### Programming Sample

The code snippet below shows how to update a shape's XForm data. The code looks for a shape names process, with the shape ID 1, and sets its X and Y coordinates to 5.

## Set Visio Shape's Line Data

Shapes can be formatted in several ways. This article shows how to specify a line's attributes.

Microsoft Visio lets users format lines in various ways. Aspose.Diagram for Java supports:

*   Weight: a line's thickness.
*   Color: set shape's line color.
*   Line Color Transparency: set shape's line color transparency in percentage.
*   Pattern: defines whether the line is solid, dashed or has another pattern.
*   Rounding: the radius of corners.
*   Beginning and ending arrows: specified whether the line has arrows.
*   Beginning and ending arrow sizes: set the arrow sizes.
*   Cap: the rounding of the line ends.

### Change the line color, weight, dash type, transparency, rounding, arrow type and arrow size of a shape's border

The [Line](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/line) property, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, supports the `Aspose.Diagram.Line` object. This property can be used to retrieve or update a shape's line data.

#### Line Data Programming Sample

The following piece of code updates the line data of shape.

## Set Visio Shape's Fill Data

Shapes can be formatted in several ways. This topic describes how to specify a shape's fill.

Microsoft Office Visio lets users format fills in various ways. The [Fill](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/fill) class of the Aspose.Diagram for Java API supports setting:

*   Background and foreground colors.
*   Transparency.
*   Fill patterns.
*   Shadows.

### Setting Fill Values

The `Fill` property, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, supports the [`Aspose.Diagram.Fill`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/fill) object. The `Fill` property can be used to retrieve or update a shape's fill data.

**The input diagram**  
![image](http://i.imgur.com/OrhEecb.png)

**The diagram after changing the fill color**  
![image](http://i.imgur.com/HO0wmZ8.png)

#### Fill Data Programming Sample

The following code snippet updates a shape's fill data. The code looks for a shape named rectangle, with the shape ID 1, and sets the fill background and foreground colors.

### Retrieve Inherited Fill Data of a Visio Shape

The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit fill data of a Visio shape. The `InheritFill` property, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) class, contains the fill formatting values for the shape inherit by the parent style and the master shape.

#### Retrieve Inherited Fill Data Programming Sample

The following code snippet retrieves the inherited fill data of the shape. Please check this sample code:

