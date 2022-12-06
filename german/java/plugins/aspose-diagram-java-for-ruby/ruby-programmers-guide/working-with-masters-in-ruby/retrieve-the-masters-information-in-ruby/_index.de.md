---
title: Rufen Sie die Master-Informationen in Ruby ab
type: docs
weight: 30
url: /de/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Rufen Sie die Masterinformationen ab**
 So rufen Sie die Masters-Informationen ab**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetMasterInfo** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Rufen Sie den diagram-Konstruktor auf, um diagram aus einer VSD-Datei zu laden

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Meister = diagram.getMasters()

ich = 0

 während ich< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen der Masterinformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
