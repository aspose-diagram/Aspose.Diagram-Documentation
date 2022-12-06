---
title: Aspose.Diagram för Python via Java 22.5 Release Notes
type: docs
weight: 23
url: /sv/java/aspose-diagram-for-python-via-java-22-5-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om utgåvan för Aspose.Diagram för Python via Java 22.5.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50923|wk: Fält Visade värden|Förbättring|
|DIAGRAMJAVA-50924|wk: hämta Alignment-värden|Förbättring|
|DIAGRAMJAVA-50934|Undersök möjligheten till parallell bearbetning av VSDX-filer|Insekt|
|DIAGRAMJAVA-50936|Fel värden för Shape.getName(), Shape.getNameU()|Insekt|
|DIAGRAMJAVA-50941|Konverterar vsd till vsdx ,Den konverterade vsdx-filen kan inte öppnas i Visio.|Insekt|
|DIAGRAMJAVA-50942|Värdet på "ToSheet" bryter mot definitionen av OpenXML i konverteringen från vsd till vsdx.|Insekt|
|DIAGRAMJAVA-50943|Fel vid inläsning av VSD-filen|Insekt|
|DIAGRAMJAVA-50951|Ändra storlek på sidolinjeformen|Insekt|
|DIAGRAMJAVA-50955|Shape.getXForm().getWidth() returnerar fel värde om width är inställd på att använda formel|Insekt|

## `?`**Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till getDisplayValue in Field**
- Hämtar det formaterade strängvärdet för detta fält.

{{< highlight "java" >}}
String str = shape.getFields().get(0).getDisplayValue();
System.out.println(str);
{{< /highlight >}}

### **Lägger till getInheritParas i Shape**
- Innehåller paragraferna för formen som ärvs av moderstilen och mastern

{{< highlight "java" >}}
int str = shape.getInheritParas().get(0).getHorzAlign().getValue();
System.out.println(str);
{{< /highlight >}}
