---
title: Installationsumgebung und Installationsrichtlinien
type: docs
weight: 20
url: /de/java/setup-environment-and-installation-guidelines/
description: Visio Diagram Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where Node.js and node-java bridge are installed. It can be installed from NPM and ZIP archive.
---
## **System Anforderungen**
Aspose.Diagram for Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Node.js](https://nodejs.org/en/download/) und[Knoten-Java](https://github.com/joeferner/node-java) Brücke installiert sind. Der Computer muss über Oracle JDK 7 oder höher verfügen, bevor die Installation eingerichtet werden kann.
## **Von NPM installieren**
You can easily use Aspose.Diagram for Node.js via Java from [NPM](https://www.npmjs.com/package/aspose.diagram) mit folgendem Befehl.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

Wenn Sie während des Installationsvorgangs auf Probleme stoßen, lesen Sie bitte https://www.npmjs.com/package/java.

## **Aus dem ZIP-Archiv installieren**
To install and use Aspose.Diagram for Node.js via Java from a ZIP archive, follow the following instructions:
### **Linux:**
-  Herunterladen und installieren[Node.js](https://nodejs.org/en/download/).
- Installieren Sie Oracle JDK (1.7 oder 1.8) für Linux, konfigurieren Sie die Umgebungsvariable JAVA_HOME.
- Installieren Sie Python 2.x
-  Installieren[Knoten-Java](https://github.com/joeferner/node-java) Brücke. Sie können die folgenden Befehle @ terminal ausführen:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Erstellen Sie eine Testdatei mit dem Namen**hallo.js**Verwenden Sie den folgenden Beispielcode im Ordner "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Führen Sie nun „node hello.js“ @command prompt aus, um es auszuführen.
### **Windows:**
- Installieren Sie Oracle JDK8 und konfigurieren Sie die Umgebungsvariable JAVA_HOME.
- Installieren Sie Node.js und fügen Sie node.exe zu PATH hinzu.
- node-gyp installieren.
- Installieren Sie Windows Build-Tools.
-  Installieren[Node-Java-Bridge](https://www.npmjs.com/package/java) und führen Sie die folgenden Befehle an der Eingabeaufforderung als Administrator aus:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Erstellen Sie eine Datei mit dem Namen**hallo.js**im Ordner „aspose.diagram.js.java“ mit dem folgenden Beispielcode:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Führen Sie nun „node hello.js“ @command prompt aus, um es auszuführen.
### **Mac:**
- Laden Sie Node.js herunter und installieren Sie es ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Installieren Sie Oracle JDK 1.8 (empfohlen) für Mac, konfigurieren Sie die Umgebungsvariable JAVA_HOME.
-  Ändern<key>JVM-Funktionen</key> Abschnitt in „/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist“ mit Root-Rechten („jdk1.8.0_152.jdk" hängt von Ihrer jdk-Version ab), damit es wie folgt aussieht:



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



- Installieren Sie Python 2.x (falls es nicht installiert ist).
- Installieren Sie die Node-Java-Bridge. Sie können die folgenden Befehle @ terminal ausführen:

`         `$ mkdir aspose.diagram.js.java

`         `$ CD aspose.diagram.js.java

`         `$ npm installiert java

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Erstellen Sie eine Testdatei mit dem Namen**hallo.js** Verwenden Sie den folgenden Beispielcode im Ordner "aspose.diagram.js.java":



{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Führen Sie nun „node hello.js“ @command prompt aus, um es auszuführen.
