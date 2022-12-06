---
title:  Convertir Visio a formato PDF
linktitle: Convertir Visio a PDF
type: docs
weight: 10
url: /es/python-java/convert-visio-to-pdf/
description: Este tema le muestra cómo convertir Visio a formatos PDF usando Aspose.Diagram para Python a través de Java. Convertir VSD, vss, vdw, vst, VSDX, VSSX, VSTX, 076181, 076181.
---
## **Exportando a PDF**
{{% alert color="primary" %}}

Aspose.Diagram para Python a través de Java escribe directamente la información sobre API y el número de versión en los documentos de salida. Por ejemplo, al renderizar un Dibujo a PDF, Aspose.Diagram for Java se completa**Solicitud**campo con valor 'Aspose.Diagram' y**Productor de PDF**campo con un valor, por ejemplo, 'Aspose.Diagram 17.9'.

Tenga en cuenta que no puede dar instrucciones al Aspose.Diagram para el Python a través del Java para cambiar o eliminar esta información de los documentos de salida.

{{% /alert %}}

Este artículo explica cómo exportar un Microsoft Visio diagram a PDF usando Aspose.Diagram para Python a través de Java.

Utilice el constructor de la clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

[El VSD diagram](ExportToPDF.vsd) es el archivo de dibujo de ejemplo para exportar PDF. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

Para exportar VSD diagram a PDF:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de clases Diagram y establezca el formato de salida en PDF.

### **Ejemplo de programación de exportación a PDF**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Dividir varias páginas**
Aspose.Diagram for Java permite dividir varias páginas al convertir Microsoft Visio Diagram a PDF. El siguiente fragmento de código muestra la funcionalidad.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
