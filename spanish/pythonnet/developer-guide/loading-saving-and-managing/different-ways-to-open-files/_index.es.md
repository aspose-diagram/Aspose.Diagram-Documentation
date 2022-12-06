---
title: Diferentes formas de abrir archivos
type: docs
weight: 10
url: /es/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Con Aspose.Diagram es sencillo abrir archivos, por ejemplo, para recuperar datos o utilizar una plantilla de diseñador para acelerar el proceso de desarrollo.

{{% /alert %}}

## **Abrir un archivo a través de una ruta**

 Los desarrolladores pueden abrir un archivo Microsoft Diagram usando su ruta de archivo en la computadora local especificándolo en el**Diagram**constructor de clases. Simplemente pase la ruta en el constructor como un*cuerda*. Aspose.Diagram detectará automáticamente el tipo de formato de archivo.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Abrir un archivo a través de una secuencia**

 También es sencillo abrir un archivo Visio como flujo. Para hacerlo, use una versión sobrecargada del constructor que toma el*BufferStream*objeto que contiene el archivo.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Abrir un archivo con LoadOptions**

 Para abrir un archivo con opciones de carga, use el**Opciones de carga**clases para configurar las opciones relacionadas de las clases para que se cargue el archivo de plantilla.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

