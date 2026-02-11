---
title: تكوين الخطوط للعرض
type: docs
weight: 10
url: /ar/net/configuring-fonts-for-rendering/
---
## **سيناريوهات الاستخدام الممكنة**

توفر واجهات برمجة التطبيقات Aspose.Diagram إمكانية عرض الصفحات بتنسيقات الصور بالإضافة إلى تحويلها إلى تنسيقات PDF و XPS. لتحقيق أقصى قدر من دقة التحويل ، من الضروري أن تكون الخطوط المستخدمة في جدول البيانات متاحة في دليل الخطوط الافتراضي لنظام التشغيل. في حالة عدم وجود الخطوط المطلوبة ، ستحاول واجهات برمجة تطبيقات Aspose.Diagram استبدال الخطوط المطلوبة بالخطوط المتاحة.

## **اختيار الخطوط**

فيما يلي العملية التي تتبعها واجهات برمجة التطبيقات Aspose.Diagram خلف الكواليس.

1. يحاول API العثور على الخطوط في نظام الملفات المطابقة لاسم الخط الدقيق المستخدم في جدول البيانات.
1.  إذا كان API لا يمكنه تحديد مكان الخط المعرف أسفل**[SaveOptions.DefaultFont] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** الخاصية ، يحاول استخدام الخط المحدد ضمن**[FontConfigs.DefaultFontName] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**منشأه.
1.  إذا كان API لا يمكنه تحديد مكان الخط المعرف أسفل**[FontConfigs.DefaultFontName] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** الخاصية ، فهو يحاول تحديد أنسب الخطوط من جميع الخطوط المتاحة.
1. أخيرًا ، إذا لم يتمكن API من العثور على أي خطوط في نظام الملفات ، فسيتم عرض الصفحة باستخدام Times New Roman.

## **تعيين مجلدات الخطوط المخصصة**

 Aspose.Diagram تقوم واجهات برمجة التطبيقات (API) بالبحث في دليل الخط الافتراضي لنظام التشغيل عن الخطوط المطلوبة. في حالة عدم توفر الخطوط المطلوبة في دليل خطوط النظام ، تقوم واجهات برمجة التطبيقات بالبحث من خلال الدلائل المخصصة (المعرفة من قبل المستخدم). ال**[FontConfigs] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** كشفت class عن عدد من الطرق لتعيين أدلة الخطوط المخصصة كما هو مفصل أدناه.

1. **[FontConfigs.SetFontFolder] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: هذه الطريقة مفيدة إذا كان هناك مجلد واحد فقط ليتم تعيينه.

1. **[FontConfigs.SetFontFolders] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**هذه الطريقة مفيدة عندما تكون الخطوط موجودة في مجلدات متعددة ويرغب المستخدم في تعيين جميع المجلدات بشكل منفصل بدلاً من دمج كل الخطوط في مجلد واحد.
1. **[FontConfigs.SetFontSources] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: هذه الآلية مفيدة عندما يرغب المستخدم في تحميل الخطوط من مجلدات متعددة أو ملف خط واحد أو بيانات الخط من مجموعة من البايتات.

{{% alert color="primary" %}}

 كلاهما**[FontConfigs.SetFontFolder] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** الأساليب تقبل معلمة ثانية من النوع المنطقي. تمرير**حقيقي** حيث أن المعلمة الثانية ستوجه Aspose.Diagram APIs للبحث في المجلدات الفرعية عن ملفات الخطوط.

{{% /alert %}}

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Setting default font
Aspose.Diagram.FontConfigs.DefaultFontName = "Arial";
// Setting the custom font directories
Aspose.Diagram.FontConfigs.SetFontFolder(Environment.GetFolderPath(Environment.SpecialFolder.Fonts), false);

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "Font.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```

{{% alert color="primary" %}}

يرجى استخدام أي من الطرق المذكورة أعلاه في بداية التطبيق ، أي ؛ قبل استدعاء أي كائنات أخرى من Aspose.Diagram APIs.

{{% /alert %}} {{% alert color="primary" %}}

إذا تم استخدام جميع الطرق المذكورة أعلاه لتعيين مصادر الخطوط ، فسيتم تفعيل الإعدادات الأخيرة فقط.

{{% /alert %}}

