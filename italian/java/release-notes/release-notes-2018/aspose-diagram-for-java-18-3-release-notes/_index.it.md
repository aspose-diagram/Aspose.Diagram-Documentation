---
title: Aspose.Diagram for Java 18.3 Note di rilascio
type: docs
weight: 100
url: /it/java/aspose-diagram-for-java-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 18.3](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-3-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50592|Aggiungere il supporto delle istruzioni di elaborazione NewValue|Aumento|
|DIAGRAMJAVA-50150|Impossibile accedere agli oggetti TabsCollection della forma|Insetto|
|DIAGRAMJAVA-50588|Output VSDX - viene aggiunta una forma di grandi dimensioni|Insetto|
|DIAGRAMJAVA-50593|VSDX in SVG - testo e colori di sfondo errati|Insetto|
|DIAGRAMJAVA-50595|Diagram diventa bianco e nero durante il salvataggio del documento VSDX|Insetto|
### **Aggiunge il membro moveTo nella classe Page**
Il membro moveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Sposta posizione pagina nel disegno Visio]
