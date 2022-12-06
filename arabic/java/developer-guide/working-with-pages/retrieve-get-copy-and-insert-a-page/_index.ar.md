---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/java/retrieve-get-copy-and-insert-a-page/
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](https://reference.aspose.com/diagram/java) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم خاصية Page.Background لتحديد ما إذا كانت الصفحة مقدمة أم صفحة خلفية.

توضح الصورة أدناه الإخراج من مقتطفات التعليمات البرمجية في هذه المقالة.

**وحدة تحكم تظهر الإخراج.** 

![ما يجب القيام به: image_بديل_نص](retrieve-get-copy-and-insert-a-page_1.png)
### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-RetrievePageInfo-RetrievePageInfo.java" >}}
## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. Aspose.Diagram له ميزات تساعدهم على القيام بذلك.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن أسلوب GetPage الذي يمكن استدعاؤه للحصول على كائن الصفحة.
### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.
#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyID-GetVisioPagebyID.java" >}}
### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.
#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyName-GetVisioPagebyName.java" >}}
## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram for Java API يسمح للمطورين بنسخ وإضافة محتوياته من Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for Java API لديه[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة فئة Diagram مجموعة من كائنات Aspose.Diagram.Page. تكشف فئة PageCollection عن طريقة Add التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-CopyVisioPage-CopyVisioPage.java" >}}
## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة النسخ الخاصة بفئة الصفحة نسخة صفحة ليتم نسخها.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **أدخل صفحة فارغة في رسم Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) يمكن إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

يسمح أسلوب Add ، الذي تم عرضه بواسطة مجموعة Pages ، للمطورين بإضافة صفحة فارغة جديدة في diagram Visio. يجب تعيين معرف الصفحة.
### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.java" >}}
## **انقل موضع الصفحة في الرسم Visio**
Aspose.Diagram for Java API يمكنه تحريك موضع الصفحة في الرسم Visio. تساعد طريقة moveTo ، التي تعرضها فئة الصفحة ، المطورين على تحريك موضع الصفحة.
### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
