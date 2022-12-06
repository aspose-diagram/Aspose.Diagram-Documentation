---
title:  Convertir Visio a formato PDF
linktitle: Convertir Visio a PDF
type: docs
weight: 10
url: /es/java/convert-visio-to-pdf/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a formatos PDF. Convierta VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM a PDF con unas pocas líneas de código.
---
## **Exportando a PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java escribe directamente la información sobre API y el número de versión en los documentos de salida. Por ejemplo, al renderizar un Dibujo a PDF, Aspose.Diagram for Java se completa**Solicitud**campo con valor 'Aspose.Diagram' y**Productor de PDF**campo con un valor, por ejemplo, 'Aspose.Diagram 17.9'.

Tenga en cuenta que no puede indicar al Aspose.Diagram for Java API que cambie o elimine esta información de los documentos de salida.

{{% /alert %}}

 Este artículo explica cómo exportar un Microsoft Visio diagram a PDF usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizar el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) constructor de clase para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

La siguiente imagen muestra el VSD diagram que los fragmentos de código debajo exportan PDF. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

**El archivo fuente.**

![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_1.png)

Para exportar VSD diagram a PDF:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de clases Diagram y establezca el formato de salida en PDF.

A continuación se muestra una imagen del archivo PDF de salida.

**El archivo PDF de salida.**

![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_2.png)
### **Ejemplo de programación de exportación a PDF**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Dividir varias páginas**
Aspose.Diagram for Java permite dividir varias páginas al convertir Microsoft Visio Diagram a PDF. El siguiente fragmento de código muestra la funcionalidad.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Usar página Guardar devolución de llamada**
En caso de que tenga varias páginas, Aspose.Diagram for Java le permite usar la devolución de llamada para guardar páginas mientras convierte Microsoft Visio Diagram a PDF. El siguiente fragmento de código muestra la funcionalidad.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **Clase TestDiagramPageSavingCallback**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
