---
title: Impostare l'orientamento e controllare l'esportazione delle pagine nascoste Visio al salvataggio
type: docs
weight: 20
url: /it/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Cambia un layout di pagina Visio in Verticale o Orizzontale**
Aspose.Diagram for Python via Java API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The PrintPageOrientation field can be set programmatically using Aspose.Diagram for Python via Java API.

Questo esempio funziona come segue:

1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Estrai una pagina Visio
1. Impostare il suo orientamento come Verticale, Orizzontale o uguale a quello della stampante.
1. Salva lo Visio diagram.

### **Esempio di programmazione dell'orientamento impostato**
L'esempio di codice seguente mostra come impostare l'orientamento della pagina Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **Controlla l'esportazione di pagine nascoste Visio al salvataggio**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram for Python via Java API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### **Nascondi una pagina nel Visio Diagram e imposta l'opzione di esportazione**
Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the page properties. The `UIVisibility` field of the page properties allows to hide the page. Developers can then use `exportHiddenPage` property which is added in the `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` and `PdfSaveOptions` classes.

#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **Impostare l'opzione di esportazione per l'immagine**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato immagine.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
