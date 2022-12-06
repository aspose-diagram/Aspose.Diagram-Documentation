---
title: Public API Changements dans Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /fr/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 5.8.0 à 5.9.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
### **Enregistrer le HTML résultant dans un flux**
La nouvelle méthode de sauvegarde a été ajoutée dans la classe Diagram. Il prend deux paramètres, l'objet flux et le format du fichier d'enregistrement.
Exemple de code :

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Copier des thèmes et une feuille de page d'un autre Visio**
La classe Diagram propose la méthode CopyTheme et la classe PageSheet propose la méthode Copy pour atteindre l'objectif de copier une forme et d'autres tâches de manipulation.
 Exemples de codes :[Copier des formes à partir d'un Visio existant](/diagram/fr/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **Les options d'enregistrement VSTX et VSSX sont ajoutées dans SaveFileFormat**
Auparavant, Aspose.Diagram API prenait en charge la lecture et l'écriture au format VSDX, mais maintenant nous avons également ajouté la prise en charge de l'écriture de diagrammes aux formats VSTX et VSSX. Exemples de codes :

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX L'option de lecture est ajoutée dans LoadFileFormat**
Auparavant, Aspose.Diagram API prenait en charge la lecture et l'écriture au format VSDX, mais maintenant nous avons également ajouté la prise en charge de la lecture au format stencil VSSX. Exemples de codes :

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
