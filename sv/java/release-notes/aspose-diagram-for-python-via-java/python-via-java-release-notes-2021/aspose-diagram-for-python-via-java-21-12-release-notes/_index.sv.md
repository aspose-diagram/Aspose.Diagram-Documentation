---
title: Aspose.Diagram för Python via Java 21.12 Release Notes
type: docs
weight: 4
url: /sv/java/aspose-diagram-for-python-via-java-21-12-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Python via Java 21.12.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50838|Centrering av text på rak linjekontakt|Insekt|
|DIAGRAMJAVA-50839|Behöver dra en rak koppling mellan formerna|Insekt|
## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.


### **Lägger till IsSavingImageSeparately i SVGSaveOptions**
- Definierar om bilden ska sparas separat.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.setIsSavingImageSeparately(true);

{{< /highlight >}}


### **Lägger till CustomImagePath i SVGSaveOptions**
- Användarens anpassade sökväg (URL) sparad i genererad svg-fil för bilden. Om den inte har definierats av användaren kommer den aktuella katalogen att användas.

{{< highlight "java" >}}

  o.setCustomImagePath("d:/output/");

{{< /highlight >}}

### **Lägger till SaveForegroundPagesOnly i PrintSaveOptions**
- Anger om alla sidor ska skrivas ut eller bara förgrunden.

{{< highlight "java" >}}

 options.setSaveForegroundPagesOnly(true);

{{< /highlight >}}
