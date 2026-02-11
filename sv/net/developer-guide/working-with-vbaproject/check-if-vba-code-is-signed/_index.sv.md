---
title: Kontrollera om VBA-koden är signerad
type: docs
weight: 100
url: /sv/net/check-if-vba-code-is-signed/
description: Kontrollera om vba-koden är signerad med biblioteket Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram låter användaren kontrollera om VBA-kodprojektet är signerat eller inte. Vänligen använd[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) egenskap för att kontrollera om VBA-kodprojektet är signerat eller inte.

{{% /alert %}}

 Följande kod förklarar hur du kontrollerar om VBA-koden är signerad eller inte med hjälp av[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) fast egendom. Du kan använda vilken som helst av dina visio-filer för att testa den här koden. För teständamål kan du använda[denna visio-fil som används i koden](1.vsdm).

## Exempelkod

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

## Konsolutgång

 Nedan är konsolutgången för ovanstående kod med hjälp av[exempel visio fil](1out.vsdm) tillhandahålls av länken.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
