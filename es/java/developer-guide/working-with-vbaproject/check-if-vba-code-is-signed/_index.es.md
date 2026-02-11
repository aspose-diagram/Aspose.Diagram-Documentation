---
title: Compruebe si el código VBA está firmado
type: docs
weight: 100
url: /es/java/check-if-vba-code-is-signed/
description: Compruebe si el código vba está firmado con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram permite al usuario verificar si el proyecto de código VBA está firmado o no. Utilice la propiedad [**Diagram.VbaProject.IsSigned**] para verificar si el proyecto de código VBA está firmado o no.

{{% /alert %}}

 El siguiente código explica cómo verificar si el código VBA está firmado o no usando la propiedad [**Diagram.VbaProject.IsSigned**]. Puede usar cualquiera de sus archivos visio para probar este código. Para fines de prueba, puede utilizar[este archivo visio utilizado en el código](1.vsdm).

## Código de muestra

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Salida de consola

 A continuación se muestra la salida de la consola del código anterior usando el[muestra visio archivo](1out.vsdm) proporcionada por el enlace.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
