---
title: Introduction
type: docs
weight: 10
url: /fr/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio enregistre des informations sur les actions entreprises sur un diagram dans le fichier. Par exemple, l'heure et la date de création du document, la dernière fois qu'il a été modifié, imprimé ou enregistré, sont enregistrées avec le fichier. Les informations sur la version de Microsoft Visio créée et la dernière modification du fichier sont également enregistrées.

Cet article explique comment récupérer ces informations.

{{% /alert %}} 
## **Obtenir la version de la bibliothèque Aspose.Diagram for Java**
 La méthode getVersion() exposée par le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) classe et la méthode getBuildNumberCreated() exposées par la[Propriétés du document](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class sont utilisés pour déterminer la version et le numéro de build complet de l'instance Microsoft Visio utilisée pour créer le document.
### **Détermination de la version de Microsoft Visio qui a créé, modifié et enregistré un document**
 La méthode getBuildNumberEdited() exposée par le[Propriétés du document](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) La classe est utilisée pour déterminer le numéro de version complet de l'instance Microsoft Visio utilisée pour modifier le document.

Les méthodes getTimeCreated(), getTimeEdited(), getTimePrinted() et getTimeSaved() exposées par le[Propriétés du document](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) classe sont utilisées pour déterminer l'heure à laquelle le document Microsoft Visio a été créé, modifié pour la dernière fois, imprimé pour la dernière fois et enregistré pour la dernière fois.

Vous pouvez également définir ces propriétés pour modifier les informations du fichier.

Les exemples de code ci-dessous montrent comment récupérer des informations sur la création du fichier ainsi que sur la date de création, de modification, d'impression et d'enregistrement.

**La sortie du code dans une fenêtre de console** 

![tâche : image_autre_texte](introduction_1.png)
#### **Exemple de programmation**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetLibraryVersion.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(path);

//Display Visio version and document modification time at different stages
System.out.println("Visio Instance Version : " + diagram.getVersion());
System.out.println("Full Build Number Created : " + diagram.getDocumentProps().getBuildNumberCreated());
System.out.println("Full Build Number Edited : " + diagram.getDocumentProps().getBuildNumberEdited());
System.out.println("Date Created : " + diagram.getDocumentProps().getTimeCreated());
System.out.println("Date Last Edited : " + diagram.getDocumentProps().getTimeEdited());
System.out.println("Date Last Printed : " + diagram.getDocumentProps().getTimePrinted());
System.out.println("Date Last Saved : " + diagram.getDocumentProps().getTimeSaved());

{{< /highlight >}}

## **Rédaction Microsoft Visio Résumé du document Info**
Microsoft Visio vous permet de définir un certain nombre de propriétés d'informations de résumé de document pour vous aider, vous et vos collègues, à identifier un diagram. Les propriétés de résumé, par exemple le titre, le sujet, l'auteur et la description, rendent le fichier plus facile à trouver lors de la recherche et plus facile à reconnaître lors de la navigation des dossiers.

 La[Propriétés du document](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)La classe expose un certain nombre de propriétés pour définir ou obtenir les informations récapitulatives d'un Microsoft Visio diagram. Aspose.Diagram for Java peut mettre à jour les informations récapitulatives du dessin, puis réécrire le fichier de dessin dans VDX.

{{% alert color="primary" %}} 

Veuillez noter que vous ne pouvez pas définir de valeurs par rapport au**Application**et**Producteur**champs, car Aspose Ltd. et Aspose.Diagram for Java xxx seront affichés contre ces champs.

{{% /alert %}} 
### **Rédaction Microsoft Visio Résumé du document Info**
Pour mettre à jour les informations récapitulatives du dessin d'un fichier VDX ou VSD existant :

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) classer.
1. Définissez les propriétés exposées par la méthode Diagram.getDocumentProps() pour définir les informations récapitulatives du fichier de dessin Visio.
1. Appelez la méthode save() de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

Vérifiez les informations récapitulatives :

1. Ouvrez le fichier de sortie VDX dans Microsoft Visio.
1.  Sélection**Info** du**Dossier** menu.

**La boîte de dialogue Info affichant les informations récapitulatives mises à jour** 

![tâche : image_autre_texte](introduction_2.png)
#### **Exemple de programmation**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioProperties.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(path);

//Set some summary information about the diagram
diagram.getDocumentProps().setCreator("Ijaz");
diagram.getDocumentProps().setCompany("Aspose");
diagram.getDocumentProps().setCategory("Drawing 2D");
diagram.getDocumentProps().setManager("Sergey Polshkov");
diagram.getDocumentProps().setTitle("Aspose Title");
diagram.getDocumentProps().setTimeCreated(DateTime.getNow());
diagram.getDocumentProps().setSubject("Visio Diagram");
diagram.getDocumentProps().setTemplate("Aspose Template");

//Write the updated file to the disk in VSDX file format
diagram.save(dataDir + "SetVisioProperties_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Détecter le format d'un fichier Visio**
 Utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, les développeurs peuvent détecter le format du fichier Visio avant de l'ouvrir car l'extension de fichier ne garantit pas que le contenu du fichier est approprié.
### **Détecter l'échantillon de programmation de format**
L'exemple de code suivant montre comment détecter un format de fichier (à l'aide du chemin d'accès au fichier ou du flux) et vérifier son extension.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectVisioFileFormat.class);

		// detect file format using the direct file path
		FileFormatInfo info = FileFormatUtil.detectFileFormat(dataDir + "Drawing1.vsdx");

		// get the detected file format
		System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

## **Détecter le format d'un fichier Visio à partir d'un InputStream**
À l'aide de Aspose.Diagram for Java API, les développeurs peuvent détecter le format d'un fichier Visio en transmettant un flux d'entrée. La méthode detectFileFormat de la classe FileFormatUtil peut être utilisée pour y parvenir.
### **Détecter le format à partir d'un exemple de programmation InputStream**
L'exemple de code suivant montre comment détecter un format de fichier à l'aide d'un flux d'entrée.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

