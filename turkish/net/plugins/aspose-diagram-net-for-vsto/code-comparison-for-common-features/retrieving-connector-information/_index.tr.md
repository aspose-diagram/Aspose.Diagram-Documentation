---
title: Bağlayıcı Bilgilerini Alma
type: docs
weight: 90
url: /tr/net/retrieving-connector-information/
---
## **VSTO**
Bağlayıcı bilgilerini almak için kod aşağıdadır:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET, kimlik ve isim - hakkında bilgi almak için mekanizmalar sağlar[sayfalar](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) ve[usta](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Ayrıca, şekilleri birbirine bağlayan öğeler olan bağlayıcılar hakkında bilgi almanızı sağlar.

{{% /alert %}} 

 bu[Bağlamak](https://reference.aspose.com/diagram/net/aspose.diagram/connect) nesne, bir Visio çizim sayfasında iki şekli birleştiren bir bağlayıcıyı temsil eder. Tarafından sunulan Connects özelliği[Sayfa](https://reference.aspose.com/diagram/net/aspose.diagram/page) class, Aspose.Diagram.Connect nesnelerinin bir koleksiyonunu destekler. Bu özellik, bir bağlayıcı hakkında kimlik ve ad bilgilerini almak için kullanılabilir.

Aspose.Diagram .NET kullanarak konektör bilgilerini almak için kullanılan kod aşağıdadır:

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[1].Connects)

 {

   //Display information about the Connectors

   Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);

   Console.WriteLine("To Shape ID : " + connector.ToSheet);

 }

 Console.ReadLine();


{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Çalışan Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
