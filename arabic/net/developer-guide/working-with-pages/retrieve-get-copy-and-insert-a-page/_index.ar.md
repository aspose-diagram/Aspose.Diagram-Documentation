---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/net/retrieve-get-copy-and-insert-a-page/
description: يشرح هذا القسم كيفية إدراج صفحة أو نسخها أو الحصول على معلومات الصفحة باستخدام Aspose.Diagram.
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

 ال[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم خاصية Page.Background لتحديد ما إذا كانت الصفحة مقدمة أم صفحة خلفية.
### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-RetrievePageInfo-RetrievePageInfo.cs" >}}
## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. Aspose.Diagram له ميزات تساعدهم على القيام بذلك.

 يقدم Aspose.Diagram for .NET[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن أسلوب GetPage الذي يمكن استدعاؤه للحصول على كائن الصفحة.
### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.
#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyID-GetVisioPagebyID.cs" >}}
### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.
#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyName-GetVisioPagebyName.cs" >}}
## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram for .NET API يسمح للمطورين بنسخ وإضافة محتوياته من Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for .NET API لديه[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن طريقة Add التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر جديد للفئة Diagram.
1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. أضف كافة الأساتذة من Visio diagram الذي تم تحميله
1. احصل على كائن الصفحة من diagram الذي تم تحميله (والذي يجب نسخه).
1. تعيين اسم كائن الصفحة والمعرف.
1. قم بإزالة الصفحة الفارغة من diagram الجديد (اختياري).
1. طريقة Call Add من فئة PageCollection.
1. احفظ diagram الجديد في تخزين الكمبيوتر.
### **نسخ نموذج لبرمجة الصفحة Visio**
يوضح مثال الكود أدناه كيفية نسخ كائن صفحة Visio إلى رسم Visio آخر.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-CopyVisioPage-CopyVisioPage.cs" >}}
## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة النسخ الخاصة بفئة الصفحة نسخة صفحة ليتم نسخها.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **أدخل صفحة فارغة في رسم Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) يمكن إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

يسمح أسلوب Add ، الذي تم عرضه بواسطة مجموعة Pages ، للمطورين بإضافة صفحة فارغة جديدة في diagram Visio. يجب تعيين معرف الصفحة.
### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.cs" >}}
## **انقل موضع الصفحة في الرسم Visio**
Aspose.Diagram for .NET API يمكنه تحريك موضع الصفحة في الرسم Visio. تساعد طريقة MoveTo ، التي تعرضها فئة الصفحة ، المطورين على تحريك موضع الصفحة.
### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
