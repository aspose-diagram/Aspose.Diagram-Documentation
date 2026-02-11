---
title: Erhalten Sie Warninformationen beim Speichern der Datei Visio
type: docs
weight: 110
url: /de/java/get-warning-information-while-saving-visio-file/
---
## **Mögliche Nutzungsszenarien**

 Manchmal versucht der Benutzer, die diagram zu speichern, die Text enthält, der keine lokale Schriftart hat. In diesem Fall gibt Aspose.Diagram beim Speichern von diagram Warnungen aus. Sie können diese Warnungen abfangen, indem Sie die implementieren**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** Schnittstelle und Einstellung**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**Eigentum.

## **Erhalten Sie Warnungen beim Speichern der Visio-Datei**

 Der folgende Beispielcode erläutert, wie Sie beim Speichern der Datei visio Warnungen erhalten. Der Code konvertiert die[Beispieldatei visio](sampleFontSubstitution.vsdx) der wirft**[FontSubstitution] (https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** Warnung beim Speichern. Diese Warnung wird dann abgefangen**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**Methode, die die Warnmeldungen auf der Konsole ausgibt. Bitte überprüfen Sie zum besseren Verständnis auch die Konsolenausgabe des unten angegebenen Codes.

## **Beispielcode**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "sampleFontSubstitution.vsdx");

// create an instance SVG save options class
Aspose.Diagram.Saving.SVGSaveOptions so = new Aspose.Diagram.Saving.SVGSaveOptions();

so.WarningCallback = new TestDiagramWarningCallback();
// save Visio drawing
diagram.Save(dataDir + "WarningCallback_out.svg", options);


public class TestDiagramWarningCallback : Aspose.Diagram.IWarningCallback
{
    public void Warning(Aspose.Diagram.WarningInfo info)
    {
        if (info.WarningType == Aspose.Diagram.WarningType.FontSubstitution)
        {
            Console.WriteLine("Diagram WARNING INFO: " + info.Description);
        }

    }
}

{{< /highlight >}}
```

## **Konsolenausgabe**

Hier ist die Konsolenausgabe des obigen Codes, wenn er mit dem bereitgestellten ausgeführt wird[Beispieldatei visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
