---
title: 在页面中绘制形状
type: docs
weight: 40
url: /zh/net/draw-shapes-in-page/
description: 本节介绍如何使用 Aspose.Diagram 在 visio 页面中绘制形状。
---
## **在页面中绘制折线**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制折线形状。为了绘制多段线形状，API 提供**绘制折线()**的方法[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)班级。下面的代码示例显示了如何在 Visio 绘图中绘制多段线。


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

## **在页面中绘制贝塞尔曲线**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制贝塞尔曲线。为了绘制贝塞尔曲线，API提供**绘制贝塞尔曲线()**的方法[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **班级。下面的代码示例显示了如何在 Visio 绘图中绘制贝塞尔曲线。


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

## **在页面中绘制样条线**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制样条形状。为了绘制贝塞尔曲线，API提供**绘制样条曲线()**的方法[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **班级。下面的代码示例显示了如何在 Visio 绘图中绘制贝塞尔曲线。


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

