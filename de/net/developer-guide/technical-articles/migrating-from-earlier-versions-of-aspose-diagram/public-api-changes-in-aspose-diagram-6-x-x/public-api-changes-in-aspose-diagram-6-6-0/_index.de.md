---
title: Öffentlich API Änderungen in Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.3.0 auf 6.6.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Fügt die Formate VSDM, VSSM und VSTM in der LoadFileFormat-Klasse hinzu**
Diese Version fügt Unterstützung für das Lesen von makrofähigen Visio-Formaten hinzu.
## **Fügt die Formate VSDM, VSSM und VSTM in der SaveFileFormat-Klasse hinzu**
Diese Version fügt Unterstützung für das Schreiben von makrofähigen Visio-Formaten hinzu.
## **Ändern Sie den VBA-Modulcode in Visio Diagram**
Wir haben die Klassen VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference und VbaProjectReferenceCollection hinzugefügt. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Mit dieser neuen Version 6.6.0 oder höher können Entwickler VBA-Modulcode extrahieren und ändern. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
## **Fügt eine ImageData-Eigenschaft in der ForeignData-Klasse hinzu**
Es stellt ein Bild eines Ole-Objekts als Byte-Array dar. Außerdem haben wir die Manipulation von OLE-Objekten verbessert. Entwickler können jetzt auch ein OLE-Objekt in der Visio diagram ersetzen. Bitte überprüfen Sie dieses Codebeispiel:

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

Fehler beim Rendern des Makros „Code“: Ungültiger Wert für Parameter lang angegeben
