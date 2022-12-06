---
title: Configurer les formes de la ligne de temps Visio
type: docs
weight: 20
url: /fr/java/configure-visio-timeline-shapes/
---
## **Définir les propriétés de la forme du jalon**
Aspose.Diagram permet aux développeurs de définir des propriétés de jalon. Cet article explique comment définir la date du jalon, le format de la date, l'indicateur et le type de mise à jour automatique.
### **Définition de la date d'étape, du format de date, de l'indicateur et du type de mise à jour automatique**
 La[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)la classe prend un[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) objet lors de l'initialisation de[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) objet. L'exemple de code de cet article définit la date du jalon, le format de la date, l'indicateur de mise à jour automatique et les propriétés du type de jalon.

|<p>**Le jalon avant la mise à jour** </p><p>![tâche : image_autre_texte](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**Le jalon après la mise à jour. Notez le format de date modifié.** </p><p>![tâche : image_autre_texte](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
Le processus de mise à jour de la date du jalon, du format de la date, de l'indicateur de mise à jour automatique et du type de jalon :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Initialisez l'objet MilestoneHelper.
1. Fixez une date jalon.
1. Définissez le format de la date du jalon.
1. Définissez un indicateur de mise à jour automatique.
1. Définir le type de jalon
1. Enregistrez le dessin Visio dans n'importe quel format pris en charge.
#### **Définir un exemple de programmation d'étape**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


Tableau des valeurs de format de date :

|**Évaluer**|**Formater la chaîne**|
|:- |:- |
|0|jjjj, aaaa-Mj|
|1|aaaa-MM-jj|
|2|aa-MMM-j|
|3|aaaa/M/j|
|4|aa-MMM.-j|
|5|j MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM j, aaaa|
|9|MMM j, aaaa|
|10|Mj-aa|
|11|Maryland|
|12|j MMMM, aaaa|
|13|j MMM, aaaa|
|14|jM-aa|
|15|dM|
|16|aa-Md|
|17|aaaa-Md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|aa|
|25|aaaa|
|26|ré|
|27|MMMM|
|28|MMM|
|29|M|
## **Définir la période et le format de date de la forme de la chronologie**
Aspose.Diagram permet aux développeurs de configurer la chronologie par programmation. Cela explique comment ajuster la période et le format de date des formes de chronologie (bloc, ligne, règle, divisé ou cylindrique).
### **Réglage de la période et du format de date**
 La[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)la classe prend un[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) objet lors de l'initialisation de[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) objet. L'exemple de code de cet article définit les valeurs de format de début, de fin et de date de la période.

|<p>**L'onglet Période de la boîte de dialogue Visio Configurer la chronologie** </p><p>![tâche : image_autre_texte](http://i.imgur.com/nHth3W8.png)</p>|<p>**L'onglet Format d'heure de la boîte de dialogue Visio Configurer la chronologie** </p><p>![tâche : image_autre_texte](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Entrée diagram** </p><p>![tâche : image_autre_texte](configure-visio-timeline-shapes_1.png)</p>|<p>**Le diagram après la modification des valeurs** </p><p>![tâche : image_autre_texte](configure-visio-timeline-shapes_2.png)</p>|
Le processus de mise à jour du format de début, de fin et de date de la période est :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Initialisez l'objet TimeLineHelper.
1. Définissez le début de la période.
1. Définissez la fin de la période.
1. Définissez un format de date.
1. Enregistrez le dessin Visio dans n'importe quel format pris en charge.
#### **Définir la période et la date Exemple de programmation**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


Tableau des valeurs de format de date :

|**Évaluer**|**Formater la chaîne**|
|:- |:- |
|0|jjjj, aaaa-Mj|
|1|aaaa-MM-jj|
|2|aa-MMM-j|
|3|aaaa/M/j|
|4|aa-MMM.-j|
|5|j MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM j, aaaa|
|9|MMM j, aaaa|
|10|Mj-aa|
|11|Maryland|
|12|j MMMM, aaaa|
|13|j MMM, aaaa|
|14|jM-aa|
|15|dM|
|16|aa-Md|
|17|aaaa-Md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|aa|
|25|aaaa|
|26|ré|
|27|MMMM|
|28|MMM|
|29|M|
## **Actualiser les jalons sur la chronologie en Visio**
Aspose.Diagram permet aux développeurs d'ajuster les jalons sur les formes de la chronologie (bloc, ligne, règle, divisé ou cylindrique) en fonction du changement de période.
### **Actualiser les jalons sur la chronologie à l'aide de la classe TimeLineHelper**
 La méthode RefreshTimeLine exposée par le[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) La classe peut être utilisée pour faire revivre des jalons sur la chronologie.

Le code ci-dessous montre comment :

1. charger un échantillon diagram.
1. obtenir une forme de chronologie.
1. initialiser l'objet TimeLineHelper.
1. définir le début de la période.
1. définir la fin de la période.
1. définir le format de la date (facultatif).
1. appelez la méthode RefreshTimeLine de l'objet TimeLineHelper.
1. enregistrer diagram
#### **Actualiser les jalons à l'aide de l'exemple de programmation TimeLineHelper**
Utilisez le code suivant dans votre application Java pour relancer les jalons sur la chronologie à l'aide de Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
### **Actualiser les jalons sur la chronologie à l'aide de la classe MilestoneHelper**
 La méthode RefreshMilestone exposée par le[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)class peut être utilisé pour actualiser les jalons sur la chronologie.

Le code ci-dessous montre comment :

1. charger un échantillon diagram.
1. obtenir une forme de chronologie.
1. ajouter Shape dans Visio diagram en utilisant la méthode AddShape.
1. initialiser l'objet MilestoneHelper.
1. définir la date d'étape.
1. définissez la propriété IsAutoUpdate de Milstone sur true.
1. appelez la méthode RefreshMilestone de l'objet MilestoneHelper.
1. enregistrer diagram
#### **Actualiser les jalons à l'aide de l'exemple de programmation MilestoneHelper**
Utilisez le code suivant dans votre application Java pour actualiser les jalons sur la chronologie à l'aide de Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}
