---
title: Installationsmiljö och installationsriktlinjer
second_title: Aspose.Diagram for Node.js via Java
type: docs
weight: 20
url: /sv/nodejsjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-nodejs-via-java-system-requirements/, /nodejsjava/system-requirements/]
keywords: nodejs, visio, instal
description: Visio Diagram Node.js är plattformsoberoende API och kan användas på vilken plattform som helst (Windows, Linux och MacOS) där Node.js och node-java-brygga är installerade. Det kan installeras från NPM och ZIP-arkiv
---
## **Systemkrav**
 Aspose.Diagram för Node.js via Java är plattformsoberoende API och kan användas på alla plattformar (Windows, Linux och MacOS) där[Node.js](https://nodejs.org/en/download/) och[nod-java](https://github.com/joeferner/node-java) bro installeras. Maskinen måste ha Oracle JDK 7 eller senare versioner innan installationen ställs in.
## **Installera från NPM**
 Du kan enkelt använda Aspose.Diagram för Node.js via Java från[NPM](https://www.npmjs.com/package/aspose.diagram) med följande kommando.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

Om du stöter på några problem under installationsprocessen, se https://www.npmjs.com/package/java.

## **Installera från ZIP-arkiv**
För att installera och använda Aspose.Diagram för Node.js via Java från ett ZIP-arkiv, följ följande instruktioner:
### **Linux:**
-  ladda ner och installera[Node.js](https://nodejs.org/en/download/).
- Installera Oracle JDK (1.7 eller 1.8) för Linux, konfigurera miljövariabeln JAVA_HOME.
- Installera python 2.x
-  Installera[nod-java](https://github.com/joeferner/node-java) bro. Du kan köra nedanstående kommandon @ terminal:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Ladda ner "Aspose.Diagram för Node.js via Java" och extrahera det till "aspose.diagram.js.java/node_modules".
- Skapa en testfil med namnet**hej.js**med följande exempelkod i mappen "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Kör nu "node hello.js" @command prompt för att köra den.
### **Windows:**
- Installera Oracle JDK8 och konfigurera miljövariabeln JAVA_HOME.
- Installera Node.js och lägg till node.exe till PATH.
- Installera node-gyp.
- Installera Windows Byggverktyg.
-  Installera[nod-java brygga](https://www.npmjs.com/package/java) och kör nedan kommandon @ kommandotolken som administratör:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Ladda ner "Aspose.Diagram för Node.js via Java" och extrahera det till "aspose.diagram.js.java/node_modules".
-  Skapa en fil med namnet**hej.js**i mappen "aspose.diagram.js.java" med följande exempelkod:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Kör nu "node hello.js" @command prompt för att köra den.
### **Mac:**
- Ladda ner och installera Node.js ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Installera Oracle JDK 1.8 (rekommenderas) för Mac, konfigurera miljövariabeln JAVA_HOME.
-  Ändra<key>JVMCapabilities</key> avsnitt i "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist" med root-behörighet. ("jdk1.8.0_152.jdk" beror på din jdk-version), får det att se ut så här:



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



- Installera python 2.x (om det inte är installerat).
- Installera node-java bridge. Du kan köra nedanstående kommandon @ terminal:

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm installera java

- Ladda ner "Aspose.Diagram för Node.js via Java" och extrahera det till "aspose.diagram.js.java/node_modules".
-  Skapa en testfil med namnet**hej.js** med följande exempelkod i mappen "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Kör nu "node hello.js" @command prompt för att köra den.


