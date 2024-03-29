﻿---
title: Abra el documento Visio mediante programación
linktitle: Abrir documento Visio
type: docs
weight: 20
url: /es/java/open-visio-document/
description: Esta página describe cómo abrir el documento Visio desde cero con la biblioteca Aspose.Diagram.
---
## **Leer un dibujo Visio existente**
Aspose.Diagram API admite la creación de los nuevos diagramas Visio desde cero y luego los guarda en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar un Visio diagram existente para fines de modificación, adición o procesamiento.
### **Leyendo un Diagram**
Usando Aspose.Diagram API, los desarrolladores pueden cargar todos los formatos de archivo Visio admitidos. Los constructores disponibles de la clase Diagram permiten hacerlo y aceptan una cadena de ruta de archivo válida o un flujo de archivo del archivo fuente Visio.

Los formatos de archivo legibles admitidos son los siguientes:
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM and VSX**

Los constructores de la clase diagram también ofrecen un parámetro opcional que define LoadFileFormat o LoadOptions. Es la información previa a la carga que los desarrolladores pueden pasar al Aspose.Diagram API. Recomendamos pasar la información realista para obtener un rendimiento ideal.
#### **Lectura Diagram Ejemplo de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
