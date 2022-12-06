---
title: Utilizando Aspose.Diagram en otros lenguajes de programación
type: docs
weight: 120
url: /es/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Esta página describe cómo utilizar Aspose.Diagram en otros lenguajes de programación.
---
## **Utilice Aspose.Diagram for .NET a través de interoperabilidad COM**
 La información de este tema se aplica a escenarios en los que los desarrolladores requieren usar[Aspose.Diagram for .NET](/diagram/es/net/home/) a través de COM Interop en cualquier idioma admitido.
### **Trabajar con interoperabilidad COM**
Aspose.Diagram for .NET se ejecuta bajo el control de .NET Framework y esto se denomina código administrado. El código escrito en todos los idiomas se ejecuta fuera del .NET Framework y se denomina código no administrado. La interacción entre el código no administrado y Aspose.Diagram ocurre a través de la instalación .NET llamada COM Interop.

Los objetos Aspose.Diagram son objetos .NET, pero cuando se usan a través de la interoperabilidad COM, aparecen como objetos COM en su lenguaje de programación. Por lo tanto, es mejor asegurarse de saber cómo crear y usar objetos COM en su lenguaje de programación, antes de comenzar a usar[Aspose.Diagram for .NET](/diagram/es/net/home/).

- En el mundo COM distinguimos servidor COM y cliente COM. El servidor COM almacenó clases COM mientras que el cliente COM le pide al servidor COM instancias de clases, es decir, objetos COM.
-  El cliente COM o simplemente la aplicación cliente puede saber algo sobre el contenido de la clase COM o desconocer por completo sus métodos y propiedades. Por lo tanto, la aplicación cliente puede descubrir la estructura de clases COM al compilar/construir o solo durante la ejecución. El proceso de "descubrimiento" se conoce como unión, por lo que tenemos**encuadernación temprana** y**encuadernación tardía**.
- en resumen, la clase COM es como una caja negra y para trabajar con ella se necesita una biblioteca de tipos, este archivo binario tiene una descripción de los métodos de la clase COM, las propiedades y cualquier lenguaje de alto nivel que admita trabajar con objetos COM, a menudo tiene una expresión de sintaxis para agregar una biblioteca de tipos, para instancia esto es[**#importar**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) en el C++.
- La biblioteca de tipos se utiliza para el enlace anticipado.
-  un objeto COM puede exponer sus métodos y propiedades de dos maneras: por medio de un**interfaz de despacho** (dispinterface) y en su**vtable** (tabla de funciones virtual).
-  dentro de**despintar** , cada método y propiedad está identificado por un miembro único; este miembro es el identificador de envío de la función (o**DISPID**).
- **vtable** es solo un conjunto de punteros a funciones que admite la interfaz de clase COM.
-  un objeto que expone sus métodos a través de ambas interfaces admite un**interfaz dual**.
- Hay ventajas para ambos tipos de encuadernación. El enlace temprano le proporciona un mayor rendimiento y verificación de sintaxis en tiempo de compilación. La vinculación en tiempo de ejecución es más ventajosa cuando está escribiendo clientes que pretende ser***compatible con futuras versiones*** de su clase COM. Con el enlace en tiempo de ejecución, la información de la biblioteca de tipos no está "conectada" a su cliente, por lo que puede tener una mayor confianza en que su cliente puede trabajar con futuras versiones de la clase COM sin cambios en el código.
-  El mecanismo de enlace tardío tiene una gran ventaja: si el creador de la DLL COM decide lanzar una nueva versión, con un diseño de interfaz de función diferente, cualquier código que llame a esos métodos no fallará a menos que los métodos ya no estén disponibles; Incluso si los**vtable**es diferente el enlace tardío logra descubrir los nuevos DISPID y llamar a los métodos apropiados.

 Estos son los temas que eventualmente necesitarás dominar:

- Usando objetos COM en su lenguaje de programación. Consulte la documentación de su lenguaje de programación y los temas específicos del lenguaje más adelante en esta documentación.
-  Trabajando con objetos COM expuestos por .NET COM Interop. Ver[Interoperar con código no administrado](https://docs.microsoft.com/en-us/dotnet/framework/interop/) y[Exposición de componentes .NET Framework a COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) en MSDN.
-  Aspose.Diagram modelo de objeto de documento. Ver[Aspose.Diagram Guía del programador](https://docs.aspose.com/diagram/net/developer-guide/) y[API Referencia](https://reference.aspose.com/diagram/net).
#### **Regístrese Aspose.Diagram for .NET con interoperabilidad COM**
Debe instalar Aspose.Diagram for .NET y asegurarse de que esté registrado con COM Interop (asegurándose de que se pueda llamar desde un código no administrado).

Para registrar Aspose.Diagram for .NET para COM Interop manualmente:

1.  Desde el**comienzo** menú, seleccione**Todos los programas** , después**Microsoft estudio visual**, **Herramientas de estudio visual** y finalmente,**Símbolo del sistema de Visual Studio**. En algunos sistemas operativos, también está disponible en la ubicación: "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1.  Ingrese el comando para registrar el ensamblado:
   1. .NET Framework 2.0
regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Preste atención a que /codebase es necesario solo si Aspose.Diagram.dll no está en GAC, el uso de esta opción hace que regasm coloque la ruta para ensamblar en el registro.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe es una herramienta incluida en .NET Framework SDK. Todas las herramientas .NET Framework SDK se encuentran en el*\Microsoft .NET\Framevork\<Versión del marco>* directorio, por ejemplo*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. Si usa Visual Studio .NET:
 Desde el**comienzo** menú, seleccione**Programas** , seguido por**Microsoft estudio visual .NET** , después**Visual Studio .NET Herramientas** y finalmente,**Símbolo del sistema de Visual Studio .NET 2003**.
Ejecuta un símbolo del sistema con todas las variables de entorno necesarias configuradas.

{{% /alert %}} 
##### **ProgID**
ProgID significa "identificador programático". Es el nombre de una clase COM que se utiliza para crear un objeto. Los ProgID consisten en el nombre de la biblioteca "Aspose.Diagram" y el nombre de la clase.
##### **Biblioteca de tipos**
Si su lenguaje de programación (por ejemplo, Visual Basic o Delphi) le permite hacer referencia a una biblioteca de tipo COM, agregue una referencia a Aspose.Diagram.tlb y vea todas las clases, métodos, propiedades y enumeraciones Aspose.Diagram for .NET en su Examinador de objetos.

Para generar un archivo TLB:

- .NET Framework 2.0
 regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
 regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
regasm "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Archivos de programa\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **Creación de objetos COM**
La creación de un objeto COM es similar a la creación de un objeto .NET normal. Una vez creado, puede acceder a los métodos y propiedades del objeto, como si fuera un objeto COM.

Algunos métodos tienen sobrecargas y COM Interop los expondrá con un sufijo numérico agregado, excepto el primer método que permanece sin cambios. Por ejemplo, las sobrecargas del método Diagram.Save se convierten en Diagram.Save, Diagram.Save_2, etc.

{{% alert color="primary" %}} 

 Para obtener más información, consulte los artículos específicos del idioma más adelante en esta documentación.

{{% /alert %}} 
## **Aspose.Diagram Recursos**
Los siguientes son los enlaces a algunos recursos útiles que puede necesitar para realizar sus tareas.
- [Aspose.Diagram for Java Documentación en línea](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram para Node.js a través de Java Documentación en línea](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram para Python vía Java Documentación en línea](https://docs.aspose.com/diagram/pythonjava/)

##### **Creación de un ensamblaje de envoltorio**
Si necesita usar muchas de las Aspose.Diagram Aspose.Diagram for .NET clases, métodos y propiedades, considere crear un conjunto contenedor (usando C# o cualquier otro lenguaje de programación .NET). Los ensamblajes de contenedor ayudan a evitar el uso de Aspose.Diagram for .NET directamente desde código no administrado.

Un buen enfoque es desarrollar un ensamblado .NET que haga referencia a Aspose.Diagram for .NET y haga todo el trabajo con él, y solo exponga un conjunto mínimo de clases y métodos al código no administrado. Su aplicación entonces debería funcionar solo con su biblioteca de contenedores.

 Reducir la cantidad de clases y métodos que necesita invocar a través de COM Interop simplifica el proyecto. El uso de clases .NET a través de COM Interop a menudo requiere habilidades avanzadas.
## **Cree un dibujo Visio vacío en PHP usando COM Interop**
### **requisitos previos**
 Configure su PHP para trabajar con COM. Ver<http://www.php.net/manual/en/ref.com.php> . Para obtener más información, consulte el artículo denominado[Utilice Aspose.Diagram for .NET a través de interoperabilidad COM](/diagram/es/net/home/).
### **Creación de un dibujo Visio vacío**
 Esta es una aplicación simple que le muestra cómo crear un dibujo Visio vacío usando[Aspose.Diagram for .NET](/diagram/es/net/home/) en PHP a través de interoperabilidad COM.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
