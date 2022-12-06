---
title: Recuperar la información de los maestros en Ruby
type: docs
weight: 30
url: /es/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Recuperar la información de los maestros**
 Para recuperar la información maestra usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerInfoMaestra** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Llame al constructor diagram para cargar diagram desde un archivo VSD

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

maestros = diagram.getMasters()

yo = 0

 mientras yo< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar la información de los maestros (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
