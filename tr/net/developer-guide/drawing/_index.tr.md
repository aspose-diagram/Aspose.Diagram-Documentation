---
title: Resim çizme
type: docs
weight: 45
url: /tr/net/drawing/
description: Bu bölüm, visio ile bir visio sayfasındaki şekillerin nasıl çizileceğini açıklar.
---
## **Sayfada Çoklu Çizgi Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada çoklu çizgi şekli çizmesine olanak tanır. Çoklu çizgi şekli çizmek için API teklifi**DrawPolyline()**yöntemi[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)sınıf. Aşağıdaki kod örneği, Visio çiziminde nasıl sürekli çizgi çizileceğini gösterir.


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

## **Bezier'i Sayfada Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada çerçeve şekli çizmesine olanak tanır. Bezier şekli çizmek için API teklif**DrawBezier()**yöntemi[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **sınıf. Aşağıdaki kod örneği, Visio çiziminde bir bezierin nasıl çizileceğini gösterir.


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

## **Sayfada Spline Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada spline şekli çizmesine olanak tanır. Bezier şekli çizmek için API teklif**DrawSpline()**yöntemi[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **sınıf. Aşağıdaki kod örneği, Visio çiziminde bir bezierin nasıl çizileceğini gösterir.


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

