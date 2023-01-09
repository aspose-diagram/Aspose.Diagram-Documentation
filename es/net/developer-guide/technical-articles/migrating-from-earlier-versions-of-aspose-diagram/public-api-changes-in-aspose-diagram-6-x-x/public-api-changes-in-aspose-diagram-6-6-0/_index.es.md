---
title: Público API Cambios en Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 6.3.0 a la 6.6.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Agrega los formatos VSDM, VSSM y VSTM en la clase LoadFileFormat**
Esta versión agrega soporte para leer formatos Visio habilitados para macros.
## **Agrega los formatos VSDM, VSSM y VSTM en la clase SaveFileFormat**
Esta versión agrega soporte para escribir formatos Visio habilitados para macros.
## **Modifique el código del módulo VBA en el Visio Diagram**
Hemos agregado las clases VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference y VbaProjectReferenceCollection. Estas clases ayudan a controlar el proyecto VBA. Usando esta nueva versión 6.6.0 o superior, los desarrolladores pueden extraer y modificar el código del módulo VBA. Por favor, compruebe este ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Error al renderizar macro 'código': valor no válido especificado para el parámetro lang
## **Agrega una propiedad ImageData en la clase ForeignData**
Representa una imagen de un objeto ole como una matriz de bytes. Además de esto, también hemos mejorado la manipulación de objetos OLE. Los desarrolladores ahora también pueden reemplazar un objeto OLE en el Visio diagram. Consulte este ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Error al renderizar macro 'código': valor no válido especificado para el parámetro lang
