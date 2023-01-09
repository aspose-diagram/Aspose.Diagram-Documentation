---
title: Ajouter un lien hypertexte à une forme Visio en PHP
type: docs
weight: 10
url: /fr/java/add-hyperlink-to-a-visio-shape-in-php/
---
## **Aspose.Diagram - Ajouter un lien hypertexte**
 Pour ajouter un lien hypertexte à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**Ajouter un lien hypertexte à la forme** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# Initialize Hyperlink object

$hyperlink = new Hyperlink();

\# Set address value

$hyperlink->getAddress()->setValue("http://www.google.com/");

\# Set sub address value

$hyperlink->getSubAddress()->setValue("Sub address here");

\# Set description value

$hyperlink->getDescription()->setValue("Description here");

\# Set name

$hyperlink->setName("MyHyperLink");

\# Add hyperlink to the shape

$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1)->getHyperlinks()->add($hyperlink);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "Hyperlinks.vdx", $saveFileFormat->VDX);

print "Added hyperlik to shape successfully!".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajouter un lien hypertexte à une forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
