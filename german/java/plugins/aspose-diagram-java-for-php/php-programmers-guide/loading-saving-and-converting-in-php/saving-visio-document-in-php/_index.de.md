---
title: Speichern des Visio-Dokuments in PHP
type: docs
weight: 100
url: /de/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Speichern des Visio-Dokuments**
 Zum Speichern von Visio-Dokumenten mit**Aspose.Diagram Java für PHP**, können Sie folgenden Code verwenden.

**PHP-Code**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Export Visio Diagram to XPS (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
