---
title: Aspose.Diagram for Java 21.6 Release Notes
type: docs
weight: 7
url: /sv/java/aspose-diagram-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 21.6.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50725|Felaktig hörnavrundning vid konvertering från vsdx till svg|Förbättring|
|DIAGRAMJAVA-50724|Regression i Aspose Diagram Java 21.3 - felaktig kontaktdisplay|Insekt|
|DIAGRAMJAVA-50727|Workiva: får standardtextblocksmarginaler|Insekt|
|DIAGRAMJAVA-50728|Workiva: ärvd fyllnadsfärggradient|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till setEmfRenderSetting i SVGSaveOptions**
- Inställning för rendering av Emf-metafil

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions();          
saveOp.setEmfRenderSetting(EmfRenderSetting.EMF_PLUS_PREFER);

{{< /highlight >}}
### **Lägger till getInheritTextBlock i Shape**
- Innehåller textblockvärdena för formen som ärvs av den överordnade stilen och huvudformen.

{{< highlight "java" >}}

 shape.getInheritTextBlock().getRightMargin().getValue()

{{< /highlight >}}
