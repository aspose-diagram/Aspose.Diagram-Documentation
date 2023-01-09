---
title: PHP'de Visio Çizimlere Yorum Ekleme
type: docs
weight: 10
url: /tr/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Visio Çizimlerine Yorum Ekle**
 Visio Çizimine Yorum Eklemek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**DiyagramaYorum Ekle** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çizimlere Yorum Ekle (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
