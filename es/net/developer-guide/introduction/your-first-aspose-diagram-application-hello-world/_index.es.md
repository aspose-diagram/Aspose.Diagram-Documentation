---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /es/net/your-first-aspose-diagram-application-hello-world/
description: Esta página describe cómo crear la primera aplicación con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) clase.
1.  Si tiene una licencia, entonces[apliquelo](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Si está utilizando la versión de evaluación, omita las líneas de código relacionadas con la licencia.
1. Cree un nuevo archivo Visio o abra un archivo Visio existente.
1. Crear un nuevo cuadro de texto.
1.  Inserta las palabras**Hello World!** en un cuadro de texto.
1. Genere el archivo Microsoft Visio modificado.

La implementación de los pasos anteriores se demuestra en los siguientes ejemplos.

### **Ejemplo de código: creación de un nuevo Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


### **Ejemplo de código: abrir un archivo existente**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.


{{< highlight csharp >}}
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

