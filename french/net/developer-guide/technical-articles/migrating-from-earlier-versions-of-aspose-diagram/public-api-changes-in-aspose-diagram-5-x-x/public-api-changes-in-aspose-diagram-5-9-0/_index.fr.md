---
title: Public API Changements dans Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 5.8.0 à 5.9.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Enregistrer le HTML résultant dans un flux**
La nouvelle méthode Save a été ajoutée dans la classe Diagram. Il prend deux paramètres, l'objet flux et le format du fichier d'enregistrement.
Exemple de code :

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Copier des thèmes et une feuille de page d'un autre Visio**
La classe Diagram propose la méthode CopyTheme et la classe PageSheet propose la méthode Copy pour atteindre l'objectif de copier une forme et d'autres tâches de manipulation.
 Exemples de codes :[Copier des formes à partir d'un Visio existant](/diagram/fr/net/add-retrieve-copy-and-read-visio-shape-data/)
## **Les options d'enregistrement VSTX et VSSX sont ajoutées dans SaveFileFormat**
Auparavant, Aspose.Diagram API prenait en charge la lecture et l'écriture au format VSDX, mais maintenant nous avons également ajouté la prise en charge de l'écriture de diagrammes aux formats VSTX et VSSX. Exemples de codes :

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX L'option de lecture est ajoutée dans LoadFileFormat**
Auparavant, Aspose.Diagram API prenait en charge la lecture et l'écriture au format VSDX, mais maintenant nous avons également ajouté la prise en charge de la lecture au format stencil VSSX. Exemples de codes :

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
