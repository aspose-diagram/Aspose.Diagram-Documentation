---
title: Convert Visio to HTML format 
linktitle: Convert Visio to HTML
type: docs
weight: 30
url: /es/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Exportar Visio a HTML** ##
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for Python via Java](https://products.aspose.com/diagram/python-java/) API.

Use the Diagram class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

 La imagen de abajo muestra un[VSD archivo](ExportToHTML.vsd) about to be saved to PNG format. You can use other diagram formats (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

**Entrada diagram.**

![todo:imagen_alternativa_texto](http://i.imgur.com/YX4BNNq.png)

In order to export VSD diagram to HTML, perform the following steps:

1. Cree una instancia de la clase Diagram.
1. Call the Dagram class' Save method and set HTML as the output format.

La siguiente imagen muestra el archivo de salida HTML.

**Output HTML diagram.**

![todo:imagen_alternativa_texto](http://i.imgur.com/syavUqI.png)

### **Save resultant HTML in the local storage**
El archivo resultante se puede guardar pasando una cadena de ruta completa, incluido el nombre del archivo y la extensión, por ejemplo, @"c:\temp\MyOutput.html".

#### **Save Resultant HTML in Local Storage Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Save resultant HTML in a stream instance**
It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.
#### **Save Resultant HTML in a Stream Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
