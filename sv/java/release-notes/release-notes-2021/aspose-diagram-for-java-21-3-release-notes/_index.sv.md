---
title: Aspose.Diagram for Java 21.3 Release Notes
type: docs
weight: 10
url: /sv/java/aspose-diagram-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

Den här sidan innehåller information om release notes för Aspose.Diagram for Java 21.3.

{{% /alert %}}
## **Förbättringar och förändringar**  ##

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50711|NullPointerException kastar när du försöker spara VDX dokument som PNG|Förbättring|
|DIAGRAMJAVA-50713|Problem med textöverlappning vid konvertering av VSDX till PDF|Förbättring|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lade till ConnectShapesViaConnector på sidan**
- Anslut former via kontakt.

{{< highlight "java" >}}

page.connectShapesViaConnector(id, "Port7", id, "Port21", id);

{{< /highlight >}}
### **Lägger till GlueShapeToConnectorBeginX på sidan**
- Limma Shape med BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorBeginX(id, "Port7", id);

{{< /highlight >}}
### **Lägger till GlueShapeToConnectorEndX i sidan**
- Limma Shape med BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorEndX(id, "Port21", id);

{{< /highlight >}}
### **Lägger till CenterDrawing på sidan**
- Centrerar en sidas former med hänsyn till sidans omfattning.



{{< highlight "java" >}}

page.centerDrawing();

{{< /highlight >}}
### **Lägger till IsContain i Shape**
- Anger om denna form innehåller en annan form.



{{< highlight "java" >}}

OLE_Shape.isContain(shape)

{{< /highlight >}}