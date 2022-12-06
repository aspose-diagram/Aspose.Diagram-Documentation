---
title: VSTO'da Diagram ve Aspose.Diagram yazdırma
type: docs
weight: 100
url: /tr/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
diagram'in nasıl yazdırılacağını gösteren kod aşağıdadır:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 diagram'in yazdırılması**varsayılan yazıcı** Aspose.Diagram for .NET'de oldukça basittir. diagram'i varsayılan yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Diagram nesnesi tarafından sunulan hiçbir parametre olmadan Yazdır yöntemini çağırın

 diagram'in yazdırılması**belirli yazıcı** Diagram'in Yazdırma yöntemi için parametre olarak yazıcının adını gerektirir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Yazıcı adı ile Diagram sınıfının Print yöntemini Print yöntemine string parametresi olarak çağırın

Varsayılan ve belirli yazıcıyı kullanmanın kodu aşağıdadır:

{{< highlight "cs" >}}

  string FilePath = "demo.vsd";

 //Load the diagram

 Diagram diagram = new Diagram(FilePath);

 //Call the print method to print whole Diagram to the default printer

 diagram.Print();

 //Call the print method to print whole Diagram to the desired printer

 diagram.Print("LaserJet1100");

 PrinterSettings settings = new PrinterSettings();

 settings.PrinterName = "LaserJet1100";

 //Call the print method to print whole Diagram to the desired printer and set document name in print job

 diagram.Print(settings, "Job name while printing with Aspose.Diagram");


{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Çalışan Kodu İndir**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
