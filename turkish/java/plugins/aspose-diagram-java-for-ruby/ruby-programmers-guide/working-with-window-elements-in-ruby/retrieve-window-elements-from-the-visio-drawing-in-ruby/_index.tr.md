---
title: Ruby'de Visio Çiziminden Pencere Öğelerini Alın
type: docs
weight: 30
url: /tr/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Visio Çiziminden Pencere Öğelerini Al**
 Kullanarak Visio Çiziminden Pencere Elemanlarını Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetWindowElements** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

pencereler = diagram.getWindows()

ben = 0

 ben iken< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden Pencere Elemanlarını Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
