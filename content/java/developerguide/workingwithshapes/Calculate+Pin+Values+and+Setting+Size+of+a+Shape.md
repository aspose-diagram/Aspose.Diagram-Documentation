+++
title = "Calculate Pin Values and Setting Size of a Shape" 
description = "" 
weight = 12034 
+++

Aspose.Diagram for Java : Calculate Pin Values and Setting Size of a Shape  

# Aspose.Diagram for Java : Calculate Pin Values and Setting Size of a Shape


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Calculate PinX and PinY Values of the Sub Shape](#CalculatePinValuesandSettingSizeofaShape-CalculatePinXandPinYValuesoftheSubShape)
    *   1.1 [Calculate PinX and PinY Programming Sample](#CalculatePinValuesandSettingSizeofaShape-CalculatePinXandPinYProgrammingSample)
*   2 [Setting Height and Width of a Shape](#CalculatePinValuesandSettingSizeofaShape-SettingHeightandWidthofaShape)
    *   2.1 [Setting Height and Width Programming Sample](#CalculatePinValuesandSettingSizeofaShape-SettingHeightandWidthProgrammingSample)
{{< /panel >}}
 

 

## Calculate PinX and PinY Values of the Sub Shape

If the shape is a children of group shape, it's xform is a relative coordinate of it's parent shape，but not absolute coordinate in the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/page). If the user require to get the absolute coordinate, then this sample code helps.

A point specified in local coordinates can be converted into parent coordinates by applying the following transformations in the following order:

1.  Subtract the value of the LocPinX property of the Cell\_Type element from the x-coordinate.
2.  Subtract the value of the LocPinY property of the Cell\_Type from the y-coordinate.
3.  Mirror the point about the y-axis if the value of the FlipX property of the Cell\_Type is equal to one.
4.  Mirror the point about the x-axis if the value of the FlipY property of the Cell\_Type is equal to one.
5.  Rotate the point counterclockwise around the origin by the value of the Angle property of the Cell\_Type.
6.  Add the value of the PinX Cell\_Type to the x-coordinate.
7.  Add the value of the PinY Cell\_Type to the y-coordinate.

### Calculate PinX and PinY Programming Sample

Use the following code in your Java application to calculate PinX and PinY values of a sub-shape using Aspose.Diagram for Java API.

## Setting Height and Width of a Shape

The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) Class allows you to control the shape size by specifying height and width of the shape using SetHeight and SetWidth methods.

The SetHeight and SetWidth methods, exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) class, support resizing a shape with the master, without the master or in the form of a group shape.

The code examples in this article set the Height and Width to resize the shape on the page.

**Input diagram**  
![](http://i.imgur.com/cTiNWa7.png)

**The diagram after the Height and Width**** have been changed**

![](https://docs2.aspose.com/diagram/java/attachments/18612228/18809111.png)

The process for setting Height and Width is:

1.  Load a diagram.
2.  Find a particular shape.
3.  Set the height of a shape.
4.  Set the Width of a shape.
5.  Save the diagram.

### Setting Height and Width Programming Sample

The code snippet below shows how to set the shape's height and width. The code looks for a shape name rectangle, with the shape ID 1, and sets its Height and Width as double.

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-Height-and-Width-002.png](https://docs2.aspose.com/diagram/java/attachments/18612228/18809111.png) (image/png)  

