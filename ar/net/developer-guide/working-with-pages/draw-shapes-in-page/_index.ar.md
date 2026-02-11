---
title: ارسم الأشكال في الصفحة
type: docs
weight: 40
url: /ar/net/draw-shapes-in-page/
description: يشرح هذا القسم كيفية رسم الأشكال في صفحة visio باستخدام Aspose.Diagram.
---
## **رسم شكل متعدد الخطوط في الصفحة**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل متعدد الخطوط في الصفحة. من أجل رسم شكل متعدد الخطوط ، العرض API**DrawPolyline ()**طريقة[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)صف دراسي. يوضح مثال الكود أدناه كيفية رسم خط متعدد في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 2), new PointF(4, 2), new PointF(3, 1) };
//Draw polyline in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPolylineInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **ارسم بيزيير في الصفحة**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل بيزير في الصفحة. من أجل رسم شكل بيزير ، عرض API**DrawBezier (اقتباسًا عن روايته)**طريقة[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **صف دراسي. يوضح مثال الكود أدناه كيفية رسم بيزير في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 2), new PointF(3.79949292203676f, 0) };
//Draw brezier in diagram
diagram.Pages[0].DrawBezier(1, 1, 2, 2, ps);
// Save diagram
diagram.Save(dataDir + "DrawBezierInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **ارسم المفتاح في الصفحة**
Aspose.Diagram for .NET API يسمح للمطورين برسم شكل خدد في الصفحة. من أجل رسم شكل بيزير ، عرض API**DrawSpline ()**طريقة[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **صف دراسي. يوضح مثال الكود أدناه كيفية رسم بيزير في رسم Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(0, 0.3270758925347308f),
                 new PointF(0.2926845121364643f, 0.3581517392187368f),
                 new PointF(0.6526026522346893f, 0.4640748257705201f),
                 new PointF(1f, 0.327075892534732f) };
//Draw Spline in diagram
diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);
// Save diagram
diagram.Save(dataDir + "DrawSplineInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

