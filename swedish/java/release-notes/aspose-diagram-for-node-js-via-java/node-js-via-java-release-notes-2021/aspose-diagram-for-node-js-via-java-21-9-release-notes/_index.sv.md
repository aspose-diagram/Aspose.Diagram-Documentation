---
title: Aspose.Diagram för Node.js via Java 21.9 Release Notes
type: docs
weight: 5
url: /sv/java/aspose-diagram-for-node-js-via-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram för Node.js via Java 21.9.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50753|wk: Kontrollera att TextAnnotation är ansluten till form|Förbättring|
|DIAGRAMJAVA-50382|Skuggningen av former saknas vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMJAVA-50754|wk - LineColor från InheritLine är inte korrekt|Insekt|
|DIAGRAMJAVA-50756|wk: PinPos null vs center-center|Insekt|
|DIAGRAMJAVA-50757|WK: getBegin/End Arrow värde felaktigt.|Insekt|
|DIAGRAMJAVA-50771|WK: kan inte få LineColor och namn för arkform|Insekt|
## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger tilldependentOnShapes i Shape**
- Returnerar en array som innehåller identifierarna för de former som är beroende av en form.



{{< highlight "java" >}}

long[]shapeids = shape.dependsOnShapes();

{{< /highlight >}}
