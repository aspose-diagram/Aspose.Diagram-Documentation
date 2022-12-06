---
title: Visio'de Çizimlere Yorum Ekleyin
type: docs
weight: 40
url: /tr/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
diagram'de yorum eklemek için kod aşağıdadır:

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET diagram sayfasında istediğiniz yere yorum yapmanızı sağlar.

{{% /alert %}} 

Page sınıfı tarafından sunulan AddComment yöntemi, bir çizim sayfasına yorum eklemenizi sağlar. Bir yorum dizesiyle birlikte X ve Y koordinatlarını alır. Kod parçacığı aşağıdadır:

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Çalışan Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
