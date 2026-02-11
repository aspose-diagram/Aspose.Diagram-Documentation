---
title: Disegna forme nella pagina
type: docs
weight: 40
url: /it/net/draw-shapes-in-page/
description: Questa sezione spiega come disegnare forme in una pagina visio con Aspose.Diagram.
---
## **Disegna polilinea nella pagina**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma polilinea in una pagina. Per disegnare una forma polilinea, l'offerta API**DisegnaPolilinea()**metodo del[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)classe. L'esempio di codice seguente mostra come disegnare una polilinea in un disegno Visio.

```
{{< highlight "csharp" >}}
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
```
## **Disegna Bezier in Page**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma più bezier in una pagina. Per disegnare una forma più bezier, l'offerta API**DrawBezier()**metodo del[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **classe. L'esempio di codice seguente mostra come disegnare un bezier in un disegno Visio.

```
{{< highlight "csharp" >}}
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
```
## **Disegna spline nella pagina**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma spline in una pagina. Per disegnare una forma più bezier, l'offerta API**DisegnaSpline()**metodo del[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram)** **classe. L'esempio di codice seguente mostra come disegnare un bezier in un disegno Visio.

```
{{< highlight "csharp" >}}
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
```
