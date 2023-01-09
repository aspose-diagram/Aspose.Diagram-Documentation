---
title: PHP'de Visio Çiziminden Pencere Öğelerini Alın
type: docs
weight: 30
url: /tr/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Visio Çiziminden Pencere Öğelerini Al**
 Kullanarak Visio Çiziminden Pencere Elemanlarını Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**GetWindowElements** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden Pencere Elemanlarını Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
