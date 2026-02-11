---
title: Hantera VBA-koder för Visio Makroaktiverad diagram.
linktitle: Diagram VBA-projekt
type: docs
weight: 200
url: /sv/net/working-with-vbaproject/
description: Lägg till VBA-modul och ändra VBA eller makro med Aspose.Diagram-biblioteket.
---
## **Lägg till en VBA-modul**
{{% alert color="primary" %}}

 Aspose.Diagram låter dig lägga till en ny VBA-modul och makrokod med Aspose.Diagram. Använd[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) metod för att lägga till den nya VBA-modulen i diagram

{{% /alert %}}

 Följande exempelkod lägger till en ny VBA-modul och makrokod och sparar utdata i formatet VSDM. En gång öppnar du utdatafilen VSDM i Microsoft Visio och klickar på**Utvecklare > Visual Basic** menykommandon kommer du att se en modul som heter "TestModule" och inuti den kommer du att se följande makrokod.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Här är exempelkoden för att generera utdatafilen VSDM med VBA-modul och makrokod.

```
{{< highlight "csharp" >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.VbaProject.Modules.Add(VbaModuleType.Procedural, "TestModule");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[index];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Ändra VBA eller makro**

{{% alert color="primary" %}} 

Du kan ändra VBA eller makrokod med Aspose.Diagram. Aspose.Diagram har lagt till följande namnområde och klasser för att läsa och ändra VBA-projektet i filen Visio.

- Aspose.Diagram.Vba
- VbaProject
- VbaModuleCollection
- VbaModule

Den här artikeln visar hur du ändrar VBA- eller makrokoden i källfilen Visio med Aspose.Diagram.

{{% /alert %}} 

Följande exempelkod laddar källfilen Visio som har en följande VBA- eller makrokod inuti

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Efter exekvering av Aspose.Diagram exempelkod kommer VBA- eller makrokoden att ändras så här

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Du kan ladda ner[källfil Visio]() och den[utgång Visio fil]() från de angivna länkarna.

```
{{< highlight "csharp" >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[2];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Förhandsämnen**
- [Kontrollera om VBA-koden är signerad](/diagram/sv/net/check-if-vba-code-is-signed/)
