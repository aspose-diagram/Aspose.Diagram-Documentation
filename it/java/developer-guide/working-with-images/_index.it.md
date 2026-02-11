---
title: Lavorare con le immagini
type: docs
weight: 70
url: /it/java/working-with-images/
---
## **Estrai tutte le immagini da una pagina Visio**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. È possibile estrarre immagini da una particolare pagina di un file Visio.
### **Estrai immagini**
L'oggetto Page Class rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Shapes esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Shape. Questa proprietà può essere utilizzata per estrarre tutte le immagini da una determinata pagina.
#### **Estrarre le immagini di esempio di programmazione**
Il seguente pezzo di codice estrae tutte le immagini da una particolare pagina Visio.


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

## **Ottieni icone di varie forme Visio**
Aspose.Diagram for Java API ora consente agli sviluppatori di ottenere icone di varie Visio forme.
### **Ottenere l'icona della forma**
Il codice negli esempi seguenti mostra come:

1. Carica uno diagram o uno stencil esistente.
1. Ottieni master dal suo indice
1. Ottieni l'icona principale.
1. Salva l'icona nello spazio locale.
#### **Ottieni un esempio di programmazione delle icone**

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

## **Sostituire una forma immagine del Visio Diagram**
Aspose.Diagram for Java API consente agli sviluppatori di accedere e sostituire le forme immagine disponibili nel Visio diagram.
### **Sostituzione di una forma immagine**
Il codice negli esempi seguenti mostra come:

1. Carica un diagram esistente.
1. Scorri le forme di pagina selettive.
1. Applica il filtro per ottenere le forme dell'immagine.
1. Salva il risultante Visio diagram nello spazio locale.
#### **Sostituire un esempio di programmazione di Picture Shape**

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

## **Importa immagine bitmap come forma Visio**
Aspose.Diagram for Java API consente ora agli sviluppatori di importare un'immagine bitmap come forma Microsoft Visio.
### **Insert a BMP Image in Visio**
Il codice negli esempi seguenti mostra come:

1. Crea uno diagram.
1. Ottenere Visio pagina
1. Importa un'immagine bitmap come forma Visio
1. Salva lo diagram.
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

