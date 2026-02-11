---
title: Abra el documento Visio mediante programación
linktitle: Abrir documento Visio
type: docs
weight: 20
url: /es/net/open-visio-document/
description: Esta página describe cómo abrir el documento Visio desde cero con la biblioteca Aspose.Diagram.
---
## **Leer un dibujo Visio existente**
Aspose.Diagram API admite la creación de los nuevos diagramas Visio desde cero y luego los guarda en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar un Visio diagram existente para fines de modificación, adición o procesamiento.
## **Leyendo un Diagram**
Usando Aspose.Diagram API, los desarrolladores pueden cargar todos los formatos de archivo Visio admitidos. Los constructores disponibles de la clase Diagram permiten hacerlo y aceptan una cadena de ruta de archivo válida o un flujo de archivo del archivo fuente Visio.

Los formatos de archivo legibles admitidos son los siguientes:
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX and VSX**

Los constructores de la clase diagram también ofrecen un parámetro opcional que define LoadFileFormat o LoadOptions. Es la información previa a la carga que los desarrolladores pueden pasar al Aspose.Diagram API. Recomendamos pasar la información realista para obtener un rendimiento ideal.
## **Lectura Diagram Ejemplo de programación**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
