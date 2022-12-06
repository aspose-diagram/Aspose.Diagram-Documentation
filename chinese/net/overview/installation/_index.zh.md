---
title: 安装
type: docs
weight: 40
url: /zh/net/installation/
description: 本页介绍如何使用 Aspose.Diagram 库创建新的 visio。
---
## **安装 Aspose.Diagram for .NET 至 NuGet**
NuGet 是针对 .NET 平台的一个以开发人员为中心的免费开源包管理系统，旨在简化开发过程中将第三方库合并到 .NET 应用程序的过程。它是一个 Visual Studio 扩展，可以轻松地在使用 .NET Framework 的 Visual Studio 项目中添加、删除和更新库和工具。通过创建 NuGet 包并将其存储在其中，可以轻松地与其他开发人员共享库或工具一个 NuGet 存储库。安装包时，NuGet 将文件复制到您的解决方案并自动进行必要的更改，例如添加引用和更改您的 app.config 或 web.config 文件。如果您决定删除该库，NuGet 会删除文件并撤销它对您的项目所做的任何更改，以免留下任何混乱。
### **参考 Aspose.Diagram for .NET**
利用这个奇妙的功能，我们捆绑了[Aspose.Diagram for .NET](https://www.nuget.org/packages/Aspose.Diagram)库到 NuGet 包并将其上传到 NuGet 存储库。使用此选项，您无需在系统上安装此组件即可使用 Aspose.Diagram for .NET。 NuGet 在 Visual Studio 2010 及更高版本、Visual Web Developer 2010 和 Windows Phone Developer Tools 7.1 中运行。在我们的测试中，我们使用 Visual Studio 2015 Ultimate 对其进行了测试。

开始：

1. 在 Visual Studio 中打开您的解决方案或项目。
1. 添加 NuGet 包管理器作为 Visual Studio 扩展：
 1. 选择**工具**菜单后跟**推广经理**.
1. 选择**在线画廊**获取在线可用软件包的完整列表。
1. 选择**NuGet 包管理器**.
1.点击**下载**.
1. 安装包管理器后，重新启动 Visual Studio 以使更改生效。
安装 NuGet 包管理器后，您可以从中查找、安装、删除和更新包**管理 NuGet 包**窗口，或通过在**包管理器控制台**专用的 Visual Studio 窗口。如果选择**工具**其次是**库包管理器**.
### **使用包管理器控制台安装包**
要使用包管理器控制台引用组件：

1. 在 Visual Studio 中打开 .NET 应用程序。
1. 在**工具**菜单，选择**库包管理器**接着**包管理器控制台**.
1. 键入命令“Install-Package Aspose.Diagram”以安装最新的完整版本，或键入命令“Install-Package Aspose.Diagram -prerelease”以安装包括修补程序在内的最新版本。
1. 按**进入**.
### **使用包管理器控制台更新包**
如果您已经通过 NuGet 引用了该组件，请按照以下步骤将引用更新为最新版本：

1. 在 Visual Studio 中打开 .NET 应用程序。
1. 来自**工具**菜单，选择**库包管理器**， 其次是**包管理器控制台**打开包管理器控制台。
1. 键入命令“Update-Package Aspose.Diagram”以引用最新的完整版本，或键入命令“Update-Package Aspose.Diagram -prerelease”以安装包括修补程序在内的最新版本。
1. 按**进入**.
### **使用包管理器 GUI 安装包**
按照以下步骤使用包管理器 GUI 引用组件：

1. 在 Visual Studio 中打开 .NET 应用程序。
1. 来自**工具**菜单，选择**库包管理器**和**管理 NuGet 包**来自**解决方案**选项。
您还可以从解决方案资源管理器中获得类似的选项：
 1. 右击项目名称。
1. 选择**管理 NuGet 包**.
1. 选择**在线的**从左侧菜单。
1. 类型**Aspose.Diagram**进入搜索框查找 Aspose.Diagram for .NET。
1. 点击**安装更新**Aspose.Diagram for .NET 最新版旁边

**![通过 NuGet 安装 Aspose Diagram](instalthroughnuget.png)**
