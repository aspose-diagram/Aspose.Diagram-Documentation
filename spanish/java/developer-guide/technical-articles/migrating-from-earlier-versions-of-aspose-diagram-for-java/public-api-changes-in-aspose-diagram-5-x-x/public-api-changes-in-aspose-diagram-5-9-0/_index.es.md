---
title: Público API Cambios en Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /es/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.8.0 a la 5.9.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **Save Resultant HTML to a Stream**
El nuevo método de guardar se ha agregado en la clase Diagram. Toma dos parámetros, el objeto de flujo y el formato de archivo de guardado.
Código de ejemplo:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Copiar temas y PageSheet de otro Visio**
La clase Diagram ofrece el método CopyTheme y la clase PageSheet ofrece el método Copy para lograr el objetivo de copiar una forma y otras tareas de manipulación.
 Códigos de ejemplo:[Copie formas de un Visio existente](/diagram/es/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX y VSSX Opciones de guardado se agregan en SaveFileFormat**
Anteriormente, Aspose.Diagram API admitía la lectura y escritura del formato VSDX, pero ahora también hemos agregado soporte para escribir diagramas en los formatos VSTX y VSSX. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX Se agrega la opción de lectura en LoadFileFormat**
Anteriormente, Aspose.Diagram API admitía la lectura y escritura del formato VSDX, pero ahora también hemos agregado compatibilidad con la lectura del formato de plantilla VSSX. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
