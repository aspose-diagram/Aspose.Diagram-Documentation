---
title: Trabajar con hipervínculos
type: docs
weight: 160
url: /es/net/working-with-hyperlinks/
description: Esta sección explica cómo agregar u obtener un hipervínculo en una forma Visio con Aspose.Diagram.
---
## **Agregar hipervínculo a una forma Visio**
Microsoft Office Visio admite la adición de hipervínculos a cualquier forma. Los hipervínculos pueden vincular a otra página o forma en el dibujo actual, una página o forma en otro dibujo, un documento que no sea un dibujo Visio, un sitio web, un sitio FTP o una dirección de correo electrónico. Los desarrolladores pueden usar Aspose.Diagram API para agregar fácilmente hipervínculos a una forma Visio.

 En el dibujo de varias páginas Visio, los hipervínculos pueden llevarlo de una forma a muchos otros tipos de enlaces.[Colección de hipervínculos](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase ofrece el método Add que se puede usar para agregar el hipervínculo de una forma.

Para identificar propiedades en Microsoft Office Visio:

1. En un Visio diagram, haga clic derecho en una forma.
1.  Seleccione**Hipervínculo.**
1. Establecer propiedades existentes
1.  Prensa**OK** botón

**Los datos del hipervínculo de una forma, como se ve en Microsoft Visio**

![todo:imagen_alternativa_texto](working-with-hyperlinks_1.png)
### **Agregar muestra de programación de hipervínculo**
El fragmento de código a continuación agrega los datos del hipervínculo de la forma.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Obtener datos de hipervínculos de las formas Visio**
Los desarrolladores pueden recuperar todos los hipervínculos de una forma Visio de la misma manera que[leer Visio datos de forma](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

En el dibujo de varias páginas Visio, los hipervínculos pueden llevarlo de una forma a muchos otros tipos de enlaces.[Colección de hipervínculos](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase permite a los desarrolladores recuperar hipervínculos.

Para identificar propiedades en Microsoft Office Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Hipervínculo.**

Todas las propiedades existentes se enumeran en el cuadro de diálogo.
**Los datos del hipervínculo de una forma, como se ve en Microsoft Visio**

![todo:imagen_alternativa_texto](working-with-hyperlinks_1.png)

**Una ventana de consola que muestra la salida de datos de forma**

![todo:imagen_alternativa_texto](working-with-hyperlinks_3.png)
### **Obtener muestra de programación de hipervínculos**
El fragmento de código siguiente lee los datos del hipervínculo de la forma.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
