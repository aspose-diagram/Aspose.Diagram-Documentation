---
title: Infoga en ny tom sida i en Visio-ritning i Ruby
type: docs
weight: 20
url: /sv/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Infoga en ny tom sida i en Visio ritning**
 För att infoga en ny tom sida i en Visio-ritning med**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**AddPage** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 def initialize()

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

 Ring diagram-konstruktören för att ladda diagram från en VSD-fil

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # Få max sid-ID

 max_sida_id = få_max_page_id(diagram)

 # Initiera ett nytt sidobjekt

 new_page = Rjb::import('com.aspose.diagram.Page').new

 # Ange namn

 new_page.setName("ny sida")



 # Ställ in sid-ID

 ny_page.setID(max_page_id + 1)

 # Eller prova sidkonstruktorn

 # Page newPage = new Page(MaxPageId + 1);

 # Lägg till en ny tom sida

 diagram.getPages().add(new_page)

 # Spara diagram

 diagram.save(data_dir + "Ny sida_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 sätter "Ladd till ny sida."

slutet

def få_max_page_id(diagram)

max = diagram.getPages().getPage(0).getID()

 i = 1

 medan jag< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Infoga en ny tom sida i en Visio-ritning (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
