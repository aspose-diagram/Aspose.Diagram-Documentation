---
title: Descargar y Configurar Aspose.Diagram en PHP
type: docs
weight: 10
url: /es/java/download-and-configure-aspose-diagram-in-php/
---
## **Descargar bibliotecas requeridas**
Descargue las bibliotecas necesarias que se mencionan a continuación. Estos son los necesarios para ejecutar Aspose.Diagram Java para ejemplos de Ruby.

- [Aspose.Diagram for Java Componente](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Descargar ejemplos de sitios de codificación social**
Las siguientes versiones de ejemplos en ejecución están disponibles para descargar en los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Instalando**
Es muy simple y fácil de instalar Aspose.Diagram Java para PHP, siga las instrucciones:

Ejecute el siguiente comando.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Usando**
Incluya los archivos necesarios para exportar el dibujo visio a un documento PDF.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Entendamos el código anterior.

1. La primera línea se asegura de que el Aspose.Diagram esté cargado y disponible.
1. Incluya los archivos que se requieren para acceder al Aspose.Diagram
1. Inicializar las bibliotecas. Las clases aspose Java se cargan desde la ruta proporcionada en el archivo aspose.yml
