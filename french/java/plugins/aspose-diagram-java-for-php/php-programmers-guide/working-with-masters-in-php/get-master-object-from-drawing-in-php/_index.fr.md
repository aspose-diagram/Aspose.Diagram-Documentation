---
title: Obtenir l'objet principal du dessin en PHP
type: docs
weight: 20
url: /fr/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Obtention d'un objet principal par ID**
 Pour obtenir un objet principal par ID à l'aide de**Aspose.Diagram Java pour PHP** , appel**get_master_object_by_id** méthode de**GetMasterObject** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Obtention d'un objet principal par nom**
 Pour obtenir un objet principal par nom à l'aide**Aspose.Diagram Java pour PHP** , appel**get_master_object_by_name** méthode de**GetMasterObject** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Obtenir l'objet principal du dessin (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
