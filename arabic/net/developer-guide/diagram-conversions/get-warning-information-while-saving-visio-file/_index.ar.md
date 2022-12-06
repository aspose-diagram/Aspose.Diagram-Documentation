---
title: الحصول على معلومات تحذير أثناء حفظ ملف Visio
type: docs
weight: 110
url: /ar/net/get-warning-information-while-saving-visio-file/
---
## **سيناريوهات الاستخدام الممكنة**

 يحاول المستخدم أحيانًا حفظ diagram الذي يحتوي على نص لا يحتوي على خط محلي. في مثل هذه الحالة ، يقوم Aspose.Diagram بإلقاء تحذيرات أثناء حفظ diagram. يمكنك التقاط هذه التحذيرات من خلال تنفيذ**[IWarningCallback] (https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** الواجهة والإعداد**[SaveOptions.WarningCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**منشأه.

## **احصل على تحذيرات أثناء حفظ ملف Visio**

 يوضح نموذج التعليمات البرمجية التالي كيفية الحصول على تحذيرات أثناء حفظ ملف visio. يقوم الكود بتحويل ملف[عينة ملف visio](sampleFontSubstitution.vsdx) الذي يرمي**[FontSubstitution] (https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** تحذير على الادخار. هذا التحذير تم القبض عليه بعد ذلك**[IWarningCallback.Warning ()] (https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**طريقة طباعة رسائل التحذير على وحدة التحكم. يرجى أيضًا التحقق من إخراج وحدة التحكم للرمز الوارد أدناه لمزيد من الفهم.

## **عينة من الرموز**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **إخراج وحدة التحكم**

هنا هو إخراج وحدة التحكم من الكود أعلاه عند تنفيذه مع المقدمة[عينة ملف visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
