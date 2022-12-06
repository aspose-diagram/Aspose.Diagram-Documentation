---
title: Recuperar información de conectores Visio en Ruby
type: docs
weight: 20
url: /es/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Recuperar Visio Información de conectores**
 Para recuperar información de conectores Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**Obtener Información de Conectores** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

conectores = diagram.getPages().getPage(0).getConnects()

yo = 0

 mientras yo< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar información de conectores Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

