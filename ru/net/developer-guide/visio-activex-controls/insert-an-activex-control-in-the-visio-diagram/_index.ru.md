---
title: Вставьте элемент управления ActiveX в Visio Diagram
type: docs
weight: 10
url: /ru/net/insert-an-activex-control-in-the-visio-diagram/
description: На этой странице описывается, как вставить элемент управления ActiveX с библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

 Разработчики могут добавлять элементы управления ActiveX непосредственно в чертежи Microsoft Visio, чтобы сделать их интерактивными с помощью[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Вставьте пример программирования элемента управления ActiveX**
[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Класс предлагает метод AddActiveXControl и позволяет разработчикам вставлять любой тип элемента управления ActiveX, такой как командная кнопка, поле со списком, флажок, список, текстовое поле, кнопка прокрутки, переключатель, метка, изображение, кнопка-переключатель и полоса прокрутки.


{{< highlight csharp >}}
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

