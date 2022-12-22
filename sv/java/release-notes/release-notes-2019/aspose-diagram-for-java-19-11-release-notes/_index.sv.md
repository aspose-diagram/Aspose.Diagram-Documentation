---
title: Aspose.Diagram for Java 19.11 Release Notes
type: docs
weight: 20
url: /sv/java/aspose-diagram-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 19.11.

{{% /alert %}} 
## **Förbättringar och förändringar**
Denna månads release tillåter formatering av Visio sidor efter[tillämpa stilmallar](/diagram/sv/java/format-visio-pages/).

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50671|Inställningen för formblad nytt fönster respekteras inte vid konvertering till SVG|Förbättring|
### **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram för JAVA. Om du har funderingar på någon av de listade ändringarna, vänligen ta upp det på Aspose.Diagram supportforum.
### **Lade till applicationStyle på sidan**
{{< highlight "java" >}}

 StyleSheet st = new StyleSheet();

dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### ` `**Tillagd kassera i Diagram klass**
Utför programdefinierade uppgifter associerade med att frigöra, släppa eller återställa ohanterade resurser.

{{< highlight "java" >}}

 diagram.dispose();

{{< /highlight >}}
