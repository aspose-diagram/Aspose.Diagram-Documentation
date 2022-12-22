---
title: 公共 API Aspose.Diagram 5.7.0 的变化
type: docs
weight: 30
url: /zh/net/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.6.0 到 5.7.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **在时间轴上设置日期模式字符串**
TimelineHelper 类中添加了新的 DateFormatStringForBE 和 DateFormatStringForIntm 属性。示例代码：

**C#**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";

// set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd"

' set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd"

{{< /highlight >}}
