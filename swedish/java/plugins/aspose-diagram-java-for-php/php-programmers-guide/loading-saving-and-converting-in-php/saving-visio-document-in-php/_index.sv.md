---
title: Sparar Visio Dokument i PHP
type: docs
weight: 100
url: /sv/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Sparar Visio Dokument**
 För att spara Visio Dokument med hjälp av**Aspose.Diagram Java för PHP**, kan du använda följande kod.

**PHP-kod**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XPS (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
