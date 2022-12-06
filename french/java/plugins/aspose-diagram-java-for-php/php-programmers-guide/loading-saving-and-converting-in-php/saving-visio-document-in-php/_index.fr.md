---
title: Enregistrement du document Visio en PHP
type: docs
weight: 100
url: /fr/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Enregistrement Visio Document**
 Pour enregistrer le document Visio à l'aide de**Aspose.Diagram Java pour PHP**, vous pouvez utiliser le code suivant.

**Code PHP**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers XPS (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
