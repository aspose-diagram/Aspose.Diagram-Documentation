---
title: Ouvrir le document Visio par programmation
linktitle: Ouvrir le document Visio
type: docs
weight: 20
url: /fr/net/open-visio-document/
description: Cette page décrit comment ouvrir le document Visio à partir de zéro avec la bibliothèque Aspose.Diagram.
---
## **Lire un dessin Visio existant**
Aspose.Diagram API prend en charge la création des nouveaux diagrammes Visio à partir de rien, puis les enregistre dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger un Visio diagram existant à des fins de modification, d'ajout ou de traitement.
## **Lecture d'un Diagram**
En utilisant Aspose.Diagram API, les développeurs peuvent charger tous les formats de fichiers Visio pris en charge. Les constructeurs disponibles de la classe Diagram permettent de le faire et ils acceptent une chaîne de chemin de fichier valide ou un flux de fichier du fichier source Visio.

Les formats de fichiers lisibles pris en charge sont les suivants :
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX and VSX**

Les constructeurs de la classe diagram offrent également un paramètre facultatif qui définit LoadFileFormat ou LoadOptions. Il s'agit des informations de préchargement que les développeurs peuvent transmettre au Aspose.Diagram API. Nous recommandons de transmettre les informations réalistes pour obtenir une performance idéale.
## **Lecture Diagram Exemple de programmation**

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

