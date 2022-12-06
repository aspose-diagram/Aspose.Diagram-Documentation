---
title: Récupérer les informations de master en PHP
type: docs
weight: 30
url: /fr/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Récupérer les informations du Master**
 Pour récupérer les informations sur les masters à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**GetMasterInfo** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations sur les maîtres (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
