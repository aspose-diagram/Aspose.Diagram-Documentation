---
title:  Convertir Visio au format PDF
linktitle: Convertir Visio en PDF
type: docs
weight: 10
url: /fr/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Exportation au format PDF**
{{% alert color="primary" %}}

Aspose.Diagram pour Python via Java écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin au format PDF, Aspose.Diagram for Java remplit**Application**champ avec la valeur 'Aspose.Diagram' et**Producteur PDF**champ avec une valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram pour Python via Java de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

Cet article explique comment exporter un Microsoft Visio diagram au format PDF en utilisant Aspose.Diagram pour Python via Java.

Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

[Le VSD diagram](ExportToPDF.vsd) est l'exemple de fichier de dessin à exporter au format PDF. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX ou VSX).

Pour exporter VSD diagram au format PDF :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save des classes Diagram et définissez le format de sortie sur PDF.

### **Exporter vers un exemple de programmation PDF**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Fractionner plusieurs pages**
Aspose.Diagram for Java permet de diviser plusieurs pages lors de la conversion du Microsoft Visio Diagram en PDF. L'extrait de code suivant montre la fonctionnalité.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
