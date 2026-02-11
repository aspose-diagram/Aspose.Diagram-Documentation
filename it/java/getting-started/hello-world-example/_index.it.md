---
title: Hello World Esempio
type: docs
weight: 100
url: /it/java/hello-world-example/
---
## **Hello World Esempio**
A "Hello World" example is traditionally used to introduce features of a programming language or software with a simple use case.

Aspose.Diagram for Java is a feature-rich Visio file processing API that allows application developers to embed Visio document creation, reading & conversion features in their Java applications. It supports working with many popular Visio file-formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. The API has strong conversion features to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

Dopo[installazione Aspose.Diagram for Java](/diagram/it/java/installation/)nel tuo ambiente, puoi eseguire l'esempio di codice seguente per vedere come funziona Aspose.Diagram API.

Sotto lo snippet di codice segue questi passaggi:

1. Crea un'istanza di un oggetto Diagram
1. Utilizzare il metodo Save dell'oggetto di classe Diagram per salvare il file su disco

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




