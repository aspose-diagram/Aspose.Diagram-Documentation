---
title: Добавить комментарии к чертежам в Visio
type: docs
weight: 40
url: /ru/net/add-comments-to-drawings-in-visio/
---
## **ВСТО**
Ниже приведен код для добавления комментариев в diagram:

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET позволяет размещать комментарии в любом месте на странице diagram.

{{% /alert %}} 

Метод AddComment, предоставляемый классом Page, позволяет добавлять комментарии на страницу документа. Он принимает координаты X и Y вместе со строкой комментария. Ниже приведен фрагмент кода:

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
