---
title: Yazı Tipi Bilgilerini Alma
type: docs
weight: 80
url: /tr/net/retrieving-font-information/
---
## **VSTO**
Yazı tipi bilgilerini almak için kullanılan kod aşağıdadır:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram, diagram'i oluşturan öğeler hakkında bilgi almak için mekanizmalara sahiptir.[sayfalar](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) şablonlar,[konektörler](/diagram/tr/net/retrieving-connector-information/)ve ayrıca yazı tipleri. Bu makale, bir diagram'de hangi yazı tiplerinin kullanıldığını nasıl bulacağınızı gösterir.

{{% /alert %}} 

 bu[Yazı tipi](https://reference.aspose.com/diagram/net/aspose.diagram/font) nesne, bir belgedeki metne uygulanan veya sistemde kullanılabilen bir yazı tipini temsil eder.

Bir Yazı Tipi nesnesi, bir adı (örneğin, "Arial"), Microsoft Visio'in bu yazı tipiyle biçimlendirilmiş metni içeren bir şeklin Karakter bölümündeki Yazı Tipi hücresinde depoladığı yazı tipi kimliğine (örneğin, 3) eşler. Yazı tipi kimlikleri, bir belge farklı sistemlerde açıldığında veya yazı tipleri yüklendiğinde veya kaldırıldığında değişebilir.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Çalışan Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
