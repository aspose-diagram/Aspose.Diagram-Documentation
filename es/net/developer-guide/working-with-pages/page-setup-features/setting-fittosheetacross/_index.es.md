---
title: Configuración de FitToSheetAcross
type: docs
weight: 10
url: /es/net/setting-fittosheetacross/
description: Esta sección explica cómo configurar fittosheetacross con Aspose.Diagram.
---
{{% alert color="primary" %}}

A veces, es necesario configurar los ajustes de configuración de página para que las páginas controlen la impresión. Estos ajustes de configuración de página ofrecen varias opciones.

{{% /alert %}}

## **Configuración de FitToSheetAcross**

Las opciones de configuración de página son totalmente compatibles con Aspose.Diagram. Este artículo explica cómo configurar las opciones de página con Aspose.Diagram y muestra ejemplos de código para configurar:

 Aspose.Diagram proporciona una clase,[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , que representa un archivo Microsoft Visio. los[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) la clase contiene un[**Paginas**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) colección que permite el acceso a cada página en el archivo Visio. Una página está representada por el[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page)clase.

 los[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la clase proporciona la[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propiedad que se utiliza para establecer las opciones de configuración de página de la página. De hecho, esto[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) La propiedad es un objeto de la[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) clase utilizada para establecer diferentes opciones de diseño de página para una página impresa. los[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class proporciona varias propiedades que se utilizan para establecer las opciones de configuración de la página. Algunas de estas propiedades se analizan a continuación.

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


