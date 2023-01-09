﻿---
title: Gestisci i codici VBA di Visio Macro abilitato diagram.
linktitle: Diagram Progetto VBA
type: docs
weight: 200
url: /it/java/working-with-vbaproject/
description: Aggiungi modulo VBA e modifica VBA o macro con la libreria Aspose.Diagram.
---
## **Aggiungi un modulo VBA**
{{% alert color="primary" %}}

Aspose.Diagram consente di aggiungere un nuovo modulo VBA e codice macro utilizzando Aspose.Diagram. Utilizzare il metodo [**Diagram.VbaProject.Modules.Add()**] per aggiungere il nuovo modulo VBA all'interno di diagram

{{% /alert %}}

 Il codice di esempio seguente aggiunge un nuovo modulo VBA e un codice macro e salva l'output nel formato VSDM. Una volta, aprirai il file di output VSDM in Microsoft Visio e fai clic sul pulsante**Sviluppatore > Visual Basic** comandi di menu, vedrai un modulo chiamato "TestModule" e al suo interno vedrai il seguente codice macro.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Ecco il codice di esempio per generare il file di output VSDM con il modulo VBA e il codice macro.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-Vba-AddModule.java" >}}

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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-Vba-ModifyModule.java" >}}

## **Argomenti avanzati**
- [Controlla se il codice VBA è firmato](/diagram/it/java/check-if-vba-code-is-signed/)
