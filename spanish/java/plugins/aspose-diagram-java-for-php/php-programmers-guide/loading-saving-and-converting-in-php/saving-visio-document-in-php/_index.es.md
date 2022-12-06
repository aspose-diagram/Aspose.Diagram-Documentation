---
title: Guardando el documento Visio en PHP
type: docs
weight: 100
url: /es/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Ahorro Visio Documento**
 Para guardar el documento Visio usando**Aspose.Diagram Java para PHP**, puede usar el siguiente código.

**Código PHP**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Export Visio Diagram to XPS (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
