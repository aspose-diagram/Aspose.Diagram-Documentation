---
title: Infoga en ActiveX-kontroll i Visio Diagram
type: docs
weight: 10
url: /sv/net/insert-an-activex-control-in-the-visio-diagram/
description: Den här sidan beskriver hur man infogar en ActiveX Control med Aspose.Diagram bibliotek.
---
{{% alert color="primary" %}}

 Utvecklare kan lägga till ActiveX-kontroller direkt till Microsoft Visio ritningar för att göra Visio diagram interaktiva genom att använda[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Infoga ett ActiveX-kontrollprogrammeringsexempel**
[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class erbjuder AddActiveXControl-metoden och tillåter utvecklare att infoga vilken typ av ActiveX-kontroll som helst som kommandoknapp, kombinationsruta, kryssruta, listbox, textbox, snurrknapp, alternativknapp, etikett, bild, växlingsknapp och rullningslist.

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
