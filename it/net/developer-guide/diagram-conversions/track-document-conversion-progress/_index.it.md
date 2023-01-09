---
title: Tieni traccia dell'avanzamento della conversione del documento
type: docs
weight: 970
url: /it/net/track-document-conversion-progress/
description: Questa sezione spiega come tenere traccia dell'avanzamento della conversione dei file visio con Aspose.Diagram.
---
## **Possibili scenari di utilizzo**

 A volte la conversione di file visio di grandi dimensioni può richiedere del tempo. Durante questo periodo, potresti voler mostrare l'avanzamento della conversione del documento anziché solo una schermata di caricamento per migliorare l'usabilità della tua applicazione. Aspose.Diagram supporta il processo di conversione del documento di monitoraggio fornendo il file**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interfaccia. Il**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**fornisce l'interfaccia**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**e**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**metodi che puoi implementare nella tua classe personalizzata. Puoi anche controllare quali pagine vengono rese come mostrato nel T*estDiagramPageSavingCallback*classe personalizzata.

## **Tieni traccia dell'avanzamento della conversione del documento**

 L'esempio di codice seguente carica il file[fonte visio file](Drawing1.vsdx) e stampa l'avanzamento della conversione nella console utilizzando il file*TestPageSavingCallback* classe personalizzata che implementa il**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**interfaccia.

## **Codice di esempio**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-1.cs" >}}

Quello che segue è il codice per il*TestDiagramPageSavingCallback*classe personalizzata.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-2.cs" >}}

## **Uscita console**

Inizia a salvare l'indice della pagina 0 delle pagine 11</br>
Terminare il salvataggio dell'indice 0 delle pagine 11</br>
Inizia a salvare l'indice della pagina 1 delle pagine 11</br>
Terminare il salvataggio dell'indice 1 delle pagine 11</br>
Inizia a salvare l'indice della pagina 2 delle pagine 11</br>
Terminare il salvataggio dell'indice 2 delle pagine 11</br>
Inizia a salvare l'indice della pagina 3 delle pagine 11</br>
Terminare il salvataggio dell'indice 3 delle pagine 11</br>
Inizia a salvare l'indice della pagina 4 delle pagine 11</br>
Terminare il salvataggio dell'indice 4 delle pagine 11</br>
Inizia a salvare l'indice della pagina 5 delle pagine 11</br>
Terminare il salvataggio dell'indice 5 delle pagine 11</br>
Inizia a salvare l'indice della pagina 6 delle pagine 11</br>
Terminare il salvataggio dell'indice 6 delle pagine 11</br>
Inizia a salvare l'indice della pagina 7 delle pagine 11</br>
Terminare il salvataggio dell'indice 7 delle pagine 11</br>
Inizia a salvare l'indice della pagina 8 delle pagine 11</br>
Terminare il salvataggio dell'indice 8 delle pagine 11
