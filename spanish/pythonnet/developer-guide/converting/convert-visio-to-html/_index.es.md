---
title:  Convertir Visio a formato HTML
linktitle: Convertir Visio a HTML
type: docs
weight: 30
url: /es/python-net/convert-visio-to-html/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a formatos html. Convierta VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM a html con unas pocas líneas de código.
---
## **Exportar Visio a HTML**
 Este artículo explica cómo exportar un Microsoft Visio diagram a HTML usando[Aspose.Diagram para Python vía .NET](https://products.aspose.com/diagram/python-net/) API.

Utilice el constructor de clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible. Los desarrolladores pueden guardar el HTML resultante en el almacenamiento local o directamente en una instancia de transmisión.

1. [Guarde el HTML resultante en el almacenamiento local](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Guarde el HTML resultante en una instancia de flujo](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

La siguiente imagen muestra un archivo VSD a punto de guardarse en formato PNG. También puede usar otros formatos diagram (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX o 34711).

|**Entrada diagram.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_6.png)|
Para exportar VSD diagram a HTML, realice los siguientes pasos:

1. Cree una instancia de la clase Diagram.
1. Llame al método Save de la clase Dagram y establezca HTML como formato de salida.
### **Guarde el HTML resultante en el almacenamiento local**
El archivo resultante se puede guardar pasando una cadena de ruta completa, incluido el nombre del archivo y la extensión, por ejemplo, @"c:\temp\MyOutput.html".
#### **Guardar HTML resultante en el ejemplo de programación de almacenamiento local**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
