---
title: Trabajando con Imprimir
type: docs
weight: 80
url: /es/net/working-with-print/
description: This section explains how to print a document via XpsPrint with Aspose.Diagram.
---
## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **Problema**
Cuando desarrolla una aplicación .NET y necesita producir algún resultado impreso, puede usar las clases en el espacio de nombres System.Drawing.Printing o las clases WPF. Pero resulta que si desarrolla una aplicación de servicio ASP.NET o Windows, sus opciones de impresión son muy limitadas, porque Microsoft recomienda no utilizar estos enfoques. Vea los vínculos abajo para más información.

<http://support.microsoft.com/kb/324565>

El uso de las clases de impresión .NET Framework no se admite desde un servicio. Esto incluye páginas ASP, que generalmente se ejecutan en el contexto del servicio del servidor.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Las clases dentro del espacio de nombres System.Drawing.Printing no se admiten para su uso dentro de un servicio Windows o una aplicación o servicio ASP.NET. Intentar utilizar estas clases desde dentro de uno de estos tipos de aplicaciones puede producir problemas inesperados, como un rendimiento del servicio disminuido y excepciones en tiempo de ejecución.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

No se admite el uso de WPF para compilar servicios Windows. Debido a que WPF es una tecnología de presentación, el servicio Windows requiere los permisos apropiados para realizar operaciones visuales que involucran la interacción del usuario. Si el servicio Windows no tiene los permisos adecuados, puede haber resultados inesperados.

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **Solución**
La forma correcta de imprimir documentos de acuerdo con Microsoft es usar XpsPrint API no administrado. Este API está disponible en Windows 7, Windows Server 2008 R2 y también en Windows Vista, siempre que esté instalada la Actualización de plataforma para Windows Vista.

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **El código**
Hemos creado la clase XpsPrintHelper con el método Print, que es muy fácil de usar. Solo necesita especificar un documento que desea imprimir, un nombre de impresora y un nombre de trabajo opcional. Si hubo algún problema al enviar o imprimir el documento, el método generará una excepción.

El último parámetro es un valor booleano que especifica si el código debe esperar hasta que se imprima el trabajo o regresar inmediatamente después de que se haya enviado el trabajo de impresión. Si elige regresar de inmediato, no podrá determinar si el documento se imprimió correctamente o no al final.
#### **Ejemplo de programación**
The following code example shows how to invoke the utility class to print via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


There are two overloads of the XpsPrintHelper.Print method. The first overload takes an Aspose.Diagram.Diagram object and saves it into a MemoryStream in the XPS format. Then it invokes the other XpsPrintHelper.Print overload.

If you want to use this sample without Aspose.Diagram (e.g. you already have an XPS document and just want to print it from an ASP.NET or Windows Service application), then you can just delete this method.
#### **XPS Stream and Print Programming Sample**
This code example convert a Diagram into an XPS stream and print.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


The second XpsPrintHelper.Print overload accepts a Stream object. The stream must contain a document in the XPS format. This method starts an XPS print job, sends the document to the XpsPrint API and then waits for the result if needed.
#### **Muestra de programación XpsPrint API**
This code example prints an XPS document using the XpsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


El código para los métodos StartJob, CopyJob, WaitForJob y CheckJobStatus, así como las definiciones de las interfaces IXpsPrintJob y IXpsPrintJobStream, es de muy bajo nivel y utiliza Platform Invoke y COM Interop. Este código no está incluido en el artículo por brevedad, pero está disponible en la descarga de muestra.

XpsPrint API también proporciona funcionalidad adicional, como monitorear el progreso del trabajo, pero nuestro XpsPrintHelper es un contenedor muy simple y no expone esta funcionalidad. Puede agregar esto usted mismo si lo desea.

{{% alert color="primary" %}}

Cuando ejecuta el proyecto, imprime un documento de muestra en la impresora especificada. Para que los resultados sean visibles, se abre la ventana de la consola. El programa muestra el mensaje de éxito o el texto de una excepción si se produjo una.

{{% /alert %}}
## **Imprimiendo un Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) proporciona cuatro métodos de sobrecarga para la impresión de los diagramas. Estos métodos son lo suficientemente flexibles para imprimir el diagram en la impresora predeterminada o en cualquiera de las impresoras disponibles con configuraciones personalizadas. Solo necesita seleccionar el método de impresión apropiado de acuerdo con el requisito.
### **Impresión en la impresora predeterminada**
La impresión del diagram en la impresora predeterminada es bastante simple en Aspose.Diagram for .NET. Realice los siguientes pasos para imprimir el diagram en la impresora predeterminada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión sin parámetros expuestos por el objeto Diagram
#### **Muestra de programación de impresión a la impresora predeterminada**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **Impresión en una impresora específica**
La impresión del diagram en la impresora específica requiere el nombre de la impresora como parámetro para el método de impresión del Diagram. Realice los siguientes pasos para imprimir el diagram en la impresora deseada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión de la clase Diagram con el nombre de la impresora como parámetro de cadena para el método de impresión
#### **Muestra de programación de impresión en una impresora específica**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **Configuración del nombre de la impresora y del documento**
Aspose.Diagram Las API permiten configurar la impresora específica y el nombre del documento para un trabajo de impresión. Realice los siguientes pasos para imprimir el diagram en la impresora deseada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión de la clase Diagram con la impresora y el nombre del documento como parámetro de cadena para el método de impresión
#### **Configuración de la impresora y el nombre del documento Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}
