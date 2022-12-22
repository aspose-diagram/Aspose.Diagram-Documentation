---
title: عام API التغييرات في Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /ar/net/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 5.6.0 إلى 5.7.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **قم بتعيين سلاسل نمط التاريخ على الجدول الزمني**
تمت إضافة خصائص DateFormatStringForBE و DateFormatStringForIntm الجديدة في فئة TimelineHelper. رموز المثال:

**C#**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";

// set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd"

' set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd"

{{< /highlight >}}
