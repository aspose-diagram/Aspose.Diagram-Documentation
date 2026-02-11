---
title: Zeichnung
type: docs
weight: 45
url: /de/net/drawing/
description: In diesem Abschnitt wird erläutert, wie Sie Formen auf einer visio-Seite mit Aspose.Diagram zeichnen.
---
## **Zeichnen Sie eine Polylinie auf der Seite**
Aspose.Diagram for .NET API ermöglicht Entwicklern das Zeichnen einer Polylinienform auf einer Seite. Um eine Polylinienform zu zeichnen, bietet das API an**DrawPolyline()**Methode der[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)Klasse. Das folgende Codebeispiel zeigt, wie eine Polylinie in einer Visio-Zeichnung gezeichnet wird.


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

## **Zeichnen Sie Bezier in Seite**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, eine Bézier-Form auf einer Seite zu zeichnen. Um eine Bezier-Form zu zeichnen, bietet das API an**DrawBezier()**Methode der[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **Klasse. Das folgende Codebeispiel zeigt, wie ein Bezier in einer Visio-Zeichnung gezeichnet wird.


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

## **Spline in Seite zeichnen**
Aspose.Diagram for .NET API ermöglicht Entwicklern das Zeichnen einer Spline-Form auf einer Seite. Um eine Bezier-Form zu zeichnen, bietet das API an**DrawSpline()**Methode der[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **Klasse. Das folgende Codebeispiel zeigt, wie ein Bezier in einer Visio-Zeichnung gezeichnet wird.


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

