---
title: Kurulum Ortamı ve Kurulum Yönergeleri
second_title: Aspose.Diagram for Node.js via Java
type: docs
weight: 20
url: /tr/nodejsjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-nodejs-via-java-system-requirements/, /nodejsjava/system-requirements/]
keywords: nodejs, visio, instal
description: Visio Diagram Node.js, platformdan bağımsızdır API ve Node.js ile node-java köprüsünün kurulu olduğu tüm platformlarda (Windows, Linux ve MacOS) kullanılabilir. NPM ve ZIP arşivinden kurulabilir
---
## **sistem gereksinimleri**
 Node.js için Aspose.Diagram via Java, platformdan bağımsızdır API ve herhangi bir platformda (Windows, Linux ve MacOS) kullanılabilir.[Node.js](https://nodejs.org/en/download/) ve[düğüm-java](https://github.com/joeferner/node-java) köprü kurulur. Kurulumu kurmadan önce makinede Oracle JDK 7 veya üzeri sürümler bulunmalıdır.
## **NPM'den yükleyin**
 Node.js için Aspose.Diagram via Java adresinden rahatlıkla kullanabilirsiniz.[NPM](https://www.npmjs.com/package/aspose.diagram) aşağıdaki komutla.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

Yükleme işlemi sırasında herhangi bir sorunla karşılaşırsanız, lütfen https://www.npmjs.com/package/java adresine bakın.

## **ZIP arşivinden yükleyin**
Bir ZIP arşivinden Aspose.Diagram for Node.js via Java'i yüklemek ve kullanmak için aşağıdaki talimatları izleyin:
### **Linux:**
-  İndirin ve kurun[Node.js](https://nodejs.org/en/download/).
- Linux için Oracle JDK (1.7 veya 1.8) yükleyin, Java_HOME ortam değişkenini yapılandırın.
- Python 2.x'i kurun
-  Düzenlemek[düğüm-java](https://github.com/joeferner/node-java) köprü. Aşağıdaki komutları @ terminalde çalıştırabilirsiniz:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- "Aspose.Diagram for Node.js via Java" dosyasını indirin ve "aspose.diagram.js.java/node_modules" içine çıkarın.
- adlı bir test dosyası oluşturun.**merhaba.js**"aspose.diagram.js.java" klasöründe aşağıdaki örnek kodu kullanarak:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Şimdi çalıştırmak için "node hello.js" @komut istemini çalıştırın.
### **Windows:**
- Oracle JDK8'i yükleyin ve Java_HOME ortam değişkenini yapılandırın.
- Node.js'yi kurun ve node.exe'yi PATH'e ekleyin.
- node-gyp'yi kurun.
- Windows Derleme Araçları'nı yükleyin.
-  Düzenlemek[düğüm-java köprüsü](https://www.npmjs.com/package/java) ve aşağıdaki komutları @ komut istemini yönetici olarak çalıştırın:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- "Aspose.Diagram for Node.js via Java" dosyasını indirin ve "aspose.diagram.js.java/node_modules" içine çıkarın.
-  adlı bir dosya oluşturun.**merhaba.js**aşağıdaki örnek kodu kullanarak "aspose.diagram.js.java" klasöründe:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Şimdi çalıştırmak için "node hello.js" @komut istemini çalıştırın.
### **Mac:**
- Node.js'yi indirin ve kurun ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- Mac için Oracle JDK 1.8'i kurun (önerilen), JAVA_HOME ortam değişkenini yapılandırın.
-  Değiştir<key>JVMCapabiliteleri</key> "/Library/Java/JavaVirtualMachines/jdk1.8.0" bölümünde_152.jdk/Contents/Info.plist", kök ayrıcalığına sahiptir. ("jdk1.8.0_152.jdk", jdk sürümünüze bağlıdır), aşağıdaki gibi görünmesini sağlayın:



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



- Python 2.x'i yükleyin (kurulu değilse).
- Node-java köprüsünü kurun. Aşağıdaki komutları @ terminalde çalıştırabilirsiniz:

`         `$ mkdir aspose.diagram.js.java

`         `$ cd aspose.diagram.js.java

`         `$ npm Java'yı kurun

- "Aspose.Diagram for Node.js via Java" dosyasını indirin ve "aspose.diagram.js.java/node_modules" içine çıkarın.
-  adlı bir test dosyası oluşturun.**merhaba.js** "aspose.diagram.js.java" klasöründe aşağıdaki örnek kodu kullanarak:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- Şimdi çalıştırmak için "node hello.js" @komut istemini çalıştırın.


