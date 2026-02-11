---
title: Hantera VBA-koder för Visio Makroaktiverad diagram.
linktitle: Diagram VBA-projekt
type: docs
weight: 200
url: /sv/java/working-with-vbaproject/
description: Lägg till VBA-modul och ändra VBA eller makro med Aspose.Diagram-biblioteket.
---
## **Lägg till en VBA-modul**
{{% alert color="primary" %}}

Aspose.Diagram låter dig lägga till en ny VBA-modul och makrokod med Aspose.Diagram. Använd metoden [**Diagram.VbaProject.Modules.Add()**] för att lägga till den nya VBA-modulen i diagram

{{% /alert %}}

 Följande exempelkod lägger till en ny VBA-modul och makrokod och sparar utdata i formatet VSDM. En gång öppnar du utdatafilen VSDM i Microsoft Visio och klickar på**Utvecklare > Visual Basic** menykommandon kommer du att se en modul som heter "TestModule" och inuti den kommer du att se följande makrokod.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Här är exempelkoden för att generera utdatafilen VSDM med VBA-modul och makrokod.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **Förhandsämnen**
- [Kontrollera om VBA-koden är signerad](/diagram/sv/java/check-if-vba-code-is-signed/)
