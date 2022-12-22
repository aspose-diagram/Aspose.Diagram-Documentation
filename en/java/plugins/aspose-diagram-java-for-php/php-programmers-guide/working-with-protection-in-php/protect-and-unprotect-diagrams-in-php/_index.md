---
title: Protect and Unprotect Diagrams in PHP
type: docs
weight: 20
url: /java/protect-and-unprotect-diagrams-in-php/
---

## **Aspose.Diagram - Protect and Unprotect Diagrams**
To Protect and Unprotect Diagrams using **Aspose.Diagram Java for PHP**, simply invoke **ProtectUnprotectDiagram** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vsd");

$diagram->getDocumentSettings()->setProtectBkgnds(1);

$diagram->getDocumentSettings()->setProtectMasters(1);

$diagram->getDocumentSettings()->setProtectShapes(1);

$diagram->getDocumentSettings()->setProtectStyles(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectDiagram.vdx", $saveFileFormat->VDX);

print "Applied protection on diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Protect and Unprotect Diagrams (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
