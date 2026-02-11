---
title: Üstbilgiler ve Altbilgilerle Çalışma
type: docs
weight: 140
url: /tr/net/working-with-headers-and-footers/
description: Bu bölümde, Microsoft Office Visio'in üstbilgilerinin ve altbilgilerinin Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
## **Visio Diyagramlarının Üstbilgilerini ve Altbilgilerini Yönetme**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Microsoft Office Visio diyagramlarının üstbilgilerini ve altbilgilerini ayarlamak için bir mekanizma sağlar. Geliştiriciler, bir belge üstbilgisinin/altbilgisinin sol, orta ve sağ tarafında görünen metin dizesini alabilir veya ayarlayabilir. Metnin yazı tipi özellikleriyle birlikte üstbilgi ve altbilgi kenar boşluğunu da ayarlayabilirler.
### **Üstbilgi ve Altbilgi Özelliklerini Ayarlama**
 bu[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class nesnesi, üst bilgi ve alt bilgi metni, yazı tipi ve kenar boşluğu değerlerinin alınmasına ve ayarlanmasına izin veren HeaderFooter özelliğini sunar. Visio çiziminin baskı ön izlemesi sırasında, kullanıcılar Microsoft Visio 2013 (Microsoft Visio 2010 >> "Üstbilgi ve Altbilgi" düğmesi) içindeki "Üstbilgi & Altbilgiyi Düzenle" bağlantı düğmesine tıklayabilirler. Aşağıdaki ekran görüntüsünde gösterildiği gibi metin eklemek için birkaç seçenek vardır. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:
#### **Programlama Örneği**
Aşağıdaki kod parçası, Üst Bilgiler ve Alt Bilgiler özelliklerini yönetmeye yardımcı olur.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

