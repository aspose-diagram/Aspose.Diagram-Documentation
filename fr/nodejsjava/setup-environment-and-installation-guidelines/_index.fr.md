---
title: Environnement de configuration et directives d'installation
second_title: Aspose.Diagram for Node.js via Java
type: docs
weight: 20
url: /fr/nodejsjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-nodejs-via-java-system-requirements/, /nodejsjava/system-requirements/]
keywords: nodejs, visio, instal
description: Visio Diagram Node.js est indépendant de la plate-forme API et peut être utilisé sur n'importe quelle plate-forme (Windows, Linux et MacOS) où Node.js et le pont node-java sont installés. Il peut être installé à partir des archives NPM et ZIP
---
## **Configuration requise**
Aspose.Diagram for Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Node.js](https://nodejs.org/en/download/) et[noeud-java](https://github.com/joeferner/node-java) pont sont installés. La machine doit avoir Oracle JDK 7 ou des versions supérieures avant de configurer l'installation.
## **Installer à partir de NPM**
You can easily use Aspose.Diagram for Node.js via Java from [MNP](https://www.npmjs.com/package/aspose.diagram) avec la commande suivante.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

Si vous rencontrez des problèmes lors du processus d'installation, veuillez vous référer à https://www.npmjs.com/package/java.

## **Installer à partir de l'archive ZIP**
To install and use Aspose.Diagram for Node.js via Java from a ZIP archive, follow the following instructions:
### **Linux :**
-  Télécharger et installer[Node.js](https://nodejs.org/en/download/).
- Installez Oracle JDK (1.7 ou 1.8) pour Linux, configurez la variable d'environnement JAVA_HOME.
- Installer Python 2.x
-  Installer[noeud-java](https://github.com/joeferner/node-java) pont. Vous pouvez exécuter les commandes ci-dessous @ terminal :



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Créez un fichier de test nommé**bonjour.js**en utilisant l'exemple de code suivant dans le dossier "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Exécutez maintenant "node hello.js" @invite de commande pour l'exécuter.
### **Windows:**
- Installez Oracle JDK8 et configurez la variable d'environnement JAVA_HOME.
- Installez Node.js et ajoutez node.exe à PATH.
- Installez node-gyp.
- Installez les outils de construction Windows.
-  Installer[pont noeud-java](https://www.npmjs.com/package/java) et exécutez les commandes ci-dessous à l'invite de commande en tant qu'administrateur :



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Créer un fichier nommé**bonjour.js**dans le dossier "aspose.diagram.js.java" en utilisant l'exemple de code suivant :

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Exécutez maintenant "node hello.js" @invite de commande pour l'exécuter.
### **Mac:**
- Téléchargez et installez Node.js ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Installez Oracle JDK 1.8 (recommandé) pour Mac, configurez la variable d'environnement JAVA_HOME.
-  Modifier<key>Capacités JVM</key> section dans "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist" avec le privilège root. ("jdk1.8.0_152.jdk" dépend de votre version de jdk), faites-le ressembler à ceci :



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



- Installez Python 2.x (s'il n'est pas installé).
- Installez le pont nœud-java. Vous pouvez exécuter les commandes ci-dessous @ terminal :

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm installer java

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
-  Créez un fichier de test nommé**bonjour.js** en utilisant l'exemple de code suivant dans le dossier "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Exécutez maintenant "node hello.js" @invite de commande pour l'exécuter.


