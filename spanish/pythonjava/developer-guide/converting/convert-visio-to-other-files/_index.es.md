---
title:  Convertir Visio a otros formatos
linktitle:  Convertir Visio a otros formatos
type: docs
weight: 40
url: /es/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML con unas pocas líneas de código.
---
**[A Microsoft Visio diagram para exportar.](ExportToXML.vsd)**

## **Exportando a XML**
Este artículo explica cómo exportar un Microsoft Visio diagram a XML usando Aspose.Diagram para Python a través de Java.

- VDX define un XML diagram.
- VTX define una plantilla XML.
- VSX define una plantilla XML.

Los constructores de la clase Diagram leen un diagram y el método Guardar se usa para guardar o exportar un diagram en un formato de archivo diferente. Los fragmentos de código de este artículo muestran cómo usar el método Guardar para guardar un archivo Visio en los formatos VDX, VTX y VSX.

### **Exportando VSD a VDX**
VDX es un formato de archivo XML basado en esquemas que le permite guardar diagramas en un formato que otros productos que no sean Microsoft Visio pueden leer. Es un formato útil para transferir diagramas entre aplicaciones de software y conservar datos editables.

Para exportar un VSD diagram a VDX:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VDX.

### **Exportando de VSD a VSX**
VSX es un formato XML para definir plantillas, los objetos básicos a partir de los cuales se construye un diagram. Cuando un archivo Visio se convierte a VSX, solo se exportan las plantillas.

Para exportar un VSD diagram a VSX:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VSX.

La siguiente imagen muestra el archivo de salida VSX. Tenga en cuenta que se exportan las plantillas utilizadas en el diagram, no el diagram en sí.

### **Exportar VSD a VTX**
TVX es una representación XML de un archivo de plantilla y almacena la configuración del documento.

Para exportar un VSD diagram a VTX:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase diagram para escribir el archivo de dibujo Visio en el formato VTX.

La siguiente imagen muestra el archivo de salida VTX.

### **Ejemplo de programación de exportación a XML**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **Exportando a XPS**
Este artículo explica cómo exportar un Microsoft Visio diagram a XPS usando Aspose.Diagram para Python a través de Java.
Utilice el constructor de la clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Los fragmentos de código de este artículo toman el diagram a continuación como entrada. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

Para exportar VSD diagram a XPS:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase Diagram y establezca XPS como formato de salida.

La siguiente imagen muestra el archivo XPS de salida.

### **Ejemplo de programación de exportación a XPS**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Exportando un Diagram a SVG**
Este artículo explica cómo exportar un Microsoft Visio diagram a SVG (Scalable Vector Graphics) usando Aspose.Diagram para Python a través de Java.

Utilice el constructor de la clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar VSD diagram a SVG, realice los siguientes pasos:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de la clase y establezca SVG como formato de exportación.

### **Exportación de Diagram a muestra de programación SVG**
Los ejemplos de código muestran cómo exportar un diagram a SVG usando Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Exportando un Diagram a XAML**
Este artículo explica cómo exportar un Microsoft Visio diagram a XAML (lenguaje de marcado de aplicación extensible) usando Aspose.Diagram para Python a través de Java.

Utilice el constructor de la clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar un VSD diagram a XAML:

1. Cree una instancia de la clase Diagram.
1. Llame al método Save de la clase y establezca XAML como formato de exportación.

### **Ejemplo de programación de exportación a XAML**
El ejemplo de código muestra cómo exportar un diagram a XAML usando Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Convert Visio Dibujo con formas selectivas**
Usando Aspose.Diagram API, los desarrolladores pueden seleccionar un grupo de formas para convertir un dibujo Visio en cualquier otro formato compatible. La clase RenderingSaveOptions ofrece un miembro Shapes para mantener el grupo de formas. Cada clase de opción de guardado es la forma extendida de la clase RenderingSaveOptions.

Para exportar un dibujo Visio con formas selectivas:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de cualquier clase SaveOption para especificar la configuración como se narra
1. Llame al método de guardado del objeto de clase Diagram y pase el objeto de clase de opción de guardado como parámetro.

### **Convertir Visio Dibujo con muestra de programación de formas selectivas**
El ejemplo de código muestra cómo exportar un dibujo con formas selectivas Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}