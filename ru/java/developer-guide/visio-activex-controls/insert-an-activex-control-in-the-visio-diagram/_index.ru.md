---
title: Вставьте элемент управления ActiveX в Visio Diagram
type: docs
weight: 10
url: /ru/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Разработчики могут добавлять элементы управления ActiveX непосредственно в чертежи Microsoft Visio, чтобы сделать их интерактивными с помощью[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Вставьте пример программирования элемента управления ActiveX**
[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Класс предлагает метод addActiveXControl и позволяет разработчикам вставлять любой тип элемента управления ActiveX, такой как командная кнопка, поле со списком, флажок, список, текстовое поле, кнопка прокрутки, переключатель, метка, изображение, кнопка-переключатель и полоса прокрутки.

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
