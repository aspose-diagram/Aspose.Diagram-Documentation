---
title: Inserisci una nuova pagina vuota in un disegno Visio in Ruby
type: docs
weight: 20
url: /it/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Inserimento di una nuova pagina vuota in un disegno Visio**
 Per inserire una nuova pagina vuota in un disegno Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Aggiungi pagina** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 def inizializza()

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

 Chiama il costruttore diagram per caricare diagram da un file VSD

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # Ottieni l'ID pagina massimo

 max_pagina_id = ottieni_max_id_pagina(diagram)

 # Inizializza un nuovo oggetto pagina

 new_page = Rjb::import('com.aspose.diagram.Page').new

 # Imposta nome

 new_page.setName("nuova pagina")



 # Imposta ID pagina

 nuovo_page.setID(max_id_pagina + 1)

 # Oppure prova il costruttore di pagine

 # Pagina newPage = new Page(MaxPageId + 1);

 # Aggiungi una nuova pagina vuota

 diagram.getPages().add(nuova_pagina)

 #Salva diagram

 diagram.save(data_dir + "NuovaPagina_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 mette "Aggiunta nuova pagina".

fine

sicuramente ottenere_max_id_pagina(diagram)

max = diagram.getPages().getPage(0).getID()

 io = 1

 mentre io< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Inserisci una nuova pagina vuota in un disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
