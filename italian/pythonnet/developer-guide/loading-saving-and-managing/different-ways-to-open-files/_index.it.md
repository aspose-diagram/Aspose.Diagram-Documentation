---
title: Diversi modi per aprire i file
type: docs
weight: 10
url: /it/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Con Aspose.Diagram è semplice aprire file, ad esempio, per recuperare dati o utilizzare un modello di designer per velocizzare il processo di sviluppo.

{{% /alert %}}

## **Apertura di un file tramite un percorso**

 Gli sviluppatori possono aprire un file Microsoft Diagram utilizzando il relativo percorso file sul computer locale specificandolo nel**Diagram**costruttore di classe. Basta passare il percorso nel costruttore come a*corda*. Aspose.Diagram rileverà automaticamente il tipo di formato del file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Apertura di un file tramite un flusso**

 È anche semplice aprire un file Visio come flusso. Per fare ciò, usa una versione sovraccaricata del costruttore che accetta il*BufferStream*oggetto che contiene il file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Apertura di un file con LoadOptions**

 Per aprire un file con opzioni di caricamento, utilizzare il file**LoadOptions**classes per impostare le opzioni correlate delle classi per il file modello da caricare.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

