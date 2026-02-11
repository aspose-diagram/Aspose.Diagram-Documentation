---
title: Compruebe si el código VBA está firmado
type: docs
weight: 100
url: /es/net/check-if-vba-code-is-signed/
description: Compruebe si el código vba está firmado con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram permite al usuario verificar si el proyecto de código VBA está firmado o no. Por favor use el[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) propiedad para verificar si el proyecto de código VBA está firmado o no.

{{% /alert %}}

 El siguiente código explica cómo verificar si el código VBA está firmado o no usando el[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) propiedad. Puede usar cualquiera de sus archivos visio para probar este código. Para fines de prueba, puede utilizar[este archivo visio utilizado en el código](1.vsdm).

## Código de muestra

```
{{< highlight "csharp" >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Salida de consola

 A continuación se muestra la salida de la consola del código anterior usando el[muestra visio archivo](1out.vsdm) proporcionada por el enlace.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
