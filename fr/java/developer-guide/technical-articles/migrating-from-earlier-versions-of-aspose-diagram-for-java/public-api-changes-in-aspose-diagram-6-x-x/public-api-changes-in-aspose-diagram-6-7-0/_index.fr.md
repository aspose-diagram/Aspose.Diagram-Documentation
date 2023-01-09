---
title: Public API Changements dans Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /fr/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.6.0 à 6.7.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
### **Ajoute la méthode detectFileFormat dans la classe FileFormatUtil**
Il détecte et renvoie les informations sur le format d'un Visio diagram stocké dans un flux d'entrée. Veuillez vérifier cet exemple de code :

**Java**

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Open the stream. Read only access to load a Visio diagram.

InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

// detect file format using an input stream

FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format

System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
