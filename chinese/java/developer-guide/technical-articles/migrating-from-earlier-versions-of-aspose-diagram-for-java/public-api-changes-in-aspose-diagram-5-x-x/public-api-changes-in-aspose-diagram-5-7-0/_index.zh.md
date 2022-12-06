---
title: 公共 API Aspose.Diagram 5.7.0 的变化
type: docs
weight: 30
url: /zh/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.6.0 到 5.7.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **在时间轴上设置日期模式字符串**
TimelineHelper 类中添加了新的 setDateFormatStringForBE 和 setDateFormatStringForIntm 方法。示例代码：

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
