---
title: Aspose.Diagram för Node.js via Java 21.11 Release Notes
type: docs
weight: 4
url: /sv/java/aspose-diagram-for-node-js-via-java-21-11-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Node.js via Java 21.11.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50806|wk: InheridetChar Color|Förbättring|
|DIAGRAMJAVA-50385|Färgen på ramar och titlar ändras vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMJAVA-50501|VSDX till PNG - Felaktig färg på former|Insekt|
|DIAGRAMJAVA-50631|Formerna är inkonsekventa efter export av VSDX till PDF|Insekt|
|DIAGRAMJAVA-50804|Anslutningstext radbryts när kopplingen ritas|Insekt|
## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till förinställt tema i form**
- Tillämpa ett förinställt tema på den här formen.

{{< highlight "java" >}}
 
 shape.setPresetTheme( PresetThemeValue.BUBBLE);

{{< /highlight >}}


### **Lägger till PresetThemeVariant i Shape**
- Använd en förinställd temavariant på den här formen

{{< highlight "java" >}}

shape.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);

{{< /highlight >}}

### **Lägger till PresetThemeQuickStyle i Shape**
- Tillämpa en förinställd temavariant quickstyle på den här formen

{{< highlight "java" >}}

shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_1);

{{< /highlight >}}
