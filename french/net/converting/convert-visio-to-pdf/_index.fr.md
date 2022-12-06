---
title:  Convertir Visio au format PDF
linktitle: Convertir Visio en PDF
type: docs
weight: 10
url: /fr/net/convert-visio-to-pdf/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en formats PDF. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en PDF avec quelques lignes de code.
---
## **Exporter au format PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin au format PDF, Aspose.Diagram for .NET remplit**Application** champ avec la valeur 'Aspose.Diagram' et**Producteur PDF** champ avec valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

 Cet article explique comment exporter un Microsoft Visio diagram au format PDF en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) constructeur de classe pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

L'image ci-dessous montre le VSD diagram que les extraits de code ci-dessous exportent au format PDF. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSM, VDX, VST, VSTX, VDX, VTX ou VSX).

|**Le fichier sources.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_1.png)|


Pour exporter VSD diagram au format PDF :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save des classes Diagram et définissez le format de sortie sur PDF.

Vous trouverez ci-dessous une image du fichier PDF de sortie.

|**Le fichier PDF de sortie.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_2.png)|
### **Exporter Microsoft Visio Dessin au format PDF**
Les exemples de code montrent comment exporter Microsoft Visio Dessin au format PDF à l'aide de C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Fractionner plusieurs pages**
Aspose.Diagram for .NET permet de diviser plusieurs pages lors de la conversion du Microsoft Visio Diagram en PDF. L'extrait de code suivant montre la fonctionnalité.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Utiliser le rappel d'enregistrement de page**
Si vous avez plusieurs pages, Aspose.Diagram for .NET permet d'utiliser le rappel d'enregistrement de page lors de la conversion du Microsoft Visio Diagram en PDF. L'extrait de code suivant montre la fonctionnalité.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **Classe TestDiagramPageSavingCallbackTestDiagramPageSavingCallback Class**
{{< highlight "java" >}}

 classe publique TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

 }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Fin de l'enregistrement diagram page {0} de pages {1}", Index + args.Pageargs1);   // ne pas sortir pages après l'index de page 8.  if (args.pageindex> = 8)   {  args.hasmorepages = false;  }   }   _x000.
