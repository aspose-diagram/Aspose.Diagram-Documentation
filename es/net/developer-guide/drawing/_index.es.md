---
title: Dibujo
type: docs
weight: 45
url: /es/net/drawing/
description: Esta sección explica cómo dibujar formas en una página visio con Aspose.Diagram.
---
## **Dibujar polilínea en página**
Aspose.Diagram for .NET API permite a los desarrolladores dibujar una forma de polilínea en una página. Para dibujar una forma de polilínea, la oferta API**dibujarpolilinea()**metodo de la[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)clase. El siguiente ejemplo de código muestra cómo dibujar una polilínea en un dibujo Visio.


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

## **Dibujar Bézier en la página**
Aspose.Diagram for .NET API permite a los desarrolladores dibujar una forma bezier en una página. Para dibujar una forma bezier, la oferta API**dibujarBezier()**metodo de la[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **clase. El siguiente código de ejemplo muestra cómo dibujar un bezier en un dibujo Visio.


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

## **Dibujar spline en la página**
Aspose.Diagram for .NET API permite a los desarrolladores dibujar una forma de spline en una página. Para dibujar una forma bezier, la oferta API**Dibujar Spline()**metodo de la[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **clase. El siguiente código de ejemplo muestra cómo dibujar un bezier en un dibujo Visio.


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

