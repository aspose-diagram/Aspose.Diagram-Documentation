---
title: Définir l'orientation et contrôler l'exportation des pages masquées Visio lors de l'enregistrement
type: docs
weight: 20
url: /fr/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Cette section explique comment définir la mise en page de la page avec Aspose.Diagram.
---
## **Changer une mise en page Visio en portrait ou paysage**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API permet aux développeurs de définir l'orientation de la page de dessin Visio par programmation. Cette rubrique d'aide explique comment accomplir cette tâche.

 Aspose.Diagram for .NET API a le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés d'impression. Le champ PrintPageOrientation des propriétés d'impression permet de faire pivoter la page. Il offre trois options : Portrait, Paysage et même que sur l'imprimante. Le champ PrintPageOrientation peut être défini par programmation à l'aide de Aspose.Diagram API.

Cet exemple fonctionne comme suit :

1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Extraire une page Visio
1. Définissez son orientation sur Portrait, Paysage ou identique à celle de l'imprimante.
1. Enregistrez le Visio diagram.
### **Définir l'exemple de programmation d'orientation**
L'exemple de code ci-dessous montre comment définir l'orientation de la page Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Contrôler l'exportation des pages masquées Visio lors de l'enregistrement**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API permet aux développeurs d'inclure ou d'exclure des pages Visio masquées lors de l'enregistrement de diagram dans des fichiers PDF, HTML, Image (PNG, JPEG, GIF), SVG et XPS. Même eux peuvent masquer les pages Visio en utilisant Aspose.Diagram API car son option est déjà disponible via la cellule UIVisibility dans la page ShapeSheet.
### **Masquer une page dans le Visio Diagram et définir l'option d'exportation**
 Aspose.Diagram for .NET API a le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés de la page. Le champ UIVisibility des propriétés de la page permet de masquer la page. Les développeurs peuvent ensuite utiliser la propriété ExportHiddenPage qui est ajoutée dans les classes SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions et PdfSaveOptions.
#### **Définir l'option d'exportation pour PDF**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Définir l'option d'exportation pour HTML**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Définir l'option d'exportation pour l'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format image.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Définir l'option d'exportation pour SVG**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Définir l'option d'exportation pour XPS**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
