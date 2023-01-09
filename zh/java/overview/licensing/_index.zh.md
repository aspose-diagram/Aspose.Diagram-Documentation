---
title: 许可
type: docs
weight: 60
url: /zh/java/licensing/
---
## **评估版限制**
免费评估版 Aspose.Diagram for Java 可从以下网址下载[Aspose 资料库](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **局限性**
评估版提供除以下功能外的所有功能：

- 您只能阅读 VSD 文件第一页的前十个形状。
- You will also see evaluation watermark in exoprted images and PDF files.

如果您想在没有评估限制的情况下试用 Aspose.Diagram，请申请 30 天的临时许可证。请参阅[如何获得临时许可证？](https://purchase.aspose.com/temporary-license)了解更多信息。
## **申请许可证**
您可以下载评估版**Aspose.Diagram**for Java 从[Aspose 资料库](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).评估版提供与产品许可版完全相同的功能。此外，当您购买许可证并添加几行代码来应用该许可证时，评估版就会成为许可证。

一旦您对您的评价感到满意**Aspose.Diagram**， 你可以[购买许可证](https://purchase.aspose.com/buy)在 Aspose 网站上。让自己熟悉所提供的不同订阅类型。如有任何疑问，请随时联系 Aspose 销售团队。

每个 Aspose 许可证都包含一年订阅，可以免费升级到在此期间发布的任何新版本或修复程序。技术支持是免费和无限制的，同时提供给许可用户和评估用户。

{{% alert color="primary" %}} 

如果你想测试**Aspose.Diagram**没有评估版本限制，请求 30 天的临时许可证。请参阅[如何获得临时许可证？](https://purchase.aspose.com/temporary-license)了解更多信息。

{{% /alert %}} 
### **设置许可证**
该许可证是一个纯文本 XML 文件，其中包含产品名称、获得许可的开发人员数量、订阅到期日期等详细信息。该文件经过数字签名，因此请勿修改该文件；即使无意中在文件中添加了额外的换行符也会使其无效。

在对文档执行任何操作之前，您需要申请许可证。确保在创建 Diagram 对象之前执行此操作。您只需为每个应用程序或进程设置一次许可证。

可以从以下位置的流或文件加载许可证：

1. 显式路径。
1. 包含 Aspose.Diagram.jar 的文件夹。

使用[许可证.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)许可组件的方法。设置许可证最简单的方法通常是将许可证文件放在与 Aspose.Diagram.jar 相同的文件夹中，并仅指定不带路径的文件名，如下例所示：
#### **示例 1**
在这个例子中**Aspose.Diagram**将尝试在包含应用程序 JAR 的文件夹中查找许可证文件。

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **示例 2**
从流中初始化许可证。

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **验证许可证**
可以验证许可证是否已正确设置。这[执照](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)类具有 isLicensed 字段，如果已正确设置许可证，该字段将返回 true。

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **应用计量许可证**
Aspose.Diagram for Java API 允许开发人员应用计量许可证。这是一种新的许可机制。新的许可机制将与现有的许可方法一起使用。那些希望根据 API 功能的使用情况进行计费的客户可以使用计量许可。详情请参阅[计量许可常见问题解答](https://purchase.aspose.com/faqs/licensing/metered)部分。

一个新班级[计量的](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered)已添加以应用计量密钥。此代码示例演示如何设置计量公钥和私钥：

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-License-PublicAndPrivateKeys-PublicAndPrivateKeys.java" >}}
