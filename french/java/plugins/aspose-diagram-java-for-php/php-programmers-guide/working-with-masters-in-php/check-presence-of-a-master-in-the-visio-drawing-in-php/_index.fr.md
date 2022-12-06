---
title: Vérifier la présence d'un maître dans le dessin Visio en PHP
type: docs
weight: 10
url: /fr/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Vérification de la présence d'un maître par ID**
 Pour vérifier la présence d'un maître par ID à l'aide de**Aspose.Diagram Java pour PHP** , appel**check_presence_master_by_id** méthode de**CheckPresenceOfMaster** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Vérification de la présence d'un maître par son nom**
 Pour vérifier la présence d'un maître par son nom à l'aide**Aspose.Diagram Java pour PHP** , appel**check_presence_master_by_name** méthode de**CheckPresenceOfMaster** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# check master object by name

$is_present = $diagram->getMasters()->isExist($master_name);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Vérifier la présence d'un maître dans le dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
