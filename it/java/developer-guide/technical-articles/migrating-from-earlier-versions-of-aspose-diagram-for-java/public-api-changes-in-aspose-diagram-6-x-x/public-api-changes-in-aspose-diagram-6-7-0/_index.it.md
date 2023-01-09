---
title: Pubblico API Modifiche Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /it/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.6.0 alla 6.7.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Aggiunge il metodo detectFileFormat nella classe FileFormatUtil**
Rileva e restituisce le informazioni sul formato di un Visio diagram memorizzato in un flusso di input. Si prega di controllare questo esempio di codice:

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
