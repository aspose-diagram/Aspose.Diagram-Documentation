---
title: Scarica e configura Aspose.Diagram in PHP
type: docs
weight: 10
url: /it/java/download-and-configure-aspose-diagram-in-php/
---
## **Scarica le librerie richieste**
Scarica le librerie richieste menzionate di seguito. Questi sono i requisiti per l'esecuzione di Aspose.Diagram Java per gli esempi di Ruby.

- [Aspose.Diagram for Java Componente](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Scarica esempi dai siti di codifica sociale**
Le seguenti versioni di esempi in esecuzione sono disponibili per il download sui siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Installazione**
È molto semplice e facile da installare Aspose.Diagram Java per PHP, segui le istruzioni:

Esegui il seguente comando.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Usando**
Includere i file richiesti per esportare il disegno visio in un documento Pdf.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Comprendiamo il codice sopra.

1. La prima riga assicura che lo Aspose.Diagram sia caricato e disponibile.
1. Includere i file necessari per accedere allo Aspose.Diagram
1. Inizializzare le librerie. Le classi aspose Java vengono caricate dal percorso fornito nel file aspose.yml
