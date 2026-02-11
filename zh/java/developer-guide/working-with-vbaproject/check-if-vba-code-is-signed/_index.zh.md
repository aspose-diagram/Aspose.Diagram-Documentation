---
title: 检查 VBA 代码是否已签名
type: docs
weight: 100
url: /zh/java/check-if-vba-code-is-signed/
description: 检查 vba 代码是否使用 Aspose.Diagram 库签名。
---
{{% alert color="primary" %}}

Aspose.Diagram 允许用户检查 VBA 代码项目是否已签名。请使用 [**Diagram.VbaProject.IsSigned**] 属性检查 VBA 代码项目是否已签名。

{{% /alert %}}

以下代码说明了如何使用 [**Diagram.VbaProject.IsSigned**] 属性检查 VBA 代码是否已签名。您可以使用任何 visio 文件来测试此代码。出于测试目的，您可以使用[代码中使用的这个 visio 文件](1.vsdm).

## 示例代码

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## 控制台输出

下面是使用上述代码的控制台输出[样本 visio 文件](1out.vsdm)由链接提供。

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
