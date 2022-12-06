﻿---
title: Enregistrer le document Visio par programmation
linktitle: Enregistrer le document Visio
type: docs
weight: 30
url: /fr/python-net/save-visio-document/
description: Cette page décrit comment enregistrer le document Visio dans un fichier, diffuser avec la bibliothèque Aspose.Diagram.
---
## **Visio Vue d'ensemble de l'enregistrement du dessin**
 Utilisez le[Diagram.Save]() méthode pour enregistrer un dessin Microsoft Visio. Il existe des surcharges qui permettent d'enregistrer un dessin dans un fichier. Le dessin peut être enregistré dans n'importe quel format d'enregistrement pris en charge par Aspose.Diagram. Pour la liste de tous les formats d'enregistrement pris en charge, consultez le[Enregistrer le format de fichier]()Enum.
## **Enregistrement Visio Diagram**
 La classe Diagram du Aspose.Diagram API représente un dessin Visio et les développeurs peuvent enregistrer son objet Visio diagram dans n'importe quel format de fichier pris en charge. Pour enregistrer un fichier Microsoft Visio, utilisez simplement le[Diagram.Save]() il accepte un nom de fichier avec un chemin complet ou un objet de flux de fichier. Aspose.Diagram API déduit le format de sauvegarde de l'extension de fichier et propose également un paramètre supplémentaire SaveFileFormat pour spécifier le format de fichier de sortie.
### **Enregistrez un Visio Diagram dans n'importe quel format de fichier pris en charge**
À l'aide de Aspose.Diagram API, les développeurs peuvent enregistrer un Visio diagram dans n'importe quel format de fichier pris en charge, comme indiqué ci-dessous :
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Enregistrement de l'exemple de programmation Diagram**
L'exemple ci-dessous enregistre un document dans un fichier.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Spécification des options d'enregistrement Visio**
 Il y a plusieurs[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Options de sauvegarde**
Ces exemples montrent comment :

- [Utilisez les options de sauvegarde Diagram](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilisez les options de sauvegarde PDF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilisez les options de sauvegarde HTML](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utiliser les options d'enregistrement d'image](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilisez les options de sauvegarde SVG](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilisez les options de sauvegarde SWF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Utilisation des options de sauvegarde Diagram**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format Visio.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseDiagramSaveOptions.py" >}}



#### **Utilisation des options de sauvegarde PDF**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UsePdfSaveOptions.py" >}}



#### **Utilisation des options de sauvegarde HTML**
The code below shows how to set save options before saving a document to HTML file format.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseHtmlSaveOptions.py" >}}



#### **Utilisation des options d'enregistrement d'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format de fichier image.



{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseImageSaveOptions.py" >}}


Utilisation des options de sauvegarde SVG

Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un document au format SVG.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseSvgSaveOptions.py" >}}

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

### ` `**Saving VSD File to Other Formats with Aspose.Diagram for Python via .NET**
En utilisant Aspose.Diagram, les développeurs n'ont pas besoin de Microsoft Office Visio dans la machine, et ils peuvent travailler indépendamment de Microsoft Office Automation.

Les extraits de code ci-dessous montrent comment :

1. Charger un diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for Python via .NET Programming Sample**
{{% alert color="primary" %}} 

importer aspose.diagram
depuis aspose.diagram import *

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-SaveDiagramTo_VDX_PDF_JPEG_withAspose.py" >}}
