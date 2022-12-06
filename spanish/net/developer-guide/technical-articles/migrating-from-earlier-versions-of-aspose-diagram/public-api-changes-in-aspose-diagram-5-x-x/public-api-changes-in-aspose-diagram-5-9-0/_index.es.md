---
title: Público API Cambios en Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.8.0 a la 5.9.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Guardar HTML resultante en una secuencia**
Se ha agregado el nuevo método Guardar en la clase Diagram. Toma dos parámetros, el objeto de flujo y el formato de archivo de guardado.
Código de ejemplo:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Copiar temas y PageSheet de otro Visio**
La clase Diagram ofrece el método CopyTheme y la clase PageSheet ofrece el método Copy para lograr el objetivo de copiar una forma y otras tareas de manipulación.
 Códigos de ejemplo:[Copie formas de un Visio existente](/diagram/es/net/add-retrieve-copy-and-read-visio-shape-data/)
## **VSTX y VSSX Opciones de guardado se agregan en SaveFileFormat**
Anteriormente, Aspose.Diagram API admitía la lectura y escritura del formato VSDX, pero ahora también hemos agregado soporte para escribir diagramas en los formatos VSTX y VSSX. Códigos de ejemplo:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX Se agrega la opción de lectura en LoadFileFormat**
Anteriormente, Aspose.Diagram API admitía la lectura y escritura del formato VSDX, pero ahora también hemos agregado compatibilidad con la lectura del formato de plantilla VSSX. Códigos de ejemplo:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
