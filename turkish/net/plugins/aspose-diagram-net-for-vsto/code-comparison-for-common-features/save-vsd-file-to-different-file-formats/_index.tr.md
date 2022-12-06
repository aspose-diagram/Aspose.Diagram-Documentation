---
title: VSD Dosyasını Farklı Dosya Biçimlerine Kaydet
type: docs
weight: 10
url: /tr/net/save-vsd-file-to-different-file-formats/
---
Bu yazımızda Aspose.Diagram for .NET'in dönüştürme özelliklerini VSTO ile karşılaştırdık. VSD dosyalarını VDX, PDF ve JPEG dosya biçimlerine dönüştürmek için .NET kod örnekleri içerir.
## **VSTO**
VSTO, Microsoft Visio dosyalarıyla programlama yapmanızı sağlar. Bir dosyayı başka formatlara kaydetmek için:

1. Bir Visio uygulama nesnesi oluşturun.
1. Uygulama nesnesini görünmez yapın.
1. diagram'i yükleyin.
1. VDX, PDF ve JPEG'e kaydedin.
1. Visio uygulama nesnesinden çıkın.

{{< highlight "csharp" >}}

 //Create Visio Application Object

Visio.Application vsdApp = Application;

//Make Visio Application Invisible

vsdApp.Visible = false;

//Create a document object and load a diagram

Visio.Document vsdDoc = vsdApp.Documents.Open("Drawing.vsd");

//Save the VDX diagram

vsdDoc.SaveAs("Drawing1.vdx");

//Save as PDF file

vsdDoc.ExportAsFixedFormat(Visio.VisFixedFormatTypes.visFixedFormatPDF,

	"Drawing1.pdf", Visio.VisDocExIntent.visDocExIntentScreen,

	Visio.VisPrintOutRange.visPrintAll, 1, vsdDoc.Pages.Count, false, true,

	true, true, true, System.Reflection.Missing.Value);

Visio.Page vsdPage = vsdDoc.Pages[1];

//Save as JPEG Image

vsdPage.Export("Drawing1.jpg");

//Quit Visio Object

vsdApp.Quit();

{{< /highlight >}}
## **Aspose.Diagram**
Aspose.Diagram ile programlama yaparken makinede Microsoft Visio'e gerek yok Microsoft Office Otomasyondan bağımsız çalışabilirsiniz. Aşağıdaki kod parçacıkları şunların nasıl yapıldığını gösterir:

1. diagram yükleyin.
1. diagram'i VDX, PDF ve JPEG'e kaydedin.

{{< highlight "csharp" >}}

 //Load diagram

Diagram vsdDiagram = new Diagram("Drawing.vsd");

//Save the diagram as VDX

vsdDiagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

//Save as PDF

vsdDiagram.Save("Drawing1.pdf", SaveFileFormat.PDF);

//Save as JPEG

vsdDiagram.Save("Drawing1.jpg", SaveFileFormat.JPEG);

{{< /highlight >}}
## **Örnek Kodu İndir**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [kaynak forge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip/indir)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip)
