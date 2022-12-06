---
title: Entorno de configuración y pautas de instalación
type: docs
weight: 20
url: /es/java/setup-environment-and-installation-guidelines/
description: Visio Diagram Node.js a través de Java es independiente de la plataforma API y se puede usar en cualquier plataforma (Windows, Linux y MacOS) donde estén instalados Node.js y node-java bridge. Se puede instalar desde NPM y archivo ZIP.
---
## **Requisitos del sistema**
 Aspose.Diagram para Node.js a través de Java es independiente de la plataforma API y se puede usar en cualquier plataforma (Windows, Linux y MacOS) donde[Nodo.js](https://nodejs.org/en/download/) y[nodo-java](https://github.com/joeferner/node-java) puente están instalados. La máquina debe tener Oracle JDK 7 o versiones superiores antes de configurar la instalación.
## **Instalar desde NPM**
 Puede usar fácilmente Aspose.Diagram para Node.js a través de Java desde[MNP](https://www.npmjs.com/package/aspose.diagram) con el siguiente comando.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

Si encuentra algún problema durante el proceso de instalación, consulte https://www.npmjs.com/package/java.

## **Instalar desde archivo ZIP**
Para instalar y usar Aspose.Diagram para Node.js a través de Java desde un archivo ZIP, siga las siguientes instrucciones:
### **Linux:**
-  Descargar e instalar[Nodo.js](https://nodejs.org/en/download/).
- Instale Oracle JDK (1.7 o 1.8) para Linux, configure la variable de entorno JAVA_HOME.
- Instalar python 2.x
-  Instalar[nodo-java](https://github.com/joeferner/node-java) puente. Puede ejecutar los siguientes comandos @ terminal:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Descargue "Aspose.Diagram para Node.js a través de Java" y extráigalo en "aspose.diagram.js.java/node_modules".
- Cree un archivo de prueba llamado**hola.js**usando el siguiente código de muestra en la carpeta "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Ahora ejecute "node hello.js" @ símbolo del sistema para ejecutarlo.
### **Windows:**
- Instale Oracle JDK8 y configure la variable de entorno JAVA_HOME.
- Instale Node.js y agregue node.exe a PATH.
- Instale el nodo-gyp.
- Instale las herramientas de compilación Windows.
-  Instalar[puente nodo-java](https://www.npmjs.com/package/java) y ejecute los siguientes comandos @ símbolo del sistema como administrador:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Descargue "Aspose.Diagram para Node.js a través de Java" y extráigalo en "aspose.diagram.js.java/node_modules".
-  Crear un archivo llamado**hola.js**en la carpeta "aspose.diagram.js.java" usando el siguiente código de muestra:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Ahora ejecute "node hello.js" @ símbolo del sistema para ejecutarlo.
### **Mac:**
- Descargue e instale Node.js ([*https://nodejs.org/en/descargar/*](https://nodejs.org/en/download/))
- Instale Oracle JDK 1.8 (recomendado) para Mac, configure la variable de entorno JAVA_HOME.
-  Modificar<key>Capacidades de JVM</key> sección en "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist" con privilegio de raíz. ("jdk1.8.0_152.jdk" depende de su versión de jdk), haga que tenga el siguiente aspecto:



{{< highlight "java" >}}

 <key>JavaVM</key>

        <dict>

                <key>JVMCapabilities</key>

                <array>

                        <string>JNI</string>

                        <string>BundledApp</string>

                        <string>CommandLine</string>

                </array>

{{< /highlight >}}



- Instale Python 2.x (si no está instalado).
- Instale el puente nodo-java. Puede ejecutar los siguientes comandos @ terminal:

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm instalar java

- Descargue "Aspose.Diagram para Node.js a través de Java" y extráigalo en "aspose.diagram.js.java/node_modules".
-  Cree un archivo de prueba llamado**hola.js** usando el siguiente código de muestra en la carpeta "aspose.diagram.js.java":



{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Ahora ejecute "node hello.js" @ símbolo del sistema para ejecutarlo.
