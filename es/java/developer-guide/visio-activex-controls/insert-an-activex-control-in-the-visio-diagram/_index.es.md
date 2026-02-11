---
title: Inserte un Control ActiveX en el Visio Diagram
type: docs
weight: 10
url: /es/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Los desarrolladores pueden agregar controles ActiveX directamente a los dibujos Microsoft Visio para hacer que los Visio diagram sean interactivos usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Insertar una muestra de programación de control ActiveX**
[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class ofrece el método addActiveXControl y permite a los desarrolladores insertar cualquier tipo de control ActiveX como botón de comando, cuadro combinado, casilla de verificación, cuadro de lista, cuadro de texto, botón giratorio, botón de radio, etiqueta, imagen, botón de alternancia y barra de desplazamiento.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

