---
title: Suivre la progression de la conversion des documents
type: docs
weight: 970
url: /fr/net/track-document-conversion-progress/
description: Cette section explique comment suivre la progression de la conversion des fichiers visio avec Aspose.Diagram.
---
## **Scénarios d'utilisation possibles**

 Parfois, la conversion de gros fichiers visio peut prendre un certain temps. Pendant ce temps, vous souhaiterez peut-être afficher la progression de la conversion du document au lieu d'un simple écran de chargement pour améliorer la convivialité de votre application. Aspose.Diagram prend en charge le processus de conversion de documents de suivi en fournissant le**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interface. La**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**l'interface fournit**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**et**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**méthodes que vous pouvez implémenter dans votre classe personnalisée. Vous pouvez également contrôler quelles pages sont rendues comme indiqué dans le T*estDiagramPageSavingCallback*classe personnalisée.

## **Suivre la progression de la conversion des documents**

 L'exemple de code suivant charge le[fichier source visio](Drawing1.vsdx) et imprime sa progression de conversion dans la console en utilisant le*TestPageSavingCallback* classe personnalisée qui implémente**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**interface.

## **Exemple de code**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

Voici le code pour le*TestDiagramPageSavingCallback*classe personnalisée.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}
```

## **Sortie console**

Commencer à enregistrer l'index de page 0 des pages 11</br>
Fin de l'enregistrement de l'index de page 0 des pages 11</br>
Commencer à enregistrer l'index de la page 1 des pages 11</br>
Fin de l'enregistrement page index 1 des pages 11</br>
Commencer à enregistrer l'index de la page 2 des pages 11</br>
Fin de l'enregistrement page index 2 des pages 11</br>
Commencer à enregistrer l'index de la page 3 des pages 11</br>
Fin de l'enregistrement page index 3 des pages 11</br>
Commencer à enregistrer l'index de la page 4 des pages 11</br>
Fin de l'enregistrement page index 4 des pages 11</br>
Commencer à enregistrer l'index de la page 5 des pages 11</br>
Fin de l'enregistrement page index 5 des pages 11</br>
Commencer à enregistrer l'index de la page 6 des pages 11</br>
Fin de l'enregistrement page index 6 des pages 11</br>
Commencer à enregistrer l'index de la page 7 des pages 11</br>
Fin de l'enregistrement page index 7 des pages 11</br>
Commencer à enregistrer l'index de la page 8 des pages 11</br>
Fin de l'enregistrement page index 8 des pages 11
