---
title: Agregar elemento de ventana a la instancia Visio en Ruby
type: docs
weight: 20
url: /es/java/add-window-element-to-the-visio-instance-in-ruby/
---
## **Aspose.Diagram - Agregar elemento de ventana a la instancia Visio**
 Para agregar un elemento de ventana a la instancia Visio mediante**Aspose.Diagram Java para rubí** , simplemente invocar**AgregarElementoDeVentana** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize window object

window = Rjb::import('com.aspose.diagram.Window').new

\# set window state

window.setWindowState(Rjb::import('com.aspose.diagram.WindowStateValue').MAXIMIZED)

\# set window height

window.setWindowHeight(500)

\# set window width

window.setWindowWidth(500)

\# set window type

window.setWindowType(Rjb::import('com.aspose.diagram.WindowTypeValue').STENCIL)

\# add window object

diagram.getWindows().add(window)

\# save in any supported format

diagram.save(data_dir + "AddWindowElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added window element to the visio instance."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar elemento de ventana a la instancia Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
