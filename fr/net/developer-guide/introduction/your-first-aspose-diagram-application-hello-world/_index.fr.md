---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /fr/net/your-first-aspose-diagram-application-hello-world/
description: Cette page décrit comment créer la première application avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) classer.
1.  Si vous avez une licence, alors[appliquez-le](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Si vous utilisez la version d'évaluation, ignorez les lignes de code liées à la licence.
1. Créez un nouveau fichier Visio ou ouvrez un fichier Visio existant.
1. Créez une nouvelle zone de texte.
1.  Insérez les mots**Hello World!** dans une zone de texte.
1. Générez le fichier Microsoft Visio modifié.

La mise en œuvre des étapes ci-dessus est illustrée dans les exemples ci-dessous.

### **Exemple de code : création d'un nouveau Diagram**

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


### **Exemple de code : ouverture d'un fichier existant**

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

