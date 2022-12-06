---
title: Définir l'orientation et contrôler l'exportation des pages masquées Visio lors de l'enregistrement
type: docs
weight: 20
url: /fr/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Changer une mise en page Visio en portrait ou paysage**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API permet aux développeurs de définir l'orientation de la page de dessin Visio par programmation. Cette rubrique d'aide explique comment accomplir cette tâche.

 Aspose.Diagram for Java API a le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés d'impression. Le champ PrintPageOrientation des propriétés d'impression permet de faire pivoter la page. Il offre trois options : Portrait, Paysage et même que sur l'imprimante. Le champ PrintPageOrientation peut être défini par programmation à l'aide de Aspose.Diagram API.

Cet exemple fonctionne comme suit :

1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Extraire une page Visio
1. Définissez son orientation sur Portrait, Paysage ou identique à celle de l'imprimante.
1. Enregistrez le Visio diagram.
### **Définir l'exemple de programmation d'orientation**
L'exemple de code ci-dessous montre comment définir l'orientation de la page Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Contrôler l'exportation des pages masquées Visio lors de l'enregistrement**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API permet aux développeurs d'inclure ou d'exclure des pages Visio masquées lors de l'enregistrement de diagram dans des fichiers PDF, HTML, Image (PNG, JPEG, GIF), SVG et XPS. Même eux peuvent masquer les pages Visio en utilisant Aspose.Diagram API car son option est déjà disponible via la cellule UIVisibility dans la page ShapeSheet.
### **Masquer une page dans le Visio Diagram et définir l'option d'exportation**
 Aspose.Diagram for Java API a le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés de la page. Le champ UIVisibility des propriétés de la page permet de masquer la page. Les développeurs peuvent ensuite utiliser la propriété ExportHiddenPage qui est ajoutée dans les classes SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions et PdfSaveOptions.
#### **Définir l'option d'exportation pour PDF**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Définir l'option d'exportation pour HTML**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Définir l'option d'exportation pour l'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format image.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Définir l'option d'exportation pour SVG**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
