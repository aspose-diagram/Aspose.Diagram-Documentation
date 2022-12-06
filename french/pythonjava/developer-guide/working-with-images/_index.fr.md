---
title: Travailler avec des images
type: docs
weight: 70
url: /fr/python-java/working-with-images/
description: Cette page décrit comment extraire, remplacer ou insérer une image d'une page du dessin Visio avec la bibliothèque Aspose.Diagram.
---
## **Extraire toutes les images d'une page Visio**
 Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Vous pouvez extraire des images d'une page particulière de[un dossier Visio](ExtractAllImagesFromPage.vsd).
### **Extraire des images**
L'objet Page Class représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Shapes exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Shape. Cette propriété peut être utilisée pour extraire toutes les images d'une page particulière.
#### **Exemple de programmation d'extraction d'images**
Le morceau de code suivant extrait toutes les images d'une page Visio particulière.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ExtractAllImagesFromPage.py" >}}
## **Obtenez des icônes de diverses formes Visio**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio formes](Timeline.vss). 
### **Obtenir l'icône de forme**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram ou un gabarit existant.
1. Obtenir le maître par son index
1. Obtenir l'icône principale.
1. Enregistrer l'icône dans l'espace local.
#### **Obtenir un exemple de programmation d'icônes**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-GetShapeIcon.py" >}}
## **Remplacer une forme d'image du Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [le Visio diagram](ExtractAllImagesFromPage.vsd).
### **Remplacement d'une forme d'image**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram existant.
1. Parcourez les formes de page sélectives.
1. Appliquer le filtre pour obtenir des formes d'image.
1. Enregistrez le résultat Visio diagram dans l'espace local.
#### **Remplacer un exemple de programmation de forme d'image**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ReplaceShapePicture.py" >}}
## **Importer l'image en tant que forme Visio**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Insérer une image dans Visio**
Le code dans les exemples ci-dessous montre comment :

1. Créez un diagram.
1. Obtenir la page Visio
1. Importer une image en tant que forme Visio
1. Enregistrez le diagram.
#### **Insérer un exemple de programmation d'image**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-InsertImageInVisio.py" >}}
