---
title: Aspose.Diagram for Java 22.10 Release Notes
type: docs
weight: 18
url: /sv/java/aspose-diagram-for-java-22-10-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om utgåvor för Aspose.Diagram for Java 22.10.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-51028|setTopPage fungerar inte|Förbättring|
|DIAGRAMJAVA-51035|wk: Geoms-egenskapen för vissa arkformer är inte korrekt löst|Förbättring|
|DIAGRAMJAVA-51030|.getName() skiljer sig ibland från namn i Visio (Aspose.Diagram Java 22.9, .vsd filer)|Insekt|
|DIAGRAMJAVA-51033|.getText() är ibland annorlunda än form.Text i Aspose.Diagram (Aspose.Diagram Java 22.9, .vsd filer)|Insekt|
|DIAGRAMJAVA-51038|När texten innehåller radbrytningar är omräkning av textens bredd felaktig|Insekt|
|DIAGRAMJAVA-51040|.getNameU() är ibland tom (Aspose.Diagram Java 22.9, .vsd filer)|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.

### **Lägger till getDisplayText i Shape**
- Få texten som visas i gränssnittet

{{< highlight "java" >}}
string text = shape.getDisplayText();
{{< /highlight >}}

### **Lägger till getInheritGeoms in Shape**
- Innehåller Geoms-värdena för formen som ärvs av huvudformen.

{{< highlight "java" >}}
int count = shape.getInheritGeoms().get(0).getCoordinateCol().getCount();
{{< /highlight >}}