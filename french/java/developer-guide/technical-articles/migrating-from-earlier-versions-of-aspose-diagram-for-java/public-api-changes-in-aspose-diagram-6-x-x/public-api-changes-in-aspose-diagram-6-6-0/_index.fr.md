---
title: Public API Changements dans Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /fr/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.3.0 à 6.6.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
### **Ajoute les formats VSDM, VSSM et VSTM dans la classe LoadFileFormat**
Cette version ajoute la prise en charge de la lecture des formats Visio prenant en charge les macros.
### **Ajoute les formats VSDM, VSSM et VSTM dans la classe SaveFileFormat**
Cette version ajoute la prise en charge de l'écriture de formats Visio prenant en charge les macros.
### **Modifier le code du module VBA dans Visio Diagram**
Nous avons ajouté les classes Vba, VbaProject et VbaModule. Ces classes aident à prendre le contrôle du projet VBA. À l'aide de cette nouvelle version 6.6.0 ou supérieure, les développeurs peuvent extraire et modifier le code du module VBA. Veuillez vérifier cet exemple de code :

**Java**

{{< highlight "java" >}}

 // charge un Visio diagram existant

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = nouveau Diagram (entrée);

// extrait le projet VBA

VbaProject v = diagram.getVbaProject();

// Itérer dans les modules et modifier le code de la macro VBA

pour (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Ajoute une méthode getImageData dans la classe ForeignData**
Il représente une image de l'objet ole sous la forme d'un tableau d'octets. Outre cela, nous avons également amélioré la manipulation des objets OLE. Les développeurs peuvent désormais également remplacer un objet OLE dans le Visio diagram. Veuillez vérifier cet exemple de code :

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
