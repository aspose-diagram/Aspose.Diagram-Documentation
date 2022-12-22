---
title: Définir l'orientation et contrôler l'exportation des pages masquées Visio lors de l'enregistrement
type: docs
weight: 20
url: /fr/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Changer une mise en page Visio en portrait ou paysage**
Aspose.Diagram for Python via Java API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The PrintPageOrientation field can be set programmatically using Aspose.Diagram for Python via Java API.

Cet exemple fonctionne comme suit :

1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Extraire une page Visio
1. Définissez son orientation sur Portrait, Paysage ou identique à celle de l'imprimante.
1. Enregistrez le Visio diagram.

### **Définir l'exemple de programmation d'orientation**
L'exemple de code ci-dessous montre comment définir l'orientation de la page Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **Contrôler l'exportation des pages masquées Visio lors de l'enregistrement**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram for Python via Java API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### **Masquer une page dans le Visio Diagram et définir l'option d'exportation**
Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the page properties. The `UIVisibility` field of the page properties allows to hide the page. Developers can then use `exportHiddenPage` property which is added in the `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` and `PdfSaveOptions` classes.

#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **Définir l'option d'exportation pour l'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format image.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
