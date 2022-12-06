---
title: Insertar una nueva página en blanco en un dibujo Visio en Ruby
type: docs
weight: 20
url: /es/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Insertar una nueva página en blanco en un dibujo Visio**
 Para insertar una nueva página en blanco en un dibujo Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**Añadir página** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def inicializar()

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

 Llame al constructor diagram para cargar diagram desde un archivo VSD

 diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

 # Obtener ID de página máxima

 máximo_página_identificación = obtener_máximo_página_id(diagram)

 # Inicializar un nuevo objeto de página

 nueva_pagina = Rjb::import('com.aspose.diagram.Page').nueva

 # Escoger un nombre

 new_page.setName("nueva página")



 # Establecer ID de página

 nuevo_página.setID(máx._id_página + 1)

 # O pruebe el constructor de página

 # Página nuevaPágina = nueva página(MaxPageId + 1);

 # Agregar una nueva página en blanco

 diagram.getPages().add(nueva_página)

 # Guardar diagram

 diagram.guardar(datos_dir + "Página Nueva_Salida.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 pone "Nueva página agregada".

final

definitivamente obtener_máximo_página_id(diagram)

máx = diagram.getPages().getPage(0).getID()

 yo = 1

 mientras yo< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Insertar una nueva página en blanco en un dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
