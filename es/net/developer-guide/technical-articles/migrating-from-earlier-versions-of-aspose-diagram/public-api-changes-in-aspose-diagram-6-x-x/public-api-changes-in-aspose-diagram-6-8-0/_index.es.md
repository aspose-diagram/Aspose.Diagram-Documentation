---
title: Público API Cambios en Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 6.6.0 a la 6.8.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Insertar un control ActiveX**
Los desarrolladores pueden insertar un control ActiveX en el Visio diagram. Hemos agregado el método AddActiveXControl en el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) clase. Por favor, compruebe este ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Error al renderizar macro 'código': valor no válido especificado para el parámetro lang
## **Establezca la casilla de verificación de color de la capa**
Los desarrolladores pueden configurar u obtener la casilla de verificación de color de la capa usando Aspose.Diagram API. Consulte este ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Error al renderizar macro 'código': valor no válido especificado para el parámetro lang
## **Agrega la propiedad InheritFill en la clase de forma**
Los desarrolladores pueden obtener o establecer la propiedad de relleno heredada. Hemos agregado la propiedad InheritFill en la clase Shape. Por favor, compruebe este ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

Error al renderizar macro 'código': valor no válido especificado para el parámetro lang
