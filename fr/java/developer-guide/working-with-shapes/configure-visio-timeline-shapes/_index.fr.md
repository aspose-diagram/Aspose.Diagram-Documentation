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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetMilestoneProps.class);  
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 22;
// Get timeline shape
Shape milestone = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set milestone date
milestoneHelper.setMilestoneDate(new DateTime(2014, 10, 21));
// Set date format
milestoneHelper.setDateFormat(21);
// Set auto update flag
milestoneHelper.setAutoUpdate(true);
// Set milestone type
milestoneHelper.setType(6);

// Save to VDX format
diagram.save(dataDir + "SetMilestoneProps_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureTimeLine.class); 
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
//timelineHelper.setDateFormatForBE(21);
// Set date format for intm of timeline shape   
//timelineHelper.setDateFormatForIntm(21);

// Or

// Set date format string for start and finish of timeline shape
timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");
// Set date format string for intm of timeline shape
timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

// Save to VDX format
diagram.save(dataDir + "ConfigureTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshTimeLine.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
timelineHelper.setDateFormatForBE(21);

//revive milestones on the timeline
timelineHelper.refreshTimeLine();

// Save to VDX format
diagram.save(dataDir + "RefreshTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshMilestoneWithMilestoneHelper.class);
        
String pageName = "Page-1";

////////////// Modify time line /////////// 
DateTime startDate = new DateTime(2015, 8, 1);
DateTime endDate = new DateTime(2016, 6, 1);
DateTime fisYear = startDate;

//Load a diagram 
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

//Get page
Page page = diagram.getPages().getPage(pageName);

long timelineId = 1;
Shape timeline = diagram.getPages().getPage(pageName).getShapes().getShape(timelineId);
double xpos = timeline.getXForm().getPinX().getValue();
double ypos = timeline.getXForm().getPinY().getValue();

// Add milestone 
String milestoneMasterName = "2 triangle milestone";

//Add Master
diagram.addMaster(dataDir + "Timeline.vss", milestoneMasterName);

//Add Shape in Visio diagram using AddShape method
long milestoneShapeId = diagram.addShape(xpos, ypos, milestoneMasterName, 0);

//Get the shape based on ID
Shape milestone = page.getShapes().getShape(milestoneShapeId);

//Instantiate MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

//Set Milestone Date
milestoneHelper.setMilestoneDate(new DateTime(2015, 8, 1));

//Set IsAutoUpdate to true
milestoneHelper.setAutoUpdate(true);

//RefreshMilesone of timeline shape
milestoneHelper.refreshMilestone(timeline);

//Save Visio file
diagram.save(dataDir + "RefreshMilestone_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

