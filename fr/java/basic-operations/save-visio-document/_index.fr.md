---
title: Enregistrer le document Visio par programmation
linktitle: Enregistrer le document Visio
type: docs
weight: 30
url: /fr/java/save-visio-document/
description: Cette page décrit comment enregistrer le document Visio dans un fichier, diffuser avec la bibliothèque Aspose.Diagram.
---
## **Visio Vue d'ensemble de l'enregistrement du dessin**
 Utilisez le[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) pour enregistrer un dessin Microsoft Visio. Il existe des surcharges qui permettent d'enregistrer un dessin dans un fichier. Le dessin peut être enregistré dans n'importe quel format d'enregistrement pris en charge par Aspose.Diagram. Pour la liste de tous les formats d'enregistrement pris en charge, consultez le[Enregistrer le format de fichier](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat)Enum.
## **Enregistrement Visio Diagram**
 La classe Diagram du Aspose.Diagram API représente un dessin Visio et les développeurs peuvent enregistrer son objet Visio diagram dans n'importe quel format de fichier pris en charge. Pour enregistrer un fichier Microsoft Visio, utilisez simplement le[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)), il accepte un nom de fichier avec le chemin complet ou un objet de flux de fichier. Aspose.Diagram API déduit le format de sauvegarde de l'extension de fichier et offre également un paramètre supplémentaire SaveFileFormat pour spécifier le format du fichier de sortie.
### **Enregistrez un Visio Diagram dans n'importe quel format de fichier pris en charge**
À l'aide de Aspose.Diagram API, les développeurs peuvent enregistrer un Visio diagram dans n'importe quel format de fichier pris en charge, comme indiqué ci-dessous :
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Enregistrement de l'exemple de programmation Diagram**
L'exemple ci-dessous enregistre un document dans un fichier.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Spécification des options d'enregistrement Visio**
 Il y a plusieurs[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Options de sauvegarde**
Ces exemples montrent comment :

- [Utilisez les options de sauvegarde Diagram](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde PDF](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde HTML](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utiliser les options d'enregistrement d'image](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilisez les options de sauvegarde SVG](/diagram/fr/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Utilisation des options de sauvegarde Diagram**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Utilisation des options de sauvegarde PDF**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Utilisation des options de sauvegarde HTML**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Utilisation des options d'enregistrement d'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document dans un format d'image.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Utilisation des options de sauvegarde SVG**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
