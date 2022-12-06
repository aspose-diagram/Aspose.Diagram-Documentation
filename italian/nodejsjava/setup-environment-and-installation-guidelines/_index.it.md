﻿---
title: Ambiente di configurazione e linee guida per l'installazione
second_title: Aspose.Diagram for Node.js via Java
type: docs
weight: 20
url: /it/nodejsjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-nodejs-via-java-system-requirements/, /nodejsjava/system-requirements/]
keywords: nodejs, visio, instal
description: Visio Diagram Node.js è indipendente dalla piattaforma API e può essere utilizzato su qualsiasi piattaforma (Windows, Linux e MacOS) in cui sono installati Node.js e bridge node-java. Può essere installato dall'archivio NPM e ZIP
---
## **Requisiti di sistema**
Aspose.Diagram for Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Node.js](https://nodejs.org/en/download/) e[nodo-java](https://github.com/joeferner/node-java) ponte sono installati. La macchina deve disporre di Oracle JDK 7 o versioni successive prima di configurare l'installazione.
## **Installa da NPM**
You can easily use Aspose.Diagram for Node.js via Java from [NPM](https://www.npmjs.com/package/aspose.diagram) con il seguente comando.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

In caso di problemi durante il processo di installazione, fare riferimento a https://www.npmjs.com/package/java.

## **Installa dall'archivio ZIP**
To install and use Aspose.Diagram for Node.js via Java from a ZIP archive, follow the following instructions:
### **Linux:**
-  Scarica e installa[Node.js](https://nodejs.org/en/download/).
- Installa Oracle JDK (1.7 o 1.8) per Linux, configura la variabile di ambiente JAVA_HOME.
- Installa Python 2.x
-  Installare[nodo-java](https://github.com/joeferner/node-java) ponte. Puoi eseguire i seguenti comandi @ terminale:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Crea un file di prova denominato**ciao.js**utilizzando il seguente codice di esempio nella cartella "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Ora esegui "node hello.js" @command prompt per eseguirlo.
### **Windows:**
- Installa Oracle JDK8 e configura la variabile di ambiente JAVA_HOME.
- Installa Node.js e aggiungi node.exe a PATH.
- Installa node-gyp.
- Installa Windows Strumenti di creazione.
-  Installare[ponte nodo-java](https://www.npmjs.com/package/java) ed esegui sotto i comandi @ prompt dei comandi come amministratore:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Crea un file denominato**ciao.js**nella cartella "aspose.diagram.js.java" utilizzando il seguente codice di esempio:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Ora esegui "node hello.js" @command prompt per eseguirlo.
### **Mac:**
- Scarica e installa Node.js ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Installa Oracle JDK 1.8 (consigliato) per Mac, configura la variabile di ambiente JAVA_HOME.
-  Modificare<key>Funzionalità JVM</key> sezione in "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist" con privilegi di root. ("jdk1.8.0_152.jdk" dipende dalla tua versione jdk), fallo apparire come segue:



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



- Installa python 2.x (se non è installato).
- Installa il bridge node-java. Puoi eseguire i seguenti comandi @ terminale:

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm installa java

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Crea un file di prova denominato**ciao.js** utilizzando il seguente codice di esempio nella cartella "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Ora esegui "node hello.js" @command prompt per eseguirlo.


