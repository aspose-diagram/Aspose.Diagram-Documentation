---
title: Ottieni informazioni di avviso durante il salvataggio del file Visio
type: docs
weight: 110
url: /it/net/get-warning-information-while-saving-visio-file/
---
## **Possibili scenari di utilizzo**

 A volte l'utente cerca di salvare lo diagram che contiene testo che non ha un font locale. In tal caso, Aspose.Diagram genera avvisi durante il salvataggio di diagram. È possibile rilevare questi avvisi implementando il**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** interfaccia e impostazione**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**proprietà.

## **Ricevi avvisi durante il salvataggio del file Visio**

 Il seguente codice di esempio spiega come ottenere avvisi durante il salvataggio del file visio. Il codice converte il file[file di esempio visio](sampleFontSubstitution.vsdx) che lancia**[Sostituzione carattere](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** avviso sul salvataggio. Questo avviso viene quindi catturato da**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**metodo che stampa i messaggi di avviso sulla console. Si prega di controllare anche l'output della console del codice indicato di seguito per una maggiore comprensione.

## **Codice di esempio**

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

## **Uscita console**

Ecco l'output della console del codice precedente quando eseguito con il file fornito[file di esempio visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
