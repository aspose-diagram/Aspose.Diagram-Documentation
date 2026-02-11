---
title: Hello World Exemple
type: docs
weight: 100
url: /fr/java/hello-world-example/
---
## **Hello World Exemple**
A "Hello World" example is traditionally used to introduce features of a programming language or software with a simple use case.

Aspose.Diagram for Java is a feature-rich Visio file processing API that allows application developers to embed Visio document creation, reading & conversion features in their Java applications. It supports working with many popular Visio file-formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. The API has strong conversion features to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

Après[installation Aspose.Diagram for Java](/diagram/fr/java/installation/)dans votre environnement, vous pouvez exécuter l'exemple de code ci-dessous pour voir comment Aspose.Diagram API fonctionne.

L'extrait de code ci-dessous suit ces étapes :

1. Instancier un objet Diagram
1. Utilisez la méthode Save de l'objet de classe Diagram pour enregistrer le fichier sur le disque

The following code snippet is a Hello World program to exhibit the working of Aspose.Diagram for Java API. 

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```




