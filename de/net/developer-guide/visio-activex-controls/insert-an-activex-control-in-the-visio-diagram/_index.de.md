---
title: Fügen Sie ein ActiveX-Steuerelement in die Visio Diagram ein
type: docs
weight: 10
url: /de/net/insert-an-activex-control-in-the-visio-diagram/
description: Auf dieser Seite wird beschrieben, wie Sie ein ActiveX-Steuerelement mit der Bibliothek Aspose.Diagram einfügen.
---
{{% alert color="primary" %}}

 Entwickler können ActiveX-Steuerelemente direkt zu Microsoft Visio-Zeichnungen hinzufügen, um Visio diagram interaktiv zu gestalten[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Fügen Sie ein Programmierbeispiel für ein ActiveX-Steuerelement ein**
[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Die Klasse bietet die AddActiveXControl-Methode und ermöglicht Entwicklern, jede Art von ActiveX-Steuerelement wie Befehlsschaltfläche, Kombinationsfeld, Kontrollkästchen, Listenfeld, Textfeld, Drehfeld, Optionsfeld, Beschriftung, Bild, Umschaltfläche und Bildlaufleiste einzufügen.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
