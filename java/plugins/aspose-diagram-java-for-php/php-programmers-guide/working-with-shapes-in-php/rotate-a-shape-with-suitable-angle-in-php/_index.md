---
title: Rotate a Shape with Suitable Angle in PHP
type: docs
weight: 80
url: /java/rotate-a-shape-with-suitable-angle-in-php/
---

## **Aspose.Diagram - Rotate a Shape with Suitable Angle**
To Rotate a Shape with Suitable Angle using **Aspose.Diagram Java for PHP**, simply invoke **RotateShape** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Rotate a Shape with Suitable Angle (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/RotateShape.php)
