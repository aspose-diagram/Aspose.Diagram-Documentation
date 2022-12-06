---
title: Aspose.Diagram for Java 18.8 Note di rilascio
type: docs
weight: 50
url: /it/java/aspose-diagram-for-java-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 18.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-8-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50611|Supporto per l'impostazione locale con API|Aumento|
|DIAGRAMJAVA-50606|VSDX in SVG - resa errata delle frecce|Insetto|
|DIAGRAMJAVA-50610|La posizione del testo sui connettori è errata nel file di output VSDX|Insetto|
|DIAGRAMJAVA-50612|Impossibile aprire il file di output VDX con Visio Viewer 2010 Professional|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiunto setLocale in LoadOption**
{{< highlight "java" >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

imposta la Locale utilizzata per diagram al momento del caricamento del file.
