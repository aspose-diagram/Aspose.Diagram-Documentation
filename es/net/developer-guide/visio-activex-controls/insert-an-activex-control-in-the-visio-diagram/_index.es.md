---
title: Inserte un Control ActiveX en el Visio Diagram
type: docs
weight: 10
url: /es/net/insert-an-activex-control-in-the-visio-diagram/
description: Esta página describe cómo insertar un control ActiveX con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

 Los desarrolladores pueden agregar controles ActiveX directamente a los dibujos Microsoft Visio para hacer que los Visio diagram sean interactivos usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Insertar una muestra de programación de control ActiveX**
[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class ofrece el método AddActiveXControl y permite a los desarrolladores insertar cualquier tipo de control ActiveX como botón de comando, cuadro combinado, casilla de verificación, cuadro de lista, cuadro de texto, botón giratorio, botón de radio, etiqueta, imagen, botón de alternar y barra de desplazamiento.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
