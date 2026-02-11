---
title: Obtenir des informations d'avertissement lors de l'enregistrement du fichier Visio
type: docs
weight: 110
url: /fr/net/get-warning-information-while-saving-visio-file/
---
## **Scénarios d'utilisation possibles**

 Parfois, l'utilisateur essaie d'enregistrer le diagram qui contient du texte qui n'a pas de police locale. Dans ce cas, Aspose.Diagram lance des avertissements lors de l'enregistrement du diagram. Vous pouvez intercepter ces avertissements en implémentant le**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** interface et réglage**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**propriété.

## **Obtenir des avertissements lors de l'enregistrement du fichier Visio**

 L'exemple de code suivant explique comment obtenir des avertissements lors de l'enregistrement du fichier visio. Le code convertit le[exemple de fichier visio](sampleFontSubstitution.vsdx) qui jette**[FontSubstitution](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** avertissement lors de la sauvegarde. Cet avertissement est alors intercepté par**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**méthode qui imprime les messages d'avertissement sur la console. Veuillez également vérifier la sortie de la console du code ci-dessous pour plus de compréhension.

## **Exemple de code**

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

## **Sortie console**

Voici la sortie de la console du code ci-dessus lorsqu'il est exécuté avec le fourni[exemple de fichier visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
