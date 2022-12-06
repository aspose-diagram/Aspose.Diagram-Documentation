---
title: Aspose.Diagram for Java Note sulla versione 19.11
type: docs
weight: 20
url: /it/java/aspose-diagram-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 19.11.

{{% /alert %}} 
## **Miglioramenti e modifiche**
La versione di questo mese consente di formattare Visio pagine per[applicare i fogli di stile](/diagram/it/java/format-visio-pages/).

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50671|L'impostazione della nuova finestra del foglio di forma non viene rispettata durante la conversione in SVG|Aumento|
### **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram per JAVA. In caso di dubbi su qualsiasi modifica elencata, segnalarla al forum di supporto Aspose.Diagram.
### **Aggiunto applyStyle in Page**
{{< highlight "java" >}}

 StyleSheet st = new StyleSheet();

dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### ` `**Aggiunto smaltimento nella classe Diagram**
Esegue attività definite dall'applicazione associate alla liberazione, al rilascio o al ripristino delle risorse non gestite.

{{< highlight "java" >}}

 diagram.dispose();

{{< /highlight >}}
