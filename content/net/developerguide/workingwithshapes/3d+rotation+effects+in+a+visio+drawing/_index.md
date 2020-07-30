---
title : "3D Rotation Effects in a Visio Drawing" 
description : "" 
weight : 12030 
toc : false
type: docs
url: /net/developerguide/workingwithshapes/3d+rotation+effects+in+a+visio+drawing/
---

# Aspose.Diagram for .NET : 3D Rotation Effects in a Visio Drawing


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Set 3D Rotation Properties in Shapesheet](#set-3d-rotation-properties-in-shapesheet)
    *   1.1 [Set 3D Rotation Properties](#set-3d-rotation-properties)
        *   1.1.1 [3D Rotation Programming Sample](#3d-rotation-programming-sample)
{{< /panel >}}
 

 

## Set 3D Rotation Properties in Shapesheet

Aspose.Diagram API allows developers to change 3D rotation values in the shapesheet. The RotationXAngle, RotationYAngle, and RotationZAngle cell values control the degree of rotation in each of the respective axes. The RotationType’s enum value controls the rotation type:

1.  Parallel rotation, where the shape is rotated without accounting for linear perspective.
2.  Perspective rotation, where the shape is rotated with linear perspective.
3.  Oblique rotation presets (bottom left, bottom right, top left and top right), where the shape is rotated with oblique projection.

The **KeepTextFlat** cell value indicates whether a shape’s text will ignore the shape’s rotation in 3-D. It does not apply to 2-D rotation. The **DistanceFromGround** cell value determines the distance the object is raised from the ground in the points when rotated in 3-D. The **Perspective** cell value determines the perspective angle for a perspective rotation, in degrees (0 to 359.9).

### Set 3D Rotation Properties

The `ThreeDFormat` member exposed by the [Shape](https://apireference.aspose.com/net/diagram/aspose.diagram/shape) class can be used to set 3d rotation properties.

The code below shows how to:

1.  Load a source drawing.
2.  Retrieve a shape by page name and ID parameters.
3.  Set 3D rotation properties.
4.  Save drawing 

#### 3D Rotation Programming Sample

Use the following code in your .NET application to set 3D rotation properties using Aspose.Diagram for .NET API.

**.NET, C#**

{{< code lang="cs" >}}
// load diagram
Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");
// get shape by ID and page name
Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);
            
// set 3D rotation properties
shape.ThreeDFormat.RotationXAngle.Value = 2.61;
shape.ThreeDFormat.RotationYAngle.Value = 2.61;
shape.ThreeDFormat.RotationZAngle.Value = 3;
shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;
shape.ThreeDFormat.Perspective.Value = 0;
shape.ThreeDFormat.DistanceFromGround.Value = 0;
shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;
// save drawing
diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

