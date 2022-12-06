---
title: 配置 Visio 时间线形状
type: docs
weight: 20
url: /zh/java/configure-visio-timeline-shapes/
---
## **设置里程碑形状属性**
Aspose.Diagram 允许开发人员设置里程碑属性。本文介绍如何设置里程碑日期、日期格式、自动更新标志和类型。
### **设置里程碑日期、日期格式、自动更新标志和类型**
这[里程碑助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)上课需要一个[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)初始化时的对象[里程碑助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)目的。本文中的代码示例设置里程碑日期、日期格式、自动更新标志和里程碑类型属性。

|<p>**更新前的里程碑** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**更新后的里程碑。请注意更改后的日期格式。** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
更新里程碑日期、日期格式、自动更新标志和里程碑类型的过程：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 初始化 MilestoneHelper 对象。
1. 设置里程碑日期。
1. 设置里程碑日期格式。
1. 设置自动更新标志。
1. 设置里程碑类型
1. 将 Visio 图形保存为任何支持的格式。
#### **设置里程碑编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


日期格式值表：

|**价值**|**格式化字符串**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|年/月/日|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|MD-YY|
|11|MD|
|12|d MMMM, yyyy|
|13|d 嗯，yyyy|
|14|dM-yy|
|15|分米|
|16|yy-Md|
|17|yyyy-MD|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|嗯嗯|
|22|嗯嗯嗯|
|23|嗯嗯|
|24|yy|
|25|yyyy|
|26|d|
|27|嗯嗯|
|28|嗯|
|29|米|
## **设置时间线形状的时间段和日期格式**
Aspose.Diagram 允许开发人员以编程方式配置时间线。这解释了如何调整时间线形状（块、线、标尺、分割或圆柱形）的时间段和日期格式。
### **设置时间段和日期格式**
这[时间线助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)上课需要一个[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)初始化时的对象[时间线助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)目的。本文中的代码示例设置时间段开始、结束和日期格式值。

|<p>**Visio 配置时间轴对话框的时间段选项卡** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/nHth3W8.png)</p>|<p>**Visio 配置时间轴对话框的时间格式选项卡** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**输入 diagram** </p><p>![待办事项：图片_替代_文本](configure-visio-timeline-shapes_1.png)</p>|<p>**值更改后的 diagram** </p><p>![待办事项：图片_替代_文本](configure-visio-timeline-shapes_2.png)</p>|
更新时间段开始、结束和日期格式的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 初始化 TimeLineHelper 对象。
1. 设置时间段开始。
1. 设置时间段结束。
1. 设置日期格式。
1. 将 Visio 图形保存为任何支持的格式。
#### **设置时间段和日期编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


日期格式值表：

|**价值**|**格式化字符串**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|年/月/日|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|MD-YY|
|11|MD|
|12|d MMMM, yyyy|
|13|d 嗯，yyyy|
|14|dM-yy|
|15|分米|
|16|yy-Md|
|17|yyyy-MD|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|嗯嗯|
|22|嗯嗯嗯|
|23|嗯嗯|
|24|yy|
|25|yyyy|
|26|d|
|27|嗯嗯|
|28|嗯|
|29|米|
## **刷新时间轴上的里程碑 Visio**
Aspose.Diagram 允许开发人员根据时间段变化调整时间轴形状（块、线、标尺、分割或圆柱形）上的里程碑。
### **使用 TimeLineHelper 类刷新时间轴上的里程碑**
公开的 RefreshTimeLine 方法[时间线助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)类可用于恢复时间轴上的里程碑。

下面的代码显示了如何：

1. 加载样本 diagram。
1. 得到一个时间线形状。
1. 初始化 TimeLineHelper 对象。
1. 设置时间段开始。
1. 设置时间段结束。
1. 设置日期格式（可选）。
1. 调用 TimeLineHelper 对象的 RefreshTimeLine 方法。
1. 保存 diagram
#### **使用 TimeLineHelper 编程示例刷新里程碑**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 恢复时间轴上的里程碑。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
### **使用 MilestoneHelper 类刷新时间轴上的里程碑**
公开的 RefreshMilestone 方法[里程碑助手](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)类可用于刷新时间轴上的里程碑。

下面的代码显示了如何：

1. 加载样本 diagram。
1. 得到一个时间线形状。
1. 使用 AddShape 方法在 Visio diagram 添加 Shape。
1. 初始化 MilestoneHelper 对象。
1. 设置里程碑日期。
1. 将 Milstone 的 IsAutoUpdate 属性设置为 true。
1. 调用 MilestoneHelper 对象的 RefreshMilestone 方法。
1. 保存 diagram
#### **使用 MilestoneHelper 编程示例刷新里程碑**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 刷新时间轴上的里程碑。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}
