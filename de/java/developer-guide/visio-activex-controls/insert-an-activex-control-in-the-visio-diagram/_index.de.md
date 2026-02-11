---
title: Fügen Sie ein ActiveX-Steuerelement in die Visio Diagram ein
type: docs
weight: 10
url: /de/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Entwickler können ActiveX-Steuerelemente direkt zu Microsoft Visio-Zeichnungen hinzufügen, um Visio diagram interaktiv zu gestalten[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Fügen Sie ein Programmierbeispiel für ein ActiveX-Steuerelement ein**
[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Die Klasse bietet die addActiveXControl-Methode und ermöglicht Entwicklern, jede Art von ActiveX-Steuerelement wie Befehlsschaltfläche, Kombinationsfeld, Kontrollkästchen, Listenfeld, Textfeld, Drehfeld, Optionsfeld, Beschriftung, Bild, Umschaltfläche und Bildlaufleiste einzufügen.

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
