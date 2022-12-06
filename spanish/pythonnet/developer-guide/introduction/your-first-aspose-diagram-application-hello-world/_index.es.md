---
title: Su primera aplicación Aspose.Diagram - Hola mundo
type: docs
weight: 30
url: /es/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

Este tema para principiantes muestra cómo los desarrolladores pueden crear una primera aplicación simple (Hello World) usando Aspose.Diagram' simple API. La aplicación crea un archivo Microsoft Visio con las palabras Hello World en la página.

{{% /alert %}}

### **Creación de la aplicación Hello World**

Para crear la aplicación Hello World usando Aspose.Diagram API:

1. Cree una instancia de la clase Workbook.
1. Aplicar la licencia:
 1. Si ha comprado una licencia, use la licencia en su aplicación para obtener acceso a la funcionalidad completa de Aspose.Diagram
 1. Si está utilizando la versión de evaluación del componente (si está utilizando Aspose.Diagram sin licencia), omita este paso.
1. Cree un nuevo archivo Microsoft Visio o abra un archivo existente en el que desee agregar/actualizar algún texto.
1.  Inserta las palabras**Hola Mundo!** en la página accedida.
1. Genere el archivo Microsoft Visio modificado.

Los siguientes ejemplos demuestran los pasos anteriores.

#### **Creando un Diagram**

El siguiente ejemplo crea un nuevo diagram desde cero, escribe las palabras "¡Hola mundo!" en la primera página y guarda el archivo.

**Crear nuevo archivo visio** 

![todo:imagen_alternativa_texto](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Abrir un archivo existente**

El siguiente ejemplo abre un archivo de plantilla Microsoft Visio existente, escribe las palabras "¡Hola mundo!" en la primera página y guarda el diagram como un archivo nuevo.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
