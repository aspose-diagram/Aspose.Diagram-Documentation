---
title: Configurazione dei caratteri per il rendering
type: docs
weight: 10
url: /it/net/configuring-fonts-for-rendering/
---
## **Possibili scenari di utilizzo**

Aspose.Diagram Le API forniscono la possibilità di eseguire il rendering delle pagine in formati immagine e di convertirle in formati PDF e XPS. Per massimizzare la fedeltà della conversione, è necessario che i caratteri utilizzati nel foglio di calcolo siano disponibili nella directory dei caratteri predefinita del sistema operativo. Nel caso in cui i font richiesti non siano presenti allora le API Aspose.Diagram cercheranno di sostituire i font richiesti con quelli disponibili.

## **Selezione dei caratteri**

Di seguito è riportato il processo che le API Aspose.Diagram seguono dietro le quinte.

1. Lo API tenta di trovare i caratteri sul file system corrispondenti al nome esatto del carattere utilizzato nel foglio di calcolo.
1.  Se API non è in grado di individuare il carattere definito in**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** proprietà, tenta di utilizzare il carattere specificato in**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**proprietà.
1.  Se API non è in grado di individuare il carattere definito in**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** proprietà, tenta di selezionare i caratteri più adatti tra tutti i caratteri disponibili.
1. Infine, se API non riesce a trovare alcun carattere nel file system, esegue il rendering della pagina utilizzando Times New Roman.

## **Imposta cartelle di caratteri personalizzati**

 Aspose.Diagram Le API ricercano i caratteri richiesti nella directory dei caratteri predefinita del sistema operativo. Nel caso in cui i caratteri richiesti non siano disponibili nella directory dei caratteri del sistema, le API effettuano la ricerca nelle directory personalizzate (definite dall'utente). Il**[FontConfigs](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class ha esposto diversi modi per impostare directory di font personalizzate come descritto di seguito.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Questo metodo è utile se c'è solo una cartella da impostare.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**Questo metodo è utile quando i font risiedono in più cartelle e l'utente desidera impostare tutte le cartelle separatamente piuttosto che combinare tutti i font in un'unica cartella.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: Questo meccanismo è utile quando l'utente desidera caricare font da più cartelle o un singolo file di font o dati di font da un array di byte.

{{% alert color="primary" %}}

 Tutti e due**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** i metodi accettano un secondo parametro di tipo booleano. Di passaggio**VERO** poiché il secondo parametro indirizzerà le API Aspose.Diagram a cercare nelle sottocartelle i file dei caratteri.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Si prega di utilizzare uno dei metodi sopra menzionati all'inizio dell'applicazione, ovvero; prima di richiamare qualsiasi altro oggetto delle API Aspose.Diagram.

{{% /alert %}} {{% alert color="primary" %}}

Se vengono utilizzati tutti i metodi sopra menzionati per impostare le origini dei caratteri, avranno effetto solo le ultime impostazioni.

{{% /alert %}}

