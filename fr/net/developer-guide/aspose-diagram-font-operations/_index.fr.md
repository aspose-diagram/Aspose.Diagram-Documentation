---
title: Aspose.Diagram Opérations sur les polices
type: docs
weight: 180
url: /fr/net/aspose-diagram-font-operations/
description: Cette page décrit comment manipuler les polices avec la bibliothèque Aspose.Diagram.
---
## **Comment spécifier l'emplacement des polices TrueType**
Aspose.Diagram permet aux développeurs de définir les répertoires de polices pour le rendu dans les diagrammes Visio. Cet article montre comment utiliser les polices des répertoires personnalisés.
### **Travailler avec des polices**
#### **Où Aspose.Diagram recherche les polices TrueType sur Windows**
 Aspose.Diagram recherche les polices dans**Windows\Polices** dossier. Ce paramètre par défaut fonctionne la plupart du temps, donc ne spécifiez vos propres dossiers de polices que si vous en avez vraiment besoin.
#### **Comment spécifier explicitement un dossier de polices**
Aspose.Diagram API a exposé la propriété FontDirs pour le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe pour spécifier les dossiers de polices comme décrit ci-dessous.

1. La propriété Diagram.FontDirs accepte un tableau de chaînes afin que le développeur puisse spécifier de nombreux répertoires de polices à l'aide de cette approche.

{{% alert color="primary" %}} 

Lorsque vous spécifiez le dossier des polices à l'aide de l'approche mentionnée ci-dessus, nous vous recommandons de définir l'emplacement de la police au démarrage de l'application, sinon vous risquez de recevoir des résultats mal formatés.

{{% /alert %}} {{% alert color="primary" %}} 

La définition du dossier de polices à l'aide de l'une des méthodes ci-dessus ne garantit pas que le Aspose.Diagram API ne recherchera pas les polices dans les emplacements par défaut tels que le dossier de polices du système.

{{% /alert %}} 
#### **Exemple de programmation**
L'exemple de code ci-dessous montre comment définir Aspose.Diagram pour rechercher dans plusieurs dossiers les polices TrueType lors du rendu ou de l'incorporation de polices.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SpecifyFontLocation-SpecifyFontLocation.cs" >}}
### **Recevoir une notification des polices manquantes et de la substitution de polices pendant le rendu**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **Notification de polices manquantes et exemple de programmation de substitution de polices**
Pour être averti de la substitution de polices lors du rendu :

1. Créer une classe qui implémente le[IAvertissementCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. Passez-le à la propriété PdfSaveOptions.WarningCallback.

Lors de l'enregistrement du dessin, l'instance de[IAvertissementCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)est appelé s'il existe des problèmes potentiels de fidélité avec le dessin. Dans ce cas, nous choisissons de traiter uniquement les avertissements de substitution de police et d'afficher l'avertissement à l'écran. L'exemple ci-dessous montre comment recevoir des notifications de substitutions de polices en utilisant[IAvertissementCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implémentation de IWarningCallback**
La dernière étape consiste à créer la classe implémentant le[IAvertissementCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)interface. Cette classe affichera tous les avertissements de substitution de polices sur la console. L'exemple ci-dessous montre comment implémenter IWarningCallback pour être averti de toute substitution de police lors de l'enregistrement du document.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
