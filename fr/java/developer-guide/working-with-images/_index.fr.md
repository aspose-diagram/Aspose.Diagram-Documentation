---
title: Travailler avec des images
type: docs
weight: 70
url: /fr/java/working-with-images/
---
## **Extraire toutes les images d'une page Visio**
Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Vous pouvez extraire des images d'une page particulière d'un fichier Visio.
### **Extraire des images**
L'objet Page Class représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Shapes exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Shape. Cette propriété peut être utilisée pour extraire toutes les images d'une page particulière.
#### **Exemple de programmation d'extraction d'images**
Le morceau de code suivant extrait toutes les images d'une page Visio particulière.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}

## **Obtenez des icônes de diverses formes Visio**
Aspose.Diagram for Java API permet désormais aux développeurs d'obtenir des icônes de différentes formes Visio.
### **Obtenir l'icône de forme**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram ou un gabarit existant.
1. Obtenir le maître par son index
1. Obtenir l'icône principale.
1. Enregistrer l'icône dans l'espace local.
#### **Obtenir un exemple de programmation d'icônes**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}

## **Remplacer une forme d'image du Visio Diagram**
Aspose.Diagram for Java API permet aux développeurs d'accéder et de remplacer les formes d'image disponibles dans le Visio diagram.
### **Remplacement d'une forme d'image**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram existant.
1. Parcourez les formes de page sélectives.
1. Appliquer le filtre pour obtenir des formes d'image.
1. Enregistrez le résultat Visio diagram dans l'espace local.
#### **Remplacer un exemple de programmation de forme d'image**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Importer une image bitmap en tant que forme Visio**
Aspose.Diagram for Java API permet désormais aux développeurs d'importer une image bitmap en tant que forme Microsoft Visio.
### **Insert a BMP Image in Visio**
Le code dans les exemples ci-dessous montre comment :

1. Créez un diagram.
1. Obtenir la page Visio
1. Importer une image bitmap en tant que forme Visio
1. Enregistrez le diagram.
#### **Insert a BMP Image Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}

