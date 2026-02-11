---
title: Création, mise en page et ajustement automatique des formes
type: docs
weight: 10
url: /fr/java/create-layout-and-auto-fit-shapes/
---
## **Création d'un Diagram**
 Aspose.Diagram for Java vous permet de lire et de créer des diagrammes Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation. La première étape lors de la création de nouveaux documents consiste à créer un diagram. Ensuite[ajouter des formes et des connecteurs](/diagram/fr/java/add-and-connect-visio-shapes/)pour construire le diagram. Utilisez le constructeur par défaut de[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe pour créer un nouveau diagram.
### **Exemple de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Formes de mise en page dans le style d'organigramme**
 Avec certains types de dessins connectés, tels que les organigrammes et les schémas de réseau, vous pouvez utiliser le**Formes de mise en page** fonctionnalité pour positionner automatiquement les formes. Le positionnement automatique est plus rapide que le déplacement manuel de chaque forme vers un nouvel emplacement.

Par exemple, si vous mettez à jour un organigramme volumineux pour inclure un nouveau processus, vous pouvez ajouter et connecter les formes qui composent le processus, puis utiliser la fonctionnalité de mise en page pour mettre automatiquement en page le dessin mis à jour.

 La méthode Layout, exposée par la[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe met en page les formes et/ou redirige les connecteurs sur toutes les pages du diagram. Cette méthode accepte un objet LayoutOptions comme argument. Utilisez les différentes propriétés exposées par la classe LayoutOptions pour disposer automatiquement les formes.

L'image ci-dessous montre le diagram chargé par les extraits de code de cet article, avant l'application de la mise en page automatique. Les extraits de code montrent comment postuler[mises en page d'organigramme](/diagram/fr/java/create-2c-layout-and-auto-fit-shapes/) et[arborescences compactes](/diagram/fr/java/create-2c-layout-and-auto-fit-shapes/).

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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Disposition des formes dans le style d'arbre compact**
 Le style d'arborescence compacte essaie de construire une structure arborescente. Il utilise le même fichier d'entrée que le[exemple ci-dessus](/diagram/fr/java/create-2c-layout-and-auto-fit-shapes/)et enregistre plusieurs styles d'arbres compacts différents.

|<p>**Arborescence compacte - vers le bas et vers la droite** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Arborescence compacte - vers le bas et vers la gauche** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Arborescence compacte - droite et bas** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Arborescence compacte - gauche et bas** </p><p>![tâche : image_autre_texte](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Pour disposer des formes dans le style d'arborescence compacte :

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classer.
1. Créez une instance de la classe LayoutOptions et définissez les propriétés de style d'arborescence compacte.
1. Appelez la méthode Layout de la classe Diagram en passant LayoutOptions.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier Visio.
#### **Exemple de programmation de style d'arborescence compacte**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Ajustement automatique du Visio Diagram**
Aspose.Diagram API prend en charge l'ajustement automatique du dessin Visio. Cette opération de fonctionnalité permet d'amener des formes extérieures à l'intérieur de la limite de page Visio.

Aspose.Diagram for Java API a la classe Diagram qui représente un dessin Visio. La classe DiagramSaveOptions expose la propriété AutoFitPageToDrawingContent pour ajuster automatiquement le dessin Visio.

Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Créez un objet de la classe DiagramSaveOptions et transmettez le format de fichier résultant.
1. Définissez la propriété AutoFitPageToDrawingContent de l'objet DiagramSaveOptions.
1. Appelez la méthode Save de l'objet de classe Diagram et transmettez également le chemin d'accès complet au fichier et l'objet DiagramSaveOptions.
### **Exemple de programmation d'ajustement automatique**
L'exemple de code suivant montre comment ajuster automatiquement les formes dans le Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}
```
## **Travailler avec le projet VBA**
### **Modifier le code du module VBA dans Visio Diagram**
Cet article montre comment modifier automatiquement un code de module VBA à l'aide de Aspose.Diagram for Java.

Nous avons ajouté les classes VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference et VbaProjectReferenceCollection. Ces classes aident à prendre le contrôle du projet VBA. Les développeurs peuvent extraire et modifier le code du module VBA.
### **Modifier l'exemple de programmation de code de module VBA**
Veuillez vérifier cet exemple de code :

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Supprimer toutes les macros du Visio Diagram**
Aspose.Diagram for Java permet aux développeurs de supprimer toutes les macros du Visio diagram.

La propriété JavaProjectData, exposée par le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe, vous permet de supprimer toutes les macros du dessin Visio.
### **Exemple de programmation de suppression de toutes les macros**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
