---
title: Aspose.Diagram Operaciones de fuentes
type: docs
weight: 180
url: /es/net/aspose-diagram-font-operations/
description: Esta página describe cómo manipular fuentes con la biblioteca Aspose.Diagram.
---
## **Cómo especificar la ubicación de las fuentes TrueType**
Aspose.Diagram permite a los desarrolladores configurar los directorios de fuentes para renderizar en diagramas Visio. Este artículo muestra cómo utilizar fuentes de directorios personalizados.
### **Trabajar con fuentes**
#### **Donde Aspose.Diagram busca fuentes TrueType en Windows**
 Aspose.Diagram busca fuentes en el**Windows\Fuentes** carpeta. Esta configuración predeterminada funciona la mayor parte del tiempo, así que solo especifique sus propias carpetas de fuentes si realmente lo necesita.
#### **Cómo especificar explícitamente una carpeta de fuentes**
Aspose.Diagram API ha expuesto la propiedad FontDirs para el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class para especificar las carpetas de fuentes como se describe a continuación.

1. La propiedad Diagram.FontDirs acepta una matriz de cadenas para que el desarrollador pueda especificar muchos directorios de fuentes usando este enfoque.

{{% alert color="primary" %}} 

Al especificar la carpeta de fuentes utilizando el enfoque mencionado anteriormente, recomendamos configurar la ubicación de la fuente al inicio de la aplicación; de lo contrario, puede obtener resultados con un formato deficiente.

{{% /alert %}} {{% alert color="primary" %}} 

Configurar la carpeta de fuentes con cualquiera de los métodos anteriores no garantiza que Aspose.Diagram API no busque las fuentes en ubicaciones predeterminadas, como la carpeta de fuentes del sistema.

{{% /alert %}} 
#### **Ejemplo de programación**
El siguiente código de ejemplo muestra cómo configurar Aspose.Diagram para buscar fuentes TrueType en varias carpetas al renderizar o incrustar fuentes.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Setting the custom font directories
diagram.FontDirs = fontDirs;

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "SpecifyFontLocation_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```
### **Reciba notificaciones de fuentes faltantes y sustitución de fuentes durante el renderizado**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **Ejemplo de programación de notificación de fuentes faltantes y sustitución de fuentes**
Para ser notificado de la sustitución de fuentes durante el renderizado:

1. Cree una clase que implemente el[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. Páselo a la propiedad PdfSaveOptions.WarningCallback.

Durante el guardado del dibujo, la instancia de[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)se llama si hay posibles problemas de fidelidad con el dibujo. En este caso, elegimos procesar solo las advertencias que son de sustitución de fuente e imprimir la advertencia en la pantalla. El siguiente ejemplo muestra cómo recibir notificaciones de sustituciones de fuentes usando[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementando IWarningCallback**
El último paso es crear la clase que implementa el[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)interfaz. Esta clase imprimirá cualquier advertencia de sustitución de fuentes en la consola. El siguiente ejemplo muestra cómo implementar IWarningCallback para recibir una notificación de cualquier sustitución de fuente durante el guardado del documento.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
