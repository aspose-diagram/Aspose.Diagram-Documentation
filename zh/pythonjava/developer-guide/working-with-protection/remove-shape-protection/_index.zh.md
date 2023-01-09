---
title: 移除形状保护
type: docs
weight: 20
url: /zh/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **移除 Visio 形状的保护**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **编辑Visio形状保护**
**锁定画面**, **锁定开始**, **锁定计算器WH**, **锁定裁剪**, **LockCustProp**, **锁定删除**, **锁定结束**, **锁定格式**, **LockFromGroupFormat**, **锁组**, **锁定高度**, **锁定移动X**, **锁定移动Y**, **锁定旋转**, **锁定选择**, **LockText编辑**, **锁定主题颜色**, **锁定主题效果**, **LockVtx编辑**和**锁定宽度**暴露的属性**保护**类支持**Aspose.Diagram.BoolValue**目的。这些属性可用于保护和取消保护形状。

在 Microsoft Office Visio 中，用户可以执行以下操作来保护任何形状：

- 在 Microsoft Office Visio 打开 diagram
- 选择任意形状
- 如果您使用的是 Visio 2007，请从“格式”菜单中选择“保护”；如果您使用的是 Visio 2010，请从“开发人员”菜单中选择“保护”
- 在“保护”窗口中，取消选中任何文本框以解锁任何形状属性
- 按“确定”

### **删除形状保护编程示例**
Use the following code in your application to do the same thing (unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-RemoveShapeProtection.py" >}}

