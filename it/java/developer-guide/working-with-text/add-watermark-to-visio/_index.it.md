---
title: Aggiungi filigrana a Visio
type: docs
weight: 10
url: /it/java/add-watermark-to-visio/
keywords: watermark, visi
description: Come aggiungere filigrana a visio utilizzando Java Diagram API.
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for Java consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Aggiungi filigrana a visio nella pagina
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Aggiungi un esempio di programmazione in filigrana**
Il codice di esempio seguente mostra come aggiungere filigrana nel file Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
