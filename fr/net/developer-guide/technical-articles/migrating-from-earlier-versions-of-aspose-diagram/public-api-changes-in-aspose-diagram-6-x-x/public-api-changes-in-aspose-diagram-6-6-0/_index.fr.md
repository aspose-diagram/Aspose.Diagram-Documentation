---
title: Public API Changements dans Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.3.0 à 6.6.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Ajoute les formats VSDM, VSSM et VSTM dans la classe LoadFileFormat**
Cette version ajoute la prise en charge de la lecture des formats Visio prenant en charge les macros.
## **Ajoute les formats VSDM, VSSM et VSTM dans la classe SaveFileFormat**
Cette version ajoute la prise en charge de l'écriture de formats Visio prenant en charge les macros.
## **Modifier le code du module VBA dans le Visio Diagram**
Nous avons ajouté les classes VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference et VbaProjectReferenceCollection. Ces classes aident à prendre le contrôle du projet VBA. À l'aide de cette nouvelle version 6.6.0 ou supérieure, les développeurs peuvent extraire et modifier le code du module VBA. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
## **Ajoute une propriété ImageData dans la classe ForeignData**
Il représente une image de l'objet ole sous la forme d'un tableau d'octets. Outre cela, nous avons également amélioré la manipulation des objets OLE. Les développeurs peuvent désormais également remplacer un objet OLE dans le Visio diagram. Veuillez vérifier cet exemple de code :

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Erreur lors du rendu de la macro 'code' : valeur non valide spécifiée pour le paramètre lang
