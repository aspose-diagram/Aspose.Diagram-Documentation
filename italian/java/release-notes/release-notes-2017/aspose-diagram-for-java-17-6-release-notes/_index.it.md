---
title: Aspose.Diagram for Java 17.6 Note di rilascio
type: docs
weight: 70
url: /it/java/aspose-diagram-for-java-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.6](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-6-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50500|Output VSDX: la dimensione della forma aggiunta manualmente non viene modificata|Aumento|
|DIAGRAMJAVA-50503|Output VSDX - l'overflow del testo durante l'aggiunta di testo su più righe|Aumento|
|DIAGRAMJAVA-50505|Si è verificato un errore di puntatore null durante la conversione della pagina di disegno in immagine|Insetto|
|DIAGRAMJAVA-50484|Visualizzazione del testo verticale della forma della casella decisionale durante il salvataggio di un disegno nel formato VSDX|Insetto|
|DIAGRAMJAVA-50486|Visualizzazione del testo verticale della forma di processo predefinita durante il salvataggio di un disegno nel formato VSDX|Insetto|
|DIAGRAMJAVA-50492|Le formule nelle celle Larghezza e Altezza non vengono mantenute|Insetto|
|DIAGRAMJAVA-50493|Missing characters on converting a VSD to SVG|Insetto|
|DIAGRAMJAVA-50494|Output VSDX - le linee di collegamento non si collegano a metà delle forme di processo|Insetto|
|DIAGRAMJAVA-50499|VSDX to PNG - a white horizontal line appears at the bottom of shape|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il metodo refreshData nella classe Shape**
Il metodo Shape.refreshData consente agli sviluppatori di aggiornare i dati dopo aver modificato la posizione della forma, il testo della forma, i geom e le connessioni.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

//Find a particular shape and update its XForm

for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())

{

    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)

    {

        shape.getXForm().getPinX().setValue(5);

        shape.getXForm().getPinY().setValue(5);

        shape.refreshData();

    }

}

{{< /highlight >}}
