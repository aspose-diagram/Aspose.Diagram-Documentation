---
title: Saving Visio Document in PHP
type: docs
weight: 100
url: /java/saving-visio-document-in-php/
---

## **Aspose.Diagram - Saving Visio Document**
To Save Visio Document using **Aspose.Diagram Java for PHP**, you can use following code.

**PHP Code**

{{< highlight php >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Download Running Code**
Download **Export Visio Diagram to XPS (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
