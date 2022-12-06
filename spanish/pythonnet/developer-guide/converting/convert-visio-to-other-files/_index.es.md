---
title:  Convertir Visio a otros formatos
linktitle:  Convertir Visio a otros formatos
type: docs
weight: 40
url: /es/python-net/convert-visio-to-other-files/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a formatos SVG, XPS, XML, XAML. Convierta VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM a SVG,XPS,XML,XAML con unas pocas líneas de código.
---
## **Exportar a XML**
### **Exportar Microsoft Visio Dibujo a PDF**
Los ejemplos de código muestran cómo exportar el dibujo Microsoft Visio a PDF usando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}

 Este artículo explica cómo exportar un Microsoft Visio diagram a XML usando[Aspose.Diagram para Python vía .NET](https://products.aspose.com/diagram/python-net/) API.

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

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXml.py" >}}

## **Exportar a XPS**
 Este artículo explica cómo exportar un Microsoft Visio diagram a XPS usando[Aspose.Diagram para Python vía .NET](https://products.aspose.com/diagram/python-net/) API.
Utilice el constructor de la clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Los fragmentos de código de este artículo toman el diagram a continuación como entrada. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX o VSX).

|**El documento fuente.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_5.png)|


Para exportar VSD diagram a XPS:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase Diagram y establezca XPS como formato de salida.
### **Exportar Microsoft Visio Dibujo a XPS**
Los ejemplos de código muestran cómo exportar el dibujo Microsoft Visio a XPS usando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXps.py" >}}

## **Exportar un Diagram a SVG**
Este artículo explica cómo exportar un Microsoft Visio diagram a SVG (Scalable Vector Graphics) usando[Aspose.Diagram para Python vía .NET](https://products.aspose.com/diagram/python-net/) API.

Utilice el constructor de la clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar VSD diagram a SVG, realice los siguientes pasos:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase y establezca SVG como formato de exportación.
### **Exportar Microsoft Visio Dibujo a SVG**
Los ejemplos de código muestran cómo exportar un diagram a SVG usando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToSvg.py" >}}

Para exportar un dibujo Visio con formas selectivas:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de cualquier clase SaveOption para especificar la configuración como se describe aquí:[Especifique Visio Guardar opciones](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Llame al método Guardar del objeto de clase Diagram y pase el objeto de clase de opción de guardar como parámetro.
### **Convertir Visio Dibujo con muestra de programación de formas selectivas**
El ejemplo de código muestra cómo exportar un dibujo con formas selectivas Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-PythonNet-ConvertVisioWithSelectiveShapes.py" >}}