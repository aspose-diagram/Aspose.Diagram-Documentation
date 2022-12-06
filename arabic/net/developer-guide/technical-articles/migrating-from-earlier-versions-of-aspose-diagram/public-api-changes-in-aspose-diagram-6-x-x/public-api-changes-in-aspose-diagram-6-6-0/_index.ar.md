---
title: عام API التغييرات في Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.3.0 إلى 6.6.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **إضافة تنسيقات VSDM و VSSM و VSTM في فئة LoadFileFormat**
يضيف هذا الإصدار دعمًا لقراءة تنسيقات Visio التي تدعم الماكرو.
## **إضافة تنسيقات VSDM و VSSM و VSTM في فئة SaveFileFormat**
يضيف هذا الإصدار دعمًا لكتابة تنسيقات Visio التي تدعم الماكرو.
## **تعديل كود وحدة VBA في Visio Diagram**
لقد أضفنا فئات VbaModule و VbaModuleCollection و VbaProject و VbaProjectReference و VbaProjectReferenceCollection. تساعد هذه الفئات في التحكم في مشروع VBA. باستخدام هذا الإصدار الجديد 6.6.0 أو أعلى ، يمكن للمطورين استخراج وتعديل رمز وحدة VBA. الرجاء التحقق من مثال هذا الرمز:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

خطأ في عرض الماكرو 'code': تم تحديد قيمة غير صالحة للمعامل lang
## **يضيف خاصية ImageData في فئة ForeignData**
إنه يمثل صورة كائن أول كمصفوفة بايت. إلى جانب ذلك ، قمنا أيضًا بتحسين معالجة كائنات OLE. يمكن للمطورين الآن أيضًا استبدال كائن OLE في Visio diagram. الرجاء التحقق من مثال الرمز هذا:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

خطأ في عرض الماكرو 'code': تم تحديد قيمة غير صالحة للمعامل lang
