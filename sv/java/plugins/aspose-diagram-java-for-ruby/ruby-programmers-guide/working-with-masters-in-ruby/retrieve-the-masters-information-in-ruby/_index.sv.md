---
title: Hämta Masters Information i Ruby
type: docs
weight: 30
url: /sv/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Hämta Masters Information**
 För att hämta Masters Information med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetMasterInfo** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Ring diagram-konstruktören för att ladda diagram från en VSD-fil

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

masters = diagram.getMasters()

i = 0

 medan jag< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Masters Information (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
