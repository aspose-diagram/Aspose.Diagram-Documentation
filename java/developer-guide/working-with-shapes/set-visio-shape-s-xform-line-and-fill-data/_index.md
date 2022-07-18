---
title: Set Visio Shape's XForm, Line and Fill Data
type: docs
weight: 70
url: /java/set-visio-shape-s-xform-line-and-fill-data/
---

## **Setting XForm Data**
The XForm element is part of the Microsoft Visio XML schema. XForm specifies a shapes position, for example width, height, rotation and whether the shape has been flipped. The [XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supports the Aspose.Diagram.XForm object. The XForm property can be used to retrieve or update a shape's XForm data. The code examples in this article change the PinX (X-coordinate) and PinY (Y-coordinate) XForm values to move the shapes on the page.

**Input diagram** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_1.png)

**The diagram after the** **PinX** **and** **PinY** **values have been changed** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_2.png)

The process for updating XForm data is:

1. Load a diagram.# Find a particular shape.# Update the shape's XForm data.
1. Save the diagram.
### **Programming Sample**
The code snippet below shows how to update a shape's XForm data. The code looks for a shape names process, with the shape ID 1, and sets its X and Y coordinates to 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Set Visio Shape's Line Data**
Shapes can be formatted in several ways. This article shows how to specify a line's attributes.

Microsoft Visio lets users format lines in various ways. Aspose.Diagram for Java supports:

- Weight: a line's thickness.
- Color: set shape's line color.
- Line Color Transparency: set shape's line color transparency in percentage.
- Pattern: defines whether the line is solid, dashed or has another pattern.
- Rounding: the radius of corners.
- Beginning and ending arrows: specified whether the line has arrows.
- Beginning and ending arrow sizes: set the arrow sizes.
- Cap: the rounding of the line ends.
### **Change the line color, weight, dash type, transparency, rounding, arrow type and arrow size of a shape's border**
The [Line](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supports the Aspose.Diagram.Line object. This property can be used to retrieve or update a shape's line data.
#### **Line Data Programming Sample**
The following piece of code updates the line data of shape.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Set Visio Shape's Fill Data**
Shapes can be formatted in several ways. This topic describes how to specify a shape's fill.

Microsoft Office Visio lets users format fills in various ways. The [Fill](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) class of the Aspose.Diagram for Java API supports setting:

- Background and foreground colors.
- Transparency.
- Fill patterns.
- Shadows.
### **Setting Fill Values**
The Fill property, exposed by the Shape class, supports the Aspose.Diagram.Fill object. The Fill property can be used to retrieve or update a shape's fill data.

|<p>**The input diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/OrhEecb.png)</p>|<p>**The diagram after changing the fill color** </p><p>![todo:image_alt_text](http://i.imgur.com/HO0wmZ8.png)</p>|
| :- | :- |
#### **Fill Data Programming Sample**
The following code snippet updates a shape's fill data. The code looks for a shape named rectangle, with the shape ID 1, and sets the fill background and foreground colors.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Retrieve Inherited Fill Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit fill data of a Visio shape. The InheritFill property, exposed by the Shape class, contains the fill formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Fill Data Programming Sample**
The following code snippet retrieves the inherited fill data of the shape. Please check this sample code:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
