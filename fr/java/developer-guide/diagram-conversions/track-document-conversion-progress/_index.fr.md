---
title: Suivre la progression de la conversion des documents
type: docs
weight: 970
url: /fr/java/track-document-conversion-progress/
description: Cette section explique comment suivre la progression de la conversion des fichiers visio avec Aspose.Diagram.
---
## **Scénarios d'utilisation possibles**

Parfois, la conversion de gros fichiers visio peut prendre un certain temps. Pendant ce temps, vous souhaiterez peut-être afficher la progression de la conversion du document au lieu d'un simple écran de chargement pour améliorer la convivialité de votre application. Aspose.Diagram prend en charge le processus de conversion de documents de suivi en fournissant l'interface IPageSavingCallback. L'interface IPageSavingCallback fournit les méthodes PageStartSaving et PageEndSaving que vous pouvez implémenter dans votre classe personnalisée. Vous pouvez également contrôler quelles pages sont rendues comme indiqué dans le T*estDiagramPageSavingCallback*classe personnalisée.

## **Suivre la progression de la conversion des documents**

 L'exemple de code suivant charge le[fichier source visio](Drawing1.vsdx) et imprime sa progression de conversion dans la console en utilisant le*TestPageSavingCallback*classe personnalisée qui implémente l'interface IPageSavingCallback.

## **Exemple de code**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

Voici le code pour le*TestDiagramPageSavingCallback*classe personnalisée.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

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
