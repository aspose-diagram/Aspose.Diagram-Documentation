---
title: Aspose.Diagram for Java 18.1 Note di rilascio
type: docs
weight: 120
url: /it/java/aspose-diagram-for-java-18-1-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 18.1](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-1-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50200|Aggiunto il supporto per duplicare/clonare una pagina diagram|Aumento|
|DIAGRAMJAVA-50408|Si è verificato un errore dopo aver rimosso una pagina da VSDM|Insetto|
|DIAGRAMJAVA-50577|VDX a VSDM - le linee di collegamento non sono collegate correttamente|Insetto|
|DIAGRAMJAVA-50578|VDX a VSDM - le linee di collegamento non sono collegate correttamente|Insetto|
|DIAGRAMJAVA-50579|Output VDX - posizionamento di tutte le forme Visio sul punto simultaneo|Insetto|
|DIAGRAMJAVA-50580|Output VDX - disposizione errata delle forme|Insetto|
### **Aggiunge un membro Copy nella classe Page**
Il membro copy accetta un'istanza della pagina di destinazione, come parametro per clonare questa pagina.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy page

newPage.copy(diagram.getPages().get(0));

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Copia la pagina Visio in un'altra istanza della pagina]
