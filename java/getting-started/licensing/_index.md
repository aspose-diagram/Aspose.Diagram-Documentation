---
title: Licensing
type: docs
weight: 60
url: /java/licensing/
---

## **Evaluation Version Limitations**
A free evaluation version of Aspose.Diagram for Java can be downloaded from [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Limitation**
The evaluation version provides all the features except the following:

- You can read only the first ten shapes of the first page of your VSD file.
- You will also see evaluation watermark in exoprted images and PDF files.

If you want to try Aspose.Diagram out without evaluation limitations, request a 30 day temporary license. Please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) for more information.
## **Applying a License**
You can download an evaluation version of **Aspose.Diagram** for Java from [Aspose Repository](https://repository.aspose.com/repo/com/aspose/aspose-diagram/). The evaluation version provides absolutely the same capabilities as the licensed version of the product. Furthermore, evaluation version simply becomes licensed when you purchase a license and add a couple of lines of code to apply the license.

Once you are happy with your evaluation of **Aspose.Diagram**, you can [purchase a license](https://purchase.aspose.com/order-online-step-1-of-8.aspx) at the Aspose website. Make yourself familiar with the different subscription types offered. If you have any questions, do not hesitate to contact the Aspose sales team.

Every Aspose license carries a one-year subscription for free upgrades to any new versions or fixes that come out during this time. Technical support is free and unlimited and provided both to licensed and evaluation users.

{{% alert color="primary" %}} 

If you want to test **Aspose.Diagram** without evaluation version limitations, request a 30-day temporary license. Please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) for more information.

{{% /alert %}} 
### **Setting a License**
The license is a plain text XML file that contains details such as the product name, number of developers it is licensed to, subscription expiry date and so on. The file is digitally signed, so do not modify the file; even the inadvertent addition of an extra line break into the file will invalidate it.

You need to apply a license before performing any operations with documents. Make sure you do this before creating a Diagram object. You are only required to set a license once per application or process.

The license can be loaded from a stream or file in the following locations:

1. Explicit path.
1. The folder that contains the Aspose.Diagram.jar.

Use the [License.setLicense()](https://apireference.aspose.com/diagram/java/com.aspose.diagram/License) method to license the component. Often the easiest way to set a license is to put the license file in the same folder as Aspose.Diagram.jar and specify just the file name without path as shown in the following example:
#### **Example 1**
In this example **Aspose.Diagram** will attempt to find the license file in the folder that contain the JARs of your application.

**Java**

{{< highlight csharp >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Example 2**
Initializes a license from a stream.

**Java**

{{< highlight csharp >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Validate the License**
It is possible to validate if the license has been set properly or not. The [License](https://apireference.aspose.com/diagram/java/com.aspose.diagram/License) class has the isLicensed field that will return true if license has been properly set.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Apply Metered License**
Aspose.Diagram for Java API allows developers to apply metered license. It is a new licensing mechanism. The new licensing mechanism will be used along with existing licensing method. Those customers who want to be billed based on the usage of the API features can use the metered licensing. For more details, please refer to [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) section.

A new class [Metered](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Metered) has been added to apply metered key. This code example demonstrates how to set metered public and private keys:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-License-PublicAndPrivateKeys-PublicAndPrivateKeys.java" >}}
