---
title: Su primera aplicación Aspose.Diagram - Hola mundo
type: docs
weight: 30
url: /es/python-java/your-first-aspose-diagram-application-hello-world/
description: Esta página describe cómo crear la primera aplicación con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

Este tutorial muestra cómo crear una primera aplicación (Hello World) usando Aspose.Diagram' simple API. Esta aplicación simple crea un archivo Microsoft Visio con el texto 'Hello World' en una página específica.

{{% /alert %}}

## **Creación de la aplicación Hello World**

Los pasos a continuación crean la aplicación Hello World usando el Aspose.Diagram API:

1. Cree una instancia de la clase Diagram.
1. Aplicar la licencia:
 1. Si ha comprado una licencia, use la licencia en su aplicación para obtener acceso a la funcionalidad completa de Aspose.Diagram
 1. Si está utilizando la versión de evaluación del componente (si está utilizando Aspose.Diagram sin licencia), omita este paso.
1. Cree un nuevo archivo Visio o abra un archivo Visio existente.
1. Crear un nuevo cuadro de texto.
1.  Inserta las palabras**Hola Mundo!** en un cuadro de texto.
1. Genere el archivo Microsoft Visio modificado.

La implementación de los pasos anteriores se demuestra en los siguientes ejemplos.

### **Ejemplo de código: crear un nuevo Diagram y escribir Hello World!**

El siguiente ejemplo abre un archivo de plantilla Microsoft Visio existente llamado "[Basic_Shapes.vss](Basic_Shapes.vss)", ingresa el texto "¡Hola mundo!" en la primera página y guarda el diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-CreatingHelloWorldVisioFile.py" >}}
