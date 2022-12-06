---
title:  Convertir Visio au format PDF
linktitle: Convertir Visio en PDF
type: docs
weight: 10
url: /fr/java/convert-visio-to-pdf/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en formats PDF. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en PDF avec quelques lignes de code.
---
## **Exportation au format PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin au format PDF, Aspose.Diagram for Java remplit**Application**champ avec la valeur 'Aspose.Diagram' et**Producteur PDF**champ avec une valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for Java API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

 Cet article explique comment exporter un Microsoft Visio diagram au format PDF en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

L'image ci-dessous montre le VSD diagram que les extraits de code ci-dessous exportent au format PDF. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX ou VSX).

**Le fichier sources.**

![tâche : image_autre_texte](how-to-convert-a-visio-diagram_1.png)

Pour exporter VSD diagram au format PDF :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save des classes Diagram et définissez le format de sortie sur PDF.

Vous trouverez ci-dessous une image du fichier PDF de sortie.

**Le fichier PDF de sortie.**

![tâche : image_autre_texte](how-to-convert-a-visio-diagram_2.png)
### **Exporter vers un exemple de programmation PDF**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Fractionner plusieurs pages**
Aspose.Diagram for Java permet de diviser plusieurs pages lors de la conversion du Microsoft Visio Diagram en PDF. L'extrait de code suivant montre la fonctionnalité.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Utiliser le rappel d'enregistrement de page**
Si vous avez plusieurs pages, Aspose.Diagram for Java permet d'utiliser le rappel d'enregistrement de page lors de la conversion du Microsoft Visio Diagram en PDF. L'extrait de code suivant montre la fonctionnalité.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **Classe TestDiagramPageSavingCallbackTestDiagramPageSavingCallback Class**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
