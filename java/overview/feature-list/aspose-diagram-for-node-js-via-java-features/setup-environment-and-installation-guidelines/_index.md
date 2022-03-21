---
title: Setup Environment and Installation Guidelines
type: docs
weight: 20
url: /java/setup-environment-and-installation-guidelines/
description: Visio Diagram Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where Node.js and node-java bridge are installed. It can be installed from NPM and ZIP archive.
---

## **System Requirements**
Aspose.Diagram for Node.js via Java is platform-independent API and can be used on any platform (Windows, Linux and MacOS) where [Node.js](https://nodejs.org/en/download/) and [node-java](https://github.com/joeferner/node-java) bridge are installed. The machine must have Oracle JDK 7 or greater versions before setting up the installation.
## **Install from NPM**
You can easily use Aspose.Diagram for Node.js via Java from [NPM](https://www.npmjs.com/package/aspose.diagram) with the following command.
{{< highlight java >}}

 $ npm install aspose.diagram

{{< /highlight >}}

If you encounter any problems during the installation process, please refer to https://www.npmjs.com/package/java.

## **Install from ZIP archive**
To install and use Aspose.Diagram for Node.js via Java from a ZIP archive, follow the following instructions:
### **Linux:**
- Download and install [Node.js](https://nodejs.org/en/download/).
- Install Oracle JDK (1.7 or 1.8) for Linux, configure JAVA_HOME environment variable.
- Install python 2.x
- Install [node-java](https://github.com/joeferner/node-java) bridge. You may run below commands @ terminal: 



{{< highlight java >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Create a test file named **hello.js** using the following sample code in "aspose.diagram.js.java" folder:

{{< highlight java >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Now run "node hello.js" @command prompt to run it.
### **Windows:**
- Install Oracle JDK8 and configure JAVA_HOME environment variable.
- Install Node.js and add node.exe to PATH.
- Install node-gyp.
- Install Windows Build Tools.
- Install [node-java bridge](https://www.npmjs.com/package/java) and run below commands @ command prompt as an administrator:



{{< highlight java >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Create a file named **hello.js** in "aspose.diagram.js.java" folder using the following sample code:

{{< highlight java >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");
var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Now run "node hello.js" @command prompt to run it.
### **Mac:**
- Download and install Node.js ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Install Oracle JDK 1.8 (recommended) for Mac, configure JAVA_HOME environment variable.
- Modify <key>JVMCapabilities</key> section in "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Info.plist" with root privilege. ("jdk1.8.0_152.jdk" depends on your jdk version), make it looks like following:



{{< highlight java >}}

 <key>JavaVM</key>

        <dict>

                <key>JVMCapabilities</key>

                <array>

                        <string>JNI</string>

                        <string>BundledApp</string>

                        <string>CommandLine</string>

                </array>

{{< /highlight >}}



- Install python 2.x (if it is not installed).
- Install node-java bridge. You may run below commands @ terminal:

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm install java

- Download "Aspose.Diagram for Node.js via Java" and extract it into "aspose.diagram.js.java/node_modules".
- Create a test file named **hello.js** using the following sample code in "aspose.diagram.js.java" folder:



{{< highlight java >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var newDiagram = new aspose.diagram.Diagram();
newDiagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

console.log("hello world");

{{< /highlight >}}

- Now run "node hello.js" @command prompt to run it.
