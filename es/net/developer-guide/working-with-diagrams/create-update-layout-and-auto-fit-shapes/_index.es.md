---
title: Crear, actualizar, diseñar y autoajustar formas
type: docs
weight: 10
url: /es/net/create-update-layout-and-auto-fit-shapes/
description: Use C# Diagram API para crear, actualizar y diseñar formas automáticamente en archivos Visio usando C# dentro de sus aplicaciones. Guía completa con ejemplos de código C#.
---
## **Creando un Diagram**
 Aspose.Diagram for .NET le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)para construir el diagram. Use el constructor predeterminado de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}

## **Formas de diseño en estilo de diagrama de flujo**
 Con ciertos tipos de dibujos conectados, como diagramas de flujo y diagramas de red, puede utilizar el**Formas de diseño** característica para posicionar formas automáticamente. El posicionamiento automático es más rápido que arrastrar manualmente cada forma a una nueva ubicación.

Por ejemplo, si está actualizando un diagrama de flujo grande para incluir un nuevo proceso, puede agregar y conectar las formas que componen el proceso y luego usar la función de diseño para diseñar automáticamente el dibujo actualizado.

 El método Layout, expuesto por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) la clase diseña las formas y/o redirige los conectores en todas las páginas de diagram. Este método acepta un[Opciones de diseño](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)objeto como argumento. Use las diferentes propiedades expuestas por la clase LayoutOptions para diseñar formas automáticamente.

La siguiente imagen muestra el diagram cargado por los fragmentos de código en este artículo, antes de que se aplique el diseño automático. Los fragmentos de código muestran cómo aplicar[diseños de diagrama de flujo](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) y[diseños de árboles compactos](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**La fuente diagram.**

![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_1.png)

Los fragmentos de código de este artículo toman la fuente diagram y le aplican varios tipos de diseño automático, guardando cada uno en un archivo separado.

|<p>**Formas de diseño de abajo hacia arriba** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Formas de diseño de arriba a abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Diseño de formas de izquierda a derecha** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Diseño de formas de derecha a izquierda** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Para diseñar formas en estilo de diagrama de flujo:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de la clase LayoutOptions y configure las propiedades relacionadas con el estilo del diagrama de flujo.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el dibujo Visio.
### **Ejemplo de programación de estilo de diagrama de flujo**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

### **Disposición de formas en el estilo de árbol compacto**
 El estilo de diseño de árbol compacto intenta construir una estructura de árbol. Utiliza el mismo archivo de entrada que el[ejemplo anterior](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) guarda en varios estilos diferentes de árboles compactos.

|<p>**Diseño de árbol compacto: abajo y a la derecha** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Diseño de árbol compacto: abajo e izquierda** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Diseño de árbol compacto: derecha y abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Diseño de árbol compacto: izquierda y abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Para diseñar formas en el estilo de árbol compacto:

1.  Crear una instancia de la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase.
1. Cree una instancia de la clase LayoutOptions y establezca propiedades de estilo de árbol compacto.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el archivo Visio.
#### **Ejemplo de programación de estilo de árbol compacto**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Ajuste automático el Visio Diagram**
 Aspose.Diagram API admite el ajuste automático del dibujo Visio. Esta función de operación ayuda a traer formas externas dentro del límite de la página Visio. Aspose.Diagram for .NET API tiene el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. los[DiagramaGuardarOpciones](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) La clase expone la propiedad AutoFitPageToDrawingContent para ajustar automáticamente el dibujo Visio.

Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Cree un objeto de la clase DiagramSaveOptions y pase el formato de archivo resultante.
1. Establezca la propiedad AutoFitPageToDrawingContent del objeto DiagramSaveOptions.
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Ejemplo de programación de ajuste automático**
El siguiente código de ejemplo muestra cómo ajustar formas automáticamente en Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}

## **Trabajando con Proyecto VBA**
### **Modifique el código del módulo VBA en Visio Diagram**
 Este artículo muestra cómo modificar un código de módulo de VBA automáticamente usando Aspose.Diagram for .NET. Hemos agregado[Módulo Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Proyecto Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReferenceVbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) y[VbaProjectReferenceCollectionVbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) clases Estas clases ayudan a controlar el proyecto VBA. Los desarrolladores pueden extraer y modificar el código del módulo VBA.
### **Modificar ejemplo de programación de código de módulo VBA**
Por favor, compruebe este ejemplo de código:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

### **Eliminar todas las macros del Visio Diagram**
 Aspose.Diagram for .NET permite a los desarrolladores eliminar todas las macros del Visio diagram. La propiedad VbProjectData, expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, le permite eliminar todas las macros del dibujo Visio.
### **Eliminar todas las macros Ejemplo de programación**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Creación de un nuevo Diagram con VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)permite a los desarrolladores crear y trabajar con Microsoft Office Visio diagramas e incorporar características en sus aplicaciones de software. Hay otras formas de trabajar con archivos Visio, más comúnmente, Microsoft Automatización. Desafortunadamente, eso tiene algunas limitaciones. Aspose.Diagram es potente y rápido y funciona de forma independiente sin Microsoft Office instalación.

 Este artículo de migración muestra cómo usar first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) y entonces[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) para crear un nuevo diagram y agregarle algunas formas. Notará que el código Aspose.Diagram es más corto que el código VSTO. Siéntase libre de usar el código como base para su propio desarrollo y mejorarlo para satisfacer sus necesidades. VSTO le permite programar con archivos Microsoft Visio. Para crear un nuevo diagram:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Cree un diagram vacío.
1. Agregue formas de Visio maestros (plantillas).
1. Guarde el archivo como VDX.
### **Crear nuevo Diagram con muestra de programación VSTO**
{{% alert color="primary" %}}

usando Visio = Microsoft.Office.Interop.Visio;
Importaciones Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Ejemplo:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}

## **Creando un Nuevo Diagram con Aspose.Diagram for .NET**
Usando Aspose.Diagram API, los desarrolladores no necesitan Microsoft Office Visio instalación en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Para crear un nuevo diagram:

1. Cree un diagram vacío.
1. Agregue formas de Visio maestros (plantillas).
1. Guarde el archivo como VDX.
### **Nuevo Diagram con Aspose.Diagram for .NET Ejemplo de programación**
{{% alert color="primary" %}}

usando Aspose.Diagram;
Importaciones Aspose.Diagram

{{% /alert %}}

Ejemplo:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Actualizar propiedades de forma**
 Al trabajar con diagramas Microsoft Visio, los usuarios pueden actualizar los atributos de forma, incluidos el texto, el estilo, la posición, la altura y el ancho. Como desarrollador de software que trabaja con archivos Visio, se le pedirá que haga esto mediante programación. La buena noticia es que es posible, ya sea usando los mecanismos de programación con archivos Visio que proporciona Microsoft, VSTO, o usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 El siguiente tema muestra cómo usar[VSTO](https://products.aspose.com/diagram/net/) y[Aspose.Diagram](https://products.aspose.com/diagram/net/) para actualizar las propiedades de la forma. Los fragmentos de código a continuación muestran cómo actualizar las propiedades de forma para VSTO y Aspose.Diagram for .NET. Siéntase libre de usar el código y aplicarlo a su situación particular.
### **Actualización de propiedades de forma con VSTO**
VSTO le permite programar con archivos Microsoft Visio. Para actualizar las propiedades de la forma:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Abra un archivo Visio VSD existente.
1. Encuentre la forma requerida.
1. Actualice las propiedades de la forma (texto, estilo de texto, posición y tamaño).
1. Guarde el archivo como VDX.
#### **Actualización de las propiedades de la forma con el ejemplo de programación de VSTO**
{{% alert color="primary" %}}

usando Visio = Microsoft.Office.Interop.Visio;
Importaciones Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Ejemplo:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}

### **Actualización de propiedades de forma con Aspose.Diagram for .NET**
Usando Aspose.Diagram API, los desarrolladores no necesitan Microsoft Office Visio en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Para actualizar las propiedades de la forma con Aspose.Diagram for .NET:

1. Abra un archivo Visio VSD existente.
1. Encuentre la forma requerida.
1. Actualice las propiedades de la forma (texto, estilo de texto, posición y tamaño).
1. Guarde el archivo como VDX.
#### **Actualización de propiedades de forma con Aspose.Diagram for .NET Ejemplo de programación**
{{% alert color="primary" %}}

usando Aspose.Diagram;
Importaciones Aspose.Diagram

{{% /alert %}}

**Ejemplo:**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}

