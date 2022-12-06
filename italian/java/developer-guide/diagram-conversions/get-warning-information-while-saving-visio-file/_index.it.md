---
title: Ottieni informazioni di avviso durante il salvataggio del file Visio
type: docs
weight: 110
url: /it/java/get-warning-information-while-saving-visio-file/
---
## **Possibili scenari di utilizzo**

 A volte l'utente cerca di salvare lo diagram che contiene testo che non ha un font locale. In tal caso, Aspose.Diagram genera avvisi durante il salvataggio di diagram. È possibile rilevare questi avvisi implementando il**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** interfaccia e impostazione**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**proprietà.

## **Ricevi avvisi durante il salvataggio del file Visio**

 Il seguente codice di esempio spiega come ottenere avvisi durante il salvataggio del file visio. Il codice converte il file[file di esempio visio](sampleFontSubstitution.vsdx) che lancia**[Sostituzione carattere](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** avviso sul salvataggio. Questo avviso viene quindi catturato da**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**metodo che stampa i messaggi di avviso sulla console. Si prega di controllare anche l'output della console del codice indicato di seguito per una maggiore comprensione.

## **Codice di esempio**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Uscita console**

Ecco l'output della console del codice precedente quando eseguito con il file fornito[file di esempio visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
