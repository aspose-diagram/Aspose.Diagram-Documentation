---
title: PHP'de boş bir Visio Diagram oluşturun
type: docs
weight: 20
url: /tr/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Boş bir Visio Diagram oluştur**
 Kullanarak boş bir Visio Diagram oluşturmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**Diyagram Oluştur** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Boş bir Visio Diagram (Aspose.Diagram) oluşturun**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
