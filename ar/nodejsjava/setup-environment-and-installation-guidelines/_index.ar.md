---
title: بيئة الإعداد وإرشادات التثبيت
second_title: Aspose.Diagram for Node.js via Java
type: docs
weight: 20
url: /ar/nodejsjava/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-nodejs-via-java-system-requirements/, /nodejsjava/system-requirements/]
keywords: nodejs, visio, instal
description: Visio Diagram Node.js هو API مستقل عن النظام الأساسي ويمكن استخدامه على أي منصة (Windows و Linux و MacOS) حيث يتم تثبيت Node.js و node-java bridge. يمكن تثبيته من أرشيف NPM و ZIP
---
## **متطلبات النظام**
 Aspose.Diagram لـ Node.js via Java مستقل عن النظام الأساسي API ويمكن استخدامه على أي منصة (Windows ، Linux و MacOS) حيث[Node.js](https://nodejs.org/en/download/) و[عقدة جافا](https://github.com/joeferner/node-java) يتم تثبيت الجسر. يجب أن يحتوي الجهاز على Oracle JDK 7 أو إصدارات أحدث قبل إعداد التثبيت.
## **التثبيت من NPM**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Node.js via Java من[NPM](https://www.npmjs.com/package/aspose.diagram) بالأمر التالي.
{{< highlight "java" >}}

 $ npm install aspose.diagram

{{< /highlight >}}

إذا واجهت أي مشاكل أثناء عملية التثبيت ، فيرجى الرجوع إلى https://www.npmjs.com/package/java.

## **التثبيت من أرشيف ZIP**
لتثبيت واستخدام Aspose.Diagram لـ Node.js via Java من أرشيف ZIP ، اتبع الإرشادات التالية:
### **لينكس:**
-  تنزيل وتثبيت[Node.js](https://nodejs.org/en/download/).
- قم بتثبيت Oracle JDK (1.7 أو 1.8) لنظام Linux ، قم بتكوين متغير بيئة JAVA_HOME.
- قم بتثبيت python 2.x.
-  تثبيت[عقدة جافا](https://github.com/joeferner/node-java) كوبري. يمكنك تشغيل الأوامر أدناه @ terminal:



{{< highlight "java" >}}

 $ mkdir aspose.diagram.js.java

$ cd aspose.diagram.js.java

$ npm install java

{{< /highlight >}}



- قم بتنزيل "Aspose.Diagram لـ Node.js via Java" واستخرجه في "aspose.diagram.js.java/node_modules".
- قم بإنشاء ملف اختبار باسم**مرحبًا**باستخدام نموذج التعليمات البرمجية التالي في مجلد "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- الآن قم بتشغيل "node hello.js" موجه الأوامر @ لتشغيله.
### **Windows:**
- قم بتثبيت Oracle JDK8 وتكوين متغير بيئة JAVA_HOME.
- قم بتثبيت Node.js وإضافة node.exe إلى PATH.
- تثبيت node-gyp.
- قم بتثبيت Windows Build Tools.
-  تثبيت[جسر عقدة جافا](https://www.npmjs.com/package/java) وقم بتشغيل أوامر @ موجه الأوامر أدناه كمسؤول:



{{< highlight "java" >}}

 > mkdir aspose.diagram.js.java

\> cd aspose.diagram.js.java

\> npm install -g node-gyp

\> npm install --global --production windows-build-tools

\> npm install java

{{< /highlight >}}

- قم بتنزيل "Aspose.Diagram لـ Node.js via Java" واستخرجه في "aspose.diagram.js.java/node_modules".
-  قم بإنشاء ملف باسم**مرحبًا**في مجلد "aspose.diagram.js.java" باستخدام نموذج التعليمات البرمجية التالي:

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- الآن قم بتشغيل "node hello.js" موجه الأوامر @ لتشغيله.
### **ماك:**
- قم بتنزيل وتثبيت Node.js ([*https://nodejs.org/en/download/*](https://nodejs.org/en/download/))
- قم بتثبيت Oracle JDK 1.8 (موصى به) لنظام التشغيل Mac ، قم بتكوين متغير بيئة JAVA_HOME.
-  تعديل<key>قدرات JVM</key> قسم في "/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk / المحتويات / Info.plist "بامتياز الجذر. (" jdk1.8.0_152.jdk "يعتمد على إصدار jdk الخاص بك) ، اجعله يبدو كما يلي:



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



- قم بتثبيت python 2.x (إذا لم يكن مثبتًا).
- تثبيت جسر عقدة جافا. يمكنك تشغيل الأوامر أدناه @ terminal:

`         ` $ mkdir aspose.diagram.js.java

`         ` $ cd aspose.diagram.js.java

`         ` $ npm تثبيت جافا

- قم بتنزيل "Aspose.Diagram لـ Node.js via Java" واستخرجه في "aspose.diagram.js.java/node_modules".
-  قم بإنشاء ملف اختبار باسم**مرحبًا** باستخدام نموذج التعليمات البرمجية التالي في مجلد "aspose.diagram.js.java":

{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("out.vsdx");

console.log("hello world");

{{< /highlight >}}

- الآن قم بتشغيل "node hello.js" موجه الأوامر @ لتشغيله.


