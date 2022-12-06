---
title: Offentlig API Ändringar i Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.3.0 till 6.6.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Lägger till formaten VSDM, VSSM och VSTM i klassen LoadFileFormat**
Denna version lägger till stöd för läsning av makroaktiverade Visio-format.
## **Lägger till formaten VSDM, VSSM och VSTM i klassen SaveFileFormat**
Denna version lägger till stöd för att skriva makroaktiverade Visio-format.
## **Ändra VBA-modulkoden i Visio Diagram**
Vi har lagt till klasserna VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference och VbaProjectReferenceCollection. Dessa klasser hjälper till att få kontroll över VBA-projekt. Med den här nya versionen 6.6.0 eller senare kan utvecklare extrahera och modifiera VBA-modulkod. Kontrollera detta kodexempel:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
## **Lägger till en ImageData-egenskap i klassen ForeignData**
Den representerar en bild av ett objekt som en byte-array. Utöver detta har vi också förbättrat manipuleringen av OLE-objekt. Utvecklare kan nu även ersätta ett OLE-objekt i Visio diagram. Kontrollera detta kodexempel:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Fel vid rendering av makrot 'kod': Ogiltigt värde angett för parameter lang
