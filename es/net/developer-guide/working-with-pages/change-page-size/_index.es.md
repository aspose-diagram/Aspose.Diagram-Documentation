---
title: Cambiar tamaño de página
type: docs
weight: 10
url: /es/net/change-page-size/
description: Esta sección explica cómo cambiar el tamaño de página en un archivo visio con Aspose.Diagram.
---
## **Cambiar tamaño de página**

 los[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objeto representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Pages expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) La clase admite una colección de objetos Aspose.Diagram.Page.
 los[Accesorios de página](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) El objeto representa los atributos de la página, como el ancho, la altura y la escala de la página. Esta propiedad se puede utilizar para cambiar el tamaño de la página.

Utilice la propiedad PageProps para cambiar el tamaño de la página.
### **Ejemplo de programación de configuración del tamaño de página**
El siguiente fragmento de código cambia el tamaño de página de diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

