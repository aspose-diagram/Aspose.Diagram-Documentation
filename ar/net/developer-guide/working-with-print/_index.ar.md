---
title: العمل مع الطباعة
type: docs
weight: 80
url: /ar/net/working-with-print/
description: يوضح هذا القسم كيفية طباعة مستند via XpsPrint باستخدام Aspose.Diagram.
---
## **كيفية طباعة مستند على الخادم via XpsPrint API**
يمكن أن تكون هذه المقالة مفيدة لأي شخص يريد إرسال مستند XPS إلى XpsPrint API غير المُدار من تطبيق .NET. لكن الهدف الرئيسي إذا كان هذا المقال هو إظهار كيفية طباعة diagram من تطبيق ASP.NET أو Windows Service باستخدام Aspose.Diagram و XpsPrint API.
### **مشكلة**
عندما تقوم بتطوير تطبيق .NET وتحتاج إلى إنتاج بعض المخرجات المطبوعة ، يمكنك استخدام الفئات في مساحة الاسم System.Drawing.Printing أو فئات WPF. ولكن ، كما اتضح ، إذا قمت بتطوير تطبيق ASP.NET أو Windows Service ، فستكون خيارات الطباعة محدودة للغاية ، لأن Microsoft يوصي بعدم استخدام هذه الأساليب. الاطلاع على الروابط أدناه للحصول على مزيد من المعلومات.

<http://support.microsoft.com/kb/324565>

استخدام فئات الطباعة .NET Framework غير مدعوم من الخدمة. يتضمن ذلك صفحات ASP ، والتي يتم تشغيلها بشكل عام في سياق خدمة الخادم.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

لا يتم دعم الفئات داخل مساحة الاسم System.Drawing.Printing للاستخدام داخل خدمة Windows أو تطبيق أو خدمة ASP.NET. قد تؤدي محاولة استخدام هذه الفئات من داخل أحد أنواع التطبيقات هذه إلى حدوث مشكلات غير متوقعة ، مثل انخفاض أداء الخدمة واستثناءات وقت التشغيل.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

استخدام WPF لإنشاء خدمات Windows غير مدعوم. نظرًا لأن WPF هي تقنية عرض تقديمي ، تتطلب خدمة Windows الأذونات المناسبة لإجراء العمليات المرئية التي تتضمن تفاعل المستخدم. إذا لم يكن لدى خدمة Windows الأذونات المناسبة ، فقد تكون هناك نتائج غير متوقعة.

يوفر كائن المستند مجموعة من أساليب الطباعة لطباعة المستندات وهذه الطرق تطبع via فئات الطباعة .NET المحددة في مساحة الاسم System.Drawing.Printing. هناك العديد من عملاء Aspose.Diagram الذين يستخدمون طريقة الطباعة هذه في تطبيقاتهم من جانب الخادم دون أي مشاكل ، ولكن هناك طريقة للامتثال لتوصيات Microsoft وهي موصوفة في هذه المقالة.
### **المحلول**
الطريقة الصحيحة لطباعة المستندات وفقًا لـ Microsoft هي استخدام XpsPrint API غير المُدار. يتوفر هذا API على Windows 7 ، Windows Server 2008 R2 وأيضًا على Windows Vista ، بشرط تثبيت تحديث النظام الأساسي لـ Windows Vista.

نظرًا لأن Aspose.Diagram يمكنه بسهولة تحويل أي مستند إلى XPS ، فنحن نحتاج فقط إلى كتابة التعليمات البرمجية التي تمرر مستند XPS إلى XpsPrint API. المشكلة الوحيدة هي أن XpsPrint API غير مُدار ويتطلب بعض المعرفة ببرنامج استدعاء النظام الأساسي.
### **الرمز**
لقد أنشأنا فئة XpsPrintHelper باستخدام طريقة الطباعة ، وهي سهلة الاستخدام للغاية. تحتاج فقط إلى تحديد المستند الذي تريد طباعته واسم الطابعة واسم المهمة الاختياري. إذا كانت هناك أي مشكلة في إرسال المستند أو طباعته ، فإن الطريقة ستطرح استثناءً.

المعلمة الأخيرة هي قيمة منطقية تحدد ما إذا كان يجب أن ينتظر الرمز حتى تتم طباعة المهمة أو يعود فورًا بعد إرسال مهمة الطباعة. إذا اخترت العودة على الفور ، فلن تتمكن من تحديد ما إذا كان المستند قد تمت طباعته بنجاح أم لا في النهاية.
#### **عينة البرمجة**
يوضح مثال الكود التالي كيفية استدعاء فئة الأداة المساعدة لطباعة via XPS.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
// Specify the name of the printer you want to print to.
const string printerName = @"\\COMPANY\Brother MFC-885CW Printer";

// Print the document.
XpsPrintHelper.Print(diagram, printerName, "My Test Job", true);

{{< /highlight >}}



هناك نوعان من التحميلات الزائدة لطريقة XpsPrintHelper.Print. يأخذ التحميل الزائد الأول كائن Aspose.Diagram.Diagram ويحفظه في MemoryStream بتنسيق XPS. ثم يستدعي XpsPrintHelper.Print الزائد الآخر.

إذا كنت تريد استخدام هذا النموذج بدون Aspose.Diagram (على سبيل المثال ، لديك بالفعل مستند XPS وترغب فقط في طباعته من تطبيق ASP.NET أو Windows Service) ، فيمكنك حذف هذه الطريقة فقط.
#### **XPS عينة برمجة الدفق والطباعة**
هذا المثال الكود يحول Diagram إلى تيار XPS ويطبع.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends an Aspose.Diagram document to a printer using the XpsPrint API.
/// </summary>
/// <param name="diagram"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Diagram diagram, string printerName, string jobName, bool isWait)
{
    if (diagram == null)
        throw new ArgumentNullException("document");

    // Use Aspose.Diagram to convert the document to XPS and store in a memory stream.
    MemoryStream stream = new MemoryStream();
    diagram.Save(stream, SaveFileFormat.XPS);
    stream.Position = 0;

    Print(stream, printerName, jobName, isWait);
}

{{< /highlight >}}



يقبل التحميل الزائد XpsPrintHelper.Print الثاني كائن دفق. يجب أن يحتوي التدفق على مستند بتنسيق XPS. تبدأ هذه الطريقة في مهمة طباعة XPS ، وترسل المستند إلى XpsPrint API ثم تنتظر النتيجة إذا لزم الأمر.
#### **عينة برمجة XpsPrint API**
يقوم مثال الرمز هذا بطباعة مستند XPS باستخدام XpsPrint API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends a stream that contains a document in the XPS format to a printer using the XpsPrint API.
/// Has no dependency on Aspose.Diagram, can be used in any project.
/// </summary>
/// <param name="stream"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Stream stream, string printerName, string jobName, bool isWait)
{
    if (stream == null)
        throw new ArgumentNullException("stream");
    if (printerName == null)
        throw new ArgumentNullException("printerName");

    // Create an event that we will wait on until the job is complete.
    IntPtr completionEvent = CreateEvent(IntPtr.Zero, true, false, null);
    if (completionEvent == IntPtr.Zero)
        throw new Win32Exception();

    try
    {
        IXpsPrintJob job;
        IXpsPrintJobStream jobStream;
        StartJob(printerName, jobName, completionEvent, out job, out jobStream);

        CopyJob(stream, job, jobStream);

        if (isWait)
        {
            WaitForJob(completionEvent);
            CheckJobStatus(job);
        }
    }
    finally
    {
        if (completionEvent != IntPtr.Zero)
            CloseHandle(completionEvent);
    }
}

{{< /highlight >}}



رمز طرق StartJob و CopyJob و WaitForJob و CheckJobStatus بالإضافة إلى تعريفات واجهات IXpsPrintJob و IXpsPrintJobStream منخفض المستوى تمامًا ويستخدم Platform Invoke و COM Interop. لم يتم تضمين هذا الرمز في المقالة للإيجاز ، ولكنه متاح في نموذج التنزيل.

يوفر XpsPrint API أيضًا وظائف إضافية ، مثل مراقبة تقدم العمل ، ولكن XpsPrintHelper الخاص بنا عبارة عن غلاف بسيط جدًا ولا يعرض هذه الوظيفة. يمكنك إضافة هذا بنفسك إذا كنت تريد ذلك.

{{% alert color="primary" %}}

عند تشغيل المشروع ، يقوم بطباعة نموذج مستند على الطابعة المحددة. لجعل النتائج مرئية ، تفتح نافذة وحدة التحكم. يعرض البرنامج رسالة النجاح أو نص الاستثناء إذا تم إلقاؤه.

{{% /alert %}}
## **طباعة Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يوفر أربع طرق للحمل الزائد لطباعة المخططات. هذه الطرق مرنة بما يكفي لطباعة diagram إلى الطابعة الافتراضية أو إلى أي طابعة متوفرة بإعدادات مخصصة. ما عليك سوى تحديد طريقة الطباعة المناسبة وفقًا للمتطلبات.
### **الطباعة على الطابعة الافتراضية**
تعد طباعة diagram إلى الطابعة الافتراضية أمرًا بسيطًا في Aspose.Diagram for .NET. قم بتنفيذ الخطوات التالية لطباعة diagram إلى الطابعة الافتراضية:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- قم باستدعاء أسلوب الطباعة مع عدم وجود معاملات كما تم كشفها بواسطة الكائن Diagram
#### **الطباعة إلى نموذج برمجة الطابعة الافتراضية**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the default printer
diagram.Print();

{{< /highlight >}}

### **الطباعة على طابعة معينة**
تتطلب طباعة diagram على الطابعة المحددة اسم الطابعة كمعامل لطريقة الطباعة لـ Diagram. قم بتنفيذ الخطوات التالية لطباعة diagram إلى الطابعة المطلوبة:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- قم باستدعاء أسلوب الطباعة للفئة Diagram باستخدام اسم الطابعة كمعامل سلسلة إلى أسلوب الطباعة
#### **الطباعة على عينة برمجة طابعة معينة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name
diagram.Print("LaserJet1100");

{{< /highlight >}}

### **إعداد اسم الطابعة والمستند**
تسمح واجهات برمجة التطبيقات Aspose.Diagram بتعيين اسم الطابعة والوثيقة المحددة لمهمة الطباعة. قم بتنفيذ الخطوات التالية لطباعة diagram على الطابعة المطلوبة:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- اتصل بأسلوب الطباعة للفئة Diagram باستخدام اسم الطابعة والوثيقة كمعامل سلسلة لأسلوب الطباعة
#### **إعداد نموذج برمجة اسم الطابعة والمستند**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.Print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

