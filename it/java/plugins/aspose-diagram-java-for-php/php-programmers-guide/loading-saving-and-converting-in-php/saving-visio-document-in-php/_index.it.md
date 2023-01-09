---
title: Salvataggio del documento Visio in PHP
type: docs
weight: 100
url: /it/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Salvataggio documento Visio**
 Per salvare il documento Visio utilizzando**Aspose.Diagram Java per PHP**, puoi usare il seguente codice.

**Codice PHP**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to XPS (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
