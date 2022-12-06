---
title: Aspose.Diagram for Java 21.2 Release Notes
type: docs
weight: 11
url: /sv/java/aspose-diagram-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 21.2.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50710|lägg till en enda rad i en Viso-fil, så att if förblir redigerbar som en rad|Förbättring|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lägger till ActivePage i Diagram**
- Anger den aktiva sidan

{{< highlight "java" >}}

 Page page = diagram.getActivePage()

{{< /highlight >}}
### **Lägger till centerDrawing in Shape**
- Centrera formen i förhållande till sidans omfattning

{{< highlight "java" >}}

 shape.centerDrawing()

{{< /highlight >}}
### **Lägger till drawLine i sidan**
- Processen att rita en enda linje.

{{< highlight "java" >}}

  diagram.getPages().get(0).drawLine(0, 0, 1, 1);

{{< /highlight >}}