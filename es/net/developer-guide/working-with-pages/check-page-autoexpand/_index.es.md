---
title: Comprobar la expansión automática de la página
type: docs
weight: 10
url: /es/net/check-page-autoexpand/
description: Esta sección explica cómo verificar o cambiar la página es expandir automáticamente en un archivo visio con Aspose.Diagram.
---
## **Cambiar tamaño de página**

 los[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objeto representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Pages expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) La clase admite una colección de objetos Aspose.Diagram.Page.
 los[Accesorios de página](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) El objeto representa los atributos de la página, como el ancho, la altura y la escala de la página. Esta propiedad se puede utilizar para comprobar la expansión automática de la página.

Use la propiedad PageProps para verificar la expansión automática de la página.
### **Ejemplo de programación de configuración del tamaño de página**
La siguiente pieza de código verifica la expansión automática de la página desde un diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

