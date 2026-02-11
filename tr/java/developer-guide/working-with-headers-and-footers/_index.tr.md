---
title: Üstbilgiler ve Altbilgilerle Çalışma
type: docs
weight: 150
url: /tr/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java, Microsoft Office Visio diyagramlarının üstbilgilerini ve altbilgilerini ayarlamak için bir mekanizma sağlar. Geliştiriciler, bir belge üstbilgisinin/altbilgisinin sol, orta ve sağ tarafında görünen metin dizesini alabilir veya ayarlayabilir. Metnin yazı tipi özellikleriyle birlikte üstbilgi ve altbilgi kenar boşluğunu da ayarlayabilirler.

{{% /alert %}} 
### **Üstbilgi ve Altbilgi Özelliklerini Ayarlama**
 bu[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class nesnesi, üst bilgi ve alt bilgi metni, yazı tipi ve kenar boşluğu değerlerinin alınmasına ve ayarlanmasına izin veren HeaderFooter özelliğini sunar. Visio çiziminin baskı ön izlemesi sırasında, kullanıcılar Microsoft Visio 2013 (Microsoft Visio 2010 >> "Üstbilgi ve Altbilgi" düğmesi) içindeki "Üstbilgi & Altbilgiyi Düzenle" bağlantı düğmesine tıklayabilirler. Aşağıdaki ekran görüntüsünde gösterildiği gibi metin eklemek için birkaç seçenek vardır. Kullanıcılar bu özellikleri programlı olarak Aspose.Diagram API kullanarak aşağıdaki gibi yönetebilir:

**Üst Bilgiler ve Alt Bilgiler metnini, kenar boşluklarını ve yazı tipi özelliklerini yönetin.** 

![yapılacaklar:resim_alternatif_Metin](working-with-headers-and-footers_1.png)

Aşağıdaki kod parçası, Üst Bilgiler ve Alt Bilgiler Özelliklerinin yönetilmesine yardımcı olur.
#### **Programlama Örnekleri**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

