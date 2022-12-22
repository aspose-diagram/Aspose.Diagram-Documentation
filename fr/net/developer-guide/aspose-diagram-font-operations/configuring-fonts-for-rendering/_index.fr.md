---
title: Configuration des polices pour le rendu
type: docs
weight: 10
url: /fr/net/configuring-fonts-for-rendering/
---
## **Scénarios d'utilisation possibles**

Aspose.Diagram APIs provide the facility to render pages in image formats as well as convert them to PDF & XPS formats. In order to maximize the conversion fidelity, it is necessary that the fonts used in the spreadsheet should be available in the operating system's default font directory. In case the required fonts are not present then the Aspose.Diagram APIs will try to substitute the required fonts with the ones available.

## **Sélection de polices**

Vous trouverez ci-dessous le processus suivi par les API Aspose.Diagram en arrière-plan.

1. Le API essaie de trouver les polices sur le système de fichiers correspondant au nom de police exact utilisé dans la feuille de calcul.
1.  Si API ne trouve pas la police définie sous**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** propriété, il tente d'utiliser la police spécifiée sous**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**propriété.
1.  Si API ne trouve pas la police définie sous**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** propriété, il essaie de sélectionner les polices les plus appropriées parmi toutes les polices disponibles.
1. Enfin, si API ne trouve aucune police sur le système de fichiers, il rend la page en utilisant Times New Roman.

## **Définir des dossiers de polices personnalisés**

 Aspose.Diagram Les API recherchent dans le répertoire de polices par défaut du système d'exploitation les polices requises. Si les polices requises ne sont pas disponibles dans le répertoire des polices du système, les API recherchent dans les répertoires personnalisés (définis par l'utilisateur). La**[FontConfigs](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class a exposé un certain nombre de façons de définir des répertoires de polices personnalisés, comme indiqué ci-dessous.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Cette méthode est utile s'il n'y a qu'un seul dossier à définir.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**Cette méthode est utile lorsque les polices résident dans plusieurs dossiers et que l'utilisateur souhaite définir tous les dossiers séparément plutôt que de combiner toutes les polices dans un seul dossier.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: Ce mécanisme est utile lorsque l'utilisateur souhaite charger des polices à partir de plusieurs dossiers ou d'un seul fichier de police ou des données de police à partir d'un tableau d'octets.

{{% alert color="primary" %}}

 Tous les deux**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** acceptent un deuxième paramètre de type booléen. Qui passe**vrai** car le deuxième paramètre dirigera les API Aspose.Diagram pour rechercher les sous-dossiers des fichiers de polices.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Veuillez utiliser l'une des méthodes mentionnées ci-dessus au début de l'application, c'est-à-dire; avant d'invoquer tout autre objet des API Aspose.Diagram.

{{% /alert %}} {{% alert color="primary" %}}

Si toutes les méthodes mentionnées ci-dessus sont utilisées pour définir les sources de police, seuls les derniers paramètres prendront effet.

{{% /alert %}}

