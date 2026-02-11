---
title: Travailler avec des images
type: docs
weight: 60
url: /fr/net/working-with-images/
description: Cette section explique comment insérer ou obtenir une image à partir d'une page visio avec Aspose.Diagram.
---
## **Extraire toutes les images d'une page Visio**
Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Vous pouvez extraire des images d'une page particulière d'un fichier Visio.
### **Extraire des images**
L'objet Page Class représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Shapes exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Shape. Cette propriété peut être utilisée pour extraire toutes les images d'une page particulière.
#### **Exemple de programmation d'extraction d'images**
Le morceau de code suivant extrait toutes les images d'une page Visio particulière.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}

## **Obtenez des icônes de diverses formes Visio**
Aspose.Diagram for .NET API permet désormais aux développeurs d'obtenir des icônes de différentes formes Visio.
### **Obtenir l'icône de forme**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram ou un gabarit existant.
1. Obtenir le maître par son index
1. Obtenir l'icône principale.
1. Enregistrer l'icône dans l'espace local.
#### **Obtenir un exemple de programmation d'icônes**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}

## **Remplacer une forme d'image du Visio Diagram**
Aspose.Diagram for .NET API permet aux développeurs d'accéder et de remplacer les formes d'image disponibles dans le Visio diagram.
### **Remplacement d'une forme d'image**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram existant.
1. Parcourez les formes de page sélectives.
1. Appliquer le filtre pour obtenir des formes d'image.
1. Enregistrez le résultat Visio diagram dans l'espace local.
#### **Remplacer un exemple de programmation de forme d'image**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Importer une image bitmap en tant que forme Visio**
Aspose.Diagram for .NET API permet désormais aux développeurs d'importer une image bitmap en tant que forme Microsoft Visio.
### **Insert a BMP Image in Visio**
Le code dans les exemples ci-dessous montre comment :

1. Créez un diagram.
1. Obtenir la page Visio
1. Importer une image bitmap en tant que forme Visio
1. Enregistrez le diagram.
#### **Insert a BMP Image Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Convertir la zone spécifiée de la page Visio en image**
Avec Aspose.Diagram for .NET API, les développeurs peuvent définir une zone avec des coordonnées XY, une largeur et une hauteur, puis convertir cette zone dans un format d'image pris en charge.
### **Convertir la zone de dessin Visio en image**
Le code dans les exemples ci-dessous montre comment :

1. Charger un dessin Visio existant
1. Définir la zone du rectangle
1. Convertir la zone spécifiée en image

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
