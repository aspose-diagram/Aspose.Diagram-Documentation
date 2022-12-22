---
title: Público API Cambios en Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /es/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 6.3.0 a la 6.6.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **Agrega los formatos VSDM, VSSM y VSTM en la clase LoadFileFormat**
Esta versión agrega soporte para leer formatos Visio habilitados para macros.
### **Agrega los formatos VSDM, VSSM y VSTM en la clase SaveFileFormat**
Esta versión agrega soporte para escribir formatos Visio habilitados para macros.
### **Modifique el código del módulo VBA en Visio Diagram**
Hemos agregado las clases Vba, VbaProject y VbaModule. Estas clases ayudan a controlar el proyecto VBA. Usando esta nueva versión 6.6.0 o superior, los desarrolladores pueden extraer y modificar el código del módulo VBA. Por favor, compruebe este ejemplo de código:

**Java**

{{< highlight "java" >}}

 // carga un Visio diagram existente

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = nuevo Diagram (entrada);

// extrae el proyecto VBA

VbaProject v = diagram.getVbaProject();

// Iterar a través de los módulos y modificar el código de macro VBA

para (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Agrega un método getImageData en la clase ForeignData**
Representa una imagen de un objeto ole como una matriz de bytes. Además de esto, también hemos mejorado la manipulación de objetos OLE. Los desarrolladores ahora también pueden reemplazar un objeto OLE en el Visio diagram. Consulte este ejemplo de código:

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
