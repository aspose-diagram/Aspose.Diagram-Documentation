---
title: عام API التغييرات في Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /ar/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.3.0 إلى 6.6.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **إضافة تنسيقات VSDM و VSSM و VSTM في فئة LoadFileFormat**
يضيف هذا الإصدار دعمًا لقراءة تنسيقات Visio التي تدعم الماكرو.
### **إضافة تنسيقات VSDM و VSSM و VSTM في فئة SaveFileFormat**
يضيف هذا الإصدار دعمًا لكتابة تنسيقات Visio التي تدعم الماكرو.
### **تعديل كود وحدة VBA في Visio Diagram**
لقد أضفنا فئات Vba و VbaProject و VbaModule. تساعد هذه الفئات في التحكم في مشروع VBA. باستخدام هذا الإصدار الجديد 6.6.0 أو أعلى ، يمكن للمطورين استخراج وتعديل رمز وحدة VBA. الرجاء التحقق من مثال هذا الرمز:

**Java**

{{< highlight "java" >}}

 // تحميل Visio diagram موجود

إدخال InputStream = FileInputStream الجديد ("c: \\ temp \\ macro.vsdm") ؛

Diagram diagram = جديد Diagram (إدخال) ؛

// استخراج مشروع VBA

VbaProject v = diagram.getVbaProject () ،

// تكرار من خلال الوحدات النمطية وتعديل كود الماكرو VBA

لـ (int i = 0 ؛ i< diagram.getVbaProject().getModules().getCount();i++)

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
### **يضيف أسلوب getImageData في فئة ForeignData**
إنه يمثل صورة كائن أول كمصفوفة بايت. إلى جانب ذلك ، قمنا أيضًا بتحسين معالجة كائنات OLE. يمكن للمطورين الآن أيضًا استبدال كائن OLE في Visio diagram. الرجاء التحقق من مثال الرمز هذا:

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
