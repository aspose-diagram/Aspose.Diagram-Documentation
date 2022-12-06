---
title: Recupera le informazioni sui master in Ruby
type: docs
weight: 30
url: /it/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Recuperare le Informazioni sui Maestri**
 Per recuperare le informazioni sui master utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetMasterInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Chiama il costruttore diagram per caricare diagram da un file VSD

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

master = diagram.getMasters()

io = 0

 mentre io< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera le informazioni sui master (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
