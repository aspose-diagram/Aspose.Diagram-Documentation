---
title: Création, mise en page et ajustement automatique des formes
type: docs
weight: 10
url: /fr/python-java/create-layout-and-auto-fit-shapes/
---
## **Création d'un Diagram**
Aspose.Diagram for Python via Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [ajouter des formes et des connecteurs](/diagram/fr/python-java/add-and-connect-visio-shapes/) pour construire le diagram. Utilisez le constructeur par défaut de la classe Diagram pour créer un nouveau diagram.
### **Exemple de programmation**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-CreateDiagram.py" >}}
## **Formes de mise en page dans le style d'organigramme**
 Avec certains types de dessins connectés, tels que les organigrammes et les schémas de réseau, vous pouvez utiliser le**Formes de mise en page** fonctionnalité pour positionner automatiquement les formes. Le positionnement automatique est plus rapide que le déplacement manuel de chaque forme vers un nouvel emplacement.

Par exemple, si vous mettez à jour un organigramme volumineux pour inclure un nouveau processus, vous pouvez ajouter et connecter les formes qui composent le processus, puis utiliser la fonctionnalité de mise en page pour mettre automatiquement en page le dessin mis à jour.

La méthode Layout, exposée par la classe Diagram, met en page les formes et/ou redirige les connecteurs sur toutes les pages du diagram. Cette méthode accepte un objet LayoutOptions comme argument. Utilisez les différentes propriétés exposées par la classe LayoutOptions pour disposer automatiquement les formes.

L'image ci-dessous montre le diagram chargé par les extraits de code de cet article, avant l'application de la mise en page automatique. Les extraits de code montrent comment appliquer des dispositions d'organigramme et des dispositions d'arborescence compactes.

**La source diagram.** 

![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_1.png)

Les extraits de code de cet article prennent la source diagram et lui appliquent plusieurs types de mise en page automatique, en enregistrant chacun dans un fichier séparé.

|<p>**Disposition des formes de bas en haut** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Disposition des formes de haut en bas** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Formes de mise en page de gauche à droite** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Formes de mise en page de droite à gauche** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_5.png)</p>|
Pour mettre en forme des formes dans un style d'organigramme :

1. Créez une instance de la classe Diagram.
1. Créez une instance de la classe LayoutOptions et définissez les propriétés liées au style Flowchart.
1. Appelez la méthode Layout de la classe Diagram en passant LayoutOptions.
1. Appelez la méthode Save de la classe Diagram pour écrire le dessin Visio.
### **Exemple de programmation de style organigramme**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInFlowchartStyle.py" >}}
### **Disposition des formes dans le style d'arbre compact**
Le style d'arborescence compacte essaie de construire une structure arborescente. Il utilise le même fichier d'entrée que l'exemple ci-dessus et enregistre dans plusieurs styles d'arbres compacts différents.

|<p>**Arborescence compacte - vers le bas et vers la droite** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Arborescence compacte - vers le bas et vers la gauche** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Arborescence compacte - droite et bas** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Arborescence compacte - gauche et bas** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Pour disposer des formes dans le style d'arborescence compacte :

1. Créez une instance de la classe Diagram.
1. Créez une instance de la classe LayoutOptions et définissez les propriétés de style d'arborescence compacte.
1. Appelez la méthode Layout de la classe Diagram en passant LayoutOptions.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier Visio.
#### **Exemple de programmation de style d'arborescence compacte**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInCompactTreeStyle.py" >}}
## **Ajustement automatique du Visio Diagram**
Aspose.Diagram API prend en charge l'ajustement automatique du dessin Visio. Cette opération de fonctionnalité permet d'amener des formes extérieures à l'intérieur de la limite de page Visio.

Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing. The DiagramSaveOptions class exposes AutoFitPageToDrawingContent property to auto fit the Visio drawing.

Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Créez un objet de la classe DiagramSaveOptions et transmettez le format de fichier résultant.
1. Définissez la propriété AutoFitPageToDrawingContent de l'objet DiagramSaveOptions.
1. Appelez la méthode Save de l'objet de classe Diagram et transmettez également le chemin d'accès complet au fichier et l'objet DiagramSaveOptions.
### **Exemple de programmation d'ajustement automatique**
L'exemple de code suivant montre comment ajuster automatiquement les formes dans le Visio diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-AutoFitShapesInVisio.py" >}}
## **Travailler avec le projet VBA**
### **Modifier le code du module VBA dans Visio Diagram**
This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for Python via Java.

Nous avons ajouté les classes VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference et VbaProjectReferenceCollection. Ces classes aident à prendre le contrôle du projet VBA. Les développeurs peuvent extraire et modifier le code du module VBA.
### **Modifier l'exemple de programmation de code de module VBA**
Veuillez vérifier cet exemple de code :

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-ModifyVBAModuleCode.py" >}}
### **Supprimer toutes les macros du Visio Diagram**
Aspose.Diagram for Python via Java allows developers to remove all macros from the Visio diagram.

La propriété JavaProjectData, exposée par la classe Diagram, vous permet de supprimer toutes les macros du dessin Visio.
### **Exemple de programmation de suppression de toutes les macros**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-RemoveMacrosFromVisio.py" >}}
