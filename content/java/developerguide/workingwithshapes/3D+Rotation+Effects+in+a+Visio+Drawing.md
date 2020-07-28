+++
title = "3D Rotation Effects in a Visio Drawing" 
description = "" 
weight = 12039 
+++

Aspose.Diagram for Java : 3D Rotation Effects in a Visio Drawing  

# Aspose.Diagram for Java : 3D Rotation Effects in a Visio Drawing


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Set 3D Rotation Properties in Shapesheet](#id-3DRotationEffectsinaVisioDrawing-Set3DRotationPropertiesinShapesheet)
    *   1.1 [Set 3D Rotation Properties](#id-3DRotationEffectsinaVisioDrawing-Set3DRotationProperties)
        *   1.1.1 [3D Rotation Programming Sample](#id-3DRotationEffectsinaVisioDrawing-3DRotationProgrammingSample)
{{< /panel >}}
 

 

## Set 3D Rotation Properties in Shapesheet

Aspose.Diagram for Java API allows developers to change 3D rotation values in the shapesheet. The RotationXAngle, RotationYAngle, and RotationZAngle cell values control the degree of rotation in each of the respective axes. The RotationType’s enum value controls the rotation type:

1.  Parallel rotation, where the shape is rotated without accounting for linear perspective.
2.  Perspective rotation, where the shape is rotated with linear perspective.
3.  Oblique rotation presets (bottom left, bottom right, top left and top right), where the shape is rotated with oblique projection.

The **KeepTextFlat** cell value indicates whether a shape’s text will ignore the shape’s rotation in 3-D. It does not apply to 2-D rotation. The **DistanceFromGround** cell value determines the distance the object is raised from the ground in the points when rotated in 3-D. The **Perspective** cell value determines the perspective angle for a perspective rotation, in degrees (0 to 359.9).

### Set 3D Rotation Properties

The `ThreeDFormat` member exposed by the [Shape](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Shape) class can be used to set 3d rotation properties.

The code below shows how to:

1.  Load a source drawing.
2.  Retrieve a shape by page name and ID parameters.
3.  Set 3D rotation properties.
4.  Save drawing 

#### 3D Rotation Programming Sample

Use the following code in your Java application to set 3D rotation properties using Aspose.Diagram for Java API.

**Java**

{{< code lang="java" >}}
// load diagram
Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");
// get shape by ID and page name
Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);
       
// set 3D rotation properties
shape.getThreeDFormat().getRotationXAngle().setValue(2.61);
shape.getThreeDFormat().getRotationYAngle().setValue(2.61);
shape.getThreeDFormat().getRotationZAngle().setValue(3);
shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);
shape.getThreeDFormat().getPerspective().setValue(0);
shape.getThreeDFormat().getDistanceFromGround().setValue(0);
shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);
// save drawing
diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

