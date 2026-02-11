---
title: احصل على Visio الشكل بما في ذلك الطفل
type: docs
weight: 110
url: /ar/net/get-visio-shape-including-child/
description: يشرح هذا القسم كيفية الحصول على شكل visio بما في ذلك الطفل مع معرف الشكل أو الاسم مع Aspose.Diagram.
---
### **استرجع Visio الشكل بما في ذلك الطفل**
كل شكل في diagram له معرف واسم. المعرف مهم عند البرمجة باستخدام Visio: إنه الطريقة الرئيسية للوصول إلى الشكل. يحتفظ كل شكل أيضًا بمعلومات حول العنصر الرئيسي (الاستنسل) الذي يتكون منه.

 أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) هو كائن في رسم Visio يحتمل أن يكون له أب أو أبناء. تدعم خاصية الأشكال ، المكشوفة بواسطة فئة الصفحة ، مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام الخاصية الأشكال لاسترداد معلومات حول الشكل.
#### **استرجع Visio عينة برمجة الشكل**
يسترد مقتطف الشفرة التالي الشكل بما في ذلك التابع. يرجى التحقق من نموذج الكود هذا:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

