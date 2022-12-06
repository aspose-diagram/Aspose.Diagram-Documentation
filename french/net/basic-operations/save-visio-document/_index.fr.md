---
title: Enregistrer le document Visio par programmation
linktitle: Enregistrer le document Visio
type: docs
weight: 30
url: /fr/net/save-visio-document/
description: Cette page décrit comment enregistrer le document Visio dans un fichier, diffuser avec la bibliothèque Aspose.Diagram.
---
## **Visio Vue d'ensemble de l'enregistrement du dessin**
 Utilisez le[Diagram.Save]() méthode pour enregistrer un dessin Microsoft Visio. Il existe des surcharges qui permettent d'enregistrer un dessin dans un fichier. Le dessin peut être enregistré dans n'importe quel format d'enregistrement pris en charge par Aspose.Diagram. Pour la liste de tous les formats d'enregistrement pris en charge, consultez le[Enregistrer le format de fichier]()Enum.
## **Enregistrement Visio Diagram**
 La classe Diagram du Aspose.Diagram API représente un dessin Visio et les développeurs peuvent enregistrer son objet Visio diagram dans n'importe quel format de fichier pris en charge. Pour enregistrer un fichier Microsoft Visio, utilisez simplement le[Diagram.Save]() il accepte un nom de fichier avec un chemin complet ou un objet de flux de fichier. Aspose.Diagram API déduit le format de sauvegarde de l'extension de fichier et propose également un paramètre supplémentaire SaveFileFormat pour spécifier le format de fichier de sortie.
### **Enregistrez un Visio Diagram dans n'importe quel format de fichier pris en charge**
À l'aide de Aspose.Diagram API, les développeurs peuvent enregistrer un Visio diagram dans n'importe quel format de fichier pris en charge, comme indiqué ci-dessous :
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF et XAM**
### **Enregistrement de l'exemple de programmation Diagram**
L'exemple ci-dessous enregistre un document dans un fichier.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Spécification des options d'enregistrement Visio**
 Il y a plusieurs[Diagram.Save]() surcharges de méthode qui acceptent un objet SaveOptions. Il doit s'agir d'un objet d'une classe dérivée de la classe SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde. Par exemple, il existe PdfSaveOptions pour le format d'enregistrement SaveFileFormat.PDF.
### **Visio Diagram Options de sauvegarde**
Ces exemples montrent comment :

- [Utilisez les options de sauvegarde Diagram](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement PDF](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement HTML](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement d'image](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement SVG](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utiliser les options d'enregistrement SWF](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Utilisation des options de sauvegarde Diagram**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Utilisation des options d'enregistrement PDF**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Utilisation des options d'enregistrement HTML**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format de fichier HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Utilisation des options d'enregistrement d'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format de fichier image.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Utilisation des options d'enregistrement SVG

Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Utilisation des options d'enregistrement SWF

Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SWF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Parfois, les développeurs doivent enregistrer ou exporter des diagrammes Visio vers différents formats de fichiers par programmation (comme VDX, PDF, JPEG, etc.).
## **Enregistrez le fichier VSD dans différents formats de fichier (VDX, PDF et JPEG)**
 Cet article fournit un exemple de code qui illustre comment utiliser[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) et[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) pour enregistrer un fichier Microsoft Visio VSD dans un fichier VDX, un fichier PDF ou un fichier JPEG par programmation. Vous trouverez ci-dessous des extraits de code parallèles pour VSTO et Aspose.Diagram for .NET qui expliquent comment enregistrer un fichier VSD dans différents formats de fichier. Vous remarquerez que le code Aspose.Diagram est plus court. N'hésitez pas à utiliser le code et à le modifier pour répondre à vos besoins spécifiques.
### **Enregistrement d'un fichier VSD dans d'autres formats avec VSTO**
VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour enregistrer un fichier dans d'autres formats :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Charger le diagram.
1. Enregistrer au VDX, PDF et JPEG.
1. Quittez l'objet d'application Visio.
#### **Enregistrement d'un fichier VSD avec un exemple de programmation VSTO**
{{% alert color="primary" %}} 

en utilisant Visio = Microsoft.Office.Interop.Visio ;
Importations Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**Enregistrement du fichier VSD dans d'autres formats avec Aspose.Diagram for .NET**
En utilisant Aspose.Diagram, les développeurs n'ont pas besoin de Microsoft Office Visio dans la machine, et ils peuvent travailler indépendamment de Microsoft Office Automation.

Les extraits de code ci-dessous montrent comment :

1. Charger un diagram.
1. Enregistrez le diagram au VSX, PDF et JPEG.
#### **Enregistrement du fichier VSD avec l'exemple de programmation Aspose.Diagram for .NET**
{{% alert color="primary" %}} 

en utilisant Aspose.Diagram ;
Importations Aspose.Diagram

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
