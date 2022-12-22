---
title: Añadir comentarios a dibujos en Visio
type: docs
weight: 40
url: /es/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
continuación se muestra el código para agregar comentarios en diagram:

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET le permite colocar comentarios en cualquier lugar de una página diagram.

{{% /alert %}} 

El método AddComment, expuesto por la clase Page, le permite agregar comentarios a una página de dibujo. Toma las coordenadas X e Y junto con una cadena de comentarios. A continuación se muestra el fragmento de código:

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
