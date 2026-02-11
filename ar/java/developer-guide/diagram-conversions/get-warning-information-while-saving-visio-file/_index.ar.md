---
title: الحصول على معلومات تحذير أثناء حفظ ملف Visio
type: docs
weight: 110
url: /ar/java/get-warning-information-while-saving-visio-file/
---
## **سيناريوهات الاستخدام الممكنة**

 يحاول المستخدم أحيانًا حفظ diagram الذي يحتوي على نص لا يحتوي على خط محلي. في مثل هذه الحالة ، يقوم Aspose.Diagram بإلقاء تحذيرات أثناء حفظ diagram. يمكنك التقاط هذه التحذيرات من خلال تنفيذ**[IWarningCallback] (https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** الواجهة والإعداد**[SaveOptions.WarningCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**منشأه.

## **احصل على تحذيرات أثناء حفظ ملف Visio**

 يوضح نموذج التعليمات البرمجية التالي كيفية الحصول على تحذيرات أثناء حفظ ملف visio. يقوم الكود بتحويل ملف[عينة ملف visio](sampleFontSubstitution.vsdx) الذي يرمي**[FontSubstitution] (https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** تحذير على الادخار. هذا التحذير تم القبض عليه بعد ذلك**[IWarningCallback.Warning ()] (https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**طريقة طباعة رسائل التحذير على وحدة التحكم. يرجى أيضًا التحقق من إخراج وحدة التحكم للرمز الوارد أدناه لمزيد من الفهم.

## **عينة من الرموز**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "sampleFontSubstitution.vsdx");

// create an instance SVG save options class
Aspose.Diagram.Saving.SVGSaveOptions so = new Aspose.Diagram.Saving.SVGSaveOptions();

so.WarningCallback = new TestDiagramWarningCallback();
// save Visio drawing
diagram.Save(dataDir + "WarningCallback_out.svg", options);


public class TestDiagramWarningCallback : Aspose.Diagram.IWarningCallback
{
    public void Warning(Aspose.Diagram.WarningInfo info)
    {
        if (info.WarningType == Aspose.Diagram.WarningType.FontSubstitution)
        {
            Console.WriteLine("Diagram WARNING INFO: " + info.Description);
        }

    }
}

{{< /highlight >}}
```

## **إخراج وحدة التحكم**

هنا هو إخراج وحدة التحكم من الكود أعلاه عند تنفيذه مع المقدمة[عينة ملف visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
