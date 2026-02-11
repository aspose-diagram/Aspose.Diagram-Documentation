---
title: Trabajar con párrafo de formas
type: docs
weight: 40
url: /es/java/working-with-shapes-paragraph/
---
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Establecer el párrafo de la forma.
#### **Ejemplo de programación de párrafos de la forma establecida**
Use el siguiente código en su aplicación Java para configurar el párrafo de la forma usando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
