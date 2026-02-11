---
title: Infoga en ActiveX-kontroll i Visio Diagram
type: docs
weight: 10
url: /sv/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Utvecklare kan lägga till ActiveX-kontroller direkt till Microsoft Visio ritningar för att göra Visio diagram interaktiva genom att använda[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Infoga ett ActiveX-kontrollprogrammeringsexempel**
[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class erbjuder addActiveXControl-metoden och låter utvecklare infoga alla typer av ActiveX-kontroller som kommandoknapp, kombinationsruta, kryssruta, listbox, textbox, snurrknapp, alternativknapp, etikett, bild, växlingsknapp och rullningslist.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
