---
title: Configurazione dei caratteri per il rendering
type: docs
weight: 10
url: /it/net/configuring-fonts-for-rendering/
---
## **Possibili scenari di utilizzo**

Aspose.Diagram APIs provide the facility to render pages in image formats as well as convert them to PDF & XPS formats. In order to maximize the conversion fidelity, it is necessary that the fonts used in the spreadsheet should be available in the operating system's default font directory. In case the required fonts are not present then the Aspose.Diagram APIs will try to substitute the required fonts with the ones available.

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Setting default font
Aspose.Diagram.FontConfigs.DefaultFontName = "Arial";
// Setting the custom font directories
Aspose.Diagram.FontConfigs.SetFontFolder(Environment.GetFolderPath(Environment.SpecialFolder.Fonts), false);

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "Font.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


{{% alert color="primary" %}}

Si prega di utilizzare uno dei metodi sopra menzionati all'inizio dell'applicazione, ovvero; prima di richiamare qualsiasi altro oggetto delle API Aspose.Diagram.

{{% /alert %}} {{% alert color="primary" %}}

Se vengono utilizzati tutti i metodi sopra menzionati per impostare le origini dei caratteri, avranno effetto solo le ultime impostazioni.

{{% /alert %}}

