﻿---
title: 使用保护
type: docs
weight: 90
url: /zh/python-java/working-with-protection/
---
## **设置保护 Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **编辑保护Visio Diagram**
DocumentSettings 类公开的 getProtectBkgnds、getProtectMasters、getProtectShapes 和 getProtectStyles 方法支持 BoolValue 对象。这些属性可用于保护和取消保护 Microsoft Visio 图。

在 Microsoft Visio 中，您以这种方式保护文档：

1. 在Microsoft Visio开一个diagram。
1. 打开绘图资源管理器窗口。
1. 右键单击 diagram 并选择**保护文档**从菜单中。
1. 在“保护文档”窗口中，选中或清除选项以锁定或解锁不同的 diagram 元素。
1. 点击**好的**.

**请查看我们如何手动检查或清除选项。** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **编辑Visio形状保护**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

这**getLockAspect（）**, **获取锁定开始()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **获取锁定删除()**, **getLockEnd()**, **获取锁定格式()**, **getLockFromGroupFormat()**, **getLockGroup()**, **获取锁定高度()**, **getLockMoveX（）**, **getLockMoveY（）**, **getLockRotate() 方法**, **获取锁定选择()**, **获取锁定文本编辑()**, **getLockThemeColors（）**, **getLockThemeEffects() 方法**, **getLockVtxEdit()**和**获取锁定宽度()**公开的方法**保护**类支持 BoolValue 对象。这些方法可用于保护/取消保护形状。

在 Visio 中，您需要执行以下操作来保护任何形状：

1. 在Microsoft Visio开一个diagram。
1. 选择一个形状。
1. 选择**保护**来自**格式**菜单 (Visio 2007)，或选择**保护**来自**开发商**菜单（Visio 2010）。
1. 在里面**保护**窗口，选择或清除选项以锁定或解锁形状属性。
1. 点击**好的**.

**形状的保护选项，如 Microsoft Visio 所示** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
