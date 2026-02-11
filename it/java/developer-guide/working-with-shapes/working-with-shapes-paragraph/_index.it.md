---
title: Lavorare con le forme Paragrafo
type: docs
weight: 40
url: /it/java/working-with-shapes-paragraph/
---
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Imposta il paragrafo della forma.
#### **Impostare l'esempio di programmazione del paragrafo della forma**
Usa il seguente codice nella tua applicazione Java per impostare il paragrafo della forma usando Aspose.Diagram for Java.

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