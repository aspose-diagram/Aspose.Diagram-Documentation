---
title: Gestisci i codici VBA di Visio Macro abilitato diagram.
linktitle: Diagram Progetto VBA
type: docs
weight: 200
url: /it/net/working-with-vbaproject/
description: Aggiungi modulo VBA e modifica VBA o macro con la libreria Aspose.Diagram.
---
## **Aggiungi un modulo VBA**
{{% alert color="primary" %}}

 Aspose.Diagram consente di aggiungere un nuovo modulo VBA e codice macro utilizzando Aspose.Diagram. Utilizzare il[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) metodo per aggiungere il nuovo modulo VBA all'interno del diagram

{{% /alert %}}

 Il codice di esempio seguente aggiunge un nuovo modulo VBA e un codice macro e salva l'output nel formato VSDM. Una volta, aprirai il file di output VSDM in Microsoft Visio e fai clic sul pulsante**Sviluppatore > Visual Basic** comandi di menu, vedrai un modulo chiamato "TestModule" e al suo interno vedrai il seguente codice macro.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Ecco il codice di esempio per generare il file di output VSDM con il modulo VBA e il codice macro.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.VbaProject.Modules.Add(VbaModuleType.Procedural, "TestModule");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[index];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **Modifica VBA o Macro**

{{% alert color="primary" %}} 

È possibile modificare VBA o codice macro utilizzando Aspose.Diagram. Aspose.Diagram ha aggiunto il seguente spazio dei nomi e classi per leggere e modificare il progetto VBA nel file Visio.

- Aspose.Diagram.Vba
- VbaProject
- VbaModuleCollection
- Modulo Vba

Questo articolo ti mostrerà come modificare il codice VBA o macro all'interno del file sorgente Visio utilizzando Aspose.Diagram.

{{% /alert %}} 

Il seguente codice di esempio carica il file sorgente Visio che contiene al suo interno un codice VBA o Macro seguente

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Dopo l'esecuzione del codice di esempio Aspose.Diagram, il codice VBA o Macro verrà modificato in questo modo

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Puoi scaricare il[fonte Visio file]() e il[output Visio file]() dai link indicati.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[2];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **Argomenti avanzati**
- [Controlla se il codice VBA è firmato](/diagram/it/net/check-if-vba-code-is-signed/)
