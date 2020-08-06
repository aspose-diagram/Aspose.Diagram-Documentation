---
title: Remove All Macros from the Visio Diagram in PHP
type: docs
weight: 30
url: /java/remove-all-macros-from-the-visio-diagram-in-php/
---

## **Aspose.Diagram - Remove All Macros from the Visio Diagram**
To Remove All Macros from the Visio Diagram using **Aspose.Diagram Java for PHP**, simply invoke **RemoveAllMacrosFromDiagram** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Remove All Macros from the Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
