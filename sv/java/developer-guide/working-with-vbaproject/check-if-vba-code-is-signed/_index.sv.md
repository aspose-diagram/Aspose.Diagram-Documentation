---
title: Kontrollera om VBA-koden är signerad
type: docs
weight: 100
url: /sv/java/check-if-vba-code-is-signed/
description: Kontrollera om vba-koden är signerad med biblioteket Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram låter användaren kontrollera om VBA-kodprojektet är signerat eller inte. Använd [**Diagram.VbaProject.IsSigned**]-egenskapen för att kontrollera om VBA-kodprojektet är signerat eller inte.

{{% /alert %}}

 Följande kod förklarar hur du kontrollerar om VBA-koden är signerad eller inte med [**Diagram.VbaProject.IsSigned**]-egenskapen. Du kan använda vilken som helst av dina visio-filer för att testa den här koden. För teständamål kan du använda[denna visio-fil som används i koden](1.vsdm).

## Exempelkod


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## Konsolutgång

 Nedan är konsolutgången för ovanstående kod med hjälp av[exempel visio fil](1out.vsdm) tillhandahålls av länken.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
