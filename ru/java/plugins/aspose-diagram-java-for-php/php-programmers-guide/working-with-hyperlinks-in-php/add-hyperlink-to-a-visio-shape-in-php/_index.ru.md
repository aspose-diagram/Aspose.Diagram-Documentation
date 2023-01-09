---
title: Добавить гиперссылку в форму Visio в PHP
type: docs
weight: 10
url: /ru/java/add-hyperlink-to-a-visio-shape-in-php/
---
## **Aspose.Diagram - Добавить гиперссылку**
 Чтобы добавить гиперссылку с помощью**Aspose.Diagram Java для PHP** , просто вызовите**аддгиперссылкатошапе** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Добавить гиперссылку в форму Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
