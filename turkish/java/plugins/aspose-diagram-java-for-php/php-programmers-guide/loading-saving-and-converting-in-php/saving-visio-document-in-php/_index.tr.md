---
title: Visio Belgesini PHP'ye Kaydetme
type: docs
weight: 100
url: /tr/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Visio Belgesi kaydediliyor**
 Kaydetmek için Visio Belgeyi kullanarak**PHP için Aspose.Diagram Java**, aşağıdaki kodu kullanabilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i XPS'ye (Aspose.Diagram) aktar**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
