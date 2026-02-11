---
title: Arbeta med former Stycke
type: docs
weight: 40
url: /sv/java/working-with-shapes-paragraph/
---
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Ställ in formens stycke.
#### **Ställ in formens styckeprogrammeringsexempel**
Använd följande kod i din Java-applikation för att ställa in formens stycke med Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
