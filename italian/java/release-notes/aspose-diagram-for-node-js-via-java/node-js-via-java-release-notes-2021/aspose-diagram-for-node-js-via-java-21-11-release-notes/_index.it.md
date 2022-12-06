---
title: Aspose.Diagram for Node.js via Java 21.11 Release Notes
type: docs
weight: 4
url: /it/java/aspose-diagram-for-node-js-via-java-21-11-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Node.js via Java 21.11.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50806|wk: InheridetChar Color|Aumento|
|DIAGRAMJAVA-50385|The color of border and titles is being changed on converting a VSDX to PDF|Insetto|
|DIAGRAMJAVA-50501|VSDX to PNG - Incorrect color of shapes|Insetto|
|DIAGRAMJAVA-50631|Shapes are inconsistent after exporting VSDX to PDF|Insetto|
|DIAGRAMJAVA-50804|Il testo del connettore va a capo quando si disegna il connettore|Insetto|
## `?`**Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge PresetTheme in Shape**
- Applica un tema preimpostato a questa forma.

{{< highlight "java" >}}
 
 shape.setPresetTheme( PresetThemeValue.BUBBLE);

{{< /highlight >}}


### **Aggiunge PresetThemeVariant in Shape**
- Applica una variante del tema preimpostato a questa forma

{{< highlight "java" >}}

shape.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);

{{< /highlight >}}

### **Aggiunge PresetThemeQuickStyle in Shape**
- Applicare uno stile rapido della variante del tema preimpostato a questa forma

{{< highlight "java" >}}

shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_1);

{{< /highlight >}}
