---
title: 打开文件的不同方式
type: docs
weight: 10
url: /zh/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

使用 Aspose.Diagram 可以轻松打开文件，例如检索数据，或使用设计器模板来加快开发过程。

{{% /alert %}}

## **通过路径打开文件**

开发人员可以通过在本地计算机上指定文件路径来打开 Microsoft Diagram 文件**Diagram**类构造函数。只需将构造函数中的路径作为*细绳*Aspose.Diagram 会自动检测文件格式类型。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **通过流打开文件**

将 Visio 文件作为流打开也很简单。为此，请使用构造函数的重载版本，该版本采用*缓冲流*包含文件的对象。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **使用 LoadOptions 打开文件**

要使用加载选项打开文件，请使用**加载选项**classes 为要加载的模板文件设置类的相关选项。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

