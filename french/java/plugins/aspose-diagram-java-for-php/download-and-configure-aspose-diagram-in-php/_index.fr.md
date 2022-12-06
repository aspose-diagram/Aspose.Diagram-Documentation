---
title: Téléchargez et configurez Aspose.Diagram en PHP
type: docs
weight: 10
url: /fr/java/download-and-configure-aspose-diagram-in-php/
---
## **Télécharger les bibliothèques requises**
Téléchargez les bibliothèques requises mentionnées ci-dessous. Ce sont les éléments requis pour exécuter Aspose.Diagram Java pour les exemples Ruby.

- [Aspose.Diagram for Java Composant](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Télécharger des exemples à partir de sites de codage social**
Les versions suivantes des exemples en cours d'exécution sont disponibles au téléchargement sur les sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Installation**
Il est très simple et facile à installer Aspose.Diagram Java pour PHP, veuillez suivre les instructions :

Exécutez la commande suivante.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Utilisant**
Incluez les fichiers requis pour exporter le dessin visio vers un document PDF.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Comprenons le code ci-dessus.

1. La première ligne s'assure que le Aspose.Diagram est chargé et disponible.
1. Inclure les fichiers nécessaires pour accéder au Aspose.Diagram
1. Initialisez les bibliothèques. Les classes aspose Java sont chargées à partir du chemin fourni dans le fichier aspose.yml
