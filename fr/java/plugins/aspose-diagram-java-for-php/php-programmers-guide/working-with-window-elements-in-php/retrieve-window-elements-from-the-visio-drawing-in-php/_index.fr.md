---
title: Récupérer les éléments de fenêtre du dessin Visio en PHP
type: docs
weight: 30
url: /fr/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Récupérer les éléments de fenêtre du dessin Visio**
 Pour récupérer des éléments de fenêtre à partir du dessin Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**GetWindowElements** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$windows=$diagram->getWindows();

$i = 0;

while ($i<(int)(string)$windows->getCount()) {

$window=$windows->get($i);

print "ID: ".(string)$window->getID();

print "Type: ".(string)$window->getWindowType();

print "Window height: ".(string)$window->getWindowHeight();

print "Window width: ".(string)$window->getWindowWidth();

print"Window state: ".(string)$window->getWindowState();

$i+= 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer des éléments de fenêtre à partir du dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
