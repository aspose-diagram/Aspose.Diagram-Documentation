---
title: PHP'de Visio Çizimine Yeni Bir Boş Sayfa Ekleme
type: docs
weight: 20
url: /tr/java/insert-a-new-blank-page-into-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Visio Çizimine Yeni Bir Boş Sayfa Ekleyin**
 Kullanarak Visio Çizimine Yeni Bir Boş Sayfa Eklemek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Sayfa ekle** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Get max page ID

$max_page_id = $diagram->getPages()->getPage(0)->getID();

$i = 1;

while ($i<(int)(string)$diagram->getPages()->getCount()) {

if ($max_page_id<$diagram->getPages()->getPage($i)->getID()){

$max_page_id=$diagram->getPages()->getPage($i)->getID();

}

$i+=1;

}

\# Initialize a new page object

$new_page = new Page();

\# Set name

$new_page->setName("new page");

\# Set page ID

$new_page->setID((int)(string)$max_page_id+1);

\# Or try the Page constructor

\# Page newPage = new Page(MaxPageId + 1);

\# Add a new blank page

$diagram->getPages()->add($new_page);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."NewPage_Output.vdx", $saveFileFormat->VDX);

print "Added new page.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çizimine Yeni Bir Boş Sayfa Ekleme (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/AddPage.php)
