---
title: Rufen Sie Visio-Konnektorinformationen in Ruby ab
type: docs
weight: 20
url: /de/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Abrufen von Visio-Verbindungsinformationen**
 Abrufen von Visio Connector-Informationen mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetConnectorsInfo** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

Konnektoren = diagram.getPages().getPage(0).getConnects()

ich = 0

 während ich< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen von Visio-Verbindungsinformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

