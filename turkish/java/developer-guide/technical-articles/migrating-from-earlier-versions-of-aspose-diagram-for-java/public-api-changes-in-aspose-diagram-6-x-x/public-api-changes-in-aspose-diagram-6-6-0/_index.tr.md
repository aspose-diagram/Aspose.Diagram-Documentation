---
title: Genel API Aspose.Diagram 6.6.0'daki değişiklikler
type: docs
weight: 30
url: /tr/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 6.3.0'dan 6.6.0'a modül/uygulama geliştiricilerinin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **LoadFileFormat sınıfına VSDM, VSSM ve VSTM formatlarını ekler**
Bu sürüm, makro özellikli Visio formatlarını okuma desteği ekler.
### **SaveFileFormat sınıfına VSDM, VSSM ve VSTM formatlarını ekler**
Bu sürüm, makro etkin Visio biçimlerini yazma desteği ekler.
### **Visio Diagram'de VBA Modül Kodunu Değiştirin**
Vba, VbaProject ve VbaModule sınıflarını ekledik. Bu sınıflar, VBA projesi üzerinde kontrol sahibi olmanıza yardımcı olur. Geliştiriciler, bu yeni sürüm 6.6.0 veya üzerini kullanarak VBA modül kodunu çıkarabilir ve değiştirebilir. Lütfen bu kod örneğini kontrol edin:

**Java**

{{< highlight "java" >}}

 // mevcut bir Visio diagram'i yükleyin

InputStream girişi = yeni FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = yeni Diagram(giriş);

// VBA projesini çıkart

VbaProject v = diagram.getVbaProject();

// Modüller arasında yineleme yapın ve VBA makro kodunu değiştirin

için (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **ForeignData sınıfına bir getImageData Yöntemi ekler**
Bir bayt dizisi olarak ole nesnesinin görüntüsünü temsil eder. Bunun yanı sıra, OLE nesnelerinin işlenmesini de geliştirdik. Geliştiriciler artık Visio diagram'deki bir OLE nesnesini de değiştirebilir. Lütfen şu kod örneğini kontrol edin:

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
