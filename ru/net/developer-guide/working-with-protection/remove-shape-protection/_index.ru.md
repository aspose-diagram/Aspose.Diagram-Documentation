---
title: Удалить защиту формы
type: docs
weight: 20
url: /ru/net/remove-shape-protection/
description: В этом разделе объясняется, как снять защиту формы.
---
## **Снять защиту формы Visio**
 Защита фигур Visio позволяет пользователям блокировать определенные аспекты фигур. Аспекты фигур, которые можно заблокировать с помощью защиты формы, включают ширину, высоту, положение x, положение y, поворот и многое другое. Разработчики могут добиться этого, используя[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Изменить защиту формы Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **ЛокКроп**, **LockCustProp**, **БлокировкаУдалить**, **ЛокЭнд**, **Формат блокировки**, **LockFromGroupFormat**, **ЛокГрупп**, **LockHeight**, **LockMoveX**, **LockMoveY**, **БлокировкаПоворот**, **LockSelect**, **LockTextПравить**, **БлокировкаТемаЦвета**, **LockThemeЭффекты**, **LockVtxПравить** а также**LockWidth** свойства, выставленные[**Защита**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) класс поддерживает**Aspose.Diagram.BoolValue** объект. Эти свойства можно использовать для защиты и снятия защиты фигур.

В Microsoft Office Visio пользователь может выполнять следующие действия для защиты любой формы:

- Открыть diagram в Microsoft Office Visio
- Выберите любую форму
- Выберите «Защита» в меню «Формат», если вы используете Visio 2007, или выберите «Защита» в меню «Разработчик», если вы используете Visio 2010.
- В окне «Защита» снимите флажок с любого текстового поля, чтобы разблокировать любой атрибут формы.
- Нажмите «ОК»
### **Удаление примера программирования защиты формы**
Используйте следующий код в своем приложении .NET, чтобы сделать то же самое (разблокировать любой атрибут формы), используя Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
