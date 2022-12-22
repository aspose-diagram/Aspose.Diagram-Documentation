---
title: عام API تغييرات في Aspose.Diagram 17.01.2019
type: docs
weight: 10
url: /ar/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 16.12.0 إلى 17.01 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **تحويل Visio الرسم بأشكال انتقائية**
يمكن للمطورين تحديد أشكال معينة لتحويل رسم Visio إلى أي تنسيق آخر مدعوم. لقد أضفنا عضو الأشكال في فئة RenderingSaveOptions لهذا الغرض. كل فئة خيار حفظ هي الشكل الممتد لفئة RenderingSaveOptions. يرجى التحقق من مثال الرمز:

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
