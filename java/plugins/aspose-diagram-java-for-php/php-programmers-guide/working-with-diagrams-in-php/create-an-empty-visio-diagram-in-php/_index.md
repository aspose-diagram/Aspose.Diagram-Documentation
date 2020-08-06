---
title: Create an empty Visio Diagram in PHP
type: docs
weight: 20
url: /java/create-an-empty-visio-diagram-in-php/
---

## **Aspose.Diagram - Create an empty Visio Diagram**
To Create an empty Visio Diagram using **Aspose.Diagram Java for PHP**, simply invoke **CreateDiagram** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Create an empty Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
