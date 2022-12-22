---
title: Aspose.Diagram for Java 20.10 Note di rilascio
type: docs
weight: 10
url: /it/java/aspose-diagram-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 20.10.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50457|Gli elementi di testo vengono spostati durante la conversione di una pagina VSD in SVG|Aumento|

## Pubblico API Modifiche
* Aggiunto IsExportScaleInMatrix in SVGSaveOptions - Definisce se è necessario esportare la scala nella matrice o meno.
```
SVGSaveOptions o = new SVGSaveOptions();
o.setExportScaleInMatrix(false);
```
