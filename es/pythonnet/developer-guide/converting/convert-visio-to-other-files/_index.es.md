---
title:  Convertir Visio a otros formatos
linktitle:  Convertir Visio a otros formatos
type: docs
weight: 40
url: /es/python-net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Exportar a XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 Este artículo explica cómo exportar un Microsoft Visio diagram a XML usando[Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX define un XML diagram.
- VTX define una plantilla XML.
- VSX define una plantilla XML.

 Los constructores de la clase [Diagram] leen un diagram y el método Guardar se usa para guardar o exportar un diagram en un formato de archivo diferente. Los fragmentos de código de este artículo muestran cómo usar el método Guardar para guardar un archivo Visio en[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) y[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

La siguiente imagen muestra el diagram que se exporta en los fragmentos de código a continuación. El archivo exportado se muestra antes de cada fragmento de código.

|**A Microsoft Visio diagram a punto de ser exportado.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_3.png)|

### **Exportar VSD a VDX**
VDX es un formato de archivo XML basado en esquemas que le permite guardar diagramas en un formato que otros productos que no sean Microsoft Visio pueden leer. Es un formato útil para transferir diagramas entre aplicaciones de software y conservar datos editables.

Para exportar un VSD diagram a VDX:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VDX.

|**El archivo VDX exportado.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_4.png)|

### **Exportar del VSD al VSX**
VSX es un formato XML para definir plantillas, los objetos básicos a partir de los cuales se construye un diagram. Cuando un archivo Visio se convierte a VSX, solo se exportan las plantillas.

Para exportar un VSD diagram a VSX:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VSX.
### **Exportar VSD a VTX**
TVX es una representación XML de un archivo de plantilla y almacena la configuración del documento.

Para exportar un VSD diagram a VTX:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase diagram para escribir el archivo de dibujo Visio en el formato VTX.
### **Exportar Microsoft Visio Dibujo a XML**
Los ejemplos de código muestran cómo exportar Microsoft Visio Dibujo a XML usando C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Utilice el constructor de la clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**El documento fuente.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Cree una instancia de la clase Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilice el constructor de la clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

To export VSD diagram to SVG, perform the following steps:

1. Cree una instancia de la clase Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Para exportar un dibujo Visio con formas selectivas:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de cualquier clase SaveOption para especificar la configuración como se describe aquí:[Especifique Visio Guardar opciones](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Llame al método Guardar del objeto de clase Diagram y pase el objeto de clase de opción de guardar como parámetro.
### **Convertir Visio Dibujo con muestra de programación de formas selectivas**
El ejemplo de código muestra cómo exportar un dibujo con formas selectivas Visio.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
