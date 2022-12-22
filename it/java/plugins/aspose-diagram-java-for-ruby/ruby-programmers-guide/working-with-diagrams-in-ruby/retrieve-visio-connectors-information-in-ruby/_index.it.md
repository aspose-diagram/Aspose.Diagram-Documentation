---
title: Recupera le informazioni sui connettori Visio in Ruby
type: docs
weight: 20
url: /it/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Recupera Visio Informazioni sui connettori**
 Per recuperare le informazioni sui connettori Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetConnectorsInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

connettori = diagram.getPages().getPage(0).getConnects()

io = 0

 mentre io< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera le informazioni sui connettori Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

