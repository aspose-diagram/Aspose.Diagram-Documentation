---
title: Belge Özeti Yazma
type: docs
weight: 70
url: /tr/net/writing-document-summary/
---
## **VSTO**
Visio belge özetini yazmak için kod aşağıdadır:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio, sizin ve iş arkadaşlarınızın bir diagram'i tanımlamasına yardımcı olacak bir dizi belge özeti bilgisi özelliği tanımlamanıza olanak tanır. Başlık, konu, yazar ve açıklama gibi özet özellikler, arama yaparken dosyayı bulmayı ve göz atarken tanımayı kolaylaştırır Dosyalar.

{{% /alert %}} 
### **Yazma Microsoft Visio Doküman Özet Bilgi**
 bu[Döküman özellikleri](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)class, bir Microsoft Visio diagram'in özet bilgilerini ayarlamak veya almak için bir dizi özellik sunar. Aspose.Diagram for .NET çizim özet bilgilerini güncelleyebilir ve ardından çizim dosyasını VDX'e geri yazabilir.

Mevcut bir VDX veya VSD dosyasının çizim özeti bilgilerini güncellemek için:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) sınıf.
1. Diagram.DocumentProps tarafından sunulan özellikleri, Visio çizim dosyası için özet bilgileri tanımlamak üzere ayarlayın.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

Özet bilgileri kontrol edin:

1. VDX çıkış dosyasını Microsoft Visio'de açın.
1.  seçme**Bilgi** dan**Dosya** Menü.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Çalışan Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
