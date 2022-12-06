---
title: Ruby'de bir Visio Diagram'e Özel Stil Sayfası uygulayın
type: docs
weight: 10
url: /tr/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'e Özel Stil Sayfası Uygula**
 Kullanarak Visio Diagram'e Özel Stil Sayfası Uygulamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**UygulaCustomStyleSheet** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage(0).getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Visio Diagram'e (Aspose.Diagram) Özel Stil Sayfası Uygulayın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
