---
title: PHP'de Diyagramları Koruma ve Korumayı Kaldırma
type: docs
weight: 20
url: /tr/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram - Diyagramları Koru ve Korumayı Kaldır**
 kullanarak Diyagramları Korumak ve Korumayı Kaldırmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**Korumayı Kaldırma Diyagramı** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vsd");

$diagram->getDocumentSettings()->setProtectBkgnds(1);

$diagram->getDocumentSettings()->setProtectMasters(1);

$diagram->getDocumentSettings()->setProtectShapes(1);

$diagram->getDocumentSettings()->setProtectStyles(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectDiagram.vdx", $saveFileFormat->VDX);

print "Applied protection on diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Diyagramları Koru ve Korumayı Kaldır (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
