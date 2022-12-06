---
title: Aspose.Diagram for Java 20.2 Release Notes
type: docs
weight: 60
url: /sv/java/aspose-diagram-for-java-20-2-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 20.2.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50361|Formens förgrundsfärg bevaras inte vid konvertering av en VST till PNG|Förbättring|
|DIAGRAMJAVA-50504|VSD till PDF - färgen på linjerna ändras|Förbättring|
## ` `**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lade till enlargePage i ImageSaveOptions**
- Anger om sidan ska förstoras

{{< highlight "java" >}}

 com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);

opt.setEnlargePage(false);

{{< /highlight >}}
### **Lade till hasHiddenInfo i Diagram**
- Indikerar om denna diagram har dold information

{{< highlight "java" >}}

 diagram.hasHiddenInfo();

{{< /highlight >}}




